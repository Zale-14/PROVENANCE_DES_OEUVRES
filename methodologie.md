# Méthodologie
## 1. Traitement des données avec OpenRefine
Pour mieux cerner notre sujet nous allons tout d’abord partir d’un traitement des données sur Openrefine. Il s’agira dans un premier temps de fusionner les données présentes dans les différentes bases de données pour établir les liens entre les objets, les auteurs et les ventes. De ce fait nous avons rassembler sur un même fichier l’ensemble des trois bases de données sur Openrefine ensuite on a procédé à un néttoyage de la nouvelle base de données en effectuant des rajouts et des suppressions de colonnes. Tout d’abord nous avons créé une page Github qui va rassembler l’ensemble de nos représentations. Selon la problématique de départ, nous avons conservé les champs qui vont nous permettre de répondre aux différentes interrogations que nous nous sommes posées.
## 2. Outils de visualisation des données
Ainsi après avoir fusionné nos bases de données en un seul fichier nous avons réalisé des visualisations sur différents outils comme ??????? etc.
Pour l’étape de la visualisation nous avons décidé de ne pas prendre les prix parce qu’ils changent d’une année à l’autre et qu’on ne dispose pas d’outils pour les convertir

## 3. Difficultés rencontrées
Nous avons eu du mal à fusionner nos données sur une même base de données.
Nous avons perdu du temps à trouver le fichier de départ. Après plusieurs tentatives dans le fichier "objets", on a finalement abandonné cette idée là. Et on est parti du fichier "vente" comme référence. Ce qui nous a permi de garder nos données dans leur intégrité. 
Au niveau de la transformation des dates également, on a eu du mal. Finalement, la formule magique qu'on a trouvé pour cela c'est de diviser la colonne qui contient nos dates en trois colonnes (une colonne année, une colonne "mois" et une colonne "jour"), avant d'appliquer enfin la formule suivante : 

value+"-"+cells["vente_date_2"].value+"-"+cells["vente_date_1"].value
