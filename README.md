# Déploiement de services web éducatifs

Ce rôle ansible a pour but de faciliter la configuration et l'installation d'un serveur à destination d'un projet éducatif.

## Prérequis

Une version d'ansible égale ou supérieur à `2.9` pour la machine qui execute le rôle. Et un OS de type Debian concernant la machine où le rôle est déployée.

## Parmètres

Retrouvez tous les paramètres dans `defaults/main.yml`.

## Dependances

Pour fonctionner, ce rôle s'appuie sur plusieurs autres rôles. Pour les installer, vous pouvez faire :
```
ansible-galaxy install -r requirements.yml
```

## Exemples

C'est le fichier `hosts.yml` qui décide avec quel utilisateur ansible va se connecter pour exécuter le playbook
ainsi que le serveur auquel se connecter. Le fichier `playbook.yml` va lui permettre d'indiquer ce qu'il faut
installer ainsi que les paramètres des différents services.

Vous pouvez partir de `hosts_example.yml` et `playbook_example.yml` pour créer vos propres fichiers.

Pour exécuter le playbook :

```
ansible-playbook -i hosts.yml playbook.yml -K
```

## License

GPLv3
