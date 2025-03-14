# Réponses Checkpoint 3

## Partie 1 : Gestion des utilisateurs

### Q.1.1.1 Créer l'utilisateur Lionel Lemarchand avec les même attribut de société que Kelly Rhameur.

![lione01](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/lionel01.png)

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/lionel02.png)


### Q.1.1.2 Créer une OU DeactivatedUsers et déplace le compte désactivé de Kelly Rhameur dedans. 

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/desactivatedgroup.png)

### Q.1.1.3 Modifier le groupe de l'OU dans laquelle était Kelly Rhameur en conséquence.

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/groupelionel.png)

### Q.1.1.4 Créer le dossier Individuel du nouvel utilisateur et archive celui de Kelly Rhameur en le suffixant par -ARCHIVE.

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/dossier-individuel.png)

## Partie 2 : Restriction utilisateurs

### Q.1.2.1 Faire en sorte que l'utilisateur Gabriel Ghul ne puisse se connecter que du lundi au vendredi, de 7h à 17h.

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/logonhoursGG.png)

### Q.1.2.2 De même, bloquer sa connexion au seul ordinateur CLIENT01.

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/computer-restricGG.png)

### Q.1.2.3 Mettre en place une stratégie de mot de passe pour durcir les comptes des utilisateurs de l'OU LabUsers.

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/acconthardpasswd.png)

## Partie 3 : Lecteurs réseaux

### Q.1.3.1 Créer une GPO Drive-Mount qui monte les lecteurs E: et F: sur les clients.

__Détail GPO Mappage de lecteur E :__

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/mappage-E.png)

__Détail GPO Mappage de lecteur F :__

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/mappage-F.png)

## Partie 1 : Gestion des utilisateurs

```bash
#Créer l'utilisateur Math (sous compte root)
useradd -m -s /bin/bash Math

#Créer le mot de passe pour l'utilisateur
passwd Math
```

### Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.

### Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?
- Un dossier utilisateur à l'emplacement de /home
- Un mot de passe robuste de 8 caractères dont au moins une majuscule et un caratère spécial
- Pas de droits root de base mais la possibilité d'effectuer des tâches d'administration en étant ajouté au groupe __sudo__ plus tard
