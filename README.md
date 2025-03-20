# ExpressJs EscaBalles starter

## Installation

```
git clone git@github.com:erralb/cesi-express.git
cd cesi-express
npm install
npm install --save-dev nodemon
```
## Démarrage du serveur

```
DEBUG=cesi-express:* npm start
```

## Déploiement sur Vercel

```
npm install -g vercel
vercel login
vercel dev
```

Testez `http://localhost:3000` et `http://localhost:3000/users` pour vérifier que tout fonctionne correctement.

Pour déployer sur Vercel : `vercel`
Pour déployer sur l'url de production : `vercel --prod`.

## Procédure initiale 

Pour créer ce dépot en partant de express-generator, il faut exécuter les commandes suivantes :

```
npm install -g express-generator
express --view=pug cesi-express
cd cesi-express
npm install
npm install --save-dev nodemon
```

### Moifications à apporter pour Vercel

```
mv app.js index.js
mkdir api
mv index.js api
```

Modifier les chemins dans les fichiers `api/index.js` et `bin/www` pour qu'ils correspondent à la nouvelle organisation des fichiers.