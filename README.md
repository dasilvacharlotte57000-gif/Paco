# Paco Arcade

Site deployable sur Render en deux modes.

## Contenu

- `index.html` : page d'accueil avec mini-jeux integres
- `render.yaml` : configuration Blueprint pour site statique
- `Dockerfile` : configuration pour deploiement Render en Web Service Docker

## Deploiement sur Render

### Option 1 : Blueprint

1. Pousse le depot sur GitHub.
2. Dans Render, cree un Blueprint.
3. Render lira `render.yaml` et deployera le site statique.

### Option 2 : Web Service Docker

1. Pousse le depot sur GitHub.
2. Dans Render, cree un `Web Service`.
3. Render detectera maintenant le `Dockerfile`.
4. Lance le deploy.

## Configuration Docker

- Image : `python:3.12-alpine`
- Port expose : `10000`
- Serveur : `python -m http.server`

## Commande locale

Pour tester avec Docker :

`docker build -t paco-arcade .`

`docker run -p 10000:10000 paco-arcade`

Puis ouvre `http://localhost:10000`.
