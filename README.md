# Plugin Avis Clients Pro 🌟

Bienvenue dans **Avis Clients Pro**, l'extension WordPress ultime pour gérer, collecter et afficher très facilement les témoignages de vos clients avec un rendu ultra-premium.

Pensé pour la conversion et l'impact visuel, ce plugin vous offre des outils d'affichage dignes des plus grandes plateformes SaaS (façon Senja.io ou Trustpilot) sans avoir besoin de la moindre connaissance technique.

---

## 🚀 Fonctionnalités Principales

- **Gestion native simplifiée :** Un type de publication dédié "Avis clients" s'ajoute à votre menu WordPress pour ajouter ou modifier vos témoignages simplement.
- **Bloc Gutenberg Ultra-puissant :** Ajoutez le bloc "Avis Clients" sur n'importe quelle page ou article via l'éditeur de site (FSE) ou l'éditeur classique.
- **SEO & Schema.org Intégré :** Le plugin calcule automatiquement votre note moyenne et injecte le format `JSON-LD` (AggregateRating) de façon invisible. Google l'interprète pour afficher les **⭐⭐⭐⭐⭐ étoiles dorées dans les résultats de recherche** !
- **Design 100% Personnalisable :** Modifiez les polices (Google Fonts incluses), les couleurs, les ombres, les bordures, l'arrondi, ou la taille des avatars.
- **Icônes SVG sur-mesure :** Choisissez parmi les icônes incluses (Étoile, Cœur, Pouce, Feu...) ou **importez votre propre code SVG** pour vos notes !
- **Disposition Modulable :** Changez l'ordre des éléments à l'intérieur de la carte (Titre en premier, puis étoiles, puis texte, ou l'inverse) via 4 simples curseurs.

---

## 💡 Les 5 Catégories de Mise en Page

Le plugin propose **5 grands types de dispositions**, chacun incluant plusieurs sous-styles pour un rendu toujours parfait :

1. **▦ Grille (Grid) :**
   - *Standard* : Une grille classique, propre et aérée pour un grand mur de témoignages.
   - *Masonry* : Une grille déstructurée très moderne où les cartes s'imbriquent comme des briques.
   - *Citation* : Ajoute un grand guillemet d'ouverture en fond de carte.
   - *Avatars Pro* : Met l'accent sur le visage de vos clients pour un rendu "expert".

2. **⟵ Carousel :**
   - Un diaporama interactif avec flèches de navigation, points de pagination et fonction *Autoplay* (défilement automatique).

3. **→ Marquee (Défilement Continu) :**
   - Les avis défilent tout seuls de droite à gauche (ou de haut en bas) en boucle infinie. Idéal pour capter l'attention. S'arrête au survol de la souris !

4. **🏆 Badge / Preuve Sociale :**
   - Affiche un résumé de vos avis (ex: "4.5/5 basé sur 120 avis").
   - *Styles inclus* : Google Trust, Pill Flottante, Social Proof Stack (avatars empilés), Mega Score, Bandeau Ruban.

5. **📸 Galerie Visuelle :**
   - *Grille Captures* : Parfait pour mettre en avant une image (capture d'écran d'un tweet, photo d'un produit).
   - *Images Immersives* : L'image prend tout le fond de la carte et le texte s'affiche par-dessus avec un élégant dégradé sombre.

---

## 📖 Comment ajouter un avis ?

1. Dans le menu de gauche de votre administration WordPress, cliquez sur **Avis clients**.
2. Cliquez sur le bouton **Ajouter un nouvel avis**.
3. Remplissez les champs :
   - **Titre de l'avis :** Le titre principal de l'avis.
   - **Contenu :** Écrivez le témoignage complet de votre client.
   - **Image mise en avant (à droite) :** Ajoutez la photo de profil de votre client (son "avatar").
   - **Note sur 5 (en bas) :** Choisissez la note attribuée.
   - **Nom du client :** Saisissez le nom (ex: "Marie Dupont").
   - **Date :** Date à laquelle l'avis a été laissé.
4. Cliquez sur **Publier**. C'est en ligne !

---

## 🎨 Comment afficher les avis sur vos pages ?

Pour afficher vos avis, nous utilisons l'éditeur de page moderne de WordPress (Gutenberg).

1. Allez sur une de vos **Pages** ou **Articles** et cliquez sur "Modifier".
2. Cliquez sur le bouton **+** (Ajouter un bloc) et cherchez "Avis Clients".
3. Cliquez dessus pour l'insérer. Un menu de réglages complet apparaît sur la droite :

### ⚙️ Onglet Réglages (Roue crantée)
- **Requête & Filtres :** Choisissez combien d'avis afficher, l'ordre (date, note, aléatoire), ou filtrez par catégorie. *(Astuce : mettez -1 pour tous les afficher !)*
- **Mise en page :** Choisissez la disposition principale et le sous-style.
- **Disposition Interne :** Choisissez l'ordre d'affichage (Titre, Étoiles, Texte, Auteur) avec des curseurs (1 à 4).
- **Options du Carousel / Défilement :** Vitesse, autoplay, nombre de colonnes affichées.
- **Avatar :** Modifiez la taille et la forme (Rond, Arrondi, Carré).
- **Bouton Voir Plus :** Activez la troncature du texte long avec un bouton "Lire la suite".
- **Éléments affichés :** Masquez facilement le titre, la date ou les étoiles si vous n'en avez pas besoin.

### 🌙 Onglet Apparence (Demi-lune)
- **Style des cartes :** Changez la couleur de fond, configurez des bordures ou une ombre portée personnalisée. Configurez également de **superbes animations de survol** (Lift, Scale, Tilt, Glow, Push).
- **Typographie & Couleurs :** Changez les polices (plus de 25 typographies Google Fonts intégrées ou saisie manuelle) et les couleurs pour le texte, le titre, l'auteur et la date indépendamment.
- **Icône de notation :** Sélectionnez l'icône de base, sa couleur, ou copiez/collez votre propre code SVG brut !

---

## 🛠️ Technique & Performance

- **Code 100% Vanilla JS & PHP natif :** Aucun framework lourd (pas de jQuery, pas de dépendances externes), ce plugin est ultra-rapide.
- **Mise en cache intelligente :** Les assets statiques sont chargés avec un système de cache robuste (filemtime) pour éviter toute latence en production.
- **Responsive Design :** Les grilles s'adaptent automatiquement aux tablettes et mobiles sans configuration nécessaire.
- **Sécurité :** Les entrées utilisateurs et les SVG personnalisés sont stricement filtrés via `wp_kses()` pour prévenir toute faille d'injection.

---

*Développé avec passion pour augmenter les conversions de votre site web.*