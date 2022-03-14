# Classification d'image de pneumonie XRay

L'objectif de ce projet est le développement d'un outils de classification d'images RayX de patients ayant une pneumonie. Ce projet s'inscrit dans une démarche d'aide médicale au diagnostique mais n'ayant pas été validé, il ne doit pas être utilisé à des fins médicales. 

Vous pouvez trouver ci-dessus différents fichiers. 

Le fichier "pneumonia_classification_Xception_TL.ipynb" met en place un modèle de réseau neuronal convolutif.
Les fichiers "app.py", "base.html", "index.html", "main.css", "main.js" permettent le déployement fe notre modèle de réseau neuronal convolutif.

### Contexte

La pneumonie est une forme d'infection respiratoire aiguë qui affecte les poumons. Les poumons sont constitués de petits sacs appelés alvéoles, qui se remplissent d'air lorsqu'une personne en bonne santé respire. Lorsqu'un individu souffre de pneumonie, les alvéoles sont remplies de pus et de liquide, ce qui rend la respiration douloureuse et limite l'apport d'oxygène.

La pneumonie est selon l'OMS, la principale cause infectieuse de décès chez les enfants dans le monde. La pneumonie a tué 740 180 enfants de moins de 5 ans en 2019, ce qui représente 14 % de tous les décès d'enfants de moins de cinq ans mais 22 % de tous les décès d'enfants âgés de 1 à 5 ans. La pneumonie affecte les enfants et les familles partout, mais les décès sont les plus élevés en Asie du Sud et en Afrique subsaharienne. Les enfants peuvent être protégés contre la pneumonie, elle peut être prévenue par des interventions simples et traitée avec des médicaments et des soins peu coûteux et de faible technologie.

La pneumonie est causée par un certain nombre d'agents infectieux, notamment des virus, des bactéries et des champignons. 

Les plus courants sont : 
Streptococcus pneumoniae – la cause la plus fréquente de pneumonie bactérienne chez les enfants ; 
Haemophilus influenzae de type b (Hib) – la deuxième cause la plus fréquente de pneumonie bactérienne ;
le virus respiratoire syncytial est la cause virale la plus fréquente de pneumonie ;

chez les nourrissons infectés par le VIH, Pneumocystis jiroveci est l'une des causes les plus courantes de pneumonie, responsable d'au moins un quart de tous les décès par pneumonie chez les nourrissons infectés par le VIH.

L'objectif principal de cette étude est de développer un algorithme permettant de différencier les individus ne présentant pas de pneumonie de ceux en présentant. Cette analyse se fera à partir de données radiographiques (Rayons X).

### Base de données (License : CC BY-NC-SA 4.0)

Le jeu de données utilisée, contient des images de tomographie par cohérence optique et de radiographie thoracique validées décrites et analysées dans "CDeep learning-based classification and referral of treatable human diseases" de l'université de Californi - San Diego. Les images OCT sont divisées en un ensemble de formation et un ensemble de test de patients indépendants.

Des images radiographiques thoraciques (antéro-postérieures) ont été sélectionnées à partir de cohortes rétrospectives de patients pédiatriques âgés de un à cinq ans du Guangzhou Women and Children's Medical Center, Guangzhou. Toutes les radiographies pulmonaires ont été réalisées dans le cadre des soins cliniques de routine des patients. Les approbations de l'Institutional Review Board (IRB)/Comité d'éthique ont été obtenues. Les travaux ont été menés conformément à la loi américaine HIPAA (Health Insurance Portability and Accountability Act) et aux principes de la Déclaration d'Helsinki.

Kermany, Daniel; Zhang, Kang; Goldbaum, Michael (2018), “Labeled Optical Coherence Tomography (OCT) and Chest X-Ray Images for Classification”, Mendeley Data, V2, doi: 10.17632/rscbjbr9sj.2 https://data.mendeley.com/datasets/rscbjbr9sj/2

### Métrique

Ici, je choisi l'exactitude comme métrique d'évaluation. Cette dernière permet indique le pourcentage de bonnes prédictions. C’est un très bon indicateur global parce très simple à comprendre. 

### Modèle

Les réseaux de neurones convolutifs (en anglais Convolutional neural networks), aussi connus sous le nom de CNNs, sont un type spécifique de réseaux de neurones qui sont généralement composés des couches suivantes : convolutifs, pooling et pleinement connectée. Ils sont trés utilisés dans le domaine du traitement de l'images.
