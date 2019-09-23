# Logiciel d'annotation : État de l'art

Dans le présent document nous évaluons plusieurs logiciels d'annotation de texte afin d'en sélectionner un pour nos travaux.

Notre objectif est de :

* Annoter des textes pour améliorer nos jeux d'entrainement
* Annoter des textes pour faire de l'extraction d'entités nommées ou de relations, voire autre

Le logiciel "Brat" a déjà été utilisé précedemment pour le début des travaux mais celui-ci, bien que très performant, pose des problèmes d'intégration avec des modèles développés en python. Une de nos contraintes est donc de choisir un logiciel qui permet facilement d'intégrer des resources python.

Il existe beaucoup de logiciels d'annotation de texte avec des capacités et des performances très différentes. On peut en trouver une liste non exhaustive sur les sites suivants :

* <https://www.datasetlist.com/tools/> (attention il y a aussi des outils d'annotation d'images)
* <https://www.quora.com/NLP-what-are-the-best-tools-for-text-annotation>
* <https://www.quora.com/What-is-the-best-open-source-text-annotation-software-The-intent-is-creation-of-a-machine-learning-corpus>
* <http://searchivarius.org/dir/000/00C/003/00I>

Nous avons sélectionner une dizaine de ces outils d'annotation de texte afin de les comparer.

## Critères

Dans un premier temps nous avons défini des critères sur lesquels nous baser pour orienter notre choix. Les voici :

* **Le langage de programmation utilisé pour déveloper le logiciel** : Le but ici est d'évaluer la facilité d'intégration de notre propre code python.
* **La documentation** : Il est important que nous ayons accès une bonne documentation, d'une part pour bien prendre en main le logiciel, et d'autre part pour résoudre au plus vite les problèmes que nous serons amené à rencontrer.
* **La communauté** : Afin de pouvoir trouver des solutions à nos problèmes, il est important qu'une large et active communauté gravite autour du logiciel.
* **L'intégration des données** : Il s'agit ici d'évaluer les formats de données acceptés par l'outil, que ce soit pour importer des données brutes ou pour exporter des données annotées.
* **Les opérations supportées** : Tous les logiciels ne supporte pas tous les types d'annotation. Dans notre cas nous cherchons entre autre à savoir si le logiciel est capable de faire de l'extraction de relation entre les entités nommées.
* **Le pricing** : Nous cherchons, dans la mesure du possible, à utiliser des outils opensource.
* **Les algorithmes intégrés** : Si possible, il est intéressant de savoir quels sont les algorithmes qui peuvent être utilisé pour les différentes tâches.
* **La flexibilité des algorithmes** : La question est de savoir dans quelles mesures il est possible d'agir sur les différents paramètres des algorithmes, voire de les modifier ou d'intégrer les notres.
* **Proof Of Concept** : Il est intéressant de voir si le logiciel a déjà été utilisé pour des projets, et si oui lesquels et quels sont les résultats.

## Comparaison

### Brat rapide annotation tool

Site officiel : <https://brat.nlplab.org/index.html>

* **Langage** : Nécessite un Server python
* **Documentation** : <https://brat.nlplab.org/manual.html>	
* **Communauté** : /
* **Intégration des données** : <https://brat.nlplab.org/features.html>
* **Opérations supportées** : <https://brat.nlplab.org/features.html>
* **Pricing** : Opensource
* **Algorithmes** : <https://brat.nlplab.org/features.html>
* **Flexibilité** : Aucune
* **POC** : <https://brat.nlplab.org/examples.html>

### NLTK

Site officiel : <https://www.nltk.org/>

* **Langage** : Python
* **Documentation** : https://www.nltk.org/
* **Communauté** : Très grande communauté
* **Intégration des données** : /
* **Opérations supportées** : /
* **Pricing** : OpenSource
* **Algorithmes** : /
* **Flexibilité** : Librairie Python
* **POC** : <https://github.com/search?q=nltk>

### SPACY

Site officiel : <https://spacy.io/>

* **Langage** : Python  
* **Documentation** : <https://spacy.io/usage>
* **Communauté** : Grande communauté
* **Intégration des données** : / 
* **Opérations supportées** : / 
* **Pricing** : OpenSource  
* **Algorithmes** : / 
* **Flexibilité** : Librairie Python
* **POC** : <https://github.com/search?utf8=✓&q=spacy&type=>

### Doccano

GitHub : <https://github.com/chakki-works/doccano>

* **Langage** : Django (python) + NodeJS (JavaScript)
* **Documentation** : 
* **Communauté** :
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** : Opensource
* **Algorithmes** :
* **Flexibilité** :
* **POC** :

### Prodigy

Site officiel : <https://prodi.gy/>

* **Langage** :
* **Documentation** :
* **Communauté** :
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** :
* **Algorithmes** :
* **Flexibilité** :
* **POC** :

### Folia

Site officiel : <https://pypi.org/project/FoLiA-Linguistic-Annotation-Tool/>

* **Langage** :
* **Documentation** :
* **Communauté** :
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** : Opensource
* **Algorithmes** :
* **Flexibilité** :
* **POC** :

### GATE

Site officiel : <https://gate.ac.uk/>

* **Langage** :
* **Documentation** :
* **Communauté** :
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** : Opensource
* **Algorithmes** :
* **Flexibilité** :
* **POC** :

### Apache UIMA

Site officiel : <https://uima.apache.org/>

* **Langage** :
* **Documentation** :
* **Communauté** :
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** : Opensource
* **Algorithmes** :
* **Flexibilité** :
* **POC** :

### Webanno

Site officiel : <https://webanno.github.io/webanno/>

* **Langage** :
* **Documentation** :
* **Communauté** :
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** : Opensource
* **Algorithmes** :
* **Flexibilité** :
* **POC** :

### Callisto

Site officiel : <https://mitre.github.io/callisto/index.html>

* **Langage** : Java
* **Documentation** : <https://mitre.github.io/callisto/manual/index.html>
* **Communauté** : Callisto users mailing list is not very active, but you may be able to get some help there
* **Intégration des données** : /
* **Opérations supportées** : /
* **Pricing** : OpenSource
* **Algorithmes** :/
* **Flexibilité** : /
* **POC** : <https://webanno.github.io/webanno/use-case-gallery/>
No longer being actively supported

### LightTag

Site officiel : <https://www.lighttag.io/>

* **Langage** :
* **Documentation** :
* **Communauté** :
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** :
* **Algorithmes** :
* **Flexibilité** :
* **POC** :

### TagTog

Site officiel : <https://www.tagtog.net>

* **Langage** :/
* **Documentation** :/
* **Communauté** :/
* **Intégration des données** :/
* **Opérations supportées** :/
* **Pricing** : <https://www.tagtog.net/-pricing>
* **Algorithmes** :/
* **Flexibilité** :/
* **POC** :/

### Marky

Site officiel : <http://www.sing-group.org/marky/>

* **Langage** : Nécessite un serveur web
* **Documentation** : <http://www.sing-group.org/marky/tutorial.html#Toc358625730>
* **Communauté** : /
* **Intégration des données** : <http://www.sing-group.org/marky/tutorial.html#outputs> 
* **Opérations supportées** : /
* **Pricing** : OpenSource
* **Algorithmes** : /
* **Flexibilité** : /
* **POC** : <http://www.sing-group.org/marky/tutorial.html>

## Choix final
