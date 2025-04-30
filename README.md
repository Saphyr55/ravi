# ravi

## Présentation du projet

ravi est un projet universitaire réalisé par deux étudiants dans le cadre d'un travail sur la conception de langages de programmation. L'objectif principal était de créer un langage de programmation spécialisé pour le développement de jeux de rôle, en utilisant une approche différente de Java.

## Caractéristiques principales

### Syntaxe fonctionnelle

ravi adopte une syntaxe inspirée des langages fonctionnels comme OCaml, avec:
- Des expressions `let` pour définir des variables et des fonctions
- Le système de type de Hindley–Milner
- Un mécanisme de pattern matching avec l'expression `match`
- Support des modules pour organiser le code

### Système de types

Le langage propose:
- Types primitifs (String, Int)
- Types algébriques (comme les listes et les types du jeu)
- Définition de types personnalisés

## Exemples de code

### Fonction

```
let player name = Game.Hero(name, 10)
end
```

## Opérateurs personnalisés

Le langage permet de définir des opérateurs personnalisés comme `<|` pour faciliter l'application de fonctions:

```
let ( <| ) f x = f x
end
```

### Pattern matching

```
let count l =
  let aux l n =
    match l with
    | Empty -> n
    | Cons (h, t) -> aux t (1 + n)
  in
  aux l 0
end
```

## Types de données

### Listes

```
type 'a List =
  | Empty
  | Cons of 'a * ('a List)
```

### Module

```
module Game =
  type Player = Hero of String * Int
  // ...
end
```

## Perspectives d'évolution

Ce projet étudiant pourrait être enrichi avec:
- Structure sur plusieurs fichiers.
- Une bibliothèque standard
- Un compilateur ou interpréteur plus performant (Peut-etre basé sur la JVM)
