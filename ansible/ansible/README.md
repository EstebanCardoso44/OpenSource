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


| Playbook            | Rôle                           |
| ------------------- | ------------------------------ |
| install_php.yml     | Installation PHP               |
| install_apache.yml  | Apache, TLS, VirtualHost HTTPS |
| install_mariadb.yml | MariaDB, base, utilisateur     |
| site.yml            | Playbook global                |

