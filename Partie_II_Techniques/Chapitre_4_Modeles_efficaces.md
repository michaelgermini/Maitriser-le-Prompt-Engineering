# Chapitre 4 : Modèles de prompts efficaces

## Patterns et templates

### Le concept de patterns

Les **patterns de prompts** sont des structures réutilisables qui ont fait leurs preuves pour des tâches spécifiques. Ils agissent comme des "recettes" standardisées pour obtenir des résultats cohérents.

### Classification des patterns

#### 1. **Patterns structuraux**
Organisent l'information de manière hiérarchique.

#### 2. **Patterns comportementaux**
Définissent comment le modèle doit penser et répondre.

#### 3. **Patterns de contenu**
Spécifient le type et le format du contenu généré.

#### 4. **Patterns métacognitifs**
Guident le processus de réflexion du modèle.

---

> **💡 Conseil** : Les patterns sont comme des LEGO - combinez-les pour créer des prompts complexes et robustes.

---

## Pattern #1 : Le pattern "Rôle-Action-Format" (RAF)

### Structure de base
```
Tu es [RÔLE]. [ACTION PRINCIPALE] en [FORMAT].
[CONTEXTE ET CONTRAINTES]
```

### Exemples d'application

**Pour l'analyse de données :**
```
Tu es un data scientist expérimenté. Analyse ce dataset CSV en format JSON structuré.
Le dataset contient des ventes mensuelles sur 2 ans.
Fournis : statistiques descriptives, tendances, anomalies, recommandations.
```

**Pour la génération de code :**
```
Tu es un développeur Python senior. Réécris cette fonction en code asynchrone.
La fonction traite des données utilisateur de manière sécurisée.
Format : fonction complète avec docstring, gestion d'erreurs, tests unitaires.
```

**Pour le conseil stratégique :**
```
Tu es un consultant en stratégie d'entreprise. Élabore un plan d'expansion internationale en format de présentation PowerPoint.
L'entreprise est une startup SaaS avec 50 employés.
Structure : 10 slides maximum, métriques clés, risques identifiés, timeline.
```

### Avantages du pattern RAF
- **Clarté** : Rôle défini élimine l'ambiguïté
- **Focus** : Action précise guide l'exécution
- **Contrôle** : Format spécifié garantit la structure

## Pattern #2 : Le pattern "Étapes Logiques" (Chain of Thought - CoT)

### Principe
Le modèle pense étape par étape, comme un humain raisonne.

### Structure de base
```
Résous ce problème en suivant ces étapes logiques :
1. [Étape 1]
2. [Étape 2]
3. [Étape 3]
...
Conclusion
```

### Exemple détaillé : Résolution mathématique

**Prompt CoT :**
```
Résous cette équation quadratique étape par étape :
3x² + 7x - 6 = 0

Étapes à suivre :
1. Identifie le type d'équation (quadratique)
2. Vérifie la factorisation possible
3. Applique la formule quadratique si nécessaire : x = [-b ± √(b²-4ac)] / 2a
4. Calcule les valeurs de a, b, c
5. Effectue les calculs
6. Vérifie les solutions
7. Donne la réponse finale
```

### Variantes du CoT

#### CoT Zero-shot
```
Explique-moi pourquoi l'énergie solaire est renouvelable.
Raisonnement étape par étape :
```

#### CoT Few-shot avec exemples
```
Voici comment résoudre des problèmes de probabilité :

Exemple 1 :
Problème : Probabilité de tirer un roi d'un jeu de 52 cartes.
Étape 1 : Nombre total de cartes = 52
Étape 2 : Nombre de rois = 4
Étape 3 : Probabilité = 4/52 = 1/13
Solution : 1/13 ou 7.69%

Maintenant résous :
Problème : Probabilité de tirer une carte rouge d'un jeu standard.
Raisonnement étape par étape :
```

### Applications avancées

#### CoT pour le débogage de code
```
Débugue cette fonction Python étape par étape :

def calculate_average(numbers):
    return sum(numbers) / len(numbers)

Problèmes potentiels :
1. Vérification du type d'entrée
2. Gestion de la liste vide
3. Gestion des types non numériques
4. Précision des calculs
5. Valeurs spéciales (NaN, infini)

Solution proposée :
```

## Pattern #3 : Le pattern "Template à Trous"

### Concept
Modèle réutilisable avec des variables à remplir.

### Structure générique
```
[INTRODUCTION CONTEXTE]

[TÂCHE SPÉCIFIQUE pour {SUJET}]

[CONTRAINTES :
- {CONTRAINTE_1}
- {CONTRAINTE_2}
- {CONTRAINTE_3}]

[FORMAT DE SORTIE : {FORMAT}]

[EXEMPLES : {EXEMPLE_OPTIONNEL}]
```

### Template spécialisé : Analyse SWOT

```
Analyse SWOT pour {ENTREPRISE} dans le secteur {SECTEUR}

CONTEXTE : {DESCRIPTION_ENTREPRISE}

ANALYSE REQUISE :
- Strengths : Forces internes positives
- Weaknesses : Faiblesses internes à améliorer
- Opportunities : Chances externes à saisir
- Threats : Menaces externes à surveiller

FORMAT : Tableau Markdown avec 4 colonnes
PROFONDEUR : 3 points par catégorie
PERSPECTIVE : Objectif et factuel
```

### Template pour la génération de contenu

```
ARTICLE SUR : {SUJET}

CIBLE : {PUBLIC} (âge, niveau d'expertise)
TON : {TON_ALIRE} (professionnel, accessible, technique)
LONGUEUR : {NOMBRE_MOTS} mots

STRUCTURE :
1. Introduction accrocheuse ({PCT_INTRO}%)
2. Corps avec {NB_SECTIONS} sections
3. Conclusion avec call-to-action

CONTRAINTES :
- Inclure {NB_SOURCES} sources citées
- Utiliser {NB_EXEMPLES} exemples concrets
- Éviter le jargon {NIVEAU_JARGON}
```

### Avantages des templates
- **Réutilisabilité** : Un template = 100 usages
- **Cohérence** : Format uniforme
- **Efficacité** : Création rapide

---

> **✓ Bonne pratique** : Créez une bibliothèque de templates personnalisés pour vos tâches récurrentes.

---

## Pattern #4 : Le pattern "Multi-Perspective"

### Principe
Examiner un problème sous plusieurs angles simultanément.

### Structure de base
```
Analyse [SUJET] sous ces perspectives :

1. **Perspective A** : [Description]
2. **Perspective B** : [Description]
3. **Perspective C** : [Description]

Pour chaque perspective, fournis :
- Points clés
- Avantages
- Limites
- Recommandations
```

### Exemple : Choix technologique

```
Analyse le choix entre React et Vue.js pour une application web sous ces perspectives :

1. **Développeur** : Courbe d'apprentissage, écosystème, communauté
2. **Performance** : Vitesse de rendu, taille du bundle, optimisation
3. **Entreprise** : Coûts de développement, maintenance, scalabilité
4. **Utilisateur** : Expérience, accessibilité, responsive design

Format : Comparatif détaillé avec scores sur 10
```

### Applications spécialisées

#### Analyse éthique
```
Évalue l'impact éthique de [TECHNOLOGIE] sous :

1. **Individus** : Vie privée, autonomie, bien-être
2. **Société** : Inégalités, emplois, cohésion sociale
3. **Environnement** : Empreinte carbone, ressources, durabilité
4. **Régulation** : Lois actuelles, besoins futurs, enforcement
```

## Patterns itératifs et multi-étapes

### Pattern "Iterative Refinement"

#### Étape 1 : Version initiale
```
Crée une première version de [TÂCHE].
```

#### Étape 2 : Analyse et feedback
```
Analyse cette version et identifie les points d'amélioration.
```

#### Étape 3 : Refinement
```
Améliore la version en appliquant ces corrections : [LISTE_CORRECTIONS]
```

#### Étape 4 : Validation finale
```
Vérifie que la version finale respecte tous les critères.
```

### Exemple complet : Rédaction d'article

**Itération 1 :**
```
Écris un article sur l'IA éthique.
```

**Itération 2 :**
```
L'article est trop général. Ajoute :
- 3 exemples concrets d'IA éthique
- Une section sur les défis actuels
- Des recommandations pratiques
```

**Itération 3 :**
```
Maintenant ajoute une introduction accrocheuse et une conclusion percutante.
```

### Pattern "Divide and Conquer"

#### Principe
Décomposer une tâche complexe en sous-tâches simples.

#### Structure
```
Tâche principale : [DESCRIPTION]

Sous-tâches :
1. [Sous-tâche 1] - Responsable : [AGENT/ROLE]
2. [Sous-tâche 2] - Responsable : [AGENT/ROLE]
3. [Sous-tâche 3] - Responsable : [AGENT/ROLE]

Coordination : [COMMENT_INTÉGRER]
```

### Exemple : Planification de projet

```
Projet : Développement d'une application mobile de fitness

Sous-tâches :

1. **Analyse des besoins** - Responsable : Product Manager
   - Entretiens utilisateurs
   - Analyse concurrentielle
   - Définition des fonctionnalités

2. **Design UX/UI** - Responsable : UX Designer
   - Wireframes
   - Maquettes
   - Tests utilisateurs

3. **Développement** - Responsable : Équipe dev
   - Architecture technique
   - Implémentation
   - Tests unitaires

Coordination : Revue hebdomadaire, jalons mensuels, documentation partagée
```

## Patterns conditionnels

### Pattern "If-Then-Else"

#### Structure de base
```
Évalue [CONDITION].
Si [CONDITION_VRAI], alors [ACTION_A].
Sinon, [ACTION_B].
```

#### Exemple : Classification adaptative

```
Analyse ce texte : "[TEXTE]"

Si le texte fait moins de 100 mots :
- Fais un résumé en 2 phrases
- Identifie 2 émotions principales

Si le texte fait entre 100-500 mots :
- Fais un résumé en 4 phrases
- Analyse le sentiment global
- Identifie les thèmes principaux

Si le texte fait plus de 500 mots :
- Crée un résumé structuré avec sections
- Analyse détaillée des arguments
- Fournis des statistiques de contenu
```

### Pattern "Conditional Branching"

#### Structure avancée
```
Étape 1 : [ANALYSE_INITIALE]

Basé sur les résultats :
- Si [CONDITION_A] : [BRANCHE_A]
- Si [CONDITION_B] : [BRANCHE_B]
- Si [CONDITION_C] : [BRANCHE_C]

Dans chaque branche : [SOUS_ÉTAPES]
```

### Exemple : Diagnostic technique

```
Diagnostique ce problème informatique : "[DESCRIPTION_BUG]"

Étape 1 : Classification du problème
- Si c'est une erreur 404 : Vérifie l'URL et la configuration serveur
- Si c'est une erreur 500 : Analyse les logs serveur
- Si c'est un problème de performance : Profile l'application

Pour chaque type :
1. Causes possibles
2. Solutions étape par étape
3. Tests de validation
4. Prévention future
```

## Combinaison de patterns

### Pattern hybride : RAF + CoT + Template

```
Tu es un [RÔLE]. Analyse [SUJET] en suivant ces étapes :

1. [ÉTAPE_1] : [DESCRIPTION]
2. [ÉTAPE_2] : [DESCRIPTION]
3. [ÉTAPE_3] : [DESCRIPTION]

Pour chaque étape, fournis :
- Analyse détaillée
- Évidence/support
- Implications

Format final : [FORMAT_SPÉCIFIÉ]
```

### Exemple : Analyse de marché

```
Tu es un analyste de marché senior. Évalue le potentiel du marché du vegan food en Europe en suivant ces étapes :

1. **Analyse de la taille du marché** : Données actuelles et projections 2030
2. **Segmentation des consommateurs** : Profils démographiques et motivations
3. **Analyse concurrentielle** : Principaux acteurs et parts de marché
4. **Tendances et drivers** : Facteurs influençant la croissance

Pour chaque étape, fournis :
- Données chiffrées (sources citées)
- Analyse qualitative
- Graphiques ASCII simples
- Implications stratégiques

Format final : Rapport exécutif de 1500 mots avec recommandations
```

## Exercices pratiques

### Exercice 1 : Création de patterns personnalisés

**Mission :** Créez un pattern pour une tâche spécifique à votre domaine.

**Étapes :**
1. Identifiez une tâche répétitive
2. Analysez les composants récurrents
3. Créez un template générique
4. Testez avec 3 exemples différents
5. Affinez basé sur les résultats

### Exercice 2 : Combinaison de patterns

**Challenge :** Combinez 3 patterns différents dans un seul prompt efficace.

**Patterns à combiner :**
- RAF (Rôle-Action-Format)
- CoT (Chain of Thought)
- Multi-perspective

**Tâche :** Analyse stratégique d'une entreprise

### Exercice 3 : Optimisation itérative

**Mission :** Améliorez un prompt faible en utilisant l'approche itérative.

**Prompt initial faible :**
```
Fais un plan pour mon projet.
```

**Objectif :** Transformer en prompt professionnel et détaillé en 3 itérations.

### Exercice 4 : Pattern conditionnel complexe

**Challenge :** Créez un système de diagnostic automatique.

**Domaine :** Support technique pour une application web

**Conditions à gérer :**
- Type d'erreur (404, 500, timeout, etc.)
- Plateforme utilisateur (mobile, desktop, browser)
- Gravité (bloquant, gênant, cosmétique)
- Contexte (nouvel utilisateur, utilisateur régulier)

---

## Évaluation du chapitre

**Maîtrise des patterns :**

**Patterns de base :**
- [ ] RAF maîtrisé
- [ ] CoT appliqué
- [ ] Templates créés

**Patterns avancés :**
- [ ] Multi-perspective utilisé
- [ ] Patterns itératifs testés
- [ ] Conditions logiques implémentées

**Créativité :**
- [ ] Combinaisons originales
- [ ] Adaptations contextuelles
- [ ] Templates personnalisés

**Score global :** _____/25

**Bibliothèque personnelle :**
- [ ] 3 templates créés
- [ ] 2 patterns hybrides testés
- [ ] Documentation complète

**Projet d'application :** Créez un pattern pour résoudre un problème réel dans votre travail/études.
