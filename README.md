# Compte Rendu - TP 5 : Comment créer un site Web sur GitHub Pages

## Objectifs du TP

Ce TP avait pour but d'apprendre à utiliser GitHub Pages pour héberger un site web à partir d'un dépôt GitHub. Les objectifs principaux étaient :

- Créer un site Web à partir d'un référentiel GitHub
- Ajouter du contenu avec Markdown et HTML
- Préparer un site Web pour le compte-rendu de la SAE 2.03

---

## 1. Créer un site Web pour un référentiel existant

Nous avons utilisé notre référentiel du TP3 pour publier un site web.

### Étapes réalisées :
- Passage du dépôt en mode public
- Accès aux paramètres GitHub Pages dans l'onglet Settings
- Choix d'un thème pour le site
- Création automatique du fichier `index.md` (page d'accueil)
- GitHub a créé une nouvelle branche `gh-pages` pour contenir le contenu web

### Mise à jour locale :
```bash
$ git fetch origin gh-pages
$ git checkout gh-pages
```

Nous avons vérifié le contenu web par défaut publié à l'adresse :
```
https://<utilisateur>.github.io/tp3/
```

---

## 2. Ajouter du contenu à l'aide de Markdown et HTML

Nous avons appris à modifier le fichier `index.md` pour personnaliser le contenu du site.

### Rappel des commandes :
```bash
$ git checkout gh-pages
$ git add index.md
$ git commit -m "Mise à jour du contenu web"
$ git push
```

### Contenu testé :
- Lien vers des pages internes et externes
- Insertion d'images internes et externes
- Tableau HTML simple
- Contenu stylisé avec CSS
- Intégration d'une vidéo YouTube

Cela nous a permis de mieux comprendre les possibilités de personnalisation avec GitHub Pages.

---

## 3. Créer un site Web pour la SAE 2.03

Nous avons préparé la création du site web pour le projet de SAE 2.03 qui traitera des services réseaux via Docker.

### Prérequis pour la SAE :
- Travail en équipe de 3 ou 4 personnes
- Création d'un dépôt `docker-sae203`
- Invitation des membres de l'équipe au projet GitHub
- Le dépôt doit être public

### À faire :
- Structurer le site (accueil, sections par thèmes, etc.)
- Préparer les fichiers Markdown pour éviter les conflits lors des contributions

---

## Conclusion

Ce TP nous a permis de mettre en place un site web à partir de GitHub Pages, d'apprendre à le modifier en Markdown/HTML, et de préparer l'environnement pour notre SAE 2.03. Nous sommes maintenant prêts à documenter nos projets de manière collaborative et professionnelle.

---

Fin du TP 5

