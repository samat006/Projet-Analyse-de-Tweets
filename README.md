
# Analyse de Tweets avec PySpark

![Python](https://img.shields.io/badge/Python-3.10-blue)
![Spark](https://img.shields.io/badge/Spark-PySpark-orange)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-13-blueviolet)

Projet d'analyse de tweets utilisant **PySpark** pour le traitement de texte et PostgreSQL pour le stockage des données nettoyées.

---

## 📦 Fonctionnalités

* Lecture de tweets depuis un fichier CSV
* Nettoyage des textes (`text_clean`) : suppression des caractères spéciaux, mise en minuscules
* Tokenization en mots (`words`)
* Vectorisation avec `CountVectorizer` (`features`)
* Encodage des labels (`label`)
* Écriture des données nettoyées dans PostgreSQL (`tweets_clean`)

---

## 🛠️ Technologies utilisées

* Python 3.10
* Apache Spark / PySpark
* Spark ML (`Tokenizer`, `CountVectorizer`, `StringIndexer`)
* PostgreSQL
* Nettoyage et prétraitement de texte

---

## ⚙️ Installation et exécution

1. Cloner le dépôt :

```bash
git clone https://github.com/<ton-utilisateur>/<nom-du-repo>.git
cd <nom-du-repo>
```

2. Installer les dépendances :

```bash
pip install -r requirements.txt
```

3. Lancer le script principal :

```bash
python main.py
```

Les données seront nettoyées et insérées dans PostgreSQL.

---

## 📁 Structure du projet

```
/projet-tweets
│
├─ data/             # fichiers CSV
├─ scripts/          # scripts PySpark
├─ notebooks/        # notebooks Jupyter
├─ README.md
└─ requirements.txt  # dépendances Python
```

---

## 💡 Remarques

* Les colonnes `Vector` (features) ne peuvent pas être directement stockées dans PostgreSQL.
* Pour conserver les vecteurs, utilisez des formats comme **Parquet** ou **Pickle**.

