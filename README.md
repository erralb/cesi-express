# ExpressJs EscaBalles starter

## Installation

```
git clone git@github.com:erralb/cesi-express.git
cd cesi-express
npm install
npm install -g yarn
```

## Démarrage du serveur

```
npm run dev
```

## Déploiement sur Vercel

```
npm install -g vercel
vercel login
vercel dev
```

Testez `http://localhost:3000` et `http://localhost:3000/users` pour vérifier que tout fonctionne correctement.

Pour déployer sur Vercel en mode `Preview` :

```
vercel
```

Pour déployer sur Vercel en `production` : 

```
vercel --prod
```

## Procédure initiale - [NE PAS SUIVRE]

**Cette procédure est donnée à titre indicatif pour expliquer comment a été créé ce dépot. Elle n'est pas à suivre pour utiliser ce dépot.**

Pour créer ce dépot en partant de express-generator, il faut exécuter les commandes suivantes :

```
npm install -g express-generator
express --view=pug cesi-express
cd cesi-express
npm install
npm install --save-dev nodemon
```

Modifier le fichier `package.json` pour ajouter une version de Pug supérieure à 3.0.0.

```
"pug": "^3.0.3",
```

puis éxecuter à nouveau `npm install`.

### Modifications à apporter pour Vercel

```
mv app.js index.js
mkdir api
mv index.js api
```

Modifier les chemins dans les fichiers `api/index.js` et `bin/www` pour qu'ils correspondent à la nouvelle organisation des fichiers.

## Point d'attention

Le répertoire `public` ne peut pas être vide sinon Vercel ne déploie pas le projet. Il faut donc ajouter au moins un fichier dans ce répertoire, même s'il n'est pas utilisé.