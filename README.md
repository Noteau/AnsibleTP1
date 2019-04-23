# AnsibleTP1
TP visant à mettre en place un wordpress ainsi qu'une base de données en liant les deux sur deux vm différentes

# Prérequis :
Ce tp nécessite deux VM présente sur le même sous-réseaux avec le port 80 ouvert (pour Apache)
Il faut aussi que Ansible et donc Python soit présent sur votre machine (sudo pip install ansible)

Une fois cela il faut faire : git clone git@github.com:Noteau/AnsibleTP1.git

Le projet copié possedera donc mes informations, pour utiliser les votres quelques paramètres doivent être modifiés. 
# Database :
Les modifications sont à faire dans le fichier main.yml au niveau du dossier playbook/wordpress/defaults

```mysql_user_name: wordpress (VOTRE_USERNAME)
mysql_user_password: wxcvbn12 (VOTRE_PASSWORD)
wp_db_name: db_name (VOTRE_NOM_DE_DATABASE)
wp_db_host: ip_address (VOTRE_ADRESSE)
```

Dans le dossier host_vars/ :

```
ansible_host: ip_address  (VOS_IP_DE_VOS_VM)
```

Une fois cela effectué  il faut lancer la commande :
```
ansible-playbook playbook/playbook.yml -i ./inventory.ini
````
