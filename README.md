# Hexa-Data Node-RED Integration

Hexa-Data, propulsé par Node-RED, offre une plateforme robuste pour l'automatisation et la gestion de projets IoT. Cette intégration permet aux utilisateurs de créer des applications qui interagissent en temps réel avec diverses données et systèmes, grâce à une série de nœuds personnalisés.

## Caractéristiques Principales

Hexa-Data comprend une bibliothèque de nœuds spécialement conçus pour une intégration facile et efficace. Voici quelques nœuds clés disponibles :

- **Lecture dernières valeurs** : Récupère les dernières valeurs des variables.
- **Lecture historique** : Obtient l'historique des variables sur une plage de temps spécifiée.
- **Création d’un rapport** : Génère des rapports dans différents formats.
- **Recherche rapport** : Liste les rapports disponibles.
- **Supprimer rapport** : Supprime un rapport spécifique.
- **Envoyer SMS** : Envoie des SMS à des numéros spécifiés.
- **Envoyer mail** : Envoie un email avec ou sans pièce jointe.

## Utilisation des Nœuds

### Lecture dernières valeurs

- **Paramètres** :
  - `Classname` : Nom de la variable, supporte les expressions régulières.
  - `Labels` : Filtre les résultats par labels (format JSON).

### Lecture historique

- **Paramètres** :
  - `Classname` : Identique à ci-dessus.
  - `Labels` : Identique à ci-dessus.
- **Entrées** :
  - `msg.from` et `msg.to` : Début et fin de la période de requête en timestamp.

### Création rapport

- **Paramètres** :
  - `Filename` : Nom du fichier à créer.
- **Entrées** :
  - `msg.payload` : Contenu du rapport.
  - `msg.filename` : Nom du fichier (dynamique).

### Envoyer SMS

- **Paramètres** :
  - `Receivers` : Numéros des destinataires.
  - `Message` : Contenu du SMS.
- **Entrées** :
  - `msg.receivers` : Liste des destinataires (format tableau de STRING).
  - `msg.payload` : Message.

### Envoyer mail

- **Paramètres** :
  - `Receivers`, `Subject`, `Message` : Détails du mail.
  - `Attachment Id` et `Attachment name` : Identifiant et nom du fichier joint.
- **Entrées** :
  - Définies dynamiquement via `msg`.

## Configuration

Assurez-vous de configurer Node-RED et Hexa-Data selon les besoins de votre projet pour une utilisation optimale de ces nœuds.

## Contribution

Les contributions à cette bibliothèque sont les bienvenues. Pour contribuer, veuillez soumettre une pull request avec vos améliorations ou ouvrir un issue pour discuter des modifications potentielles.

## Licence

Ce projet est distribué sous la licence MIT. Voir le fichier `LICENSE` pour plus de détails.
