# Méthodologie
## 1. Traitement de données
Etant donné que nous disposons déjà des données fournies par l’INHA, nous avons premièrement cherché à identifier les données utiles pour notre analyse afin de les normaliser selon leur pertinence, de manière à avoir un corpus propre et exploitable. Cette étape s’est donc substituée à celle de la récolte des données, l’une des étapes clés de la datavisualisation. Pour cette phase, les outils de traitement de données (notamment OpenRefine, LibreOffice, NotePad++…) nous ont été d’un apport inestimable.  
Avec OpenRefine, il était question d’identifier dans chaque base de données (fichier) les champs (colonnes) nécessaires pour visualiser la mobilité des œuvres d’art ;
De procéder à l’élimination des champs vides qui n’ont aucune utilité, au renommage de certaines colonnes, car certaines pouvaient prêter à confusion ou alors la matrice la plus importante du nom était cachée du fait de la longueur de celle-ci ;

Pour ce qui est des dates, le passage du format français au format anglo saxon permet de faciliter l’identification du type de métadonnées par les outils de visualisation avec la fonction suivante : value+"-"+cells["vente_date_2"].value+"-"+cells["vente_date_1"].value
L’usage de LibreOffice est lié au fait qu’on pouvait facilement déplacer une colonne d’un point A à un point B en faisant un copier-coller, ce qui est difficilement réalisable avec OpenRefine.  

Quant à NotPad++, il a surtout servi à créer des codes lors de la fusion, il permet alors de remplacer des quantités importantes de caractères grâce à la fonction « rechercher & remplacer ».
En effet, il était indispensable de mettre les trois bases de données normalisées dans un seul et unique fichier. Il s’agit dans un premier temps de fusionner les données présentées dans les différentes bases de données pour établir les liens entre les objets, les collectionneurs et les ventes… Cette union a été rendue possible grâce à une clé d’identification unique qui relie le fichier ventes à celui des objets et enfin à celui des acteurs grâce au Template suivant : cell.cross(“nomduprojet”, “nomColonneeCléIntermédiaire”)[0].cells[“nomColonneArécupérer”].value
## Pistes de réflexions 
Le troisième jour du séminaire a été un tournant décisif dans la réalisation du projet parce que c’était le dernier jour avant la présentation devant le jury. Ainsi plusieurs pistes de réflexions ont été soulevées afin de trouver la bonne astuce ou technique qui nous a permis d’avoir une approche globale du sujet et d’en définir les différents axes de visualisation qui permettraient d’apporter des réponses à notre problématique. Cette image ci-dessous retrace les différentes pistes de réflexion qui nous ont conduit aux résultats obtenus.
[priémere réflexion](pistes.jpg)


# A supprimer
Création du site web 
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
