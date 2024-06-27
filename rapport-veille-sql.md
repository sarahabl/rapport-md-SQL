# SQL et Bases de Données Relationnelles

## Intro
En tant que développeur front-end moderne, maîtriser SQL est devenu une **compétence essentielle** pour créer des applications web performantes, dynamiques et riches en données. SQL permet de **stocker**, **manipuler**, **récupérer et analyser des données** de manière efficace, en tirant parti de la puissance des **bases de données relationnelles**.

Ce rapport de veille vise à synthétiser les points clés à retenir sur SQL pour les développeurs front-end.  Il couvrira les concepts de base, les requêtes courantes, les techniques d'optimisation, les aspects de sécurité, les cas d'utilisation courants, les alternatives à SQL et les bases de données populaires, afin de vous offrir une vue d'ensemble complète.

### Définitions
1. **SQL** : Acronyme de Structured Query Language (Langage de Requête Structuré), est un langage standardisé utilisé pour gérer et manipuler les bases de données relationnelles. Il permet aux utilisateurs de créer, lire, mettre à jour et supprimer des données dans une base de données relationnelle.
2. **Base de données** : Ensemble structuré d'informations, organisé de manière à faciliter l'accès, la gestion et la mise à jour des données. Les bases de données sont utilisées par les organisations pour stocker, gérer et récupérer des informations cruciales.
3. **Base de données relationnelle** : Un type de base de données qui organise les données en table. Chaque table, également appelée relation, contient des lignes (enregistrements) et des colonnes (champs). Les tables peuvent être reliées entre elles par des relations basées sur des clés.

## L’importance des Bases de Données Relationnelles

### Les caractéristiques d'une Base de Données Relationnelle
- Tables : Les données sont organisées en tables, chaque table ayant des colonnes définies par un schéma (structure) fixe.
- Schéma Rigide : La structure des tables est définie à l'avance par un schéma, ce qui impose une certaine rigidité mais assure la cohérence des données.
- SQL (Structured Query Language) : Les bases de données relationnelles utilisent le langage SQL pour interroger et manipuler les données. SQL est un langage standardisé, ce qui le rend puissant et polyvalent.
- Clés Primaires et Étrangères :
  - Clé Primaire : Un identifiant unique pour chaque enregistrement dans une table.
  - Clé Étrangère : Un champ qui crée un lien entre deux tables, établissant une relation entre les données.

### Pourquoi utiliser une Base de Données Relationnelle ?
- Cohérence des Données : Les relations définies par des clés primaires et étrangères garantissent la cohérence et l'intégrité des données.
- Sécurité et Transactions : Supporte les transactions ACID (Atomicité, Cohérence, Isolation, Durabilité) qui assurent que les opérations sont traitées de manière fiable.
- Normalisation : Permet de minimiser la redondance et d'organiser les données de manière logique et efficace.
- Langage Standardisé : L'utilisation de SQL permet une grande puissance et flexibilité pour les requêtes et les opérations sur les données.

### Les transactions et intégrité des données
Les transactions et l'intégrité des données sont des mécanismes essentiels pour maintenir la fiabilité, la cohérence et la robustesse des bases de données relationnelles. Ils permettent de s'assurer que toutes les opérations sont effectuées de manière sûre et que les données restent toujours précises et cohérentes.

En résumé : 
- **Les transactions** : Assurent que les séries d'opérations sont exécutées de manière atomique, cohérente, isolée et durable.
- **L'intégrité des Données** : Garantis que les données sont correctes et cohérentes, en respectant des règles spécifiques aux entités, aux relations entre entités et aux valeurs des colonnes. Par exemple en interdisant les entrées orphelines dans les tables enfants.

## Le rôle du langage SQL

### Concepts de base du SQL :
- **Bases de données relationnelles**: Elles stockent les données dans des tables structurées, reliées entre elles par des relations définies.
- **Langage SQL**: Permet de créer, lire, mettre à jour et supprimer des données dans les bases de données relationnelles.
- **Tables**: Composées de lignes (enregistrements) et de colonnes (champs), représentant des données organisées.
- **Requêtes SQL**: Instructions permettant d'interagir avec les bases de données, comme SELECT, INSERT, UPDATE et DELETE.

### Quand utilise-t-on SQL ?
SQL est utilisé dans une large variété de cas d'utilisation, notamment :

1. **Gestion de bases de données**:
- Création et modification de structures de bases de données
- Insertion, mise à jour, suppression et récupération de données
- Administration des utilisateurs et des permissions

2. **Développement d'applications**:
- Backend d'applications web pour stocker et récupérer des données
- Persistance des données dans les applications de bureau et mobiles (produits, stocks, transactions, etc.)
- Synchronisation entre appareils et serveurs

3. **Analyse et Reporting**:
- Extraction de données pour rapports et tableaux de bord
- Analyse de données pour identifier des tendances et des modèles

#### Cas d'utilisation courants :
- E-commerce: gestion des produits, commandes et clients
- CMS: stockage et récupération de contenu
- Gestion de la relation client (CRM): suivi des interactions avec les clients
- Applications de réseaux sociaux: gestion des profils, des publications et des interactions
- Jeux en ligne: sauvegarde des données des joueurs et du jeu

#### Fonctionnalités clés de SQL :
- **Recherche et filtrage de données**: Localiser des informations spécifiques dans de grandes quantités de données.
- **Tri et regroupement**: Organiser les données de manière significative pour une analyse plus facile.
- **Agrégations**: Calculer des valeurs récapitulatives (somme, moyenne, etc.) pour obtenir une vue d'ensemble des données.
- **Jointure de tables**: Combiner des données provenant de plusieurs tables pour obtenir une vue complète des relations.
- **Modification de données**: Insérer, mettre à jour et supprimer des données de manière efficace.
- **Contrôle des transactions**: Garantir l'intégrité des données lors des opérations simultanées.
- **Sécurité des données**: Protéger les données contre les accès non autorisés et les modifications malveillantes. SQL permet de contrôler l'accès aux données et les actions des utilisateurs, limiter l'accès à des sous-ensembles de données sensibles, protéger les données en repos et en transi et d'éviter les injections SQL.

### Requêtes SQL courantes
- **SELECT**: Extraire des données d'une ou plusieurs tables.
- **FROM**: Spécifier la table source des données.
- **WHERE**: Filtrer les résultats en fonction de conditions spécifiques.
- **ORDER BY**: Trier les résultats par une ou plusieurs colonnes.
- **JOIN**: Combiner des données de plusieurs tables.
- **GROUP BY**: Regrouper les résultats par une ou plusieurs colonnes.
- **UPDATE**: Mettre à jour une donnée
- **AGGREGATIONS**: Calculer des valeurs résumées (SUM, AVG, COUNT, MIN, MAX).

### Techniques d'optimisation des requêtes SQL
1. **Indexation**: Créer des index sur les colonnes fréquemment interrogées.
2. **Utiliser des vues matérialisées**: Pré-calculer des requêtes complexes pour des performances accrues.
3. **Analyser les requêtes**: Identifier les goulots d'étranglement et optimiser les requêtes en conséquence.
4. **Choisir le bon type de jointure**: Sélectionner la jointure la plus adaptée à la requête.


## Conclusion
SQL est un outil essentiel pour les développeurs front-end, cela nous permet : 
- Comprendre le fonctionnement global des applications notamment l’architecture
- Communiquer efficacement avec les développeurs et administrateurs de bases de données
- Optimiser les requêtes de données
- Travailler avec des API qui abstrait les détails de la base de données


### Ressources
De nombreuses ressources en ligne sont disponibles pour approfondir os connaissances en SQL et devenir un développeur front-end accompli : 
- https://www.data-bird.co/blog/langage-sql
- https://aws.amazon.com/fr/what-is/sql/
- https://sql.sh/cours/jointures
- https://datascientest.com/index-sql-tout-savoir#:~:text=Le%20r%C3%B4le%20des%20index%20SQL,exploration%20rapide%20de%20la%20data.
