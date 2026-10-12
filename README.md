# Olympe Training

Application de musculation sur le thème des dieux de l'Olympe. Elle tient dans un seul fichier HTML, fonctionne sur téléphone et peut s'installer sur l'écran d'accueil comme une vraie appli.

## Fonctionnalités

- **Programmes par dieu** : Hermès, Zeus, Arès, Apollon, Athéna, Artémis, Poséidon.
- **Programmes par déesse**, selon la zone à travailler : Psyché (séries parfaites), Aphrodite (fessiers), Déméter (jambes), Nikè (ventre), Iris (bras et dos), Héra (silhouette complète).
- **Séance du jour** : séries, répétitions, tempo, temps de repos, minuteur et charges notées.
- **Démos animées** de chaque exercice, avec les muscles travaillés surlignés et une planche anatomique face/dos. Le mannequin est féminin pour les programmes des déesses.
- **Variété** : les exercices changent toutes les 4 semaines, avec un bouton « Autre variante » pour en changer à tout moment.
- **Cycle de 12 semaines**, avec semaines de décharge et durée cible de chaque séance.
- **Forme du jour** à partir des données de la montre (sommeil, fréquence cardiaque au repos, VFC), avec adaptation automatique de la séance.
- **Statistiques** : calories, volume soulevé, meilleures séances, records, ce qui rend performant.
- **Repas du jour** calculés selon le poids et l'objectif, suivi de la discipline et liste de courses.
- **Lecteur de musique** intégré pour tes fichiers audio, plus des mix motivation vers YouTube Music.
- **Mode poids libres ou machines.**

## Contenu du dossier

| Fichier | Rôle |
|---|---|
| `index.html` | L'application complète |
| `manifest.webmanifest` | Permet d'installer l'appli sur le téléphone |
| `sw.js` | Permet d'ouvrir l'appli hors connexion |
| `icons/` | Icônes de l'appli |
| `.nojekyll` | Indique à GitHub Pages de publier les fichiers tels quels |

## Mettre en ligne avec GitHub Pages

1. Sur [github.com](https://github.com), clique sur **New repository**, nomme-le par exemple `olympe-training`, laisse-le **Public**, puis **Create repository**.
2. Sur la page du dépôt, clique sur **uploading an existing file**, glisse **tout le contenu** de ce dossier (pas le dossier lui-même), puis clique sur **Commit changes**.
   - Le fichier `.nojekyll` est caché sur certains ordinateurs. S'il n'apparaît pas, ce n'est pas grave : l'appli fonctionne quand même.
3. Va dans **Settings → Pages**. Sous **Branch**, choisis `main` et le dossier `/ (root)`, puis **Save**.
4. Après 1 à 2 minutes, l'appli est en ligne à l'adresse :
   `https://TON-PSEUDO.github.io/olympe-training/`

Avec Git en ligne de commande :

```bash
cd olympe-training
git init
git add .
git commit -m "Olympe Training"
git branch -M main
git remote add origin https://github.com/TON-PSEUDO/olympe-training.git
git push -u origin main
```

Puis active GitHub Pages comme à l'étape 3.

## Installer l'appli sur ton téléphone

- **iPhone (Safari)** : ouvre l'adresse, touche le bouton **Partager**, puis **Sur l'écran d'accueil**.
- **Android (Chrome)** : ouvre l'adresse, touche **⋮**, puis **Installer l'application** (ou **Ajouter à l'écran d'accueil**).

L'appli s'ouvre ensuite en plein écran, avec son icône, et fonctionne même sans réseau une fois ouverte une première fois.

## Mettre à jour l'appli

1. Remplace `index.html` sur GitHub par la nouvelle version.
2. Dans `sw.js`, change la ligne `const VERSION = 'olympe-v1';` en `'olympe-v2'` (puis v3, etc.) pour que les téléphones téléchargent bien la nouvelle version.

## Tes données

Tout reste **sur ton téléphone**, dans le navigateur : séances, charges, repas, musiques, vidéos et image de fond. Rien n'est envoyé sur GitHub ni ailleurs. Conséquences :

- Utilise toujours le même téléphone et le même navigateur.
- Si tu effaces les données du site ou désinstalles l'appli, l'historique est perdu.
- Les données saisies dans la version sur Claude ne sont pas transférées vers la version GitHub, qui démarre vide.

## Bon à savoir

- Les données de la montre se recopient à la main. Une page web ne peut pas lire Apple Santé, Health Connect, Garmin ou Samsung Health.
- Les musiques YouTube Music s'ouvrent dans l'appli YouTube Music. Le lecteur intégré lit les fichiers audio que tu ajoutes depuis ton téléphone.
- Le score de forme et les quantités des repas sont des repères, pas un avis médical.
