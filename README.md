[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/637AiCGX)
# Exercice 2.1 : Dessiner le schéma relationnel (MCD et MLD) d'une bibliothèque pour comprendre les liens logiques

## Contexte
La bibliothèque municipale "Le Savoir Partagé" est en pleine crise. Leur système de gestion actuel repose sur un mélange de cahiers papier et de fichiers Excel désorganisés. Résultat : ils ne savent jamais si un livre est réellement en rayon, qui est en retard, ou combien d'exemplaires d'un best-seller ils possèdent vraiment.

Tu viens d'être missionné par Mme Bénie, la directrice de la bibliothèque municipale. Son diagnostic est sans appel : "On ne s'en sort plus." L'établissement gère 15 000 ouvrages et 2 000 adhérents avec un fichier Excel qui pèse 50 Mo et trois cahiers à spirales pour les retours. Le système craque de partout et génère des situations absurdes tous les jours :

Le cauchemar des doublons : Quand ils achètent 5 exemplaires du dernier "Astérix", ils créent 5 lignes identiques dans Excel. Résultat ? Impossible de savoir quel exemplaire précis a été déchiré par un chien ou égaré. Ils ne savent pas si l'exemplaire N°4 est en rayon ou chez un abonné.

La traque des retardataires : Actuellement, pour savoir qui n'a pas rendu son livre, Mme Bénie doit croiser manuellement le cahier des sorties avec la liste des emails. S'il y a une faute de frappe sur le nom de l'adhérent, le mail de relance n'arrive jamais.

L'énigme des auteurs : Un coup l'auteur est saisi "Victor Hugo", un coup "Hugo, Victor", un coup "V. Hugo". Pour sortir la liste des œuvres d'un même écrivain, c'est un calvaire de filtres.

L'expérience client gâchée : Un adhérent appelle pour réserver un livre. Excel dit "Disponible", l'adhérent traverse toute la ville, mais arrivé sur place : le livre est en fait en réparation depuis un mois. L'information n'était notée nulle part.

Ta mission : En tant que Data Analyst, tu dois dessiner l'architecture de leur future base de données SQL. Tu vas concevoir le MCD (la logique métier) puis le MLD (la structure technique des tables). Sans un schéma parfait, le futur logiciel ne fonctionnera jamais.

 

## Objectifs pédagogiques
À la fin de cet exercice, tu seras capable de :

Isoler les entités (distinguer l'objet physique de l'œuvre littéraire).

Définir les attributs et assurer l'atomicité des données (une info par colonne).

Modéliser les cardinalités pour traduire les règles métier (qui emprunte quoi et combien).

Modéliser les relations complexes : Gérer les emprunts (Qui a quoi ? Depuis quand ?) et les auteurs multiples.
Passer du conceptuel au technique : Transformer tes idées (MCD) en exploitables (MLD) avec clés primaires et étrangères.
Garantir l'intégrité via les clés primaires (ID uniques).

 

## Modalités pédagogiques
L’exercice sera réalisé selon les modalités suivantes :

Méthode : Apprentissage par la conception (MCD et MLD).

Durée : 3 jours (Analyse > Modélisation > Documentation).

Outils : Lucidchart, Draw.io, ou tout outil de diagramme de ton choix.

Collaboration : Utilise le canal dédié pour poser la question fatale : "Si un livre a deux auteurs, je fais comment ?".

 

## Astuces de Data Analyst
L'œuvre vs l'Exemplaire : Un livre (ex: "Le Petit Prince") peut exister en 10 exemplaires physiques dans la bibliothèque. Si tu ne crées qu'une table "Livre", comment sais-tu quel exemplaire précis est abîmé ?
L' Atomicité : Ne crée jamais une colonne "Adresse" unique. Sépare le Code Postal, la Ville et la Rue. C'est la base pour faire des stats propres par ville plus tard !
Les Cardinalités : Demande-toi toujours : "Un Adhérent peut-il avoir zéro emprunt ?" (Oui -> 0,N) ou "Un livre peut-il appartenir à deux adhérents en même temps ?" (Non -> 0,1).
 

## Livrables
Le Schéma MCD : Une image nette (PNG/PDF) ou un lien vers votre diagramme.

Le Schéma MLD : Une image nette (PNG/PDF) ou un lien vers votre diagramme.

Le Dictionnaire des Données : Un tableau listant chaque champ, son type (INT, VARCHAR, DATE) et sa description.

Dépôt GitHub : Un dossier **Exo-Library-MCD-MLD-DICO** contenant vos fichiers.

Note pour la soumission :

Le lien vers le repos Github sur lequel vous allez déposer votre travail :

Pour la classe 2026-janvier-da-soir-b cliquez ici
Pour la classe 2026-janvier-da-midi-c cliquez ici

après avoir déposer votre travail sur Github, veuillez copier l'url du repos Github et finaliser votre soumission en le soumettant sur canvas.
