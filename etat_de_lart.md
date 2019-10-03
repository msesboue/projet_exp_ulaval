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
* **Description** :
  * Une interface graphique agréable et facile à manipuler
  * Permet de faire de l'annotation à plusieurs niveaux : entités nommées, relations
  * Utilise des svg pour la visualisation
  * Permet de passer facilement d'une document à l'autre
  * Permet de passer facilement du texte annoté, au texte brut
  * possibilité de faire l'annotation collaborative
  * Possibilité de définir nos propres labels
  * **Problème** : Le format du texte annoté n'est pas facile à manipuler. format .txt avec structure particulière (standoff format).

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
* **Documentation** : peu de documentation mais code opensource. <https://github.com/chakki-works/doccano/wiki>
* **Communauté** : Communauté GitHub seulement
* **Intégration des données** :
* **Opérations supportées** : provides annotation features for text classification, sequence labeling and sequence to sequence.
* **Pricing** : Opensource
* **Algorithmes** : /
* **Flexibilité** : /
* **POC** : Demos
  * Named entity recognition
  * Sentiment Analysis
  * Machine translation
* **Description** :
  * Une interface graphique agréable et facile à manipuler
  * Possibilité de définir nos propres labels
  * Supporte le format JSON à l'importation des données comme à l'exportation
  * possibilité de faire l'annotation collaborative
  * **Problème** : Ne semble pas proposer l'annotation de relation

### Prodigy

Site officiel : <https://prodi.gy/>

* **Langage** : Python
* **Documentation** : Très bonne <https://prodi.gy/docs/>
* **Communauté** : large et active <https://support.prodi.gy/>
* **Intégration des données** : Supporte la plupart de formats pour l'importation, CSV, JSON, TXT, HTML ... <https://prodi.gy/features/>
* **Opérations supportées** : Named entity recognition, Text Classification, computer vision.
* **Pricing** : 400 $ - 10 000 $ (US dollars)
* **Algorithmes** : Possibilité d'intégrer ses porpres modèles développés en python. Le modèle est mis à jour en live en fonction des annotations faites manuellement.
* **Flexibilité** : voir ci-dessus
* **POC** : Live Demo <https://prodi.gy/demo?view_id=ner>

### FoLia Annotation Tool (FLAT)

Site officiel : <https://pypi.org/project/FoLiA-Linguistic-Annotation-Tool/>

* **Langage** : Django (Python)
* **Documentation** : complète <https://flat.readthedocs.io/en/latest/user_guide.html>
* **Communauté** :
* **Intégration des données** : Basé seulement sur le format de données Folia <https://proycon.github.io/folia/>. Possibilité de transformer certains formats en format FoLia : <https://www.ubiquitypress.com/site/chapters/10.5334/bbi.6/download/1022/>
* **Opérations supportées** : annotations manuelles seulement
* **Pricing** : Opensource -- GNU Public License v3
* **Algorithmes** : /
* **Flexibilité** : /
* **POC** : Demo <https://www.youtube.com/watch?v=tYF6grtldVQ>
* **Description** :
  * Une interface graphique agréable et facile à manipuler
  * Possibilité de définir nos propres labels
  * possibilité de faire l'annotation collaborative
  * Versionning
  * Possibilité d'ajouter un niveau de confidence aux annotations
  * Basé sur le format Folia, un format basé sur le XML
  * Sytème de gestion de fichiers/documents intégré
  * plusieurs types de visualisation possibles
  * Possibilité de filtrer le type d'annotation que l'on veut visualiser
  * Conserve la structure des documents (titres, paragraphes, images ...)
  * Bibliothèques python associées au format Folia : <https://pypi.org/project/FoLiA/>
  * Supporte l'annotation de relation de dépendance

### GATE

Site officiel : <https://gate.ac.uk/>

* **Langage** : Java
* **Documentation** : Très bonne, documentation, wiki, demo
* **Communauté** : Mailing list
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** : Opensource
* **Algorithmes** :
* **Flexibilité** :
* **POC** :
* **Description** :
  * Une interface graphique plus complexe et moins agréable à utiliser. Mais cela va avec la quantité de fonctionnalités offertes.
  * Possibilité de définir des pipelines pour les différentes étapes d'annotation
  * beaucoup de plugins disponibles pour différentes applications
  * un plugin existe pour la langue française <https://gate.ac.uk/sale/tao/splitch15.html#x20-38700015.2>
  * Supporte une grande variété de format pour l'importation, entre autre le texte brut et le format XML. Certains formats JSON sont supportés via des plugins. L'exportation se fait principalement dans un format XML.
  * supporte l'extraction de relation <https://gate.ac.uk/sale/talks/gate-course-may10/track-3/module-11-ml-adv/module-11-relations.pdf>
  * intègre par défaut certains algorithmes de machine learning

### Apache UIMA

Site officiel : <https://uima.apache.org/>

* **Langage** : Java / C++
* **Documentation** :
* **Communauté** :
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** : Opensource
* **Algorithmes** :
* **Flexibilité** :
* **POC** :
* **Description** :
  * Framework pour intégrer un ensemble d'apllication de traitement de données non structurées
  * Apache UIMA est un framework vide de base. Sa force vient de sa communuauté et des nombreux plugins qui y sont liés.
  * Prévu pour gérer de grosses quantités de données
  * <https://uima.apache.org/doc-uima-why.html>

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
* **Description** :
  * Définition des labels par couche et manuellement
  * De même pour la définition de relations
  * Interface graphique agréable et facile à utiliser
  * Gestion de plusieurs documents facilité
  * Possibilité d'intégrer des outils extèrieure pour certaines tâches
  * Automation feature : permet d'utiliser un outil externe pour faire des propositions d'annotation
  * Quelques tutorials : <https://www.youtube.com/channel/UCew3TzVAw4MHIt0zAHFIcxQ>

### Callisto

Site officiel : <https://mitre.github.io/callisto/index.html>

* **Langage** : Java
* **Documentation** : <https://mitre.github.io/callisto/manual/index.html>
* **Communauté** : Callisto users mailing list is not very active, but you may be able to get some help there
* **Intégration des données** : /
* **Opérations supportées** : /
* **Pricing** : OpenSource
* **Algorithmes** : /
* **Flexibilité** : /
* **POC** : <https://webanno.github.io/webanno/use-case-gallery/>
* **Description** :
  * **Problème** : No longer being actively supported

### LightTag

Site officiel : <https://www.lighttag.io/>

* **Langage** :
* **Documentation** : correcte <https://guide.lighttag.io>
* **Communauté** :
* **Intégration des données** :
* **Opérations supportées** :
* **Pricing** : <https://www.lighttag.io/pricing>
* **Algorithmes** :
* **Flexibilité** :
* **POC** :

### TagTog

Site officiel : <https://www.tagtog.net>

* **Langage** : /
* **Documentation** : complète <https://docs.tagtog.net/>
* **Communauté** : /
* **Intégration des données** : /
* **Opérations supportées** : /
* **Pricing** : <https://www.tagtog.net/-pricing>
* **Algorithmes** : /
* **Flexibilité** : /
* **POC** : /

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
* **Description** :
  * Interface graphique correcte
  * Permet l'annotation collaborative
  * Possibilité d'éditer les documents tant que l'annotation n'est pas commencée
  * Format d'importation : .html .htm .txt. Possibilité de passer un URL
  * Possibilité de définir nos propres labels
  * **Problème** : 
    * pas de'information sur les possibilités d'intégrer des outils
    * Pas d'information sur le format des fichiers annotés

## Choix finaux

Parmis les outils brièvement présentés ci-dessus, nous avons d'office exclus ceux qui n'étaient pas opensource. Parmis ceux restant, trois ont retenu notre attention :

* Gate :
  * Notre choix principal se porte sur le logiciel GATE pour la richesse des outils qu'il intègre. De plus de nombreux projets on été réalisés avec lui, produisant ainsi plusieurs articles de recherche et une solide communauté.
  * Le fait que certains algorithmes de NLP soient déjà intégrés est aussi intéressant.
  * Étant donné l'étendue des possibilités offertes par ce logiciel, il faut prendre en compte que le temps de prise en main peut être plus long que pour d'autres outils.
* Webanno :
  * Cet outil est aussi un potentiel choix étant donné son interface graphique plus simple tout en offrant les fonctionnalités que nous recherchons.
  * De plus il permet d'intégrer des outils externes, ou leurs résultat, ce qui peut être intéressant pour construire une potentielle pipeline
  * Même si la prise en main devrait être plus simple, il propose moins de fonctionnalités que GATE.
* Folia :
  * Cet outil est intéressant non seulement pour son interface graphique agréable et intuitive mais également pour la possibilité d'intégrer des niveaux de confidence sur les annotations. Cette information peut potentiellement être utile par la suite.
  * Le format de données annotées est aussi intéressant car il semble être bien établi et utilise le XML, un langage autour duquel gravite beaucoup d'outils qui permettent de faire énormément de choses. Il existe également des bibliothèques Python pour manipuler ce format.
  * Ce format étant nouveau pour nous, il faut prendre en compte le temps de prise en main.

**Quelque soit le choix final, le premier point à tester et valider est le format de données annotées.**
