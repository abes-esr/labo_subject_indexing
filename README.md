# Subject indexing as semantic search. A demo.


**Goal**. The main goal of this notebook is to build a system for subject indexing. It aims to predict RAMEAU subject headings (a francophone controlled vocabulary used for indexing library resources) for documents, using the documents's descriptions (bibliographic records).

**Approach**. The subject indexing problem is reframed as a semantic search problem. The vector for each subject heading is calculated as the average of the embeddings of documents associated with that subject heading. Documents are indexed by finding the closest subject headings in a semantic (embedding) space

**Nota Bene** :
- In this notebook, the method is applied to RAMEAU, a large francophone subject headings vocabulary. It could be applied to other indexing vocabularies.
- The dataset is a demo one. In real life, our training dataset includes 400,000 bibliographic records of books. This number increases significantly when the French dissertations dataset is included (over 400,000 records).
- This method focuses on concept indexing, where all subjects are represented as nouns ("Butter", "Atheism", etc.). Geographical or chronological indexing would be better served by other approaches, such as Named Entity Recognition (NER).
- It is recommended to run this document in a GPU environment (ex : Google Colab). The embedding of 10, 000 documents will take 10 minutes (vs. 2 hours on CPU).


More information (FR) : 
- [Final report on a hands-on experiment conducted with twelve French academic libraries in 2024](https://fil.abes.fr/2025/04/10/lindexation-rameau-assistee-par-ia-retour-sur-une-experimentation-prometteuse/)
- General overview of the approach (soon)


This demo notebook was developed by the 'labo', a unit of Abes (Agence bibliographique de l'enseignement supérieur (France)).
