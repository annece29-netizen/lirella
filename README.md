# Lirella 📚

Application web pour cataloguer sa bibliothèque personnelle exactement comme elle est rangée à la maison : par pièce, par étagère. Pensée pour Marine, lectrice passionnée avec de nombreux livres auto-édités que les applications classiques (Gleeph, LibraryThing...) ignorent.

**Appli en ligne :** https://annece29-netizen.github.io/lirella/

## À quoi ça sert

- Créer ses propres bibliothèques (Salon, Chambre, Bureau...) avec un nombre d'étagères personnalisé
- Ranger chaque livre sur une étagère précise, comme dans la vraie vie
- Ajouter un livre en scannant son code-barre (titre, auteur, couverture et résumé récupérés automatiquement) ou à la main pour les livres introuvables en ligne
- Découvrir des nouveautés littéraires suggérées automatiquement

Toutes les données restent **sur l'appareil** (stockage local du navigateur) : pas de compte, pas d'abonnement, rien n'est envoyé sur un serveur.

## Comment l'utiliser

1. Ouvrir le lien de l'appli sur son téléphone.
2. Entrer son prénom au premier lancement.
3. Créer une première bibliothèque (onglet **Bibliothèque** → *+ Nouvelle*), en indiquant son nom et son nombre d'étagères.
4. Ajouter un livre (onglet **Ajouter**) :
   - **Scanner le code-barre** : autoriser l'accès à la caméra, puis pointer le téléphone vers le code-barre du livre (13 chiffres sous le code-barre). Si le code est illisible, un lien permet de le saisir à la main.
   - **Ajouter manuellement** : pour un livre auto-édité ou introuvable, en renseignant titre, auteur, catégorie, bibliothèque et étagère.
5. Retrouver ses livres dans l'onglet **Bibliothèque**, classés par bibliothèque puis par étagère.
6. Modifier ou supprimer une bibliothèque via l'icône crayon sur sa carte.

## Important : la caméra ne fonctionne que via ce lien en ligne

Le scan par caméra nécessite une connexion sécurisée (HTTPS), fournie par l'hébergement GitHub Pages. Si le fichier `index.html` est ouvert directement depuis un ordinateur ou envoyé par message, la caméra ne s'activera pas — il faut toujours passer par le lien https://annece29-netizen.github.io/lirella/.

## Stack technique

- HTML, CSS, JavaScript purs (aucun framework)
- [ZXing](https://github.com/zxing-js/library) pour la lecture de code-barres via la caméra
- API [Google Books](https://developers.google.com/books) pour récupérer titre, auteur, couverture et résumé à partir de l'ISBN
- Stockage local du navigateur (`localStorage`), aucune base de données externe
- Hébergement : GitHub Pages

## Mettre à jour l'appli

Depuis le dossier du projet :

```
git add .
git commit -m "Description de la modification"
git push origin master
```

Le site se met à jour en une à deux minutes.
