# 🗺️ JobMap by LTd

**Trouvez des Emplois et Candidats sur une Carte Interactive**

JobMap est une application web innovante qui révolutionne le recrutement en combinant la puissance de la cartographie interactive avec des fonctionnalités avancées de recherche d'emploi et de gestion de candidatures.

![JobMap Interface](https://github.com/user-attachments/assets/d91ea0cc-ada3-4a27-9c2b-079f69a6a8e5)

## ✨ Caractéristiques principales

### 🎯 Pour les Recruteurs
- **Publication d'offres enrichies** avec tous les détails (salaire, contrat, télétravail)
- **Tableau de bord** avec statistiques en temps réel
- **Gestion des candidatures** reçues
- **Système de favoris** pour sauvegarder les meilleurs profils
- **Association candidats-offres** avec calcul d'itinéraire

### 💼 Pour les Candidats
- **Recherche avancée** avec filtres multiples
- **Candidature en 1 clic** sur les offres qui vous intéressent
- **Suivi des candidatures** avec statuts
- **Favoris** pour sauvegarder les offres intéressantes
- **Visualisation géographique** des opportunités

### 🗺️ Cartographie Interactive
- **Carte Leaflet** avec marqueurs personnalisés
- **Clustering automatique** pour les zones denses
- **Calcul d'itinéraire** (voiture, vélo, marche)
- **Géolocalisation** automatique
- **Navigation fluide** avec zoom et déplacement

## 🚀 Démarrage rapide

### Prérequis
Aucun ! L'application fonctionne directement dans votre navigateur.

### Installation

1. **Cloner le dépôt**
```bash
git clone https://github.com/lyam08888/JobMap-by-LTd.git
cd JobMap-by-LTd
```

2. **Ouvrir l'application**
```bash
# Option 1 : Ouvrir directement le fichier
open index.html

# Option 2 : Utiliser un serveur local
python3 -m http.server 8000
# Puis naviguer vers http://localhost:8000
```

3. **C'est tout !** 🎉

## 📚 Documentation

- **[FEATURES.md](FEATURES.md)** - Guide complet des fonctionnalités pour utilisateurs
- **[TECHNICAL.md](TECHNICAL.md)** - Documentation technique pour développeurs

## 🎯 Utilisation

### Création de compte

1. Cliquez sur l'icône utilisateur en haut à gauche
2. Choisissez "Je suis candidat" ou "Je suis recruteur"
3. Remplissez le formulaire d'inscription
4. Connectez-vous et profitez de toutes les fonctionnalités !

### Recherche d'emploi

1. Utilisez la barre de recherche pour trouver des postes
2. Activez les filtres avancés pour affiner votre recherche
3. Cliquez sur les résultats pour voir les détails
4. Postulez en un clic ou sauvegardez en favoris

### Publication d'offre

1. Connectez-vous en tant que recruteur
2. Cliquez sur "Poster une offre" dans le menu
3. Remplissez le formulaire complet
4. Votre offre apparaît immédiatement sur la carte !

## 🛠️ Technologies

- **Frontend:** HTML5, CSS3, JavaScript ES6+
- **Cartographie:** Leaflet.js, Leaflet Routing Machine, Marker Cluster
- **Style:** Tailwind CSS
- **Icônes:** Font Awesome 6
- **Typographie:** Google Fonts (Inter)
- **Persistance:** LocalStorage API

## 📊 Fonctionnalités détaillées

### Filtres avancés
- ✅ Type de contrat (CDI, CDD, Freelance, Stage)
- ✅ Niveau d'expérience (Débutant, Junior, Confirmé, Senior)
- ✅ Mode de télétravail (Présentiel, Hybride, 100% Remote)
- ✅ Salaire minimum
- ✅ Localisation géographique

### Tri intelligent
- Par pertinence
- Par date (plus récent d'abord)
- Par salaire (croissant ou décroissant)

### Gestion des données
- Sauvegarde automatique des favoris
- Historique des candidatures
- Persistance locale (pas de perte de données)

## 🌟 Points forts

- **✨ Interface moderne** et intuitive
- **🚀 Performance optimisée** avec clustering et lazy loading
- **📱 Responsive** - fonctionne sur tous les appareils
- **🔒 Sécurisé** - données stockées localement
- **🌐 Sans backend** - déploiement simple et rapide
- **♿ Accessible** - navigation au clavier, contrastes élevés

## 📈 Données

L'application contient actuellement **22 offres d'emploi et profils de candidats** répartis dans **10 villes françaises** :
- Paris
- Lyon
- Marseille
- Toulouse
- Nice
- Nantes
- Strasbourg
- Montpellier
- Bordeaux
- Lille

## 🔧 Développement

### Structure du projet
```
JobMap-by-LTd/
├── index.html          # Application principale
├── FEATURES.md         # Documentation utilisateur
├── TECHNICAL.md        # Documentation technique
└── README.md          # Ce fichier
```

### Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. Fork le projet
2. Créez une branche (`git checkout -b feature/AmazingFeature`)
3. Committez vos changements (`git commit -m 'Add some AmazingFeature'`)
4. Push vers la branche (`git push origin feature/AmazingFeature`)
5. Ouvrez une Pull Request

## 🐛 Bugs connus

Aucun bug bloquant identifié. Si vous en trouvez un, merci d'ouvrir une issue !

## 📝 Changelog

### Version 2.0 (Octobre 2024)
- ✅ Ajout des filtres avancés
- ✅ Système de favoris complet
- ✅ Candidature en 1 clic
- ✅ Tableau de bord recruteur
- ✅ Enrichissement des données
- ✅ Documentation complète
- ✅ Amélioration de l'UI/UX

### Version 1.0 (Version initiale)
- Carte interactive basique
- Recherche simple
- Affichage des offres et candidats

## 🎯 Roadmap

### À court terme
- [ ] Tests automatisés
- [ ] Mode sombre
- [ ] Export CSV/PDF

### À moyen terme
- [ ] Backend avec API REST
- [ ] Authentification OAuth
- [ ] Messagerie intégrée
- [ ] Notifications push

### À long terme
- [ ] Application mobile (React Native)
- [ ] Intelligence artificielle pour matching
- [ ] Analytics avancés
- [ ] Intégrations tierces (LinkedIn, Indeed)

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## 👥 Auteurs

- **LTd Team** - *Développement initial et améliorations majeures*

## 🙏 Remerciements

- Leaflet.js pour la cartographie
- OpenStreetMap pour les données cartographiques
- OSRM pour le calcul d'itinéraire
- Tailwind CSS pour le framework CSS
- Font Awesome pour les icônes
- La communauté open source

## 📞 Contact

Pour toute question ou suggestion, n'hésitez pas à ouvrir une issue sur GitHub.

---

**Fait avec ❤️ en France** 🇫🇷

*JobMap by LTd - Votre carrière commence ici*
