# 🍷 Tempus Vinum

**Tempus Vinum** est une application web élégante de gestion de cave à vin, entièrement développée en un seul fichier HTML. Gérez votre collection de vins avec style et simplicité.

![Tempus Vinum](https://img.shields.io/badge/Version-1.0-8B0000?style=for-the-badge)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)

---

## 📋 Table des matières

- [Fonctionnalités](#-fonctionnalités)
- [Aperçu](#-aperçu)
- [Installation](#-installation)
- [Utilisation](#-utilisation)
- [Stockage des données](#-stockage-des-données)
- [Technologies](#-technologies)
- [Configuration personnalisée](#-configuration-personnalisée)
- [Contribution](#-contribution)
- [Licence](#-licence)

---

## ✨ Fonctionnalités

### 🎯 Gestion de cave personnalisable
- **Configuration flexible** : Définissez le nombre d'étagères et d'emplacements selon votre cave réelle
- **Zone spéciale** : Espace dédié aux grandes bouteilles (Magnum, Jéroboam, Champagne)
- **Représentation visuelle 3D** : Interface graphique réaliste avec effet de cave en bois
- **Code couleur** : Identification visuelle rapide par type de vin (Rouge, Blanc, Rosé, Champagne, Autre)

### 📝 Informations détaillées sur chaque bouteille
- **Informations générales** : Appellation, Domaine, Récoltant, Millésime
- **Caractéristiques** : Couleur, Type, Région, Pays, Cépage, Degré d'alcool, Contenance
- **Conservation** : Prix d'achat, Date limite de consommation, Bio/Biodynamie
- **Accords mets/vins** : Recherche automatique via l'API Claude (Anthropic)
- **Notes personnelles** : Vos commentaires et dégustations

### 📊 Statistiques en temps réel
- Nombre total de bouteilles
- Emplacements vides disponibles
- Valeur totale de la collection

### 🔍 Inventaire et recherche
- Liste complète de toutes vos bouteilles
- Moteur de recherche par nom, domaine, appellation, année, région
- Accès rapide aux détails de chaque bouteille

### 💾 Sauvegarde automatique
- Stockage local dans le navigateur (localStorage)
- Aucune connexion internet requise après le chargement
- Données conservées entre les sessions

---

## 🖼️ Aperçu

### Configuration de la cave
Interface intuitive pour définir la structure de votre cave avec configuration suggérée basée sur une cave standard (5 étagères × 6 emplacements + 7 grandes bouteilles).

### Vue de la cave
Représentation graphique 3D avec :
- Fond bois sombre réaliste
- Emplacements avec effet de profondeur
- Code couleur par type de vin
- Animation au survol
- Icônes 🍷 et 🍾

### Inventaire
Liste détaillée et recherchable de toute votre collection avec toutes les informations essentielles.

---

## 🚀 Installation

### Option 1 : Téléchargement direct

1. Téléchargez le fichier `tempus-vinum.html`
2. Ouvrez-le avec votre navigateur préféré
3. C'est tout ! Aucune installation supplémentaire nécessaire

### Option 2 : Clone du dépôt
```bash
git clone https://github.com/votre-username/tempus-vinum.git
cd tempus-vinum
```

Ouvrez ensuite `tempus-vinum.html` dans votre navigateur.

### Option 3 : GitHub Pages

1. Forkez ce dépôt
2. Activez GitHub Pages dans les paramètres
3. Accédez à `https://votre-username.github.io/tempus-vinum/`

---

## 📖 Utilisation

### 1. Configuration initiale

**Première utilisation :**
1. Allez dans l'onglet **Configuration**
2. Cliquez sur **"Appliquer cette configuration"** pour la configuration suggérée (5×6 + 7)
3. Ou définissez votre propre configuration personnalisée

### 2. Ajouter une bouteille

1. Allez dans l'onglet **Ma Cave**
2. Cliquez sur un emplacement vide (symbole **+**)
3. Remplissez les informations de la bouteille
4. Cliquez sur **Enregistrer**

**💡 Astuce** : Laissez le champ "Accords mets/vins" vide pour une suggestion automatique via l'API Claude.

### 3. Modifier ou supprimer une bouteille

1. Cliquez sur l'emplacement occupé
2. Modifiez les informations souhaitées
3. **Enregistrer** pour sauvegarder ou **Supprimer** pour retirer la bouteille

### 4. Rechercher dans l'inventaire

1. Allez dans l'onglet **Inventaire**
2. Utilisez la barre de recherche pour filtrer par :
   - Nom du domaine
   - Appellation
   - Année
   - Région

---

## 💾 Stockage des données

### LocalStorage

Toutes vos données sont stockées localement dans votre navigateur via `localStorage` :

- **Avantages** :
  - Aucun serveur requis
  - Données privées et sécurisées
  - Fonctionnement hors ligne
  - Gratuit et illimité

- **Limitations** :
  - Données liées au navigateur utilisé
  - Suppression si vous effacez les données de navigation
  - Non synchronisé entre appareils

### Sauvegarde manuelle

**Pour sauvegarder vos données :**
1. Ouvrez la console du navigateur (F12)
2. Tapez : `localStorage.getItem('wineCellar')`
3. Copiez le résultat dans un fichier texte

**Pour restaurer vos données :**
1. Ouvrez la console du navigateur
2. Tapez : `localStorage.setItem('wineCellar', 'VOTRE_SAUVEGARDE')`
3. Rechargez la page

### Migration vers Supabase (optionnel)

Pour synchroniser entre appareils, vous pouvez intégrer Supabase :

1. Créez un compte sur [supabase.com](https://supabase.com)
2. Créez une table `wines` avec les colonnes appropriées
3. Modifiez les fonctions `loadData()` et `saveData()` pour utiliser l'API Supabase

---

## 🛠️ Technologies

- **HTML5** : Structure de l'application
- **CSS3** : Design moderne avec gradients et animations
- **JavaScript (Vanilla)** : Logique applicative sans framework
- **LocalStorage API** : Persistance des données
- **Anthropic Claude API** : Suggestions d'accords mets/vins (optionnel)

### Architecture

- **Fichier unique** : Tout le code dans un seul fichier HTML
- **Aucune dépendance externe** : Pas de bibliothèques tierces
- **Responsive** : Adapté mobile et desktop
- **Progressive Web App ready** : Peut être converti en PWA

---

## ⚙️ Configuration personnalisée

### Modifier les tailles par défaut

Dans le fichier HTML, ligne ~700 :
```javascript
config: { rows: 5, cols: 6, specialZone: 7 }
```

### Personnaliser les couleurs

Dans la section `<style>`, lignes ~150-180, modifiez les gradients :
```css
.cell.red { 
    background: linear-gradient(145deg, #8B0000 0%, #5a0000 100%);
}
```

### Ajouter de nouvelles contenances

Ligne ~430 dans le HTML :
```html

    375 ml (Demi-bouteille)
    750 ml (Bouteille standard)
    

```

---

## 🤝 Contribution

Les contributions sont les bienvenues ! Voici comment participer :

1. **Forkez** le projet
2. **Créez** une branche pour votre fonctionnalité (`git checkout -b feature/AmazingFeature`)
3. **Committez** vos changements (`git commit -m 'Add some AmazingFeature'`)
4. **Pushez** vers la branche (`git push origin feature/AmazingFeature`)
5. **Ouvrez** une Pull Request

### Idées de contributions

- [ ] Export/Import en CSV
- [ ] Graphiques statistiques
- [ ] Mode sombre
- [ ] Impression de l'inventaire
- [ ] Scan de codes-barres
- [ ] Intégration avec des bases de données de vins (Vivino, Wine-Searcher)
- [ ] Mode multi-caves
- [ ] Notifications pour les vins à boire
- [ ] Historique de dégustation

---

## 📄 Licence

Ce projet est sous licence **MIT** - voir le fichier [LICENSE](LICENSE) pour plus de détails.
```
MIT License

Copyright (c) 2024 Tempus Vinum

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
```

---

## 🙏 Remerciements

- Design inspiré des caves à vin traditionnelles
- API Claude par [Anthropic](https://www.anthropic.com) pour les suggestions d'accords
- Icônes emoji pour l'interface utilisateur

---

## 📧 Contact

**Créateur** : Marc Seatelli  
**Email** : mseatelli@gmail.com  
**Projet** : [https://github.com/mseatelli/tempus-vinum](https://github.com/mseatelli/tempus-vinum)

---

## 🍷 Profitez de votre cave !

*"Le temps révèle le vin - Tempus Vinum"*

⭐ Si vous aimez ce projet, n'oubliez pas de lui donner une étoile !
