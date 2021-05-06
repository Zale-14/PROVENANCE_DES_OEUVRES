# Méthodologie
## 1. Création du site web 
Pour les besoins du projet, nous avons crée un site web à partir de github qui va nous permettre de rassembler et publier toutes les informations collectées dans le processus de réalisation du projet. Nous avons crée une page principale appélée "Provenance des oeuvres" qui va contenir (ou héberger) les pages annexes par le biais de liens internes.
## 2. Traitement des données avec OpenRefine
Pour mieux cerner notre sujet nous avons fait un traitement des données sur Openrefine. Il s’agit dans un premier temps de fusionner les données présentes dans les différentes bases de données pour établir les liens entre les objets, les collectionneurs et les ventes. De ce fait, nous avons rassemblé sur un même fichier l’ensemble des trois bases de données sur Openrefine ensuite nous avons procédé à un néttoyage de la nouvelle base de données en effectuant des rajouts et des suppressions de colonnes. Tout d’abord nous avons créé une page Github qui va rassembler l’ensemble de nos représentations. Selon la problématique de départ, nous avons conservé les champs qui vont nous permettre de répondre aux différentes interrogations que nous nous sommes posées.
## 3. Outils de visualisation des données
Ainsi après avoir fusionné nos bases de données en un seul fichier, nous avons réalisé des visualisations sur différents outils tels que Flourish et datawrapper.
Pour l’étape de la visualisation des données, nous avons décidé de mettre l'accent sur les champs qui peuvent nous permettre d'avoir des visuels en adéquation avec nos attentes.

## 4. Difficultés rencontrées
Nous avons voulu au début utiliser la base de données "Objet" comme base de données de référence et d'y joindre les deux autres bases de données "vente" et "collectionneurs". La base de données "objet" étant volumineuse nous avons eu des difficultés à fusionner nos données qui sont liées notamment à des pertes de données.
Nous avons perdu du temps à trouver le fichier de départ. Après plusieurs tentatives de fusion en vain  le fichier "objets", nous avons décidé de surseoir au fichier "objet" comme fichier de référence et nous avons choisi à la place la base de données "vente". Cette dernière nous a permis de garder nos données dans leurs intégralités car elle est moins volumineuse contrairement à la base de données "objet". 

Une autre difficulté liée à la fusion des données, a été constatée au niveau de la transformation des dates. Finalement, la formule magique qu'on a trouvé pour cela c'est de diviser la colonne qui contient nos dates en trois colonnes (une colonne année, une colonne "mois" et une colonne "jour"), avant d'appliquer enfin la formule suivante : 

```
value+"-"+cells["vente_date_2"].value+"-"+cells["vente_date_1"].value
```
