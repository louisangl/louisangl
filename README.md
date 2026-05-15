<div align="center">
  <img src="./banner.png" alt="Louis Angleys — Ingénieur IA Générative & Systèmes Agentiques" width="100%"/>
</div>

---

Ingénieur diplômé de l'ENAC (École Nationale de l'Aviation Civile), je me spécialise dans la conception de systèmes IA orientés production : pipelines RAG/GraphRAG, agents autonomes, observabilité. Mon parcours mêle formation d'ingénieur classique — algorithmique, réseaux, mécanique du vol — à une pratique intensive de l'écosystème LLM depuis 2023.

Ce qui me motive vraiment : appliquer ces outils à des problèmes industriels concrets, en particulier dans l'aéronautique où les enjeux de **décarbonation** sont massifs et où la data reste encore largement sous-exploitée. Réduire l'empreinte carbone d'un vol de quelques pourcents à l'échelle d'une flotte, c'est un impact réel — et c'est le genre de problème où physique, données et IA se rejoignent.

Je cherche une première opportunité (CDI, V.I.E, ou expérience à l'international) pour mettre ces compétences au service de projets ambitieux.

---

## Ce sur quoi je travaille

### GraphRAG — Groupe ADP `Stage PFE · 6 mois · Orly`

Durant mon stage de fin d'études au sein de la Direction Innovation du Groupe ADP (Aéroports de Paris), j'ai conçu un système **GraphRAG** de bout en bout pour optimiser des processus métiers complexes.

Le problème de départ : les systèmes RAG vectoriels classiques échouent sur les requêtes "multi-hop" — celles qui nécessitent de traverser plusieurs documents liés pour construire une réponse. Par exemple : *"Quelles procédures de maintenance sont impactées par ce nouveau marché de signalisation ?"* implique de relier un marché à des équipements, puis des équipements à des manuels — une chaîne de causalité qu'un RAG vectoriel ne voit pas.

La solution : remplacer la recherche vectorielle pure par un **graphe de connaissances** (Neo4j, puis Apache AGE en pré-production), et orchestrer la récupération via un pipeline **ReAct** qui raisonne sur la nécessité d'aller chercher des informations complémentaires dans le graphe. Résultat sur notre golden dataset interne : **55% → 80% de correctness** sur les requêtes multi-hop.

→ Architecture, choix techniques et leçons apprises : [`graphrag-pipeline`](https://github.com/louisangl/graphrag-pipeline)

---

### Aircraft Fuel Digital Twin `En cours`

Projet personnel à la croisée de ma formation aéronautique et de mes intérêts pour la décarbonation. L'idée : construire un **jumeau numérique** de consommation carburant d'un aéronef à partir de données de vol réelles.

Ingestion des trajectoires ADS-B via l'API OpenSky Network, puis application d'un modèle physique maison — équations de traînée, poussée et variation de masse — pour reconstituer la consommation litre par litre et estimer l'empreinte CO₂ par vol. À terme : comparer des scénarios de trajectoire alternatifs sur leur impact environnemental, et explorer un couplage avec un modèle ML pour la prédiction.

---

### Chatbot LLM orienté production `En cours`

Stack MLOps légère autour d'un chatbot LLM : inférence **Groq**, observabilité complète via **Langfuse** (traces, évaluations, coûts), architecture modulaire pensée pour l'itération rapide. L'objectif est moins le chatbot lui-même que la stack de monitoring et d'évaluation autour — ce qui manque dans la plupart des projets LLM publics.

---

### PINNs — Physics-Informed Neural Networks `Exploration`

Réseaux de neurones contraints par des équations différentielles, appliqués à des problèmes de dynamique de vol. L'idée : ne pas traiter la physique comme une boîte noire mais en faire une contrainte explicite dans la loss. PyTorch.

---
 
## Stack
 
**Langages & backend**  
![Python](https://img.shields.io/badge/Python-0f1923?style=flat-square&logo=python&logoColor=7ab8e0)
![FastAPI](https://img.shields.io/badge/FastAPI-0f1923?style=flat-square&logo=fastapi&logoColor=5dcaa5)
![Docker](https://img.shields.io/badge/Docker-0f1923?style=flat-square&logo=docker&logoColor=7ab8e0)
![Git](https://img.shields.io/badge/Git-0f1923?style=flat-square&logo=git&logoColor=f0997b)
![CI/CD](https://img.shields.io/badge/CI%2FCD-0f1923?style=flat-square&logo=githubactions&logoColor=7ab8e0)
 
**Data & bases**  
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-0f1923?style=flat-square&logo=postgresql&logoColor=7ab8e0)
![pgvector](https://img.shields.io/badge/pgvector-0f1923?style=flat-square&logo=postgresql&logoColor=5dcaa5)
![Neo4j](https://img.shields.io/badge/Neo4j-0f1923?style=flat-square&logo=neo4j&logoColor=5dcaa5)
![Apache AGE](https://img.shields.io/badge/Apache%20AGE-0f1923?style=flat-square&logo=apache&logoColor=f0997b)
![Spark](https://img.shields.io/badge/Spark-0f1923?style=flat-square&logo=apachespark&logoColor=ef9f27)
 
**ML & IA**  
![PyTorch](https://img.shields.io/badge/PyTorch-0f1923?style=flat-square&logo=pytorch&logoColor=ef9f27)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-0f1923?style=flat-square&logo=scikitlearn&logoColor=ef9f27)
![Hugging Face](https://img.shields.io/badge/Hugging%20Face-0f1923?style=flat-square&logo=huggingface&logoColor=ef9f27)
![LangGraph](https://img.shields.io/badge/LangGraph-0f1923?style=flat-square&logo=langchain&logoColor=a99de8)
 
**Observabilité & infra**  
![Langfuse](https://img.shields.io/badge/Langfuse-0f1923?style=flat-square&logoColor=a99de8)
![Groq](https://img.shields.io/badge/Groq-0f1923?style=flat-square&logoColor=5dcaa5)
![Azure](https://img.shields.io/badge/Azure-0f1923?style=flat-square&logo=microsoftazure&logoColor=7ab8e0)
 

## Projets académiques

Projets réalisés à l'ENAC (Toulouse) et à la Sapienza Università di Roma (Erasmus 2024). Détails et code dans [`academic-projects`](https://github.com/louisangl/academic-projects).

- **Optimisation de trajectoires par algorithme génétique** — optimisation 2D en espace contraint, programmation fonctionnelle, ENAC
- **Simulation de trafic aérien Java / MCTS** — moteur de simulation avec agents décisionnels, méthode Agile, ENAC
- **Cinématique inverse par réseau de neurones** — apprentissage de la fonction inverse position → angles, PyTorch, Sapienza di Roma

---

## Ailleurs

En dehors du code, je suis de près les marchés financiers — analyse macro, stratégies de couverture, comportement des actifs en période de stress. Un autre terrain où les données et le raisonnement structuré font la différence.

Je voyage quand je peux (Colombie, Chine, États-Unis), je fais du calisthenics, du tennis et du trail.

---

## Contact

[![LinkedIn](https://img.shields.io/badge/LinkedIn-louis--angleys-0a66c2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/louis-angleys-10110422a/)
&nbsp;
[![Email](https://img.shields.io/badge/Email-louis.angleys%40icloud.com-1a1a1a?style=flat-square&logo=apple&logoColor=white)](mailto:louis.angleys@icloud.com)