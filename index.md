# Cycle de l'eau
Notre projet se base sur l'étude du cycle de l'eau. En étudiant ses facteurs de variation et l'impact sur son environnement 

## Water Cycle
Our project is based on the study of the water cycle. By studying its variation factors and the impact on its environment

## Introduction 

Le cycle de l'eau est un processus naturel qui se produit sur Terre et qui implique l'évaporation de l'eau des océans, des rivières et des lacs, qui se transforme en vapeur d'eau pour finalement produire de la pluie, de la neige ou d'autres formes de précipitations. L'eau qui tombe sur la terre s'infiltre dans le sol ou retourne dans les océans, les rivières et les lacs, où elle peut être utilisée par les plantes, les animaux et les êtres humains. Le cycle de l'eau est un processus continu et vital pour la vie sur Terre. Dans notre modélisation, nous nous intéresserons sur la viabilité de l’eau et d’expliquer les différents facteurs qui modifient la dynamique de l’eau

![image](https://user-images.githubusercontent.com/125458910/233639121-37499bbf-42df-4153-96ec-f7acb25dd636.png)


## Présentation de l'équipe

|(´・ω・｀)| ( ͡° ͜ʖ ͡°) | ಠ_ಠ | :) |
|-----|--|--|--|
| J.Gueneau| E.Mcirdi | J.sahie  | Itokiana  |


## Description synthétique du projet

**Problématique :** 
En quoi la modélisation et la simulation informatique du cycle de l'eau à travers des codes permettent-elles d'améliorer notre compréhension de ce processus naturel et de mieux évaluer la durabilité d'un territoire ?

**Hypothèse principale :**
Le viabilité de l’eau est perturbé par des différents facteurs environnementaux.  

**Hypothèses secondaires :** 
Le cycle de l'eau peut être perturbé en bien comme en mal  par certaines actions de l'Homme.

**Objectifs :**
Réussir à expliquer simplement et montrer à travers un modèle simple, les différents facteurs pouvant affecter la viabilité de l'eau dans un écosystème donné. Ainsi, notre objectif démontrera que l’eau est très sensible aux changements. 

## Modèle :
Notre modèle a pour but de montrer comment différents facteurs peuvent affecter la viabilité de l'eau dans un écosystème donné. Pour cela nous créer un monde virtuel grâce à Python qui sera composées de nombreuses cellules, faisant base de représentation de l’eau, celles-ci seront colorées de 2 couleurs principaux pour démontrer la viabilité, ainsi : 

Rouge : Eau Non vivable
Vert : Eau Vivable  

La viabilité sera influencé dans notre modèle par  3 facteurs :
-Température 
-Précipitations
-Proximité d’une rivière

Ainsi grâce à ces facteurs nous pouvons montrer, même si il n’est pas modélisé dans notre modèle que le réchauffement climatique peut affecter l’écosystème dans laquelle nous vivons, étant donné qu’il augmente les températures et les précipitations ce qui touche la viabilité de nos eaux. 

## Modélisation du projet (base du modèle) : 

Pour instaurer notre modèle dans Python, nous avons créés des tableaux en utilisant les bibliothèques NumPy et Matplotlib.

![image](https://user-images.githubusercontent.com/125458910/233635110-a93eec54-6f3d-420f-963f-79a46dff91b2.png)
Pour instaurer nos facteurs : 
- "temp_min" et "temp_max" définissent les limites de la température d'une cellule  dans le  tableau "monde" 

=> "precipitation" est une liste contenant les valeurs de précipitation en pourcentage
=>"riviere" : liste booléenne qui représente qui représente la présence ou l'absence d'une rivière pour chaque mois de l'année.
=> "monde" sera la représentation de notre carte avec des cellules de 20x20.

## Modification des valeurs : 
Nous avons modélisé notre monde  dans une matrice de 20x20 cellules. L’habitabilité des cellules  sera une variable binaire appelée "monde", où 1 signifie habitable et 0 signifie inhabitable.  Ensuite, nous utilisons une boucle for pour parcourir chaque cellule de la matrice et déterminer si elle est habitable ou non. 
![image](https://user-images.githubusercontent.com/125458910/233635402-da0b0045-cfb5-42bd-9ea2-2d03ee086247.png)
Cette partie du modèle est responsable de la création du monde virtuel c’est ce qui nous permet de générer notre monde. Nous avons modélisé notre monde  dans une matrice de 20x20 cellules, chaque cellule étant initialement définie comme non habitable. 
Pour chaque facteur on a définie des plages définie, si la température de la cellule est en dehors de la plage définie, ou si les précipitations sont trop faibles ou trop élevées, ou si la cellule se trouve dans une zone inappropriée par rapport à la rivière, elle est considérée comme non habitable. Sinon, elle est considérée comme habitable.

## Instauration de la dynamique : 
![image](https://user-images.githubusercontent.com/125458910/233635767-e57b8c85-3379-4ca7-b1f4-bc48b47c581c.png)![image](https://user-images.githubusercontent.com/125458910/233635816-54cdfc29-3c14-409b-9057-389115ec58f9.png)

Pour instaurer une dynamique, nous avons simulé une semaine de changements climatiques aléatoires en affectant des valeurs aléatoires à la température, la précipitation et le niveau de la rivière pour chaque jour de la semaine. Il y a une boucle for pour chaque jour de la semaine et une autre boucle for pour modifier les variables du monde virtuel chaque jour. À chaque jour, la température minimale et maximale est modifiée de façon aléatoire, la quantité de précipitation est modifiée de façon aléatoire pour chaque jour et la position de la rivière est décalée d'un ou deux éléments de façon aléatoire. Enfin, une boucle parcourt toute la matrice pour générer la carte de l'environnement, qui montre les zones habitables en vert et les zones non habitables en rouge. La température minimale et maximale est modifiée en ajoutant une valeur aléatoire entre -5 et 5 à chaque itération. Les précipitations sont également modifiées aléatoirement en ajoutant une valeur aléatoire entre -10 et 10 à chaque jour. Si la valeur des précipitations est inférieure à 0 ou supérieure à 100, elle est ajustée à 0 ou 100 respectivement. La position de la rivière est modifiée aléatoirement en décalant la liste de la rivière vers la gauche ou vers la droite d'une position (de -1, 0 ou 1).

## Résultats

![image](https://user-images.githubusercontent.com/125458910/233636035-746039ac-db08-4526-9045-d0c91da8632b.png)

![image](https://user-images.githubusercontent.com/125458910/233636064-5576629a-63af-499d-8d92-e758fd4b45d8.png)

## Conclusion 
Le modèle que nous avons créé vise à simuler la viabilité de l'eau dans un écosystème donné en fonction de trois facteurs clés : la température, les précipitations et la présence d'une rivière. Le modèle utilise des données aléatoires pour générer des résultats différents à chaque exécution et simule la dynamique sur une période de 7 jours. Les résultats sont affichés sous forme d'une carte qui montre les zones habitables en vert et non habitables en rouge. Le modèle est simple mais efficace et il permet de mieux comprendre les enjeux environnementaux actuels et de sensibiliser le à l'importance de préserver notre écosystème. 
Présentation du choix de modélisation, des outils, du code et des résultats (tableaux, courbes, animations...) (**avec une analyse critique**).

## Lien vers page de blog : <a href="blog.html"> C'est ici ! </a>

## Bibliographie :

**Carte mentale de vos mots-clés, en utilisant** <a href="https://framindmap.org/mindmaps/index.html">Framindmap </a> 

Liste de l'ensemble des ressources bibliographiques utilisées pour vos travaux. **<= Indiquez le canal utilisé pour les trouver (Google Scholar, sources wikipedia, ressources en ligne SU, ...)**
