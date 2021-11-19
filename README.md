# TP numéro 11

## Objectif:

Utiliser un fact Ansible pour compléter un fichier de configuration

## Besoin:

- Créer un Playbook *config.yaml* tel que:
  - S’exécute sur les host *back*
  - Crée un fichier `/etc/my.cnf.d/listen.cnf` contenant:

```
[server]
bind-address=<ip du serveur>
```

  - Redémarre le service mariadb


> Le module **copy** dispose d’un paramètre *content* pour écrire un fichier à la volée  
S’assurer que les facts soient collectés peu importe la configuration par défaut  
Utiliser le fact *ansible_facts.default_ipv4.address*
