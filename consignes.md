# Spécification claire — Plugin WordPress « Avis clients »

## Comment lire ce document
Ce document sépare deux niveaux :

- **Demande client sur le plugin** : ce que le plugin doit faire, sans jargon technique inutile.
- **Recommandation de construction par l’IA** : la manière conseillée de le fabriquer pour que ce soit propre, sécurisé et évolutif.

Le but est de permettre de valider le besoin sans avoir besoin d’être experte WordPress. Les parties “recommandation” servent surtout à cadrer le développement.

---

## 1) But du plugin

### Demande client sur le plugin
Le plugin doit permettre de :

- Créer des avis clients dans l’administration WordPress.
- Ranger ces avis dans des catégories.
- Afficher ces avis sur une page via un bloc Gutenberg.
- Choisir comment ils s’affichent : nombre, ordre, éléments visibles, mise en page simple.
- Préparer une évolution future pour récupérer des avis depuis une plateforme externe comme Google.

### Recommandation de construction par l’IA
Le plugin doit être conçu comme un vrai mini-système de gestion d’avis, pas comme un simple bloc décoratif. Cela évite de devoir tout refaire plus tard si une v2 avec synchronisation externe est développée.[web:3][page:1]

---

## 2) Ce qui est inclus en v1

### Demande client sur le plugin
La version 1 doit inclure :

- Un espace “Avis clients” dans l’admin WordPress.
- La possibilité d’ajouter un avis avec : titre, texte, image, note, nom du client, date.
- Une catégorie pour classer les avis (exemples : Site web, Notion, SEO, Formation).
- Un bloc Gutenberg pour afficher la liste des avis.
- Des réglages simples dans l’éditeur : nombre d’avis, tri, catégories, mise en page, éléments affichés.
- Un style visuel de base simple et propre.

### Recommandation de construction par l’IA
Pour la v1, il faut rester simple. D’autres plugins vont beaucoup plus loin avec synchronisation multi-plateformes ou widgets complexes, mais ici il vaut mieux privilégier une base claire, éditoriale et maintenable.[web:3][page:1]

---

## 3) Ce qui n’est pas demandé en v1

### Demande client sur le plugin
La version 1 ne doit **pas** inclure :

- La connexion à Google Reviews.
- L’import/export d’avis.
- Des rôles ou workflows avancés de modération.
- Un slider ou carousel.
- Des options visuelles très poussées comme choix de couleurs, typo ou animations.
- Une gestion multilingue avancée.

### Recommandation de construction par l’IA
Ce périmètre limité est une bonne chose. Il réduit le risque de dérive du projet et aide à livrer quelque chose de fiable avant d’ajouter des options plus complexes.[page:1]

---

## 4) Parcours attendu

### Demande client sur le plugin
#### Côté administration
Une personne de l’équipe doit pouvoir :
- aller dans “Avis clients”,
- créer un nouvel avis,
- remplir les informations,
- le publier,
- lui attribuer une ou plusieurs catégories.

#### Côté édition de page
Une personne qui rédige une page doit pouvoir :
- ajouter le bloc “Avis clients”,
- choisir quels avis afficher,
- régler leur présentation,
- publier la page.

#### Côté visiteur
Le visiteur du site doit voir une liste d’avis claire, jolie et cohérente avec le site.

### Recommandation de construction par l’IA
Le parcours doit rester proche du fonctionnement natif de WordPress, car cela réduit la courbe d’apprentissage et limite les erreurs en back-office.[page:2]

---

## 5) Informations à stocker pour chaque avis

### Demande client sur le plugin
Chaque avis doit contenir :

- Un titre.
- Un texte.
- Une image ou photo.
- Une note sur 5.
- Le nom du client.
- La date de l’avis.
- Une ou plusieurs catégories.

### Recommandation de construction par l’IA
Pour éviter un système compliqué, il est conseillé d’utiliser au maximum les champs déjà prévus par WordPress :

- le titre WordPress = titre de l’avis,
- le contenu WordPress = texte de l’avis,
- l’image mise en avant = photo ou avatar,
- les autres infos = champs complémentaires.[page:2]

C’est plus simple à administrer et plus propre techniquement qu’un système qui redouble tous les champs.[page:2]

---

## 6) Comportements à décider clairement

### Demande client sur le plugin
Voici les choix conseillés à valider :

- Le titre affiché est bien le titre WordPress.
- Le texte affiché est bien le contenu WordPress.
- La date affichée côté site est une vraie “date d’avis”, pas forcément la date de publication.
- L’image est optionnelle.
- Si aucun avis ne correspond aux filtres du bloc, il faut un message propre ou aucun affichage cassé.

### Recommandation de construction par l’IA
Ces choix doivent être tranchés dans la spec, sinon la personne en charge du développement risque d’inventer sa propre logique. C’est souvent là que naissent les développements flous ou incohérents.[page:2]

---

## 7) Ce que le bloc Gutenberg doit permettre

### Demande client sur le plugin
Le bloc “Avis clients” doit permettre de choisir :

- le nombre d’avis à afficher,
- les catégories à afficher,
- l’ordre d’affichage,
- la note minimale,
- les éléments visibles ou non : étoiles, image, titre, texte, nom, date,
- une mise en page simple en grille ou en liste,
- le nombre de colonnes si on choisit une grille.

### Recommandation de construction par l’IA
Il est préférable que le bloc se mette à jour automatiquement à partir des vrais avis enregistrés. Cette approche est cohérente avec les plugins de reviews plus avancés et simplifie aussi une future v2 avec synchronisation externe.[web:3][page:1]

---

## 8) Style visuel attendu

### Demande client sur le plugin
Le plugin doit fournir un style de base :

- simple,
- neutre,
- propre,
- facile à intégrer dans le thème existant,
- sans casser le design du site.

### Recommandation de construction par l’IA
Il vaut mieux fournir peu de styles mais une structure CSS claire. Beaucoup de plugins ajoutent des styles lourds ou très imposés ; ici, l’objectif est au contraire un rendu discret et adaptable.[page:1][page:2]

---

## 9) Sécurité

### Demande client sur le plugin
Le plugin doit être sécurisé au minimum sur les points suivants :

- seules les personnes autorisées peuvent modifier les avis,
- les données saisies sont vérifiées avant enregistrement,
- le plugin ne doit pas afficher du contenu dangereux ou mal formé,
- il ne doit pas générer d’erreurs visibles en usage normal.

### Recommandation de construction par l’IA
Cette partie n’est pas “optionnelle” ou “bonus”. Même pour un plugin simple, il faut prévoir la vérification des droits, la validation des champs, le contrôle des formulaires et la sécurisation de l’affichage pour éviter les bugs et failles basiques.[page:2]

### Ce que cela veut dire concrètement pour le développement
- Vérifier que l’utilisateur a le droit de modifier l’avis.
- Vérifier que le formulaire envoyé est légitime.
- Nettoyer les champs avant de les enregistrer.
- Réafficher proprement toutes les données côté site.
- Éviter les paramètres non contrôlés dans les filtres et tris.

---

## 10) Préparation de la v2

### Demande client sur le plugin
Même si la v1 ne se connecte à aucune plateforme externe, le plugin doit être préparé pour qu’une v2 puisse plus tard :

- récupérer des avis depuis Google ou une autre source,
- éviter les doublons,
- stocker l’origine d’un avis,
- enregistrer un identifiant externe,
- garder le même bloc d’affichage.

### Recommandation de construction par l’IA
C’est un très bon besoin à garder dans la spec. Des plugins comme OmniReview montrent l’intérêt d’un stockage local structuré quand on synchronise ensuite des avis externes.[web:3]

Le plus important est donc de prévoir dès maintenant :
- un champ “source”,
- un champ “identifiant externe”,
- un champ “lien externe”.

---

## 11) Livrables attendus

### Demande client sur le plugin
Les livrables attendus sont :

- le dossier complet du plugin,
- un plugin installable dans WordPress,
- un README simple expliquant l’installation et l’usage,
- une courte note expliquant comment la v2 pourrait être branchée plus tard.

### Recommandation de construction par l’IA
Il faut aussi demander une structure de fichiers claire et un code organisé, pour que le plugin soit relisible et maintenable ensuite.[page:2]

---

## 12) Critères d’acceptation simples

### Demande client sur le plugin
Le projet sera considéré comme validé si :

- un menu “Avis clients” existe dans l’admin,
- on peut créer un avis,
- les champs sont bien enregistrés,
- les catégories fonctionnent,
- le bloc Gutenberg existe,
- le bloc affiche bien les avis,
- les options du bloc changent réellement l’affichage,
- le rendu front est propre,
- il n’y a pas d’erreurs visibles,
- le plugin est suffisamment clair pour être repris plus tard.

### Recommandation de construction par l’IA
Ces critères sont plus utiles qu’un texte très théorique. Ils servent de checklist concrète pour vérifier si la mission est bien terminée.[page:2]

---

## 13) Décisions déjà recommandées

### Demande client sur le plugin
Voici les décisions les plus simples à valider dès maintenant :

- Utiliser le titre WordPress pour le titre de l’avis.
- Utiliser le contenu WordPress pour le texte de l’avis.
- Utiliser l’image mise en avant comme photo/avatar.
- Utiliser une date d’avis dédiée.
- Rester sur un affichage grille ou liste en v1.
- Ne pas faire de carousel en v1.
- Ne pas ajouter d’options visuelles avancées en v1.

### Recommandation de construction par l’IA
Ces décisions simplifient fortement le projet et le rendent plus réaliste à produire proprement.[page:2]

---

## 14) Résumé ultra simple

### Demande client sur le plugin
Créer un plugin WordPress qui ajoute un type de contenu “Avis clients”, avec des catégories, une note, un nom, une date et une image, puis un bloc Gutenberg permettant d’afficher ces avis sur le site avec quelques réglages simples.

### Recommandation de construction par l’IA
Le construire de manière propre, sécurisée et évolutive, pour qu’une future version puisse connecter des avis externes sans devoir tout refaire.[web:3][page:1]