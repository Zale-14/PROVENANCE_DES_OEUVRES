# Méthodologie
## 1. Traitement de données
Etant donné que nous disposons déjà des données fournies par l’INHA, nous avons premièrement cherché à identifier les données utiles pour notre analyse afin de les normaliser selon leur pertinence, de manière à avoir un corpus propre et exploitable. Cette étape s’est donc substituée à celle de la récolte des données, l’une des étapes clés de la datavisualisation. Pour cette phase, les outils de traitement de données (notamment OpenRefine, LibreOffice, NotePad++…) nous ont été d’un apport inestimable.  
Avec OpenRefine, il était question d’identifier dans chaque base de données (fichier) les champs (colonnes) nécessaires pour visualiser la mobilité des œuvres d’art ;
De procéder à l’élimination des champs vides qui n’ont aucune utilité, au renommage de certaines colonnes, car certaines pouvaient prêter à confusion ou alors la matrice la plus importante du nom était cachée du fait de la longueur de celle-ci ;

Pour ce qui est des dates, le passage du format français au format anglo saxon permet de faciliter l’identification du type de métadonnées par les outils de visualisation avec la fonction suivante : 
```
value+"-"+cells["vente_date_2"].value+"-"+cells["vente_date_1"].value
```
L’usage de LibreOffice est lié au fait qu’on pouvait facilement déplacer une colonne d’un point A à un point B en faisant un copier-coller, ce qui est difficilement réalisable avec OpenRefine.  

Quant à NotPad++, il a surtout servi à créer des codes lors de la fusion, il permet alors de remplacer des quantités importantes de caractères grâce à la fonction « rechercher & remplacer ».
En effet, il était indispensable de mettre les trois bases de données normalisées dans un seul et unique fichier. Il s’agit dans un premier temps de fusionner les données présentées dans les différentes bases de données pour établir les liens entre les objets, les collectionneurs et les ventes… Cette union a été rendue possible grâce à une clé d’identification unique qui relie le fichier ventes à celui des objets et enfin à celui des acteurs grâce au Template suivant :

```
cell.cross(“nomduprojet”, “nomColonneeCléIntermédiaire”)[0].cells[“nomColonneArécupérer”].value
```
## Pistes de réflexions 
Le troisième jour du séminaire a été un tournant décisif dans la réalisation du projet parce que c’était le dernier jour avant la présentation devant le jury. Ainsi plusieurs pistes de réflexions ont été soulevées afin de trouver la bonne astuce ou technique qui nous a permis d’avoir une approche globale du sujet et d’en définir les différents axes de visualisation qui permettraient d’apporter des réponses à notre problématique. Cette image ci-dessous retrace les différentes pistes de réflexion qui nous ont conduit aux résultats obtenus.

![réfléxion](https://user-images.githubusercontent.com/75143201/117734790-7780d300-b1f4-11eb-92cb-d53f673f7ec0.jpg)

![reflexion](https://user-images.githubusercontent.com/75143201/117734968-dd6d5a80-b1f4-11eb-921c-5ff5496796fb.jpg)

![reflexion_2](https://user-images.githubusercontent.com/75143201/117735029-f8d86580-b1f4-11eb-929d-9f49c3b293be.jpg)

