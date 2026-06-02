# TP3 - Stack LAMP automatisée avec TLS et durcissement Ansible

## Objectif

Déployer automatiquement une stack LAMP sécurisée pour Acme Corp avec Ansible.

## Architecture

```text
Poste Ansible Kali
        |
        | SSH
        |
+-------+-------+----------------+
|               |                |
web1            web2             db1
Apache/PHP      Apache/PHP       MariaDB
HTTPS 8443      HTTPS 8444       DB acme_db


ansible/inventory.ini
[web] : web1, web2
[db]  : db1

Les 3 VM sont simulés en tant que conteneur debian :
services:
  web1:
    build: .
    container_name: securebox-web1
    ports:
      - "2221:22"
      - "8082:80"
      - "8443:443"

  web2:
    build: .
    container_name: securebox-web2
    ports:
      - "2222:22"
      - "8083:80"
      - "8444:443"

  db1:
    build: .
    container_name: securebox-db1
    ports:
      - "2223:22"
      - "3307:3306"

| Playbook            | Rôle                           |
| ------------------- | ------------------------------ |
| install_php.yml     | Installation PHP               |
| install_apache.yml  | Apache, TLS, VirtualHost HTTPS |
| install_mariadb.yml | MariaDB, base, utilisateur     |
| site.yml            | Playbook global                |

