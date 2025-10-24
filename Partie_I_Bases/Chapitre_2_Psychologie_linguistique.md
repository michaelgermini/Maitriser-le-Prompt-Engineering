# Chapitre 2 : Psychologie et linguistique des prompts

## Comment le langage influence les modèles

### Théorie linguistique des LLM

Les grands modèles de langage ne "comprennent" pas le langage comme les humains. Ils opèrent sur des **patterns statistiques** appris à partir de milliards de tokens d'entraînement. Cependant, des principes linguistiques et psychologiques peuvent être utilisés pour influencer leurs réponses.

### Le paradoxe de l'IA linguistique

> **Concept clé** : Les LLM sont des systèmes statistiques qui simulent la compréhension linguistique.

Cette dualité crée des opportunités uniques pour le Prompt Engineering :
- **Avantage** : Prédictibilité statistique
- **Défi** : Absence de véritable compréhension sémantique

### Principes psycholinguistiques appliqués

#### 1. **Priming cognitif**
Le langage utilisé au début du prompt "prime" le modèle vers certains modes de pensée.

**Exemple inefficace :**
```
Écris un poème.
```

**Exemple avec priming :**
```
Imagine-toi comme un poète romantique du XIXe siècle, inspiré par Wordsworth et Shelley. Compose un poème lyrique sur la nature printanière, utilisant un langage archaïque et des métaphores naturelles.
```

#### 2. **Ancrage contextuel**
Les premiers mots établissent le cadre cognitif pour toute la réponse.

**Sans ancrage :**
```
Explique l'inflation économique.
```

**Avec ancrage fort :**
```
En tant qu'économiste chevronné travaillant pour la Banque Centrale Européenne, explique à un ministre des finances comment l'inflation affecte l'économie réelle, en utilisant des exemples concrets de politique monétaire.
```

#### 3. **Charge cognitive distribuée**
Répartir l'information complexe en chunks digestibles améliore la compréhension du modèle.

---

> **💡 Conseil** : Les LLM traitent mieux les informations structurées hiérarchiquement que les paragraphes denses.

---

## Principes de clarté, concision et précision

### Le triangle d'or du Prompt Engineering

```
     Précision
    /        \
   /          \
Clarté ---- Concision
```

Ces trois principes sont interdépendants mais parfois contradictoires.

### 1. **Clarté** : Éliminer l'ambiguïté

#### Techniques pour améliorer la clarté

**a) Définir explicitement les termes**
```
Mauvais : "Fais une analyse SWOT."
Correct : "Réalise une analyse SWOT (Strengths, Weaknesses, Opportunities, Threats) pour une startup de e-commerce vendant des produits bio."
```

**b) Utiliser des connecteurs logiques**
```
Plutôt que : "Fais ça, puis fais ça."
Utilisez : "D'abord, [action1]. Ensuite, [action2]. Enfin, [action3]."
```

**c) Spécifier le format de sortie**
```
Format souhaité : JSON, Markdown, liste numérotée, tableau, etc.
```

#### Métriques de clarté

| Niveau | Description | Exemple |
|--------|-------------|---------|
| **Faible** | Ambigu, vague | "Écris quelque chose" |
| **Moyen** | Instructions de base | "Écris un article de 500 mots" |
| **Élevé** | Spécifications détaillées | "Écris un article de 500 mots avec intro, 3 sections, conclusion" |
| **Expert** | Métriques de qualité incluses | "Écris un article... avec au moins 3 sources citées" |

### 2. **Concision** : Maximiser l'efficacité

#### Loi de Pareto appliquée aux prompts
**80% de l'efficacité** vient de **20% du contenu du prompt**.

#### Techniques d'optimisation

**a) Supprimer les redondances**
```
Redondant : "Je veux que tu écrives, que tu composes, que tu crées un texte..."
Concise : "Écris un texte sur..."
```

**b) Utiliser des abréviations standardisées**
```
- LLM = Large Language Model
- NLP = Natural Language Processing
- API = Application Programming Interface
```

**c) Structurer hiérarchiquement**
```
Plutôt que : "Fais une analyse complète avec tous les détails possibles"
Utilisez :
- Niveau 1 : Vue d'ensemble
- Niveau 2 : Analyse détaillée
- Niveau 3 : Recommandations spécifiques
```

#### Impact économique de la concision

**Étude de cas :** Réduction de tokens
- Prompt verbeux : 150 tokens → Réponse : 200 tokens
- Prompt concis : 50 tokens → Réponse : 180 tokens
- **Économie : 35% de réduction des coûts**

### 3. **Précision** : Cibler exactement le résultat souhaité

#### Niveaux de précision

**Précision sémantique**
- Utiliser des termes techniques appropriés
- Éviter les synonymes ambigus

**Précision quantitative**
- Spécifier les nombres : "3 exemples", "500 mots", "5 minutes"
- Définir les plages : "entre 800-1000 mots"

**Précision qualitative**
- "Ton professionnel mais accessible"
- "Niveau universitaire avancé"
- "Style journalistique d'investigation"

---

> **✓ Bonne pratique** : Utilisez la technique "SMART" pour vos prompts :
> - **S**pécifique
> - **M**esurable
> - **A**tteignable
> - **R**elevant
> - **T**ime-bound (si applicable)

---

## Cas d'erreurs courantes

### Erreur #1 : Le prompt trop vague

**Symptôme :**
```
"Donne-moi des idées pour mon projet."
```

**Problème :** Aucun contexte, aucune contrainte, aucun objectif défini.

**Solution :**
```
Je développe une application mobile de fitness pour seniors. J'ai besoin de 5 idées innovantes pour la fonctionnalité principale "suivi de l'activité physique", qui doit être simple d'utilisation, motivante, et adaptée aux limitations physiques des utilisateurs âgés de 65+ ans.
```

### Erreur #2 : Le prompt contradictoire

**Exemple problématique :**
```
Écris un texte court et détaillé sur la Seconde Guerre mondiale.
```

**Pourquoi contradictoire :**
- "Court" vs "détaillé" sont antagonistes
- Le modèle doit arbitrer entre les deux

**Version corrigée :**
```
Écris un résumé concis de 200 mots sur les causes principales de la Seconde Guerre mondiale, en te concentrant sur 3 événements déclencheurs majeurs.
```

### Erreur #3 : Le prompt trop technique pour la tâche

**Exemple :**
```
Utilise l'algorithme de transformée de Fourier rapide pour analyser cette série temporelle et identifier les fréquences dominantes, puis applique un filtre Butterworth d'ordre 4 avec une fréquence de coupure de 0.2 pour supprimer le bruit.
```

**Problème :** Prompt sur-qualifié pour une tâche simple d'analyse de données.

**Solution adaptée :**
```
Analyse cette série de données de ventes mensuelles. Identifie les tendances saisonnières et les anomalies. Présente tes conclusions sous forme de graphique ASCII simple.
```

### Erreur #4 : Absence de contraintes de format

**Prompt sans format :**
```
Crée un plan de cours sur le machine learning.
```

**Résultat typique :** Texte narratif désorganisé, difficile à utiliser.

**Prompt avec format :**
```
Crée un plan de cours structuré sur le machine learning pour des étudiants en master. Utilise ce format précis :

# Plan de Cours : Machine Learning

## Objectifs d'apprentissage
- Objectif 1
- Objectif 2

## Structure du cours (12 semaines)

### Semaine 1 : Introduction
**Thèmes :** [liste]
**Activités :** [liste]
**Ressources :** [liste]

[Continue pour chaque semaine]
```

### Erreur #5 : Le prompt "fourre-tout"

**Anti-pattern :** Tout mélanger dans un seul prompt
- Contexte + instruction + exemples + contraintes + format

**Solution :** Structurer en sections claires avec des en-têtes.

### Erreur #6 : Négliger le contexte culturel

**Exemple problématique pour un public international :**
```
Explique comment fonctionne un chèque en bois.
```

**Problème :** "Chèque en bois" est une expression idiomatique française pour "chèque sans provision".

**Solution :**
```
Explique le concept de "chèque sans provision" (aussi appelé "bounced check" en anglais ou "chèque en bois" en français familier).
```

## Analyse psychologique des interactions IA

### Théorie des attentes de confirmation

Les LLM ont tendance à confirmer les biais présents dans les prompts.

**Exemple :**
```
Prompt biaisé : "Pourquoi les jeunes sont-ils paresseux de nos jours ?"
Réponse typique : Confirme le biais en donnant des raisons.

Prompt neutre : "Quelles sont les principales motivations des jeunes générations sur le marché du travail ?"
Réponse typique : Analyse équilibrée.
```

### Effet d'ancrage numérique

Les nombres mentionnés influencent les réponses quantitatives.

**Expérience :**
- Prompt : "Estime le prix d'une maison familiale" → Réponse moyenne
- Prompt : "Estime le prix d'une maison familiale de 200m²" → Réponse plus élevée
- Prompt : "Estime le prix d'une maison familiale modeste" → Réponse plus basse

### Influence du ton du prompt

| Ton du prompt | Influence sur la réponse |
|---------------|------------------------|
| Autoritaire ("Tu dois...") | Réponses plus formelles, structurées |
| Collaboratif ("Pourrions-nous...") | Réponses plus créatives, participatives |
| Urgent ("Il est crucial que...") | Réponses plus concises, prioritaires |
| Éducatif ("Apprenons ensemble...") | Réponses plus pédagogiques, avec explications |

## Exercices pratiques

### Exercice 1 : Diagnostic d'erreurs

**Mission :** Analysez ces prompts et identifiez les erreurs courantes.

```
1. "Fais-moi un super rapport sur l'environnement."
2. "Écris un texte long et court sur l'IA."
3. "Sois créatif et suit exactement ce format : 1,2,3,4."
4. "Explique-moi ce qu'est un algorithme de tri."
```

Pour chaque prompt :
- Identifiez l'erreur
- Expliquez pourquoi c'est problématique
- Proposez une correction

### Exercice 2 : Optimisation de concision

**Challenge :** Réduisez ce prompt verbeux tout en gardant son efficacité.

**Prompt original (156 mots) :**
```
Je souhaiterais que vous puissiez m'aider à créer une présentation PowerPoint sur les avantages et les inconvénients des réseaux sociaux dans la vie professionnelle. Je voudrais que cette présentation soit composée de 10 slides environ, avec des bullet points clairs et compréhensibles, et qu'elle contienne des exemples concrets tirés du monde réel. Aussi, il faudrait inclure quelques statistiques récentes si possible, et terminer par des recommandations pratiques pour les professionnels qui utilisent les réseaux sociaux dans leur travail quotidien.
```

**Objectif :** Réduire à moins de 50 mots tout en gardant toutes les spécifications essentielles.

### Exercice 3 : Test A/B de précision

**Expérience :** Créez deux versions d'un prompt pour la même tâche.

**Tâche :** Générer une description de produit pour un smartphone.

**Version A :** Vague et générale
**Version B :** Précise et détaillée

Comparez les résultats obtenus et analysez les différences.

### Exercice 4 : Étude culturelle

**Mission :** Adaptez ce prompt pour différents contextes culturels.

**Prompt de base :**
```
Écris un discours de motivation pour des étudiants de terminale.
```

**Adaptations requises :**
1. Contexte français (lycée)
2. Contexte américain (high school)
3. Contexte asiatique (préparation aux examens nationaux)

## Outils d'auto-évaluation

### Checklist de qualité du prompt

- [ ] **Clarté** : Chaque instruction est-elle compréhensible isolément ?
- [ ] **Concision** : Y a-t-il des mots inutiles ?
- [ ] **Précision** : Les spécifications sont-elles mesurables ?
- [ ] **Cohérence** : Toutes les parties sont-elles alignées ?
- [ ] **Complétude** : Toutes les informations nécessaires sont-elles fournies ?

### Score de qualité

| Critère | Score (/5) | Justification |
|---------|------------|---------------|
| Clarté |     |             |
| Concision |     |             |
| Précision |     |             |
| Structure |     |             |
| **Total** |     |             |

### Métriques quantitatives

- **Ratio concision** : Mots du prompt / Efficacité perçue
- **Score de spécificité** : Nombre de contraintes explicites
- **Taux d'ambiguïté** : Mots vagues / Mots total

---

## Évaluation du chapitre

**Auto-évaluation psycholinguistique :**

**Compréhension des principes :**
- [ ] Clarté, concision, précision
- [ ] Influence du langage sur les LLM
- [ ] Erreurs courantes identifiées

**Application pratique :**
- [ ] Diagnostic d'erreurs dans les prompts
- [ ] Optimisation de concision
- [ ] Adaptation culturelle

**Score global :** _____/20

**Forces identifiées :**
- [ ] Analyse psychologique
- [ ] Techniques linguistiques
- [ ] Créativité dans les formulations

**Axes d'amélioration :**
- [ ] Précision dans les formulations
- [ ] Concision sans perdre d'information
- [ ] Adaptation contextuelle

**Projet personnel :** Créez un prompt "parfait" pour un domaine qui vous intéresse.
