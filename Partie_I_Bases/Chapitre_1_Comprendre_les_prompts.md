# Chapitre 1 : Comprendre les prompts

## Définition et rôle des prompts

### Définition technique

Un **prompt** est une séquence textuelle qui sert d'instruction ou de requête à un modèle de langage. Il agit comme le "programme" que nous écrivons pour guider l'IA vers le résultat souhaité.

### Rôle dans l'architecture IA

Le prompt remplit plusieurs fonctions cruciales :

#### 1. **Contexte initial**
Fournit le contexte nécessaire pour que le modèle comprenne la tâche.

#### 2. **Instructions comportementales**
Définit comment le modèle doit se comporter (ton, style, format).

#### 3. **Contraintes de sortie**
Spécifie les limitations et exigences de la réponse.

#### 4. **Exemples de référence**
Montre au modèle des exemples de ce qui est attendu.

### Modèle mathématique simplifié

Considérons le prompt comme une fonction qui transforme une requête brute en une instruction optimisée :

```
Prompt_Optimisé = f(Réponse_Attendue, Contexte, Contraintes, Exemples)
```

Où :
- **Réponse_Attendue** : Ce que vous voulez obtenir
- **Contexte** : Informations nécessaires
- **Contraintes** : Limites et règles
- **Exemples** : Modèles de référence

---

> **✓ Bonne pratique** : Un bon prompt contient toujours ces 4 éléments : **Quoi** (tâche), **Comment** (méthode), **Pourquoi** (contexte), et **Exemples** (référence).

---

## Types de prompts

### Classification principale

#### 1. **Prompts d'instruction** (Instruction-based)
Directives explicites sur ce que le modèle doit faire.

**Exemple simple :**
```
Écris un email professionnel pour refuser une invitation à une conférence.
```

**Exemple détaillé :**
```
Rédige un email de refus poli pour une invitation à la conférence TechInnovate 2024.
Ton: Professionnel mais chaleureux
Longueur: 100-150 mots
Points à couvrir:
- Remercier pour l'invitation
- Expliquer brièvement l'indisponibilité
- Proposer une alternative
- Terminer positivement
```

#### 2. **Prompts de question** (Question-based)
Questions qui encouragent le raisonnement et l'explication.

**Exemple :**
```
Explique-moi pourquoi l'apprentissage automatique est important pour l'analyse de données financières. Utilise des exemples concrets et structure ta réponse en 3 parties.
```

#### 3. **Prompts contextuels** (Context-based)
Fournissent un contexte riche avant la requête principale.

**Exemple :**
```
Tu es un chef cuisinier expérimenté avec 15 ans d'expérience dans la gastronomie française. Un client végétarien te demande de créer un menu complet pour un dîner de 6 personnes. Le budget est de 50€ par personne. Propose 3 options de menu différentes, en précisant les ingrédients, le temps de préparation et les accords mets-vins adaptés.
```

### Classification par complexité d'apprentissage

#### 4. **Prompts zéro-shot** (Zero-shot)
Aucune exemple fourni - le modèle doit généraliser à partir de son entraînement.

**Exemple :**
```
Classe ce texte en positif, négatif ou neutre :
"Le nouveau modèle d'iPhone est innovant mais son prix reste élevé."
```

#### 5. **Prompts few-shot** (Few-shot)
Quelques exemples fournis pour guider le modèle.

**Exemple :**
```
Voici des exemples de classification de sentiments :

Texte: "Ce restaurant est excellent, j'y retournerai !"
Sentiment: Positif

Texte: "Le service était lent et la nourriture froide."
Sentiment: Négatif

Texte: "C'était correct pour le prix."
Sentiment: Neutre

Maintenant, classe ce texte :
"Le film était intéressant mais trop long."
```

#### 6. **Prompts one-shot** (One-shot)
Un seul exemple fourni.

**Exemple :**
```
Voici un exemple de résumé exécutif :
Article: "La société TechCorp annonce un bénéfice trimestriel de 2.3 milliards de dollars, en hausse de 15% par rapport à l'année précédente. Cette performance est attribuée aux nouvelles initiatives d'IA et à l'expansion en Asie."
Résumé: "TechCorp réalise un bénéfice record de 2.3Mds$ (+15%), tiré par l'IA et l'Asie."

Maintenant, résume cet article :
[Article plus long inséré ici]
```

### Classification par objectif

| Type | Objectif | Exemple d'usage |
|------|----------|-----------------|
| **Créatif** | Génération originale | Écriture d'histoires, poésie |
| **Analytique** | Analyse et raisonnement | Résolution de problèmes, critiques |
| **Informatif** | Transmission de connaissances | Explications, tutoriels |
| **Conversationnel** | Interaction naturelle | Chatbots, assistants virtuels |
| **Technique** | Tâches spécialisées | Code, mathématiques, analyse de données |

---

> **⚠️ Attention** : Évitez de mélanger les types de prompts dans une seule requête. Un prompt créatif ne devrait pas contenir d'éléments analytiques contradictoires.

---

## Exemples concrets

### Exemple 1 : Rédaction d'article de blog

**Prompt inefficace :**
```
Écris un article sur l'IA.
```

**Pourquoi inefficace :**
- Trop vague
- Aucun contexte
- Pas de structure demandée
- Pas de longueur spécifiée

**Prompt optimisé :**
```
Tu es un journaliste technologique spécialisé en IA. Écris un article de blog de 800 mots sur "Les 5 tendances IA qui transformeront le marketing en 2024".

Structure :
1. Introduction accrocheuse (150 mots)
2. Les 5 tendances détaillées (500 mots) :
   - Personnalisation hyper-ciblée
   - Génération de contenu automatisé
   - Chatbots conversationnels avancés
   - Analyse prédictive du comportement client
   - Intégration multicanal
3. Impact sur les entreprises (100 mots)
4. Conclusion avec perspectives (50 mots)

Ton : Expert mais accessible
Utilise des exemples concrets d'entreprises
Inclue des statistiques récentes
```

### Exemple 2 : Analyse de code

**Prompt inefficace :**
```
Corrige ce code Python.
```

**Prompt optimisé :**
```
Tu es un développeur Python senior. Analyse ce code et propose des améliorations :

```python
def calculate_average(numbers):
    total = 0
    for num in numbers:
        total += num
    return total / len(numbers)
```

1. Identifie les problèmes potentiels
2. Propose une version améliorée avec :
   - Gestion des erreurs
   - Validation des inputs
   - Optimisations de performance
3. Explique tes changements
4. Fournis des tests unitaires
```

### Exemple 3 : Génération de contenu éducatif

**Prompt pour créer un quiz :**
```
Crée un quiz interactif sur les algorithmes de machine learning pour des étudiants en licence.

**Spécifications :**
- Niveau : Intermédiaire
- Nombre de questions : 10
- Types de questions : QCM (4 choix), Vrai/Faux, Questions ouvertes courtes
- Thèmes couverts :
  - Régression linéaire
  - Arbres de décision
  - Réseaux de neurones
  - SVM
- Format de sortie : JSON structuré avec questions, réponses, et explications

**Structure JSON attendue :**
{
  "quiz": {
    "title": "...",
    "description": "...",
    "questions": [
      {
        "id": 1,
        "type": "multiple_choice",
        "question": "...",
        "options": ["A", "B", "C", "D"],
        "correct_answer": "A",
        "explanation": "..."
      }
    ]
  }
}
```

### Exemple 4 : Résolution de problème mathématique

**Prompt avec raisonnement étape par étape :**
```
Résous ce problème de probabilité en détaillant chaque étape de ton raisonnement :

"Une urne contient 5 boules rouges et 3 boules bleues. On tire 2 boules sans remise. Quelle est la probabilité d'obtenir exactement une boule rouge ?"

**Instructions :**
1. Identifie les concepts probabilistes utilisés
2. Calcule les cas favorables
3. Calcule le nombre total de cas possibles
4. Applique la formule de probabilité
5. Vérifie le résultat
6. Donne l'interprétation finale

**Format de réponse :**
- Énoncé du problème
- Concepts clés
- Calcul détaillé
- Résultat final
- Vérification
```

---

> **💡 Conseil** : Commencez toujours par tester vos prompts avec des exemples simples avant de les complexifier. Un prompt qui fonctionne pour une tâche basique sera plus facile à adapter.

---

## Analyse comparative des types de prompts

### Tableau de performance

| Critère | Zéro-shot | Few-shot | One-shot |
|---------|-----------|----------|----------|
| **Facilité d'écriture** | ⭐⭐⭐ | ⭐⭐ | ⭐ |
| **Précision** | ⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐ |
| **Généralisation** | ⭐⭐⭐ | ⭐⭐ | ⭐ |
| **Coût en tokens** | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ |
| **Rapidité d'exécution** | ⭐⭐⭐ | ⭐⭐ | ⭐⭐ |

### Quand utiliser quel type ?

#### Utilisez Zéro-shot pour :
- Tâches simples et directes
- Quand vous n'avez pas d'exemples
- Tests rapides
- Économies de tokens

#### Utilisez Few-shot pour :
- Tâches complexes nécessitant des exemples
- Formats de sortie spécifiques
- Cohérence stylistique
- Haute précision requise

#### Utilisez One-shot pour :
- Quand un seul exemple suffit
- Économies de tokens avec précision suffisante
- Tâches très spécialisées

## Exercices pratiques

### Exercice 1 : Transformation de prompt
**Objectif :** Transformer un prompt inefficace en prompt optimisé

**Prompt initial inefficace :**
"Écris une histoire."

**Votre mission :** Créez un prompt détaillé qui produira une histoire engageante de 500 mots sur un thème donné.

### Exercice 2 : Classification de prompts
**Objectif :** Analyser et classifier différents types de prompts

Analysez ces prompts et identifiez leur type :
1. "Explique la photosynthèse en termes simples."
2. "Tu es un détective. Résous cette énigme : [énigme détaillée]"
3. "Traduis ce texte en français : [texte en anglais]"
4. "Voici un exemple de résumé... Maintenant résume cet article."

### Exercice 3 : Création de prompt zero-shot vs few-shot
**Objectif :** Comprendre la différence pratique

Créez deux versions d'un prompt pour classifier des emails comme "spam" ou "non-spam" :
- Version zéro-shot
- Version few-shot avec 3 exemples

Comparez les résultats obtenus.

---

## Évaluation du chapitre

**Auto-évaluation :**

- [ ] Je comprends la différence entre types de prompts
- [ ] Je peux identifier un prompt inefficace
- [ ] Je sais structurer un prompt optimisé
- [ ] J'ai pratiqué la transformation de prompts

**Score de maîtrise :** _____/10

**Points à améliorer :**
- [ ] Structure des prompts
- [ ] Choix du type approprié
- [ ] Détail des instructions
- [ ] Fourniture d'exemples

**Prochaine étape :** Expérimentez avec les exemples de ce chapitre dans votre interface IA préférée.
