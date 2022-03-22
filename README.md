# Classification d'image de pneumonie XRay

Veuillez trouver ci-dessus :

- Le fichier "pneumonia_classification_Xception_TL.ipynb" qui met en place un modèle de réseau neuronal convolutif.

- Les fichiers "app.py", "base.html", "index.html", "main.css", "main.js" permettant le déployement de notre modèle.


### Contexte

La pneumonie est infection respiratoire aiguë qui affecte les poumons. Les poumons sont constitués de petits sacs appelés alvéoles, qui se remplissent d'air lorsqu'une personne en bonne santé respire. Lorsqu'un individu souffre de pneumonie, les alvéoles sont remplies de pus et de liquide, ce qui rend la respiration douloureuse et limite l'apport d'oxygène.

La pneumonie est selon l'Organisation Mondiale de la Santé, la principale cause infectieuse de décès chez les enfants dans le monde. Cependant elle peut être prévenue par un diagnostique précoce et traitée avec des médicaments peu coûteux.

L'objectif de ce projet est mettre en place un classificateur d'images (Rayons X) permettant de différencier un patient atteint d'une pneumonie, d'un patient non atteint. Il s'inscrit dans une démarche d'aide médicale au diagnostique mais n'ayant pas été validé par des experts, il ne doit pas être utilisé à des fins médicales.


### Base de données

Le jeu de données utilisé, contient des images de tomographie par cohérence optique et de radiographie thoracique validées décrites et analysées dans "CDeep learning-based classification and referral of treatable human diseases" de l'université de Californi - San Diego. Les images OCT sont divisées en un ensemble de formation et un ensemble de test de patients indépendants.

Ici j'utilise seulement, les images radiographiques thoraciques (antéro-postérieures) sélectionnées à partir de cohortes rétrospectives de patients pédiatriques âgés de un à cinq ans du Guangzhou Women and Children's Medical Center, Guangzhou. Toutes les radiographies pulmonaires ont été réalisées dans le cadre des soins cliniques de routine des patients. Les approbations de l'Institutional Review Board (IRB)/Comité d'éthique ont été obtenues. Les travaux ont été menés conformément à la loi américaine HIPAA (Health Insurance Portability and Accountability Act) et aux principes de la Déclaration d'Helsinki.

Kermany, Daniel; Zhang, Kang; Goldbaum, Michael (2018), “Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images for Classification”, Mendeley Data, V2, doi: 10.17632/rscbjbr9sj.2 https://data.mendeley.com/datasets/rscbjbr9sj/2

### Choix de la métrique

Je choisi l'exactitude comme métrique d'évaluation. Cette dernière indique le pourcentage de prédictions correctement réalisées. C’est un très bon indicateur global parce très simple à comprendre. 

### Choix du modèle

Les réseaux de neurones convolutifs (en anglais Convolutional neural networks), aussi connus sous le nom de CNNs, sont un type spécifique de réseaux de neurones qui sont généralement composés des couches suivantes : convolutifs, pooling et pleinement connectée. Ils sont trés utilisés dans le domaine du traitement de l'images.

Cependant la faible quantité de données ne permet pas l'entraînement du modèle à partir de zéro. C'est pourquoi j'utilise le transfer learning. Cette méthode vise à transférer les connaissances apprisent par un modèle pré-entraînésur un grand jeu de données, à une tache similaire. Il peut être vu comme la capacité d’un système à reconnaître et appliquer des connaissances et des compétences, apprises à partir de tâches antérieures, sur de nouvelles tâches ou domaines partageant des similitudes.
