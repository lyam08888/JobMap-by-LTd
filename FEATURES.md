# JobMap - Guide des Fonctionnalités

## 🎯 Vue d'ensemble

JobMap est une application de cartographie interactive pour mettre en relation recruteurs et candidats. Cette version améliorée offre une expérience complète et fluide pour tous les utilisateurs.

## 👥 Pour les Recruteurs

### Publication d'offres enrichie
- **Titre du poste** : Nom du poste à pourvoir
- **Localisation** : Ville et position sur la carte
- **Description détaillée** : Présentation complète du poste
- **Compétences requises** : Liste des technologies/compétences
- **Informations contractuelles** :
  - Type de contrat (CDI, CDD, Freelance, Stage)
  - Fourchette de salaire
  - Niveau d'expérience requis (Débutant, Junior, Confirmé, Senior)
  - Mode de télétravail (Présentiel, Hybride, 100% Remote)

### Tableau de bord
Accessible depuis le menu utilisateur, le tableau de bord affiche :
- Nombre d'offres publiées
- Nombre de candidatures reçues
- Nombre de candidats sauvegardés
- Liste de vos offres avec détails
- Nombre de candidatures par offre

### Gestion des candidats
- **Favoris** : Sauvegarder les profils intéressants en un clic
- **Association** : Créer un itinéraire entre un candidat et une offre
- **Vue détaillée** : Accès aux coordonnées et informations complètes

## 💼 Pour les Candidats

### Recherche d'emploi avancée
- **Recherche textuelle** : Par poste, compétence, entreprise ou ville
- **Filtres de base** : Tous / Emplois / Profils
- **Filtres avancés** :
  - Type de contrat
  - Niveau d'expérience
  - Mode de télétravail
  - Salaire minimum
- **Tri** : Par pertinence, date, salaire

### Candidature simplifiée
- Postuler en un clic depuis la fiche détaillée d'une offre
- Statut visible (candidature envoyée)
- Suivi de toutes vos candidatures dans un espace dédié

### Gestion personnelle
- **Favoris** : Sauvegarder les offres intéressantes
- **Mes candidatures** : Voir toutes vos candidatures avec leur statut
- **Profil** : Accès à votre profil et informations

## 🗺️ Fonctionnalités cartographiques

### Visualisation interactive
- Marqueurs colorés : Bleu pour les emplois, Vert pour les candidats
- Clusters automatiques pour les zones denses
- Popups avec informations rapides
- Zoom et navigation fluides

### Calcul d'itinéraire
1. Définir un point de départ (bouton "Départ")
2. Sélectionner une destination (bouton "Arrivée")
3. Choisir le mode de transport : Voiture, Vélo, Marche
4. Visualiser l'itinéraire sur la carte

### Géolocalisation
- Détection automatique de votre position
- Marqueur personnalisé pour votre localisation
- Recherche facilitée autour de vous

## 💾 Persistance des données

Toutes les données importantes sont sauvegardées localement :
- **Favoris** : Jobs et candidats sauvegardés
- **Candidatures** : Historique complet
- Les données restent disponibles même après fermeture du navigateur

## 🎨 Interface utilisateur

### Design moderne
- Interface épurée et professionnelle
- Typographie Google Fonts (Inter)
- Icônes Font Awesome
- Animations fluides et transitions

### Responsive
- Adapté aux ordinateurs de bureau
- Compatible tablettes
- Optimisé pour mobile

### Notifications
- Messages de confirmation pour chaque action
- Toast notifications colorés (succès, info, erreur)
- Feedback visuel immédiat

## 📊 Données enrichies

### 22 offres et profils complets
Chaque offre d'emploi contient :
- Titre et entreprise
- Localisation précise
- Salaire proposé
- Type de contrat
- Niveau d'expérience
- Mode de télétravail
- Compétences requises
- Date de publication

Chaque profil candidat contient :
- Nom et titre professionnel
- Localisation
- Expérience professionnelle
- Disponibilité
- Prétention salariale
- Compétences
- Contact (email, téléphone)

## 🔐 Authentification

Deux types de comptes :
- **Recruteur** : Publier des offres, gérer les candidatures
- **Candidat** : Postuler, sauvegarder des offres

## 🚀 Utilisation rapide

1. **Sans compte** : Explorer la carte et voir toutes les offres/candidats
2. **Créer un compte candidat** : Postuler et sauvegarder vos favoris
3. **Créer un compte recruteur** : Publier des offres et trouver des talents
4. **Rechercher** : Utiliser la barre de recherche et les filtres avancés
5. **Naviguer** : Cliquer sur les marqueurs ou les cartes de résultats
6. **Agir** : Postuler, sauvegarder, calculer un itinéraire

## 🎯 Cas d'usage

### Recruteur cherchant un développeur
1. Se connecter avec un compte recruteur
2. Filtrer par "Profils" + "Développeur" dans la recherche
3. Affiner avec filtres avancés (expérience, localisation)
4. Consulter les profils intéressants
5. Sauvegarder en favoris les meilleurs candidats
6. Associer un candidat à une offre existante
7. Calculer l'itinéraire pour un éventuel rendez-vous

### Candidat cherchant un emploi
1. Se connecter avec un compte candidat
2. Rechercher par compétences (ex: "React")
3. Filtrer par "Remote" ou "Hybride"
4. Définir un salaire minimum
5. Trier par salaire décroissant
6. Consulter les offres détaillées
7. Postuler en un clic
8. Sauvegarder les offres intéressantes pour plus tard
9. Suivre ses candidatures dans l'espace dédié

## 💡 Astuces

- **Favoris** : Cliquez sur le cœur pour sauvegarder rapidement
- **Itinéraire** : Définissez le départ puis la destination pour un calcul automatique
- **Filtres** : Combinez recherche textuelle et filtres avancés pour plus de précision
- **Carte** : Cliquez sur les résultats pour centrer la carte
- **Zoom** : Utilisez la molette ou les boutons +/- pour zoomer
- **Clusters** : Cliquez sur un cluster pour zoomer et voir le détail

## 🔄 Mises à jour futures

Fonctionnalités envisagées :
- Système de messagerie intégré
- Notifications en temps réel
- Export de données (CSV, PDF)
- Système de notation/avis
- API backend pour authentification réelle
- Mode sombre
- Multilingue
- Statistiques avancées
