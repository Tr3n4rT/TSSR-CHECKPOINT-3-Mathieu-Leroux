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

### Q.2.1.1 Sur le serveur, créer un compte pour ton usage personnel.

```bash
#Créer l'utilisateur Math (sous compte root)
useradd -m -s /bin/bash Math

#Créer le mot de passe pour l'utilisateur
passwd Math
```

### Q.2.1.2 Quelles préconisations proposes-tu concernant ce compte ?
- Un dossier utilisateur à l'emplacement de /home
- Un mot de passe robuste de 8 caractères dont au moins une majuscule et un caratère spécial
- Pas de droits root de base mais la possibilité d'effectuer des tâches d'administration en étant ajouté au groupe __sudo__ plus tard

## Partie 2 : Configuration de SSH
La configuration demandé pour toutes les questions de cette partie a été effectué en éditant le fichier à l'emplacement `/etc/ssh/sshd_conf.d/local.conf`. La capture de cette configuration répondant à toutes les questions est à la suite de la question __Q.2.2.3__

### Q.2.2.1 Désactiver complètement l'accès à distance de l'utilisateur root.
### Q.2.2.2 Autoriser l'accès à distance à ton compte personnel uniquement.
### Q.2.2.3 Mettre en place une authentification par clé valide et désactiver l'authentification par mot de passe

![lione02](https://github.com/Tr3n4rT/TSSR-CHECKPOINT-3-Mathieu-Leroux/blob/main/images/configuration-ssh.png)


## Partie 3 : Analyse du stockage

### Q.2.3.1 Quels sont les systèmes de fichiers actuellement montés ?
- linux_raid_member
- ext2
- LVM2_member
- ext4
- swap

### Q.2.3.2 Quel type de système de stockage ils utilisent ?
- Disk
- Raid1
- lvm

### Q.2.3.3 Ajouter un nouveau disque de 8,00 Gio au serveur et réparer le volume RAID

### Q.2.3.4 Ajouter un nouveau volume logique LVM de 2 Gio qui servira à héberger des sauvegardes. Ce volume doit être monté automatiquement à chaque démarrage dans l'emplacement par défaut : /var/lib/bareos/storage.

### Q.2.3.5 Combien d'espace disponible reste-t-il dans le groupe de volume ?
