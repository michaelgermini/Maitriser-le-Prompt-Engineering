# Chapitre 6 : Optimisation et évaluation des prompts

## Tester la performance des prompts

### Méthodologie de test systématique

#### 1. **Tests unitaires**
Évaluez des prompts spécifiques sur des tâches isolées.

**Exemple :**
```
Test : Classification de sentiment
Prompt : "Classe ce texte en positif/négatif/neutre : [TEXTE]"
Métriques :
- Précision : 85%
- Rappel : 78%
- F1-Score : 81%
```

#### 2. **Tests d'intégration**
Évaluez des workflows complets avec plusieurs prompts enchaînés.

#### 3. **Tests de robustesse**
Testez avec des inputs variés et edge cases.

### Framework d'évaluation A/B

#### Structure des tests
```
Expérience : Comparaison de deux variantes de prompt

Groupe A : Prompt original
Groupe B : Prompt optimisé

Tâche : [DESCRIPTION]
Échantillon : 100 exemples
Juges : 3 évaluateurs humains
Métriques : Pertinence, créativité, cohérence
```

#### Analyse statistique
- Test de Student pour la significativité
- Intervalle de confiance à 95%
- Effect size (taille de l'effet)

---

> **✓ Bonne pratique** : Utilisez toujours des tests contrôlés avec des échantillons représentatifs pour valider vos optimisations.

---

## Mesurer la pertinence et la créativité des réponses

### Métriques de pertinence

#### 1. **Pertinence sémantique**
Mesure dans quelle mesure la réponse correspond à la requête.

**Outils :**
- **BERTScore** : Similarité sémantique avec référence
- **BLEURT** : Évaluation linguistique entraînée
- **ROUGE** : Pour les tâches de résumé

#### 2. **Pertinence contextuelle**
Évaluation de l'adéquation au contexte fourni.

**Checklist :**
- [ ] Toutes les contraintes respectées
- [ ] Contexte correctement interprété
- [ ] Objectifs atteints
- [ ] Informations pertinentes incluses

#### 3. **Pertinence pragmatique**
Utilité réelle de la réponse pour l'utilisateur.

### Métriques de créativité

#### 1. **Diversité lexicale**
Mesure la variété du vocabulaire utilisé.

```
Diversité = Nombre de mots uniques / Nombre total de mots
Seuil idéal : 0.6-0.8 pour la créativité équilibrée
```

#### 2. **Originalité des idées**
Évaluation de la nouveauté du contenu généré.

**Approches :**
- Comparaison avec corpus de référence
- Score de surprise informationnelle
- Évaluation humaine subjective

#### 3. **Cohérence créative**
Créativité sans sacrifier la logique.

**Métriques combinées :**
- **Score de créativité** : Moyenne de diversité + originalité + cohérence
- **Échelle** : 1-10 (1 = reproduction, 10 = innovation radicale)

### Tableau de bord d'évaluation

| Métrique | Outil | Seuil acceptable | Seuil excellent |
|----------|-------|------------------|-----------------|
| **Pertinence** | BERTScore | > 0.7 | > 0.85 |
| **Créativité** | Diversité lexicale | > 0.5 | > 0.7 |
| **Cohérence** | Perplexité | < 50 | < 30 |
| **Utilité** | Score humain | > 6/10 | > 8/10 |
| **Efficacité** | Tokens/réponse | < 200 | < 100 |

## Ajustement automatique et révision

### Optimisation par itération

#### 1. **Analyse des erreurs**
Identifiez les patterns d'échec :
- Types d'erreurs fréquentes
- Contextes problématiques
- Limites du prompt

#### 2. **Refinement progressif**
```
Version 1 : Prompt de base
↓ Analyse des problèmes
Version 2 : Corrections appliquées
↓ Tests supplémentaires
Version 3 : Optimisations avancées
↓ Validation finale
```

#### 3. **A/B Testing continu**
Maintenez deux versions en production :
- Version stable (performante)
- Version expérimentale (testée)

### Techniques d'optimisation automatique

#### 1. **Prompt Tuning**
Ajustement automatique des paramètres :
- Temperature pour la créativité
- Top-p pour la diversité
- Max tokens pour la concision

#### 2. **Few-shot dynamique**
Sélection automatique des exemples les plus pertinents.

#### 3. **Calibration adaptative**
Ajustement du prompt basé sur les performances passées.

### Outils d'optimisation

#### 1. **Auto-evaluation**
```python
def evaluate_prompt(prompt, test_cases):
    scores = []
    for case in test_cases:
        response = generate_response(prompt, case.input)
        score = calculate_metrics(response, case.expected)
        scores.append(score)
    return statistics.mean(scores)
```

#### 2. **Optimisation bayésienne**
Utilisation d'algorithmes pour explorer l'espace des prompts optimaux.

#### 3. **Reinforcement Learning from Human Feedback (RLHF)**
Intégration du feedback humain pour améliorer continuellement.

### Workflow d'optimisation complet

```
1. Définition des objectifs
   ↓
2. Création baseline
   ↓
3. Collecte de données de test
   ↓
4. Itération et A/B testing
   ↓
5. Analyse des métriques
   ↓
6. Refinement du prompt
   ↓
7. Validation à échelle
   ↓
8. Déploiement et monitoring
```

## Exercices pratiques

### Exercice 1 : Évaluation comparative

**Mission :** Comparez deux prompts pour la même tâche.

**Tâche :** Génération de descriptions de produits

**Prompt A :** Simple
**Prompt B :** Optimisé avec techniques avancées

**Évaluation :**
- Métriques quantitatives (longueur, diversité)
- Évaluation qualitative (3 juges humains)
- Analyse statistique des différences

### Exercice 2 : Optimisation itérative

**Challenge :** Améliorez un prompt faible en 4 itérations.

**Prompt initial :** "Écris un article."

**Itérations :**
1. Ajout de spécifications de base
2. Amélioration stylistique
3. Optimisation structurelle
4. Peaufinage créatif

**Tracking :** Mesurez l'amélioration à chaque étape.

### Exercice 3 : Création d'un framework d'évaluation

**Mission :** Développez un système d'évaluation personnalisé.

**Éléments :**
- Métriques pertinentes pour votre domaine
- Script d'automatisation
- Interface de visualisation
- Rapport automatique

---

## Évaluation du chapitre

**Maîtrise de l'optimisation :**

**Tests et métriques :**
- [ ] Framework d'évaluation implémenté
- [ ] Métriques pertinentes sélectionnées
- [ ] A/B testing réalisé

**Optimisation :**
- [ ] Itération systématique appliquée
- [ ] Ajustements automatiques testés
- [ ] Améliorations mesurées

**Score global :** _____/15

**Projet d'optimisation :** Optimisez un prompt pour une tâche réelle et mesurez les gains de performance.
