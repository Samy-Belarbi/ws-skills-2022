# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- Comment développer en utilisant un système de _livereloading_ (`nodemon` par exemple) ✔️
- La connexion de mon application à une base de données avec et sans ORM/ODM (avec `mongodb` puis `mongoose` par exemple) ✔️
- Le développement d'une API REST et GraphQL (avec les packages `express` et `graphql` par exemple) ❌ / ✔️
- _Bonus : la manipulation des fichiers système avec `fs` et l'utilisation des streams en NodeJS_ ❌ / ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
// Fs permet de créer et lire des fichiers via Node
const fs = require("fs"); // File System

module.exports = async (bot) => {
  fs.readdirSync("./Commands") // On lui donne le le dossier où il va venir lire les fichiers
    .filter((f) => f.endsWith(".js")) // On vérifie bien qu'on lui donne que les fichiers JS
    .forEach(async (file) => {
      const command = require(`../Commands/${file}`); // On importe le fichier de la commande

      if (!command.name || typeof command.name !== "string") {
        throw new TypeError(`La commande ${file.slice(0, file.length - 3)} n'a pas de nom !`);
      } // On vérifie bien que la commande a un nom, sinon on envoie une erreur (en enlevant le ".js" du file);

      bot.commands.set(command.name, command); // On rajoute la commande au bot

      console.log(`Commande ${file} chargée avec succès !`);
    });
};
```

### Utilisation dans un projet ✔️

[lien github] https://github.com/Samy-Belarbi/bot-discord

Description : Bot Discord qui permet d'envoyer un lien via la commande !meet

### Utilisation en production si applicable❌ / ✔️

[lien du projet](...)

Description :

### Utilisation en environement professionnel ❌ / ✔️

Description :

## 🌐 J'utilise des ressources

### Titre

- lien
- description

## 🚧 Je franchis les obstacles

### Point de blocage ❌ / ✔️

Description:

Plan d'action : (à valider par le formateur)

- action 1 ❌ / ✔️
- action 2 ❌ / ✔️
- ...

Résolution :

## 📽️ J'en fais la démonstration

- J'ai ecrit un [tutoriel](...) ❌ / ✔️
- J'ai fait une [présentation](...) ❌ / ✔️
