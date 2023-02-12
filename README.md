# Projet : Détection et classification d'anomalies dans un signal de rayonnement gamma.

<b> Auteurs : </b> Damien BOUET, Pierre CHARDIN, Noé DEBROIS et Marion POIRIER<br>
<b> Date : </b> de Février 2022 à Janvier 2023<br>
<b> Implication personnelle : </b> 100 heures

## Contexte et objectifs

Ce projet a pour but de déployer et d'évaluer un système de détection d'anomalies dans une serie temporelle.
Nous nous intéresserons ici à un signal de rayonnement gamma, et séparerons le projet en 2 parties, avec 2 approches différentes :
- La première partie, basée sur l'algorithme de la Matrix Profile, détectera dans le signal des motifs récurrents et les classifiera.
Elle permettra ainsi de détecter les anomalies ou comportement du rayonnement qui se sont déjà produit dans le passé et de les classifier en différents groupes par ressemblance.

- La deuxième partie, basée sur la prédiction du signal par un réseau de neurones récurrents LSTM puis la comparaison entre le signal et le modèle, détectera toutes les anomalies majeures du signal. Elle permettra de détecter les anomalies, peu importe qu'elles se soient déjà produites ou non : cette deuxième approche permettra donc, entre autres, de détecter des anomalies qui ne se sont jamais produite, complétant ainsi les fonctionnalité de la première apporche.

Ainsi, dans un cadre, par exemple, de surveillance nucléaire, ce système permettra de détecter en temps réel des potentielles anomalies ou comportements caractéristiques dans la mesure du rayonnement gamma. Ce système pourra ainsi alerter les opérateurs qu'une anomalie est en train de se produire (2<sup>ème</sup> approche) et sera même capable d'indiquer de quel type d'anomalie ou de comportement il s'agit, dans l'hypothèse où une situation similaire s'est déjà produite dans le passé (1<sup>ère</sup> approche). Cette 1<sup>ère</sup> approche apportera même une aide aux experts, pour comprendre les comportements du système nucléaire étudié, en leur fournissant les motifs récurrents regroupés par catégories.

## Technologies utilisées

#### 1<sup>ère</sup> approche
- Matrix Profile
- K-means
#### 2<sup>ème</sup> approche
- Réseau de neurones récurrents LSTM (Tensorflow)
- Utilisation d'un seuil intelligent pour déduire les anomalies de l'erreur de prédiction
- Méthode de Pruning pour écarter les faux-positifs


## Références bibliographiques
- Yeh and al, “Matrix Profile I: all pairs similarity joins for time series: a unifying view that includes motifs discords and shapelets”, Proc of 16th
IEEE ICDM, 2016,
- NASA Article : K. Hundman, V. Constantinou, C. Laporte, I. Colwell, and T. Soderstrom, “Detecting Spacecraft Anomalies Using LSTMs and Nonparametric
Dynamic Thresholding,” in Proc. of the 24th ACM SIGKDD, 2018,

