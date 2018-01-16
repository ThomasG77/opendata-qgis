L'objectif principal est de permettre de prendre en main QGIS pour comprendre à quoi il peut servir dans le cadre de l'OpenData.


Nous partons du présupposé que vous avez installé QGIS. Nous nous basons sur la version 2.18.

Vous devez après avoir récupéré ce dépôt, allez dans fr-en-adresse-et-geolocalisation-etablissements-premier-et-second-degre/ et décompresser les 2 fichiers zip (lié à des contraintes de taille de fichier sur Github) et faire de même avec `ADMIN-EXPRESS-COG_1-0__SHP__FRA_2017-06-19.7z`

## Première approche: les données administratives "de base"

Pour cela, nous allons commencer par réutiliser des données OpenData. Nous allons commencer avec avec celles d'Admin Express. Il existe deux types de versions:

* celle à rythme mensuel qui prend en compte les regroupements de communes comme les communes nouvelles
* celle annuelle qui est mis à jour une fois par an

Vous devez allez sur le site <http://professionnels.ign.fr/adminexpress> pour le récupérer.

Sinon vous pouvez aussi utiliser le lien direct <https://wxs-telechargement.ign.fr/x02uy2aiwjo9bm8ce5plwqmr/telechargement/prepackage/ADMINEXPRESS-COG-PACK_2017-07-07$ADMIN-EXPRESS-COG_1-0__SHP__FRA_2017-06-19/file/ADMIN-EXPRESS-COG_1-0__SHP__FRA_2017-06-19.7z>

Après récupération, décompresser le fichier (il vous faudra [7zip](http://www.7-zip.org/) si vous ne l'avez pas)

Allez ensuite dans `ADMIN-EXPRESS-COG_1-0__SHP__FRA_2017-06-19/ADMIN-EXPRESS-COG/1_DONNEES_LIVRAISON_2017-06-19/ADE-COG_1-0_SHP_LAMB93_FR` et copiez le fichier `Projet_Carto_ADMIN_EXPRESS_1-1_FXX.qgs` dedans (ce dernier est au même niveau que ce README.md)
Ce fichier est un report d'un projet QGIS livré avec les données Admin Express mensuelles. Le crédit est donc IGN.

Double-cliquez dessus et normalement QGIS va l'ouvrir pour vous.

Nous allons explorer trois points principaux:

* Naviguer sur la carte (zoom, dézoom, zoomer sur la couche)
* Sélectionner les informations depuis la carte
* Sélectionner les informations depuis la table attributaire

## Utiliser des fonds de plan pour se repérer

Dans le premier cas, nous avons vu comment ouvrir un projet QGIS existant mais souvent lorsqu'on ouvre un fichier cartographique provenant d'un portail OpenData, il n'est pas toujours possible de se répérer. Il nous faut du contexte.

Pour cela, nous allons voir comment utiliser un plugin QGIS nommé QuickMapServices pour avoir des fonds de plan.

## Afficher des données ponctuelles, les écoles, provenant d'un portail OpenData

Pour cela, se rendre sur <https://www.data.gouv.fr/fr/datasets/adresse-et-geolocalisation-des-etablissements-denseignement-du-premier-et-second-degres-1/>

Nous allons avoir 2 approches pour faire la même chose:

* en passant par un fichier dit SIG (spécifique à la cartographie)
* en passant par un fichier dit "à plat"

Nous allons ainsi découvrir comment ajouter une couche de fichiers SHP, comment ajouter des points sur une carte depuis un fichier contenant des coordonnées de points.

## Compter les écoles par communes

* Utilisation des outils de traitement de QGIS (fonction compter les points uniques par polygones)

## Rapporter à la population

Population légale 2015 <https://www.insee.fr/fr/statistiques/3292622?sommaire=3292701>

## Aller plus loin

Compter les effectifs d'élèves pour rapporter le nombre d'élèves à la population

<https://www.data.gouv.fr/fr/datasets/effectifs-deleves-des-ecoles-du-premier-degre-public-et-prive-sous-tutelle-du-ministere-en-charge-de-leducation-nationale/>

## Ressources QGIS

* <https://qgis.org>
* <http://www.geoinformations.developpement-durable.gouv.fr/qgis-supports-pedagogiques-r947.html>
* <http://ouvrir.passages.cnrs.fr/tutoqgis/>
* <http://sigea.educagri.fr/tutoriels-de-logiciels-sig/qgis.html>
