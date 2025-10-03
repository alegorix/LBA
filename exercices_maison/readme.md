# ☕ Projet de Site Web : Le Grain Doré

Ce dépôt contient deux journées-projets complètes (8 heures chacune). L'objectif est de construire un site web de A à Z pour un café fictif, "Le Grain Doré".

- **Jour 1 :** Création de toute la structure du site avec HTML sémantique.
- **Jour 2 :** Mise en forme et responsive design avec CSS.

---

## 📅 Jour 1 : Projet HTML (8h) - Le Squelette du Site

**Objectif :** Maîtriser la structure HTML en construisant le squelette d'un site de 4 pages. À la fin, le site sera fonctionnel mais sans aucun style.

### **Bloc 1 : Planification et Page d'Accueil (2h)**

1.  **Préparation de l'environnement :**
    - Créez un dossier principal : `le-grain-dore`
    - À l'intérieur, créez la structure suivante :
      ```
      le-grain-dore/
      ├── index.html
      ├── pages/
      └── images/
      ```

2.  **Structure de base de `index.html` :**
    - Ajoutez le squelette HTML5.
    - Dans le `<head>`, ajoutez un `<title>` et les balises `<meta>` essentielles.
    - Dans le `<body>`, définissez les zones sémantiques : `<header>`, `<nav>`, `<main>`, `<footer>`.

3.  **Contenu du Header, Footer et Navigation :**
    - Remplissez le `<header>` avec un `<h1>Le Grain Doré</h1>`.
    - Dans le `<footer>`, ajoutez un paragraphe de copyright.
    - Dans la balise `<nav>`, créez le menu avec une liste `<ul>` contenant les liens vers les pages :
      ```html
      <nav>
        <ul>
          <li><a href="index.html">Accueil</a></li>
          <li><a href="pages/carte.html">Notre Carte</a></li>
          <li><a href="pages/galerie.html">Galerie</a></li>
          <li><a href="pages/contact.html">Contact</a></li>
        </ul>
      </nav>
      ```

### **Bloc 2 : Contenu des Pages (2h)**

1.  **Finaliser la Page d'Accueil (`index.html`) :**
    - Dans `<main>`, ajoutez des sections `<section>` pour la présentation du café et ses spécialités, avec des titres `<h2>`, des paragraphes `<p>` et une image `<img>` (utilisez `https://via.placeholder.com/300` pour l'instant).

2.  **Créer la Page "Notre Carte" (`pages/carte.html`) :**
    - Copiez la structure de `index.html`.
    - Modifiez le titre.
    - Dans `<main>`, utilisez des listes de description `<dl>`, `<dt>`, `<dd>` pour présenter le menu des cafés et des pâtisseries.

### **Bloc 3 : Pages "Galerie" et "Contact" (2h30)**

1.  **Créer la Page "Galerie" (`pages/galerie.html`) :**
    - Copiez la structure de base.
    - Dans `<main>`, créez une galerie avec plusieurs balises `<figure>`, contenant chacune une `<img>` et une `<figcaption>`.

2.  **Créer la Page "Contact" (`pages/contact.html`) :**
    - Copiez la structure de base.
    - Ajoutez une section pour l'adresse.
    - Créez un formulaire de contact `<form>` complet avec des `<label>`, des `<input>` (text, email), une `<textarea>` et un `<button>`.

### **Bloc 4 : Finalisation et Vérification (1h30)**

1.  **Vérification des Liens :**
    - Ouvrez `index.html` dans votre navigateur et testez **tous** les liens du menu.
    - **Attention :** Pour les pages dans le dossier `pages/`, le lien vers la page d'accueil doit être `../index.html`.

2.  **Nettoyage du Code :**
    - Assurez-vous que votre code est bien indenté.
    - Vérifiez que toutes les images ont un attribut `alt` descriptif.

---

## 🎨 Jour 2 : Projet CSS (8h) - Donner Vie au Site

**Objectif :** Appliquer des styles, créer une mise en page avec Flexbox/Grid et rendre le site responsive.

### **Bloc 1 : Configuration et Styles Globaux (2h)**

1.  **Lier la feuille de style :**
    - Créez un dossier `css` et à l'intérieur un fichier `style.css`.
    - Liez ce fichier à **toutes** vos pages HTML via la balise `<link>` dans le `<head>`.
      ```html
      <link rel="stylesheet" href="css/style.css">
      
      <link rel="stylesheet" href="../css/style.css">
      ```

2.  **Reset et Variables CSS :**
    - Dans `style.css`, commencez par un "reset" de base et définissez des variables pour les couleurs et polices.
      ```css
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }
      
      :root {
        --primary-color: #6a4f4b; /* Marron café */
        --secondary-color: #f4e8d8; /* Beige clair */
        --text-color: #333;
        --main-font: 'Arial', sans-serif;
      }
      h1 {
        color: var(--primary-color); /* Applique la couleur #6a4f4b */
        }

      body {
        font-family: var(--main-font); /* Applique la police 'Arial', sans-serif */
        background-color: var(--secondary-color); /* Applique le fond beige clair */
        }

      ```

3.  **Styles de base :**
    - Appliquez vos variables au `<body>` (police, couleurs).
    - Définissez les styles pour les titres (`h1`, `h2`) et les paragraphes.
    - Créez une classe `.container` pour centrer le contenu et appliquez-la aux balises `<main>`.

### **Bloc 2 : Layout et Navigation (2h)**

1.  **Styliser Header et Footer :**
    - Donnez-leur une couleur de fond (`background-color`), de l'espacement interne (`padding`) et centrez le texte.

2.  **Barre de Navigation avec Flexbox :**
    - Ciblez la liste `nav ul` pour aligner les éléments horizontalement.
      ```css
      nav ul {
        list-style: none;
        display: flex;
        justify-content: center;
        background-color: var(--primary-color);
        padding: 15px 0;
      }
      ```
    - Stylisez les liens `nav a` (couleur, décoration de texte, padding) et ajoutez un effet au survol (`:hover`).

### **Bloc 3 : Style des Composants (2h30)**

1.  **Galerie d'images avec Grid :**
    - Utilisez CSS Grid pour créer une grille d'images responsive.
      ```css
      .gallery-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 15px;
      }
      ```

2.  **Formulaire de Contact :**
    - Stylisez les champs `<input>`, `<textarea>` et le `<button>` pour un look moderne et une bonne expérience utilisateur.

### **Bloc 4 : Responsive Design (1h30)**

1.  **Ajouter la balise Meta Viewport :**
    - Assurez-vous que cette ligne est présente dans le `<head>` de **toutes** vos pages HTML.
      ```html
      <meta name="viewport" content="width=device-width, initial-scale=1.0">
      ```

2.  **Media Queries :**
    - À la fin de `style.css`, ajoutez des media queries pour ajuster la mise en page sur les écrans plus petits.
      ```css
      /* Pour tablettes et écrans plus petits */
      @media (max-width: 768px) {
        nav ul {
          flex-direction: column; /* Empile les liens verticalement */
        }
      }
      
      /* Pour mobiles */
      @media (max-width: 480px) {
        body {
          font-size: 14px; /* Réduit la taille de la police */
        }
      }
      ```

---

## 🚀 Comment Utiliser ce Dépôt

1.  **Clonez ou téléchargez** ce dépôt.
2.  **Suivez l'exercice du Jour 1** en créant et modifiant les fichiers HTML.
3.  **Continuez avec l'exercice du Jour 2** en écrivant le code dans le fichier `style.css`.
4.  Ouvrez le fichier `index.html` dans votre navigateur à tout moment pour voir votre progression.
5.  Utilisez les outils de développement de votre navigateur (F12) pour tester le responsive design.

Bon codage !
