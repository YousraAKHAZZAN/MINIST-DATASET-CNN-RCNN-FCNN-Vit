#LAB2 : DEEP LEARNING 


# MINIST-DATASET-CNN-RCNN-FCNN-Vit
## Introduction  
Ce laboratoire vise à approfondir la compréhension des architectures de réseaux neuronaux en vision par ordinateur, en mettant l'accent sur les Convolutional Neural Networks (CNN) et les Region-based Convolutional Neural Networks (RCNN). Ces modèles sont largement utilisés pour la classification et la détection d'objets dans les images.  

---

## Concepts clés  

### 1. Convolutional Neural Networks (CNN)  
Les CNN sont des réseaux de neurones conçus spécifiquement pour traiter des données sous forme d'images. Ils sont constitués de plusieurs couches principales :  
- **Couches de convolution** : Extraction des caractéristiques locales grâce à l'application de filtres.  
- **Couches de pooling** : Réduction de la dimensionnalité tout en préservant les informations essentielles.  
- **Couches fully connected** : Interprétation des caractéristiques extraites pour réaliser la classification.  

Les CNN sont efficaces pour la classification d'images, notamment avec des datasets comme MNIST, CIFAR-10 et ImageNet.  

### 2. Region-based Convolutional Neural Networks (RCNN)  
Les RCNN sont une extension des CNN conçue pour la détection d'objets. Ils identifient d'abord des régions d'intérêt (RoI) dans une image avant de classer les objets à l'intérieur de ces régions. Il existe plusieurs variantes :  
- **RCNN** : Détecte des régions candidates et applique un CNN à chacune d'elles (très lent).  
- **Fast R-CNN** : Amélioration qui réduit la redondance en extrayant d'abord des caractéristiques globales.  
- **Faster R-CNN** : Introduit un réseau de propositions de région (RPN) pour accélérer l'identification des RoI.  

---

## Comparaison CNN vs RCNN  

| Critère          | CNN | Faster R-CNN |
|-----------------|-----|-------------|
| **Objectif** | Classification | Détection d'objets |
| **Précision** | Bonne sur des tâches simples | Meilleure pour des images complexes avec plusieurs objets |
| **Vitesse** | Rapide pour la classification | Plus lent en raison de l'analyse des régions |
| **Complexité** | Plus simple | Plus complexe en raison du RPN |
| **Application** | Catégorisation d'images | Détection d'objets et reconnaissance de scène |

---

## Expérimentation et Résultats  
Nous allons implémenter ces architectures en utilisant le dataset MNIST pour observer leurs performances.  

### 1. Classification avec CNN  
- Construction d'un CNN sur MNIST  
- Entraînement du modèle et évaluation des performances (Accuracy, F1-score)  

### 2. Détection avec Faster R-CNN  
- Adaptation d'un Faster R-CNN pour détecter les chiffres  
- Comparaison des performances avec le CNN  

**Analyse des résultats** :  
- Le CNN est efficace pour classer des images simples mais limité pour la détection d’objets.  
- Le Faster R-CNN offre de meilleures performances sur des images plus complexes, bien que plus coûteux en calcul.  

---

## Conclusion  
Ce laboratoire met en évidence les différences entre les CNN et les RCNN. Alors que les CNN sont idéaux pour la classification, les RCNN et leurs variantes sont plus adaptés aux tâches de détection. L'évolution vers des modèles plus avancés, comme les Vision Transformers (ViT), ouvre de nouvelles perspectives en vision par ordinateur.  
