# QIX Arcade

Un remake du jeu d'arcade **Qix** (1981), jouable dans le navigateur et présenté dans une borne d'arcade rétro.

Il marche sur **ordinateur, téléphone et tablette**, et s'installe comme une application.

**4 langues :** français, English, Deutsch, ไทย. On choisit la langue avec les boutons **FR · EN · DE · ไทย** en haut de l'écran d'accueil. Au premier lancement, le jeu prend la langue du téléphone ou du navigateur, puis il retient le choix.

> 🇬🇧 Arcade remake of Qix (1981) in a retro cabinet. Pick your language on the title screen.
> 🇩🇪 Arcade-Remake von Qix (1981) im Retro-Automaten. Sprache auf dem Startbildschirm wählen.
> 🇹🇭 เกม Qix (1981) แบบตู้อาร์เคดย้อนยุค เลือกภาษาได้ที่หน้าจอเริ่มต้น

## Jouer

- **En ligne :** <https://chtipilot.github.io/GAME_1/>. GitHub Pages doit être activé, voir plus bas.
- **Sur votre ordinateur :** téléchargez `index.html` et ouvrez-le dans un navigateur.

## Sur téléphone et tablette

Sur un écran tactile, la borne se transforme en console plein écran, sans défilement :

- **Portrait :** l'écran de jeu est en haut, le joystick et les boutons en dessous.
- **Paysage :** le joystick est à gauche, l'écran au centre et les boutons à droite.

Pour vous déplacer, deux façons au choix :

- **Le joystick rouge :** posez le doigt dessus et glissez dans la direction voulue.
- **Toucher l'écran de jeu :** le losange se dirige vers votre doigt. Gardez le doigt posé pour avancer, et glissez pour changer de direction.

Autres comportements :

- La partie se met en pause toute seule si vous quittez l'application ou recevez un appel.
- L'écran reste allumé pendant la partie, sur les appareils qui le permettent.
- Le téléphone vibre quand vous perdez une vie ou piégez une étincelle, sur Android et quand le son est activé.

### Installer l'application

Une fois installé, le jeu s'ouvre en plein écran depuis son icône et marche **sans Internet**.

- **Android (Chrome) :** sur l'écran d'accueil du jeu, touchez **INSTALLER L'APPLI**, ou passez par le menu ⋮ → **Installer l'application**.
- **iPhone / iPad (Safari) :** touchez **Partager** puis **Sur l'écran d'accueil**.

## But du jeu

Clôturez **75 %** de l'écran. Quittez la bordure en traçant une ligne dans la zone noire, puis revenez sur une bordure pour refermer la forme. C'est toujours le côté sans Qix qui est capturé.

- Le **Qix**, faisceau de lignes blanches, vous fait perdre une vie s'il touche votre tracé.
- Les **étincelles** longent les bordures. Elles ne peuvent pas vous toucher pendant que vous tracez.
- La **mèche**, sauf en mode Débutant, brûle votre tracé si vous restez immobile.

## Commandes

| Action | Clavier | Borne / écran tactile |
|---|---|---|
| Se déplacer et tracer | Flèches (ou ZQSD / WASD) | Joystick rouge, ou doigt sur l'écran de jeu |
| Tracé rapide | Espace | Bouton A (rouge) |
| Tracé lent, points ×2 | Maj (maintenu) | Bouton B (jaune), maintenu |
| Start | Entrée | START |
| Pause | P | PAUSE |
| Son | M | SON |
| Plein écran | F | ÉCRAN (absent sur iPhone) |
| Difficulté (accueil) | 1 à 5 | Boutons de difficulté |

## Fonctionnalités

- **5 difficultés :** Débutant (sans mèche, 5 vies), Facile, Normal, Difficile, Expert.
- **1 ou 2 joueurs** chacun son tour, avec leurs noms. Les joueurs changent à chaque vie perdue, et chacun garde son propre écran.
- **10 meilleurs scores** enregistrés sur l'appareil, avec nom, score, niveau, difficulté et date.
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

## Fichiers

| Fichier | Rôle |
|---|---|
| `index.html` | Le jeu complet |
| `manifest.webmanifest` | Nom, icônes et couleurs de l'application installée |
| `sw.js` | Garde le jeu en mémoire pour jouer sans Internet |
| `icons/` | Icônes de l'application (Android, iPhone, ordinateur) |

Après une modification du jeu, changez la ligne `const VERSION = 'qix-v4';` dans `sw.js` (par exemple `qix-v5`). Les téléphones où le jeu est installé récupèrent ainsi la nouvelle version.

## Activer GitHub Pages

1. Sur GitHub, ouvrez ce dépôt puis **Settings → Pages**.
2. Sous **Build and deployment**, choisissez **Deploy from a branch**, puis la branche `main` et le dossier `/ (root)`. Cliquez sur **Save**.
3. Au bout d'une à deux minutes, le jeu est en ligne à l'adresse affichée en haut de la page.

## Remarques

- Les records et les noms restent sur l'appareil où l'on joue (`localStorage`). Ils ne sont pas partagés entre appareils.
- Les polices viennent de Google Fonts. Après la première visite, elles sont gardées en mémoire pour jouer hors ligne.
- Qix est une marque de son éditeur d'origine. Ce projet est un hommage amateur, sans lien avec lui.
