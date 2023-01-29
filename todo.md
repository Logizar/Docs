# version

0.0.1.3-alpha 

## 0.0.1.3-alpha

### En cours

- [] Ajouter un logo au projet
	- [x] Intégrer la possibilité de mettre des photos sur des projets partout
	- [] S'assurer que les photos apparaissent partout
	- [] Ajouter une fonctionnalité permettant d'uploader, modifier et supprimer des photos 

### 29/01/2023

- [x] Augmentation de la taille maximal d'un résumé d'un projet à 100 (29/01/2023)
- [x] Ajout du statut de projet *Aucun* (29/01/2023)

### < 29/01/2023

- [] Fixer la barre de sélection des catégories (15/06/2022)
- [] Correction de bugs approfondie et review

- [x] Le lien du tableau de bord apparait lorsqu'on est pas connecté (11/06/2022) -
- [x] La description des projets ne tient pas compte des espaces  (15/06/2022) -
- [x] Dans l'url si quelqu'un utilise l'expression ?w=... la valeur de w apparaitra sur n'importe qu'elle page
- [x] (Critique) Utiliser les stopwords français dans le moteur de recherche
- [x] (Critique) Echapper les mots clés pour éviter les injections sql dans le moteur de recherche
- [x] (Critique) Supprimer les espaces vides des mots clés utilisés par le moteur de recherche
- [x] Mettre les tailles maximales dans les champs de formulaire - (25/07/2022)
- [x] Mauvais usage du webmanifest - (25/07/2022)
- [x] Le filtre par catégorie au niveau de la page de recherche doit aussi changer le nombre de résultat automatiquement
- [x] Le lien en dessous du champ n'est pas correcte. (17/07/2022) - (25/07/2022)
- [x] Utiliser les versions longue dans la livrable (17/07/2022) - (25/07/2022)

-----------------------------------------------------

- [] Ajouter un compteur de visites   (Pas prioritaiez)
- [] Ajouter la notion de d'envergures  (Pas prioritaiez)
- [] Compter le nombre de clique sur un projet  (Pas prioritaiez)
	
- [] Améliorer l'interface du tableau de bord  (Pas prioritaire)
- [] Ajouter une page à propos (Pas prioritaiez)

## 0.0.1.3-alpha

- [x] Bug - La description des projets ne tient pas compte des retours à a ligne (15/06/2022) 
- [x] La description des projets doit prendre en compte liens cliquables au rendu
- [x] Faire en sorte que le lien vers un projet se fasse vers un lien personnalisé, celui choisi par l'utilisateur
	- [x] Chaque projet doit posséder un lien unique
	- [x] Le lien vers le projet est déterminé à partir de son nom
	- [x] Le lien est déterminé lors de création du projet
	- [x] Tous les projets ayant déjà été créé devront mettre à jour ce lien
	- [x] Les caractères autorisé sont les lettres, chiffres et : - .
	- [x] Si un projet possède le lien alors on l'utilise sinon on utilise le lien usant de l'identifiant
	- [x] Modification du nom de code

- [x] Ajouter le type de projet (idée,test,hackathon,projet de formation, projet personnel, produit,concept)
	- [x] Moduler l'interface de l'administration de sorte à avoir les modules suivants:
		- [x] Gérer les catégories
		- [x] Gérer les autres catégories
		- [x] Gérer les types de projet
	- [x] Implémenter la gestion des types de projets 

- [x] Ajouter le status du projet (en cours, en pause, terminé, abondonné)
- [x] Ajouter un système de tags au projets, maximum 5
- [x] Ajouter l'état est opensource
- [x] Ajouter le type de projet au formulaire de création de projet
- [x] Ajouter le livrable (Application web, Application mobile, Application web/mobile, API, Logiciel de bureau, Application multiplaforme)
- [x] Ajouter des liens aux projets (Site web, Github) (Section accéssibilité)

- [x] Ajouter un module de gestion des livrables à l'administration
	- [x] Ajouter la liste des livrables au formulaire de création d'un projet

- [x] Ajouter la possibilité de modifier le type de projet, les tags, l'état opensource, le livrable et les liens du projets

- [x] Mettre à jour le formulaire et la carte d'un projet

## 0.0.1.2

- [x] Ajouter un panneau à l'accueil qui permet de filter les projets en fonction de la catégories
- [x] Faire un petit moteur de recherche


## v0.0.1.1

- [x] Créer un petit système de role pour gérer l'administration de la plateforme : user, admin; Seul le rôle admin à droit aux fonctionnalités d'administration
- [x] Mettre à jour seeder pour qu'il créé toujours un adminstrateur (Pas obligatoire)
- [x] Créer une administration qui permet de gérer les catégories
- [x] Ajouter les fonctionnalités pour l'ajout, la modification et l'affichage des catégories : 3 catégories max
	- [x] Ajout des champs de création de catégories au formulaire de création de projet
	- [x] Ajout les catégories aux composants d'affichage des projets
	- [x] Ajout d'une section de modification des catégories à la page de modification
	
## Next

- [o] Tags, Stades, Plateforme, Collaborateur, Screenshots, Branding, logo, photo utilisateur	

## Bugs résolu

- [x] Une erreur se produit lorsqu'on ajoute une catégorie vide de type Autre dans le formulaire de création d'un projet (29/01/2023)
- [x] Augmenter la taille du resumé des projets à 100 (Resolution le: 29/01/2023)
- [x] Revoir le composant de création des tags (Resolution le: 29/01/2023)
- [x] Dans l'administration le modèle de d'ajout d'une catégorie conserve toujours la valeur précédente de son affichage (Resolution le: 29/01/2023)

## Bugs

- [] Sécurité autour de la validation des catégories incomplète. Toutes les conditions de validitée ne sont pas respectées (24/07/2022) | Intégrité

- [] S'il y'a une erreur dans le formulaire de création du projet, le projet risque d'être enristré si l'erreur intervient après la ligne de création du projet. (23/07/2022) | Metier

- [] Vérifier que les données sont trimées avant d'être insérée en base de données (18/07/2022) | Intégrité

- [] Le champs statut et le type de projet n'ont pas de valeur par défaut au niveau de la modification.  (17/07/2022) | Intégrité

- [] Corriger le rendu des cartes de projets (16/07/2022) | Design

- [] Faire un bouton qui permet d'afficher les informations des projets en mode mobile(16/07/2022) | Design

- [] Limités la taille des urls et autres contenu à risque de dépassement avec des ... (16/07/2022) | Design

- [] (Critique) On ne vérifie pas que le statut existe bel et bien (16/07/2022) | Intégrité

- [] Gestion des doublons dans les tags (15/07/2022)

- [] Limitée les tags à 10 (15/07/2022)

- [] Vulnérabilité au niveau de la sélection du type et du livrable d'un projet. Pas de contrôle de l'existence des valeurs dans la base de données (15/07/2022) | Intégrité

- [] Pas de contrôle au niveau des tags, les tags doivent avoir une taille max de 100 caractères et doivent être en petits caractères 15/07/2022) | Intégrité

- [] Gestion des caractères spéciaux au niveau des entrées | Intégrité

- [] Gestion des erreurs php des formulaires livewire | Intégrité

- [] Bien sécuriser les forumlaires des catégories | Intégrité

- [] Pas de control de vérification du role administrateur lors de l'ajout d'une catégorie | Intégrité

- [] Uniformiser le design des modals, utiliser des composants | Desisgn

- [] Mettre en place en place un loader au niveau des interactions instannées | Desisgn

- [] Vérifier que le nom d'une catégorie est unique | Intégrité

- [] Pas de control de l'appartenance du projet avant supression ou modification (15/06/2022) | Intégrité

- [] Réduire le texte de l'input du nom de code (23/07/2022) | Intégrité

## Others
	- [] Créer un outil pour peupler la base de données en local uniquement !!! (Pas obligation)
	- [] (!) Ajouter des tags au projet et les visualiser dans l'administration et affichier les autres catégories dans l'admin (Pas obligatoire)
	- [] Ajouter les tags aux formulaires de projets (Pas obligatoire)
	- [] Faire en sorte qu'un administrateur puisse créer d'autres administrateur (Pas obligatoire)
	- [] Intégrer une gestion des utilisateurs (Nommer ou démettre un administrateur) - (Pas obligatoire)
	- [] Utiliser un système de pagination sur les catégories | sur les projets
