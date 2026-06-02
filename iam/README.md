# TP2 - IAM centralisé et centralisation des logs

## Objectif

Ce TP met en place les fondations d'identité et de journalisation de l'infrastructure SecureBox pour Acme Corp.

La stack déployée comprend :

- OpenLDAP : annuaire centralisé des utilisateurs
- phpLDAPadmin : interface d'administration LDAP
- Keycloak : fournisseur d'identité SSO / OIDC
- PostgreSQL : base de données persistante Keycloak
- Grafana : interface de visualisation
- Loki : stockage et requêtage des logs
- Promtail : collecte des logs Docker vers Loki

## Architecture

```text
Utilisateurs
    |
    | Authentification SSO
    v
Grafana ---- OIDC ---- Keycloak ---- LDAP ---- OpenLDAP
   |
   | Requêtes LogQL
   v
Loki <---- Promtail <---- Logs conteneurs Docker
