## ProjectComplexCard


## Version 0.0.1

Ce composant affiche un projet sous-forme d'une carte. Contrairement au ProjectSimpleCard, ce composant essaie d'afficher le plus
d'informations sur le projet dont : le nom, le type, le livrable, les catégories, l'etat opensource, le nom de créateur, l'état du projet.


## TagInput

15/07/22

### Version 0.0.1

Ce composant est un champ texte qui permet de créer des tags qui sont réprésentés par les mots séparés par des virgules dans le champ.
Le composant affiche les tags résultant au dessous du champ, en veuillant à ce que chaque tag ne soit pas vide et soit en minuscule.
Le composant met à jour sa liste de tags à chaque saisie du clavier et emet un événement *tagsInputChanged* en envoyant la liste des tags.
e


## AlertCodenameMissing

08/07/22

### Version 0.0.1

Intervient au niveau d'un projet. Il affiche un message indiquant à l'utilisateur que le projet ne possède pas d'url car il ne possède
pas d'un nom de code. Le message invite l'utilisateur à corriger cela en fournissant un lien vers la page de modification du projet
pour renseigner un nom de code.


## ProjectSimpleCardEmptyList

### Version 0.0.2 25/07/22

Le composant affiche le nombre de projets qui possède dans sa liste si la propriété show_counter est à true. L'expression qui
s'affichera sera "nombre-de-projets Résultat(s si il y'a plus d'un projet). Cette modification a été faite pour l'affichage des résultats
de recherche d'un projet dans le listing des projets. Tout changement sur le nombre de projets changera par correspondance du nombre, l'expression de compteur.

### Version 0.0.1 05/07/22

Ce composant est similaire au ProjectSimpleCardList à la différence qu'il ne génère pas la liste des projets automatiquement. Il reçoit
la liste à afficher en entrée. Il gère aussi l'évènement *projectsSelectedByCategorizationSidebar* cependant au lieu de récupérer les
projets correspondant dans la base de données, il effectue un filtre sur la liste des projets qu'il a reçu.


## SimpleSearchBox

05/07/22

### Version 0.0.1

Ce composant est responsable de l'affiche de la barre de recherche. Il gère automatique l'affichage de la précédente requête de recherche.


## CategorizationSidebar

### Version 0.0.1

Ce composant affiche une barre de menu type latérale qui propose une liste de sélection des catégories systèmes
disponibles. Elle permet de sélectionner les catégories qui devront être affichée par un composant d'affichage.
A chaque sélection, elle émet un évènement *projectsSelectedByCategorizationSidebar* avec comme données les identifiants
des catégories sélectionnées. Il possède une version d'affichage pour petits écrans. Dans ce cas, il s'agit d'une liste 
déroulante proposant les catégiries à sélectionner.


## ProjectSimpleCardList

Ce composant permet d'afficher des composants *ProjectSimpleCard*, c'est à dire des cartes de projets, avec un affichage en grille.

### Version 0.0.2

Il écoute l'évènement *projectsSelectedByCategorizationSidebar* qui provient d'un composant de sélection de catégories.
Il reçoit ainsi les id catégories des projets à afficher. Il récupère les projets correspondants et les affiches.
Si la liste est vite alors il affiche tous les projets.

#### Bugs

L'affichage des *ProjectSimpleCard* se fait selon deux modes. L'un avec le système de grille (display:grid) s'il y'a moins de 3 projets
et l'autre avec un système de colonnes (column-3xs) s'il y'a plus de 3 projets. En effet, lorsqu'on utilise les colonnes avec moins de
3 projets, le navigateur semble force le remplissage des 3 colonnes en comblant le vide par le découpage du composant de l'avant dernière
colonne, ce qui engendre des cassures dans son rendu. Un partie du compasant dans la colonne 2 et l'autre dans la colonne 3. Ce phénomène ne se produit que lorsqu'il y'a moins de 3 projets. Ainsi, lorsqu'on a moins de 3 projets le composant opte pour l'affiche en grille pour simuler l'affiche en grille et colonne des projets.

### Version 0.0.1

Ce composant permet d'afficher des composants *ProjectSimpleCard* avec un affichage en grille.



## ProjectSimpleCard

Ce composant affiche un projet sous-forme d'une carte.

### Version 0.0.2

Ajout des catégories au composant. L'affichage des catégories est géré par le composant CategoryLiner

### Version 0.0.1

Il contient :
- Le nom du projet
- Le nom du créateur
- Le résumé du projet limité à 30 mots et si le résumé n'est pas définie, la description du projet limitée à 30 mots
- Un menant vers la fiche du projet

En cliquant sur la carte, on redirigé sur la carte du projet


## CategoryLiner

Affiche les catégories d'un projet en ligne.

### Version 0.0.1

- Les catégories de type system utilise un badge de couleur bleu.
- Les catégories de type system utilise un badge de couleur indigo.
- Les projets sans catégories utilisent un badge de couleur jaune avertissement de texte "Projet".


## ProjectDeleteButton

### Version 0.0.1

Ce composant est un bouton autonome qui permet de gérer la suppression d'un projet.
Lorqu'on clique sur lui il exige une confirmation de suppression. Si confirmation alors il supprime le projet et redirige sur le tableau de bord. 
