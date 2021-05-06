# Méthodologie
## 1. Création du site web 
Pour les besoins du projet, nous avons crée un site web à partir de github qui va nous permettre de rassembler et publier toutes les informations collectées dans le processus de réalisation du projet. Nous avons crée une page principale appélée "Provenance des oeuvres" qui va contenir (ou héberger) les pages annexes par le biais de liens internes.
## 2. Traitement des données avec OpenRefine
Pour mieux cerner notre sujet nous avons fait un traitement des données sur Openrefine. Il s’agit dans un premier temps de fusionner les données présentes dans les différentes bases de données pour établir les liens entre les objets, les collectionneurs et les ventes. De ce fait, nous avons rassemblé sur un même fichier l’ensemble des trois bases de données sur Openrefine ensuite nous avons procédé à un néttoyage de la nouvelle base de données en effectuant des rajouts et des suppressions de colonnes. Tout d’abord nous avons créé une page Github qui va rassembler l’ensemble de nos représentations. Selon la problématique de départ, nous avons conservé les champs qui vont nous permettre de répondre aux différentes interrogations que nous nous sommes posées.
## 3. Outils de visualisation des données
Ainsi après avoir fusionné nos bases de données en un seul fichier nous avons réalisé des visualisations sur différents outils comme ??????? etc.
Pour l’étape de la visualisation nous avons décidé de ne pas prendre les prix parce qu’ils changent d’une année à l’autre et qu’on ne dispose pas d’outils pour les convertir

## 4. Difficultés rencontrées
Nous avons eu du mal à fusionner nos données sur une même base de données.
Nous avons perdu du temps à trouver le fichier de départ. Après plusieurs tentatives dans le fichier "objets", on a finalement abandonné cette idée là. Et on est parti du fichier "vente" comme référence. Ce qui nous a permi de garder nos données dans leur intégrité. 
Au niveau de la transformation des dates également, on a eu du mal. Finalement, la formule magique qu'on a trouvé pour cela c'est de diviser la colonne qui contient nos dates en trois colonnes (une colonne année, une colonne "mois" et une colonne "jour"), avant d'appliquer enfin la formule suivante : 

```
value+"-"+cells["vente_date_2"].value+"-"+cells["vente_date_1"].value
```
