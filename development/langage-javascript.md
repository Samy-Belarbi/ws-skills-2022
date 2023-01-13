# Langage Javascript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les `structures` de base du langage ✔️
- les normes `ecmascript` ✔️
- l'utilisation de l'`asynchrone` ✔️
- les spécifités du mot-clef `this` ✔️

## 💻 Je code en Javascript

### Un exemple de code commenté ✔️

```javascript
// Générateur de bouton
export const buttonGenerator = (id, innerText, onClick) => {
  const button = document.createElement("button"); // Création de l'élément HTML bouton
  button.id = id; // Attribution de l'id au bouton récupéré dans les params
  button.innerText = innerText; // Attribution du text à insérer dans le bouton

  if (onClick === undefined) {
    // Vérification si la fonction à attribuer à l'event click a bien été fournie
    return button;
  }

  button.addEventListener("click", onClick); // Si oui, on lui rajoute via l'event listener
  return button; // On renvoie le bouton
};
```

### Utilisation dans un projet ✔️

[lien github] https://github.com/Samy-Belarbi/Gymnotes

Description : Site permettant d'enregistrer ses séances de sports et d'être assisté durant celles-ci.

### J'ai utilisé ce langage en production ✔️

[lien du projet] https://samybelarbi.sites.3wa.io/

Description : Site permettant d'enregistrer ses séances de sports et d'être assisté durant celles-ci.

### J'ai utilisé ce langage en environement professionnel ✔️

Description : Gestion du front avec React d'une appli.

## 🌐 J'utilise des ressources

### Titre

- Stack Overflow
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
