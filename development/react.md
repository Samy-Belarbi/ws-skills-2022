# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ✔️
- les composants enfants et les _props_ qu'on leur passe ✔️
- le déclenchement d'instructions en fonction des actions de l'utilisateur ✔️
- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ✔️
- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ❌ / ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```javascript
// Calculatrice via React

const ops = ["/", "*", "-", "+", "."]; // Toutes les opérations disponibles

const Calculator = () => {
  /* STATES */

  // En dehors de la parenthèse
  const [calc, setCalc] = useState("");

  // Dans la parenthèse
  const [result, setResult] = useState("");

  // COMPORTEMENTS
  // Fonction qui permet de mettre à jour le state du calcul et du résultat
  const updateCalc = (value) => {
    if (
      (ops.includes(value) && calc === "") ||
      (ops.includes(value) && ops.includes(calc.slice(-1))) ||
      (calc.includes(".") && value === ".") ||
      (value === "0" && calc.slice(0) === "0" && !calc.includes("."))
    ) {
      return;
    }

    setCalc(calc + value);

    if (!ops.includes(value)) {
      setResult(eval(calc + value).toString());
    }
  };

  // Fonction qui permet de faire le calcul
  const calculate = () => {
    if (!ops.includes(calc.charAt(calc.length - 1))) {
      setCalc(eval(calc).toString());
      setResult("");
    }
  };

  // Fonction qui permet de supprimer le dernier nombre et mettre à jour le state
  const deleteLastNumber = () => {
    if (calc !== "") {
      const newValue = calc.slice(0, -1);
      const lastCharac = newValue.charAt(newValue.length - 1);
      setCalc(newValue);

      if (!ops.includes(lastCharac) && lastCharac !== "") {
        setResult(eval(newValue).toString());
      }

      if (!ops.includes(lastCharac) && lastCharac === "") {
        setResult("");
      }

      return;
    }
  };

  // AFFICHAGE
  return (
    <div className="calculator">
      <div className="result">
        {result ? <span>({result})</span> : ""}
        {calc || "0"}
      </div>
      <div className="operators">
        <button onClick={() => updateCalc("/")}>/</button> {/* Au clic de tous les boutons on va appeler UpdateCalc */}
        <button onClick={() => updateCalc("*")}>*</button>
        <button onClick={() => updateCalc("-")}>-</button>
        <button onClick={() => updateCalc("+")}>+</button>
        <button onClick={deleteLastNumber}>DEL</button>
      </div>
      <div className="digits">
        {Array(9)
          .fill(0)
          .map((_, i) => (
            <button key={i + 1} onClick={() => updateCalc(String(i + 1))}>
              {i + 1}
            </button>
          ))}{" "}
        {/* Création des boutons de la calculatrice de 0 à 9 */}
        <button onClick={() => updateCalc(".")}>.</button>
        <button onClick={() => updateCalc("0")}>0</button>
        <button onClick={calculate}>=</button> {/* Au clic on va calculer le résultat de l'opération donnée */}
      </div>
    </div>
  );
};
```

### Utilisation dans un projet ✔️

[lien github] https://github.com/Samy-Belarbi/calculator

Description : Simple calculatrice via React

### Utilisation en production si applicable ✔️

[lien du projet] https://calculator-eight-theta.vercel.app/

Description : Simple calculatrice via React

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
