# QIX Arcade

Un remake du jeu d'arcade **Qix** (1981), jouable dans le navigateur et présenté dans une borne d'arcade dessinée en HTML/CSS.

Le jeu tient dans un seul fichier, `index.html`. Il n'a besoin d'aucune installation ni d'aucune bibliothèque.

## Jouer

- **En ligne :** activez GitHub Pages sur ce dépôt (voir plus bas), puis ouvrez `https://<votre-nom>.github.io/<nom-du-depot>/`.
- **Sur votre ordinateur :** téléchargez `index.html` et ouvrez-le dans un navigateur.

## But du jeu

Clôturez **75 %** de l'écran. Quittez la bordure en traçant une ligne dans la zone noire, puis revenez sur une bordure pour refermer la forme. C'est toujours le côté sans Qix qui est capturé.

- Le **Qix**, faisceau de lignes blanches, vous fait perdre une vie s'il touche votre tracé.
- Les **étincelles** longent les bordures. Elles ne peuvent pas vous toucher pendant que vous tracez.
- La **mèche**, sauf en mode Débutant, brûle votre tracé si vous restez immobile.

## Commandes

| Action | Clavier | Borne |
|---|---|---|
| Se déplacer et tracer | Flèches (ou ZQSD / WASD) | Joystick rouge |
| Tracé rapide | Espace | Bouton A (rouge) |
| Tracé lent, points ×2 | Maj (maintenu) | Bouton B (jaune) |
| Start | Entrée | START |
| Pause | P | PAUSE |
| Son | M | SON |
| Plein écran | F | ÉCRAN |
| Difficulté (accueil) | 1 à 5 | — |

Sur téléphone, le joystick et les boutons de la borne marchent au doigt.

## Fonctionnalités

- **5 difficultés :** Débutant (sans mèche, 5 vies), Facile, Normal, Difficile, Expert.
- **1 ou 2 joueurs** chacun son tour, avec leurs noms. Les joueurs changent à chaque vie perdue, et chacun garde son propre écran.
- **10 meilleurs scores** enregistrés dans le navigateur, avec nom, score, niveau, difficulté et date.
- **Étincelles piégeables :** refermez une zone autour d'une étincelle pour la détruire. Elle rapporte 1 000 points × le niveau et revient 12 secondes plus tard.
- **Division des Qix :** dès le niveau 3, deux Qix apparaissent. Séparez-les dans deux zones pour terminer le niveau avec un gros bonus.
- **Sons rétro** générés par le navigateur (Web Audio), sans fichier audio.

## Points

| Événement | Points |
|---|---|
| Zone capturée, tracé rapide | 10 par pixel |
| Zone capturée, tracé lent | 20 par pixel |
| Étincelle piégée | 1 000 × niveau (×2, ×3… si plusieurs d'un coup) |
| Niveau réussi | 500 × niveau + 1 000 par point de % au-delà de 75 % |
| Qix séparés | 10 000 × niveau + 100 par % clôturé |

## Publier avec GitHub Pages

1. Créez un dépôt sur GitHub, par exemple `qix-arcade`.
2. Déposez-y les fichiers `index.html` et `README.md` (bouton **Add file → Upload files**).
3. Ouvrez **Settings → Pages**.
4. Sous **Build and deployment**, choisissez **Deploy from a branch**, puis la branche `main` et le dossier `/ (root)`. Cliquez sur **Save**.
5. Au bout d'une minute ou deux, le jeu est en ligne à l'adresse affichée en haut de la page.

## Remarques

- Les records et les noms restent dans le navigateur de chaque joueur (`localStorage`). Ils ne sont pas partagés entre appareils.
- Les polices viennent de Google Fonts. Sans connexion Internet, le jeu fonctionne avec des polices de remplacement.
- Qix est une marque de son éditeur d'origine. Ce projet est un hommage amateur, sans lien avec lui.
