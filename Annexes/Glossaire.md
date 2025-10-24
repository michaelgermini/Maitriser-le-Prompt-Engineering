# Annexes

## Glossaire des termes clés

### Concepts fondamentaux

#### **Prompt Engineering**
> Art et science de concevoir des instructions efficaces pour guider les modèles d'intelligence artificielle générative vers des réponses pertinentes et de haute qualité.

#### **Large Language Model (LLM)**
> Modèle d'intelligence artificielle entraîné sur d'énormes quantités de données textuelles, capable de générer du texte cohérent et contextuellement approprié.

#### **Token**
> Unité de base du traitement du texte dans les LLM. Un token peut être un mot complet, une partie de mot, ou un caractère spécial.

#### **Embedding**
> Représentation vectorielle d'un token dans un espace multidimensionnel, capturant ses relations sémantiques avec d'autres tokens.

#### **Attention Mechanism**
> Composant clé des transformers qui permet au modèle de se concentrer sur différentes parties de l'entrée simultanément.

### Types de prompts

#### **Prompt zéro-shot (Zero-shot)**
> Prompt qui demande au modèle d'effectuer une tâche sans exemples préalables, en s'appuyant uniquement sur son entraînement général.

#### **Prompt few-shot (Few-shot)**
> Prompt qui fournit quelques exemples pour guider le modèle vers le comportement souhaité.

#### **Prompt one-shot (One-shot)**
> Variante du few-shot avec exactement un exemple de référence.

#### **Chain of Thought (CoT)**
> Technique qui encourage le modèle à raisonner étape par étape, comme un humain, pour améliorer la qualité des réponses complexes.

### Patterns et techniques

#### **Pattern RAF (Rôle-Action-Format)**
> Structure de prompt organisant l'instruction en trois parties : le rôle à adopter, l'action à effectuer, et le format de sortie attendu.

#### **Template à trous**
> Modèle de prompt réutilisable avec des variables (trous) à remplir selon le contexte spécifique.

#### **Iterative Refinement**
> Processus d'amélioration progressive d'un prompt par itérations successives basées sur les résultats obtenus.

#### **Conditional Branching**
> Logique conditionnelle dans les prompts permettant d'adapter la réponse selon des critères spécifiques.

### Métriques et évaluation

#### **Perplexité**
> Mesure de la capacité d'un modèle à prédire une séquence de texte. Plus la perplexité est basse, meilleur est le modèle.

#### **BLEU Score**
> Métrique d'évaluation de la qualité des traductions automatiques, comparant la similarité avec des références humaines.

#### **ROUGE Score**
> Métrique pour évaluer la qualité des résumés automatiques en mesurant le chevauchement avec les textes de référence.

#### **BERTScore**
> Évaluation sémantique utilisant des embeddings BERT pour mesurer la similarité entre textes générés et références.

### Technologies et plateformes

#### **Transformer**
> Architecture de réseau de neurones révolutionnaire introduite en 2017, base de tous les LLM modernes.

#### **GPT (Generative Pre-trained Transformer)**
> Famille de modèles développés par OpenAI, dont GPT-3, GPT-4, spécialisés dans la génération de texte.

#### **API (Application Programming Interface)**
> Interface permettant à des applications externes de communiquer avec un service ou modèle IA.

#### **Fine-tuning**
> Processus d'ajustement d'un modèle pré-entraîné sur un dataset spécifique pour améliorer ses performances sur une tâche donnée.

### Concepts avancés

#### **Hallucination**
> Phénomène où un LLM génère des informations plausibles mais factuellement incorrectes.

#### **Bias (Biais)**
> Tendance systématique d'un modèle à produire des réponses influencées par les biais présents dans ses données d'entraînement.

#### **Temperature**
> Paramètre contrôlant le degré de créativité/ aléatoire dans les réponses générées (0 = déterministe, 1+ = créatif).

#### **Top-p (Nucleus Sampling)**
> Technique de sampling où seules les p premières probabilités cumulées sont considérées pour la génération.

#### **Context Window**
> Nombre maximum de tokens qu'un modèle peut traiter simultanément dans une conversation.

### Applications spécifiques

#### **RAG (Retrieval-Augmented Generation)**
> Technique combinant recherche d'information et génération pour produire des réponses plus précises et actualisées.

#### **Prompt Chaining**
> Enchaînement séquentiel de prompts où la sortie d'un prompt sert d'entrée au suivant.

#### **Meta-prompting**
> Prompts qui génèrent ou optimisent d'autres prompts automatiquement.

#### **Safety Alignment**
> Processus d'alignement des modèles IA sur des valeurs humaines et des principes éthiques.

### Éthique et gouvernance

#### **IA Responsible (IA Responsable)**
> Approche du développement de l'IA qui prend en compte les impacts sociaux, éthiques et environnementaux.

#### **Fairness**
> Principe selon lequel les systèmes IA devraient traiter équitablement tous les groupes d'utilisateurs.

#### **Transparency**
> Capacité à expliquer et comprendre les décisions prises par un système IA.

#### **Accountability**
> Responsabilité des développeurs et utilisateurs des systèmes IA concernant leurs impacts et utilisations.
