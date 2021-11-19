# TP numéro 8

## Objectif:

Initialiser un rôle db et y ajouter des tâches
Construire un playbook exécutant ce rôle sur les machines back
Exécuter ce playbook


## Besoin:

- Utiliser **ansible-galaxy** pour initialiser les répertoires nécessaire au rôle
- Ajouter au rôle *db* les tâche suivantes:
  - une tâche *dnf* qui installe le paquet *mariadb*
  - une tâche *systemd* qui démarre le service *mariadb*
- Construire un playbook *mariadb.yaml* qui attribue le rôle *db* aux machine *back*
- Exécuter ce playbook sur l’inventaire *inventory*
