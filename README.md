# Analyse de Textes avec NLP et Clustering sur les articles de CleRMa
Ce projet vise à analyser une collection d'articles du laboratoire en sciences de gestion CleRMa, extraire des insights pertinents grâce à des techniques de traitement du langage naturel (NLP) et de clustering, et identifier des thèmes récurrents au fil du temps.

## Comment ça marche ?

Le code principal pour l'analyse et le clustering se trouve dans le notebook `Topic modeling.ipynb`. Le notebook contient toutes les étapes nécessaires, y compris l'extraction des lettres, le nettoyage et la préparation des données, l'analyse NLP, le clustering et le topic modeling à l'aide de BERTopic.

Les graphiques et visualisations résultants sont générés dans le dossier output. Deux fichiers HTML sont créés :

- `visualize_documents_all.html` : Visualisation de tous les documents et clusters

https://html-preview.github.io/?url=https://github.com/moblangeois/Topic-modeling-articles-CleRMa/blob/main/output/visualize_documents_all.html

- `visualize_topics_over_time.html` : Visualisation des topics et clusters au fil du temps

https://html-preview.github.io/?url=https://github.com/moblangeois/Topic-modeling-articles-CleRMa/blob/main/output/visualize_topics_over_time.html


## Dépendances
Le projet utilise plusieurs bibliothèques Python importantes pour le traitement des données, le NLP, le clustering, et la visualisation, dont :

- Pandas pour la manipulation des données
- re (RegEx) pour les expressions régulières
- Collections pour les structures de données avancées
- dotenv pour la gestion des variables d'environnement
- BERTopic pour le topic modeling avancé
- spaCy et nltk pour le NLP
- HDBSCAN et UMAP pour le clustering et la réduction de dimension
- Matplotlib et Seaborn pour la visualisation
- OpenAI pour l'intégration de modèles de langage avancés

## Configuration Initiale
Variables d'environnement : Le code utilise une clé API OpenAI, qui doit être configurée comme une variable d'environnement (OPENAI_API_KEY).
Modèles spaCy : Un modèle spaCy en français (fr_core_news_md) est chargé pour le traitement du langage naturel.
Détection de la langue : Un détecteur de langue est ajouté au pipeline spaCy pour filtrer les phrases non françaises.

## Clustering et Topic Modeling
Le projet utilise BERTopic pour le topic modeling, en appliquant différentes techniques pour la représentation des topics, y compris :

- KeyBERT pour l'extraction de mots-clés
- Maximal Marginal Relevance (MMR) pour la diversité des mots-clés
- PartOfSpeech et OpenAI GPT-3.5 Turbo pour des représentations améliorées

Les topics identifiés sont ensuite visualisés et analysés pour comprendre les thèmes principaux et leur évolution dans le temps.