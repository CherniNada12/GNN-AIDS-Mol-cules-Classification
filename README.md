# **GNN-AIDS-Molécules-Classification 📘**

## **Description du projet**

Ce projet utilise des **graphes moléculaires** pour représenter différentes molécules testées contre le virus du SIDA (HIV).  
Chaque graphe correspond à une molécule :  

- Les **nœuds (nodes)** représentent des atomes  
- Les **arêtes (edges)** représentent des liaisons chimiques  

**Objectif :** classifier les molécules selon leur activité biologique :  

- `0` → **molécule active** (agit contre le VIH)  
- `1` → **molécule inactive**  

Ce projet explore différentes approches :  

- **Méthodes classiques de Machine Learning (ML)**  
- **Embeddings de graphes** (Shallow Embedding : Graph2Vec, Node2Vec)  
- **Graph Neural Networks (GNN)**

---

## **Dataset**

Le dataset **AIDS** contient plusieurs fichiers :  

| Fichier | Description |
|---------|-------------|
| `AIDS_graph_indicator.txt` | Indique à quel graphe appartient chaque nœud |
| `AIDS_graph_labels.txt` | Label global du graphe (0=active, 1=inactive) |
| `AIDS_node_labels.txt` | Type d’atome encodé en entier (C=0, O=1, N=2 …) |
| `AIDS_node_attributes.txt` | Attributs des nœuds : chem, charge, x, y |
| `AIDS_A.txt` | Liste des arêtes (from_node, to_node) |
| `AIDS_edge_labels.txt` | Type de liaison chimique (simple=0, double=1, triple=2) |

---

## **Installation**

1. Cloner le dépôt :  
```bash
git clone https://github.com/votre-utilisateur/GNN-AIDS-Molécules-Classification.git
cd GNN-AIDS-Molécules-Classification


numpy
pandas
networkx
matplotlib
scikit-learn
xgboost
torch
torch-geometric
karateclub

## **Étapes du projet**

### **1️⃣ Construction des graphes avec NetworkX**
- Lire les fichiers du dataset  
- Créer les graphes avec **nœuds, arêtes, labels et attributs**  

### **2️⃣ Analyse Exploratoire (EDA)**
- Analyser la **distribution du nombre de nœuds et d’arêtes**  
- **Visualiser les graphes**  

### **3️⃣ Préprocessing**
- **Normalisation** des attributs : `chem`, `charge`, `x`, `y`  
- **Encodage des labels**  

### **4️⃣ Méthodes ML classiques**
- Extraire des **features globales** : nombre de nœuds, degré moyen, densité  
- Utiliser des **classificateurs** : RandomForest, XGBoost  

### **5️⃣ Shallow Embedding (Graph2Vec, Node2Vec)**
- Transformer les graphes en **vecteurs fixes**  
- Utiliser des modèles ML classiques sur ces embeddings  

### **6️⃣ Graph Neural Networks (GNN)**
- Modèles : **GCN, GAT, GraphSAGE**  
- Entrée : graphes moléculaires avec **features**  
- Sortie : **classification binaire** (active/inactive)  



## **Références**

- [PyTorch Geometric](https://pytorch-geometric.readthedocs.io/)  
- [Karate Club – graph embedding](https://karateclub.readthedocs.io/)  





---

Si tu veux, je peux te créer **la version finale avec le code Python pour chaque étape** intégré dans le README, ce qui le rend **complètement prêt à GitHub**, avec EDA, construction des graphes, ML classique, embeddings et GNN.  

Veux‑tu que je fasse ça ?
