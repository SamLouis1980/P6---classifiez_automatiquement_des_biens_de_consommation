#  Classification automatique de biens de consommation – Place de Marché

## Contexte

L’entreprise **Place de Marché** développe une plateforme e-commerce où les vendeurs postent une **photo** et une **description textuelle** de leurs produits.  
Actuellement, la **catégorie d’un article** est renseignée manuellement, ce qui engendre des erreurs et nuit à l’expérience utilisateur.  

Dans une optique de **scalabilité**, l’entreprise souhaite étudier la **faisabilité d’un moteur de classification automatique** basé sur les images et descriptions des articles.  
Une deuxième phase du projet implique une **classification supervisée** à partir des images, avec **data augmentation**, ainsi qu’un **script de collecte via API** pour enrichir la base de données avec de nouveaux produits (ex. : produits à base de champagne).

## Objectif

- Étudier la **faisabilité** du regroupement automatique des produits de même catégorie via **clustering** sur features texte et image
- Réaliser des **prétraitements** et des **extractions de caractéristiques** multi-modales :
  - Texte : Bag of Words, TF-IDF, Word2Vec, BERT, USE
  - Image : SIFT, CNN avec Transfer Learning (VGG16, ResNet, EfficientNet, NASNet)
- Réduire la dimension des features (PCA, t-SNE) et visualiser les regroupements
- Comparer les regroupements avec les vraies catégories (métriques de clustering)
- Implémenter une **classification supervisée** des images avec évaluation de la performance
- Collecter et sauvegarder via un **script API** les produits liés à un mot-clé (ex: “champagne”)

## Technologies utilisées

- **Texte** : `nltk`, `Word2Vec`, `TF-IDF`, `BERT`, `USE`, `sklearn.feature_extraction`
- **Images** : `cv2`, `VGG16`, `ResNet50`, `EfficientNet`, `MobileNetV2`, `NASNetMobile`
- **Modélisation** : `KMeans`, `MiniBatchKMeans`, `PCA`, `t-SNE`, `StratifiedKFold`
- **Clustering metrics** : `adjusted_rand_score`, `silhouette_score`
- **Évaluation** : `classification_report`, `confusion_matrix`, `accuracy_score`
- **Prétraitement & pipelines** : `ImageDataGenerator`, `StandardScaler`, `LabelEncoder`
- **API & scripts** : `requests`, `json`, `pandas`, `csv`
- **Deep Learning** : `TensorFlow`, `Keras`, `SentenceTransformers`, `Transformers`

## Structure du projet

- notebook_pretraitement_feature_extraction_faisabilite.ipynb
- notebook_pretraitement_feature_extraction_faisabilite_techniques_avancees.ipynb
- notebook_faisabilité_classification_des_images_SIFT.ipynb
- notebook_faisabilité_classification_des_images_CNN.ipynb
- notebook_classification_supervisee_des_images_VGG16.ipynb
- notebook_traitement_avec_techniques_recentes_EfficientNet.ipynb
- Script_Python.ipynb - Script d'extraction via API
- Resultat_script_python.csv
- presentation.pptx - Présentation complète du projet
