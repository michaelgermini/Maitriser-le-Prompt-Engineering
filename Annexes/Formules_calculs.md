# Formules et calculs en Prompt Engineering

## 📊 Métriques quantitatives de performance

### 1. Efficacité des tokens

#### Ratio d'efficacité des prompts
```
Efficacité = (Qualité_de_la_réponse × Pertinence) / Nombre_de_tokens_utilisés
```

Où :
- **Qualité_de_la_réponse** : Score subjectif 1-10
- **Pertinence** : Score de similarité sémantique 0-1 (BERTScore)
- **Nombre_de_tokens_utilisés** : Tokens consommés pour le prompt + réponse

**Interprétation :**
- > 0.7 : Excellent (qualité élevée, tokens optimisés)
- 0.4-0.7 : Bon (équilibre acceptable)
- < 0.4 : À optimiser (trop verbeux ou peu pertinent)

#### Coût-efficacité
```
Coût_efficacité = Bénéfice_obtenu / (Coût_tokens × Temps_de_génération)
```

**Variables :**
- **Bénéfice_obtenu** : Valeur ajoutée (productivité gagnée, etc.)
- **Coût_tokens** : Prix par token selon le modèle
- **Temps_de_génération** : Durée de la réponse IA

### 2. Métriques de qualité du texte

#### Score de lisibilité (indice de Flesch)
```
Flesch_Score = 206.835 - 1.015 × (Mots_phrases_moyens) - 84.6 × (Syllabes_mots_moyens)
```

**Échelle d'interprétation :**
- 90-100 : Très facile (5ème année)
- 80-89 : Facile (6ème année)
- 70-79 : Assez facile (7ème année)
- 60-69 : Standard (8-9ème année)
- 50-59 : Assez difficile (10-12ème année)
- 30-49 : Difficile (collège)
- 0-29 : Très difficile (université)

#### Diversité lexicale
```
Diversité_lexicale = Nombre_de_mots_uniques / Nombre_total_de_mots
```

**Seuils optimaux :**
- **Technique/Scientifique** : 0.6-0.7 (vocabulaire spécialisé)
- **Créatif/Littéraire** : 0.7-0.8 (richesse expressive)
- **Commercial/Marketing** : 0.5-0.6 (accessibilité)

### 3. Métriques de cohérence

#### Score de cohérence sémantique
```
Cohérence = Moyenne_similarité_embeddings(Phrase_i, Phrase_i+1)
```

Calculé sur toutes les paires de phrases consécutives dans le texte.

#### Indice de répétition
```
Répétition = 1 - (Nombre_de_mots_uniques / Nombre_total_de_mots)
```

**Interprétation :**
- < 0.3 : Bonne variété
- 0.3-0.5 : Répétition acceptable
- > 0.5 : Répétition excessive (à corriger)

---

## 🤖 Métriques d'évaluation des modèles

### 4. Perplexité (qualité de prédiction)

#### Calcul de perplexité
```
Perplexité = exp(-1/N × Σ log(P(token_i | contexte)))
```

Où :
- **N** : Nombre total de tokens
- **P(token_i | contexte)** : Probabilité du token prédit

**Interprétation :**
- < 10 : Excellente performance
- 10-20 : Bonne performance
- 20-50 : Performance acceptable
- > 50 : Performance à améliorer

### 5. BLEU Score (traduction et génération)

#### BLEU-4 (4-grammes)
```
BLEU = BP × exp(1/4 × Σ w_n × log(Précision_n-gramme))
```

Avec :
- **BP** : Facteur de pénalité de brièveté
- **w_n** : Poids des n-grammes (généralement 0.25 chacun)
- **Précision_n-gramme** : Précision des n-grammes

**Échelle :**
- 0.0-0.3 : Mauvaise traduction
- 0.3-0.6 : Traduction acceptable
- 0.6-0.8 : Bonne traduction
- 0.8-1.0 : Excellente traduction

### 6. ROUGE Score (résumé automatique)

#### ROUGE-N (chevauchement de n-grammes)
```
ROUGE-N = (Σ Nombre_n-grammes_communs) / (Σ Nombre_n-grammes_référence)
```

#### ROUGE-L (plus longue sous-séquence commune)
```
ROUGE-L = F1-Score(LCS, référence)
```

Où **LCS** = Longest Common Subsequence

---

## 📈 Métriques de performance business

### 7. ROI du Prompt Engineering

#### Calcul du retour sur investissement
```
ROI = (Bénéfices_générés - Coûts_investis) / Coûts_investis × 100
```

**Bénéfices typiques :**
- Temps de production réduit
- Qualité améliorée
- Satisfaction client accrue
- Revenus additionnels

**Coûts typiques :**
- Formation des équipes
- Temps d'expérimentation
- Abonnements API
- Outils et infrastructure

#### Time-to-Value
```
TtV = Temps_pour_résultats_mesurables / Investissement_total
```

**Objectif :** < 3 mois pour la plupart des applications

### 8. Métriques de productivité

#### Gains de productivité
```
Productivité_améliorée = (Tâches_automatisées × Temps_moyen_par_tâche) / Temps_total_disponible × 100
```

#### Efficacité de l'équipe
```
Efficacité = (Objectifs_atteints / Ressources_utilisées) × 100
```

---

## 🔬 Métriques statistiques pour A/B testing

### 9. Test de signification statistique

#### Test Z pour proportions
```
Z = (p1 - p2) / √(p × (1-p) × (1/n1 + 1/n2))
```

Où :
- **p1, p2** : Proportions des deux groupes
- **p** : Proportion globale
- **n1, n2** : Tailles d'échantillon

**Seuil de significativité :**
- |Z| > 1.96 : Significatif à 95%
- |Z| > 2.58 : Significatif à 99%

#### Test T pour moyennes
```
t = (moyenne1 - moyenne2) / √(s1²/n1 + s2²/n2)
```

**Degrés de liberté :** n1 + n2 - 2

### 10. Intervalle de confiance

#### Pour une proportion
```
IC = p ± z × √(p × (1-p) / n)
```

#### Pour une moyenne
```
IC = moyenne ± t × (écart_type / √n)
```

---

## 🎯 Métriques d'optimisation de prompts

### 11. Score composite de qualité

#### Formule pondérée
```
Score_global = (0.3 × Pertinence) + (0.25 × Cohérence) + (0.2 × Créativité) + (0.15 × Efficacité) + (0.1 × Innovation)
```

**Pondérations ajustables selon le contexte d'usage**

#### Score d'optimisation itérative
```
Amélioration = (Score_nouvelle_version - Score_version_précédente) / Score_version_précédente × 100
```

**Objectif :** Amélioration > 10% à chaque itération majeure

### 12. Métriques de robustesse

#### Score de généralisation
```
Robustesse = Moyenne_scores_sur_ensembles_de_test_diversifiés
```

**Ensembles de test :**
- Différents niveaux de complexité
- Domaines variés
- Styles linguistiques divers

#### Taux d'échec
```
Taux_échec = Nombre_réponses_insatisfaisantes / Nombre_total_requêtes × 100
```

**Objectif :** < 5% pour un prompt production-ready

---

## 💰 Métriques économiques

### 13. Coût par valeur ajoutée

#### Cost-per-Value
```
CPV = Coût_total_API / Valeur_business_générée
```

**Optimisation :** Réduire CPV tout en maintenant la qualité

#### Break-even analysis
```
Point_mort = Coûts_fixes / (Prix_vente_unitaire - Coûts_variables_unitaire)
```

**Application :** Quand l'investissement en Prompt Engineering devient rentable

### 14. Métriques de scalabilité

#### Scalabilité verticale
```
Performance_échelle = Temps_réponse_base / (Temps_réponse_échelle × Facteur_échelle)
```

#### Scalabilité horizontale
```
Efficacité_distribution = Performance_totale / (Performance_unitaire × Nombre_instances)
```

---

## 📊 Tableaux de référence des seuils

### Seuils de performance par domaine

| Métrique | Excellent | Bon | Acceptable | À améliorer |
|----------|-----------|-----|------------|-------------|
| **Pertinence** | > 0.85 | 0.7-0.85 | 0.5-0.7 | < 0.5 |
| **Cohérence** | > 0.9 | 0.75-0.9 | 0.6-0.75 | < 0.6 |
| **Créativité** | > 0.8 | 0.6-0.8 | 0.4-0.6 | < 0.4 |
| **Efficacité** | > 0.8 | 0.6-0.8 | 0.4-0.6 | < 0.4 |
| **Lisibilité** | > 70 | 50-70 | 30-50 | < 30 |

### Seuils de coût par modèle

| Modèle | Coût/token | Usage recommandé | Limite mensuelle suggérée |
|--------|------------|------------------|---------------------------|
| **GPT-4** | $0.03 | Haute qualité | $300 |
| **GPT-3.5** | $0.002 | Itération rapide | $50 |
| **Claude 3** | $0.015 | Analyse complexe | $200 |
| **Gemini Pro** | $0.001 | Usage général | $30 |

### Facteurs de conversion

#### Tokens vers mots
```
Nombre_mots ≈ Nombre_tokens × 0.75
```

#### Tokens vers caractères
```
Nombre_caractères ≈ Nombre_tokens × 4
```

#### Coût mensuel estimé
```
Coût_mensuel ≈ Requêtes_jour × Tokens_moyens × Coût_token × 30
```

---

## 🧮 Exemples de calculs pratiques

### Exemple 1 : Évaluation d'un prompt marketing

**Données :**
- Tokens utilisés : 150 (prompt) + 300 (réponse) = 450
- Qualité perçue : 8/10
- Pertinence (BERTScore) : 0.82
- Coût token : $0.002

**Calculs :**
```
Efficacité = (8 × 0.82) / 450 ≈ 0.0146
Coût_total = 450 × 0.002 = $0.90
CPV = 0.90 / (8 × 0.82) ≈ $0.14 par point de qualité
```

### Exemple 2 : Comparaison A/B de prompts

**Prompt A :**
- Score qualité : 7.2
- Tokens : 280
- Temps génération : 3.2s

**Prompt B :**
- Score qualité : 8.1
- Tokens : 320
- Temps génération : 2.8s

**Analyse :**
```
Amélioration_qualité = (8.1 - 7.2) / 7.2 ≈ 12.5%
Efficacité_A = 7.2 / 280 ≈ 0.0257
Efficacité_B = 8.1 / 320 ≈ 0.0253
Différence = (0.0253 - 0.0257) / 0.0257 ≈ -1.6% (légère baisse)
```

**Conclusion :** Qualité supérieure compense la légère baisse d'efficacité.

### Exemple 3 : ROI d'un projet Prompt Engineering

**Investissement initial :**
- Formation équipe : $5,000
- Outils et API (3 mois) : $2,000
- Temps développement : $8,000
- **Total : $15,000**

**Bénéfices après 6 mois :**
- Productivité gagnée : 20 heures/semaine × 25 semaines × $50/h = $25,000
- Qualité améliorée : +15% satisfaction client = $10,000 valeur ajoutée
- Automatisation tâches : $8,000 économies
- **Total bénéfices : $43,000**

**Calcul ROI :**
```
ROI = (43,000 - 15,000) / 15,000 × 100 = 186.7%
Payback_period = 15,000 / (43,000 / 6) ≈ 2.1 mois
```

**Conclusion :** Investissement hautement rentable avec retour rapide.

---

## 📈 Graphiques et visualisations recommandés

### Types de visualisations pour le reporting

1. **Évolution des performances** : Graphiques linéaires
2. **Comparaison de prompts** : Diagrammes en barres
3. **Distribution des scores** : Histogrammes
4. **Corrélations** : Nuages de points
5. **ROI dans le temps** : Graphiques cumulés

### Outils de visualisation
- **Python** : Matplotlib, Seaborn, Plotly
- **Tableau** : Pour analyses interactives
- **Google Data Studio** : Gratuit et collaboratif
- **Power BI** : Pour entreprises

### KPIs dashboard recommandé

**Section Performance :**
- Score de qualité moyen
- Taux de succès des prompts
- Temps de génération moyen

**Section Économie :**
- Coût par requête
- ROI global
- Économies réalisées

**Section Utilisation :**
- Nombre de requêtes par jour
- Modèles les plus utilisés
- Erreurs les plus fréquentes

Ces formules et métriques constituent un cadre rigoureux pour évaluer, optimiser et justifier vos investissements en Prompt Engineering.
