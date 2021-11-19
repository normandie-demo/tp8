# Correction TP 8


## Utiliser **ansible-galaxy** pour initialiser les répertoires nécessaire au rôle

```
mkdir roles
ansible-galaxy role init db --offline --init-path roles
```

## Modifier le rôle db

Editer le fichier *roles/db/tasks/main.yml*

```yaml
---
# tasks file for db

- name: installation de mariadb
  ansible.builtin.dnf:
    name: mariadb-server

- name: demarrer MariaDB
  ansible.builtin.systemd:
    name: mariadb
    state: started

```

## Exécuter ce playbook sur l’inventaire *inventory*

```Shell
ansible-playbook -i inventory mariadb.yaml
```

Lien vers le dossier [corrections](../Correction)