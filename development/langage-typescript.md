# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ✔️
- les types de bases ✔️
- comment et pourquoi étendre une interface ✔️
- les classes et les decorators ❌ / ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
// Fonction qui renvoie une cellule de mon Tic Tac Toe
const Cell = ({ player, index, onClick, cellClassName }: CellProps) => { // Attribution des props à l'interface en dessous
  return (
    <div className={cellClassName[index]} data-cell-index={index} {...{ onClick }}>
      <span data-cell-index={index}>{player}</span>
    </div>
  );
};

interface CellProps = {
  player?: string, // On utilise "?" pour permettre de rendre Player optionnel, mais sinon ce sera un string
  cellClassName: Array<string>, // cellClassName est un tableau de string
  onClick(e: React.MouseEvent): void, // onClick sera une fonction qui reçevra un MouseEvent et qui ne renverra rien
  index: number, // Index est un number
};
```

### Utilisation dans un projet ✔️

[lien github] https://github.com/Samy-Belarbi/tictactoe

Description : Simple Tic Tac Toe w/ ReactJs, ViteJs & TypeScript.

### Utilisation en production si applicable ✔️

[lien du projet] https://tic-tac-toe-lemon-pi.vercel.app/

Description : Simple Tic Tac Toe w/ ReactJs, ViteJs & TypeScript.

### Utilisation en environement professionnel ✔️

Description : Gestion du typage du front via React d'une appli.

## 🌐 J'utilise des ressources

### Titre

- https://www.totaltypescript.com/
- Training TS

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
