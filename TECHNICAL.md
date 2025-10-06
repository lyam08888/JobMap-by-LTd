# Guide Technique - JobMap

## Architecture

### Structure du fichier
```
index.html
├── HEAD (Styles et CDN)
├── BODY
│   ├── Startup Overlay (animation de démarrage)
│   ├── Toast Container (notifications)
│   ├── Map Container (carte Leaflet)
│   ├── UI Overlay
│   │   ├── User Menu
│   │   ├── Search Panel (recherche + filtres)
│   │   └── Routing Controls
│   └── Modals
│       ├── Details Modal
│       ├── Login Modal
│       ├── Signup Modals (candidate/employer)
│       ├── Post Job Modal
│       ├── Profile Modal
│       ├── Match Modal
│       ├── Favorites Modal
│       ├── Applications Modal
│       └── Dashboard Modal
```

## État de l'application

```javascript
// Variables d'état principales
let currentUser = null;              // Utilisateur connecté
let currentFilter = 'all';           // Filtre actif (all/job/candidate)
let currentSort = 'relevance';       // Tri actif
let advancedFilters = {...};         // Filtres avancés
let routingControl = null;           // Contrôle d'itinéraire Leaflet
let userLocation = {...};            // Position de l'utilisateur
let routeStartPoint = null;          // Point de départ pour itinéraire
let candidateToMatch = null;         // Candidat à associer

// Données
let data = [...];                    // Offres et candidats
let savedJobs = [...];               // IDs des offres sauvegardées
let savedCandidates = [...];         // IDs des candidats sauvegardés
let applications = [...];            // Candidatures envoyées
```

## Fonctions principales

### Utilitaires
- `showToast(message, type)` - Affiche une notification
- `toggleFavorite(itemId, itemType)` - Gère les favoris
- `isFavorite(itemId, itemType)` - Vérifie si en favori
- `applyToJob(jobId, ...)` - Enregistre une candidature
- `sortData(dataToSort)` - Trie les données selon currentSort

### Modals
- `openModal(modalId)` - Ouvre un modal
- `closeAllModals()` - Ferme tous les modals
- `showDetailsModal(itemId)` - Affiche détails offre/candidat
- `openFavoritesModal()` - Affiche les favoris
- `openApplicationsModal()` - Affiche les candidatures
- `openDashboardModal()` - Affiche le tableau de bord recruteur
- `openMatchModal(candidateId)` - Associe candidat à offre

### Authentification
- `updateAuthUI()` - Met à jour le menu utilisateur

### Carte
- `displayData(filteredData, showList)` - Affiche marqueurs et liste
- `getUserLocation()` - Géolocalise l'utilisateur
- `calculateRoute(start, end, profile)` - Calcule un itinéraire
- `clearRoute()` - Efface l'itinéraire

### Recherche
- `performSearch()` - Applique recherche et filtres

## Modèle de données

### Offre d'emploi (Job)
```javascript
{
    id: number,
    type: 'job',
    title: string,
    company: string,
    location: { lat: number, lon: number },
    city: string,
    tags: string[],
    description: string,
    salary: string,              // Format: "35000-50000"
    contractType: string,        // CDI, CDD, Freelance, Stage
    experience: string,          // Débutant, Junior, Confirmé, Senior
    remote: string,              // Présentiel, Hybride, Remote
    postedDate: string           // Format: YYYY-MM-DD
}
```

### Profil candidat (Candidate)
```javascript
{
    id: number,
    type: 'candidate',
    name: string,
    title: string,
    location: { lat: number, lon: number },
    city: string,
    tags: string[],
    description: string,
    experience: string,          // Débutant, Junior, Confirmé, Senior
    availability: string,        // Immédiate, 1 mois, 2 mois, etc.
    expectedSalary: string,      // Format: "35000-50000"
    email: string,
    phone: string
}
```

### Candidature (Application)
```javascript
{
    id: number,
    jobId: number,
    candidateName: string,
    candidateEmail: string,
    coverLetter: string,
    status: string,              // Envoyée, En cours, Acceptée, Refusée
    date: string                 // ISO timestamp
}
```

### Utilisateur (User)
```javascript
{
    name: string,
    email: string,
    type: string                 // 'recruiter' or 'candidate'
}
```

## LocalStorage

```javascript
// Clés utilisées
localStorage.getItem('savedJobs')           // Array<number>
localStorage.getItem('savedCandidates')     // Array<number>
localStorage.getItem('applications')        // Array<Application>
```

## Événements

### Recherche et filtres
```javascript
searchInput.addEventListener('keyup', performSearch);
filterButtons.addEventListener('click', changeFilter);
sortDropdown.addEventListener('change', changeSort);
advancedFilters.addEventListener('change', performSearch);
```

### Carte
```javascript
resultsList.addEventListener('click', showDetails);
map.on('popupopen', attachDetailsButton);
```

### Modals
```javascript
document.addEventListener('click', closeModalOnBackdrop);
formSubmit.addEventListener('submit', handleFormSubmit);
```

## Styles CSS personnalisés

### Classes importantes
- `.custom-marker-icon` - Marqueurs de carte
- `.filter-btn.active` - Bouton de filtre actif
- `.toast.show` - Notification visible
- `.favorites-tab-btn.active` - Onglet favori actif
- `.modal-backdrop` - Fond de modal
- `.modal-panel` - Contenu de modal

### Transitions
- Modals : fade in/out avec scale
- Toast : slide up from bottom
- Filters : smooth background color
- User menu : opacity + transform

## Dépendances externes

### CDN utilisés
```html
<!-- Tailwind CSS -->
<script src="https://cdn.tailwindcss.com"></script>

<!-- Leaflet (carte) -->
<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"></script>

<!-- Leaflet Routing Machine -->
<link rel="stylesheet" href="https://unpkg.com/leaflet-routing-machine@latest/dist/leaflet-routing-machine.css" />
<script src="https://unpkg.com/leaflet-routing-machine@latest/dist/leaflet-routing-machine.js"></script>

<!-- Leaflet Marker Cluster -->
<link rel="stylesheet" href="https://unpkg.com/leaflet.markercluster@1.4.1/dist/MarkerCluster.css" />
<script src="https://unpkg.com/leaflet.markercluster@1.4.1/dist/leaflet.markercluster.js"></script>

<!-- Font Awesome -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
```

## Améliorations futures possibles

### Backend
- API REST pour authentification
- Base de données PostgreSQL/MongoDB
- Upload de fichiers (CV, photos)
- Email notifications
- WebSocket pour temps réel

### Frontend
- React/Vue pour composants réutilisables
- TypeScript pour typage statique
- Tests unitaires (Jest)
- Tests E2E (Cypress/Playwright)
- PWA avec service worker
- Webpack/Vite pour bundling

### Fonctionnalités
- Chat intégré
- Vidéo-conférence
- Calendrier de rendez-vous
- Système de rating
- Analytics avancés
- Export PDF/CSV
- API publique

## Performance

### Optimisations actuelles
- Marker clustering pour performance carte
- Debouncing sur recherche
- LocalStorage pour cache
- Lazy loading des modals

### Optimisations possibles
- Virtual scrolling pour longues listes
- Image lazy loading
- Code splitting
- Service worker caching
- CDN pour assets statiques

## Compatibilité

### Navigateurs supportés
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+

### Fonctionnalités requises
- ES6+ JavaScript
- LocalStorage
- Geolocation API
- Fetch API
- CSS Grid/Flexbox

## Déploiement

### Fichiers à déployer
```
index.html          (application principale)
FEATURES.md         (documentation utilisateur)
TECHNICAL.md        (documentation technique)
```

### Hébergement recommandé
- GitHub Pages (gratuit)
- Netlify (gratuit)
- Vercel (gratuit)
- Amazon S3 + CloudFront
- Azure Static Web Apps

### Configuration minimale
Aucune configuration serveur requise - application 100% client-side.
Il suffit de servir le fichier HTML avec n'importe quel serveur web.

## Debug

### Console logs utiles
```javascript
console.log('Current user:', currentUser);
console.log('Filtered data:', filteredData);
console.log('Saved jobs:', savedJobs);
console.log('Applications:', applications);
```

### Vérification LocalStorage
```javascript
// Dans la console du navigateur
localStorage.getItem('savedJobs')
localStorage.getItem('savedCandidates')
localStorage.getItem('applications')

// Reset
localStorage.clear()
```

### Test des modals
```javascript
// Dans la console
openModal('favorites-modal')
openModal('dashboard-modal')
openModal('applications-modal')
```
