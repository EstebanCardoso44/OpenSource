# Rapport de durcissement - TP3 SecureBox

## Objectif

Déployer automatiquement une stack LAMP sécurisée pour Acme Corp avec Ansible.

Le déploiement comprend :

- 2 serveurs web Apache/PHP : `web1` et `web2`
- 1 serveur base de données MariaDB : `db1`
- HTTPS avec certificat autosigné
- durcissement Apache/SSH
- gestion des secrets avec Ansible Vault

## Environnement de test

Aucune VM dédiée n’étant disponible, l’environnement de test a été simulé avec trois conteneurs Debian accessibles en SSH :

| Hôte | Rôle | Port SSH | Port applicatif |
|---|---|---:|---:|
| web1 | Apache + PHP | 2221 | 8443 → 443 |
| web2 | Apache + PHP | 2222 | 8444 → 443 |
| db1 | MariaDB | 2223 | 3307 → 3306 |

Ansible administre ces conteneurs comme des hôtes distants classiques via SSH.

## Mesures de durcissement appliquées

| Mesure | Description | Statut |
|---|---|---|
| Séparation des rôles | Rôles Ansible `apache`, `php`, `mariadb`, `hardening` | Appliqué |
| Apache2 | Installation automatisée sur les hôtes web | Appliqué |
| PHP | Installation PHP et modules nécessaires | Appliqué |
| MariaDB | Installation sur l’hôte BDD | Appliqué |
| Base applicative | Création de la base `acme_db` | Appliqué |
| Utilisateur applicatif | Création de l’utilisateur MariaDB `app` | Appliqué |
| Secrets | Mot de passe BDD stocké dans `vault.yml` chiffré | Appliqué |
| TLS | Certificat autosigné généré automatiquement | Appliqué |
| HTTPS | VirtualHost Apache configuré sur le port 443 | Appliqué |
| Redirection HTTP vers HTTPS | VirtualHost port 80 redirige vers HTTPS | Appliqué |
| Headers sécurité | X-Frame-Options, X-Content-Type-Options, X-XSS-Protection, Referrer-Policy, CSP | Appliqué |
| ModSecurity | Module Apache ModSecurity installé et activé | Appliqué |
| Permissions web | `/var/www/acme` en `0750`, fichiers web en `0640` | Appliqué |
| SSH root | `PermitRootLogin no` configuré | Appliqué |
| Signature Apache | `ServerSignature Off` | Appliqué |
| Version Apache | `ServerTokens Prod` | Appliqué |
| UFW | Prévu pour VMs réelles, limité en environnement Docker | Partiel |

## Validation HTTPS

Commandes utilisées :

```bash
curl -k -v https://localhost:8443
curl -k -v https://localhost:8444

SSL connection using TLSv1.3
Server certificate: CN=securebox.local
HTTP/1.1 200 OK
SecureBox - Apache/PHP HTTPS OK
