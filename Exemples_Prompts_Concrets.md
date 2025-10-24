# 🎯 Exemples de Prompts Concrets - Prêts à l'Emploi

## 📝 Introduction

Cette collection présente des **exemples de prompts concrets et directement utilisables** pour les cas d'usage les plus courants. Chaque exemple est testé, optimisé et accompagné d'explications pour vous permettre de les adapter facilement à vos besoins.

---

## 💼 BUSINESS & MARKETING

### 📧 Email marketing personnalisé

**Prompt :**
```
Tu es un copywriter marketing senior spécialisé dans l'email marketing B2B. Crée une séquence d'emails automatisée pour promouvoir [PRODUIT/SERVICE] auprès de [SEGMENT_CLIENT].

Contexte :
- Entreprise : [NOM_ENTREPRISE]
- Positionnement : [VALEUR_UNIQUE]
- Pain points clients : [PROBLÈMES_CLIENTS]
- Solution proposée : [BÉNÉFICES_PRODUIT]

Séquence de 5 emails :
1. **Email 1** : Hook et identification problème (lundi)
2. **Email 2** : Éducation et valeur ajoutée (mercredi)
3. **Email 3** : Témoignages et preuve sociale (vendredi)
4. **Email 4** : Offre limitée et urgence (mardi suivant)
5. **Email 5** : Dernière chance et call-to-action final (jeudi)

Contraintes :
- Ton : Professionnel mais accessible
- Longueur : 150-200 mots par email
- Personnalisation : Variables [PRENOM], [ENTREPRISE_CLIENT]
- CTA clair et spécifique dans chaque email
- Métriques d'engagement à optimiser

Format de sortie : Code HTML responsive pour outil d'emailing
```

**Résultat attendu :** Séquence d'emails prête à être importée dans votre outil d'emailing (Mailchimp, Sendinblue, etc.)

---

### 📊 Analyse concurrentielle

**Prompt :**
```
Tu es un analyste stratégique senior dans le secteur [DOMAINE]. Réalise une analyse concurrentielle complète de [ENTREPRISE_CIBLE] vs ses 3 principaux concurrents.

Éléments à analyser :
1. **Positionnement marché**
   - Parts de marché actuelles
   - Segmentation clients
   - Proposition de valeur

2. **Offre produits/services**
   - Catalogue complet
   - Prix et politique tarifaire
   - Innovation et R&D

3. **Stratégie marketing**
   - Canaux de distribution
   - Campagnes publicitaires
   - Présence digitale (SEO, réseaux sociaux)

4. **Performance financière**
   - Chiffre d'affaires (estimation)
   - Marge et rentabilité
   - Investissements stratégiques

5. **Forces & Faiblesses**
   - SWOT détaillé
   - Opportunités de différenciation
   - Menaces potentielles

Sources : Données publiques, rapports sectoriels, analyses d'experts
Format : Rapport structuré avec tableaux comparatifs
Perspective : Objectif et factuel, recommandations actionnables
```

---

### 🎯 Brief créatif campagne

**Prompt :**
```
Tu es un directeur artistique senior pour une agence de publicité digitale. Développe le brief créatif complet pour la campagne [NOM_CAMPAGNE] de [MARQUE_CLIENT].

Contexte campagne :
- Objectif business : [RÉSULTAT_ATTENDU - ex: +30% ventes]
- Target audience : [PROFILS_DÉTAILLÉS - âge, CSP, comportements]
- Concurrents principaux : [LISTE_3_CONCURRENTS]
- Budget créatif : [ENVELOPPE_DISPONIBLE]
- Timeline : [DURÉE_CAMPAGNE]

Concept créatif :
- Insight consommateur : [COMPRÉHENSION_PROFONDE]
- Plateforme principale : [CANAUX_PRIORITAIRES]
- Tone of voice : [PERSONNALITÉ_MARQUE]
- Claim/tagline : [MESSAGE_CENTRAL]

Déclinaisons :
1. **Digital** : Posts réseaux sociaux, bannières display
2. **Vidéo** : Format court (15s) et long (60s)
3. **Print** : Affiches et brochures
4. **Événementiel** : Activation terrain

Métriques de succès :
- KPIs créatifs : Reach, engagement, mémorisation
- KPIs business : Conversions, ROI, notoriété
- Points de mesure : Pré-test, post-test, tracking continu

Format de livraison : Brief créatif professionnel complet
```

---

## 💻 DÉVELOPPEMENT & TECH

### 🔧 Debug de code

**Prompt :**
```
Tu es un développeur senior expérimenté en [LANGAGE_PROGRAMMATION]. Analyse ce code et identifie les bugs potentiels :

```[LANGAGE]
[COLLER_LE_CODE_ICI]
```

Problème décrit : [DESCRIPTION_ERREUR_OU_COMPORTEMENT_ATTENDU]

Analyse systématique :
1. **Erreurs de syntaxe** : Vérifications basiques
2. **Logique algorithmique** : Cohérence du raisonnement
3. **Gestion d'erreurs** : Try/catch et edge cases
4. **Performance** : Optimisations possibles
5. **Sécurité** : Vulnérabilités potentielles
6. **Bonnes pratiques** : Conventions et standards

Pour chaque problème identifié :
- Localisation précise (ligne/fonction)
- Description du bug
- Impact potentiel
- Code corrigé proposé
- Explication de la correction

Format : Rapport de debug structuré avec priorité des corrections
```

---

### 🚀 Optimisation performance

**Prompt :**
```
Tu es un architecte logiciel senior spécialisé en optimisation performance. Analyse et optimise cette fonction [NOM_FONCTION] :

```[LANGAGE]
[CODE_DE_LA_FONCTION]
```

Contexte d'usage :
- Fréquence d'appel : [NOMBRE_FOIS_SECONDE/MINUTE]
- Volume de données : [TAILLE_INPUT_TYPICAL]
- Contraintes système : [CPU/MÉMOIRE_DISPONIBLE]
- SLA requis : [TEMPS_RÉPONSE_MAXIMUM]

Analyse actuelle :
1. **Complexité algorithmique** : O(n), O(log n), etc.
2. **Utilisation mémoire** : Allocation/désallocation
3. **I/O bottlenecks** : Lectures/écritures
4. **Cache efficiency** : Hits/misses

Optimisations proposées :
1. **Algorithme** : Amélioration de complexité
2. **Structure données** : Choix plus efficace
3. **Memoization** : Cache intelligent
4. **Parallélisation** : Traitement concurrent
5. **Lazy loading** : Chargement à la demande

Métriques attendues :
- Réduction temps exécution : [CIBLE_%]
- Économie mémoire : [CIBLE_%]
- Maintenabilité : [IMPACT_SUR_CODE]

Format : Code optimisé + explication détaillée + benchmarks
```

---

### 🏗️ Architecture système

**Prompt :**
```
Tu es un architecte système senior pour applications [TYPE_APPLICATION - web/mobile/SaaS]. Conceois l'architecture complète pour [NOM_APPLICATION].

Exigences fonctionnelles :
- Utilisateurs cibles : [NOMBRE_UTILISATEURS]
- Cas d'usage principaux : [LISTE_FONCTIONS_CRITIQUES]
- Performance requise : [SLA_DÉTAILLÉS]
- Sécurité : [NIVEAU_CONFORMITÉ - RGPD, SOC2, etc.]

Contraintes techniques :
- Technologies imposées : [STACK_TECHNIQUE]
- Infrastructure : [CLOUD_PROVIDER - AWS/GCP/Azure]
- Budget annuel : [ENVELOPPE_INFRASTRUCTURE]
- Évolutivité : [OBJECTIF_SCALE_3ANS]

Architecture proposée :
1. **Couche présentation** : Frontend + API Gateway
2. **Couche application** : Services métier + logique
3. **Couche données** : Base + cache + stockage
4. **Infrastructure** : Serveurs + réseau + sécurité

Diagrammes requis :
- Architecture générale (composants)
- Flux de données utilisateur
- Déploiement et scaling
- Sécurité et monitoring

Recommandations :
- Technologies complémentaires
- Stratégie de migration
- Plan de contingence
- Métriques de succès
```

---

## 🎨 CRÉATIF & CONTENU

### 📝 Article de blog viral

**Prompt :**
```
Tu es un rédacteur de contenu viral pour [PLATEFORME_CIBLE - Medium/LinkedIn/Substack]. Crée un article destiné à devenir viral sur [SUJET_TENDANCE].

Analyse préalable :
- Tendances actuelles : [RECHERCHE_GOOGLE_TRENDS]
- Angle original : [DIFFÉRENCIATEUR_UNIQUE]
- Insight psychologique : [HOOK_ÉMOTIONNEL]

Structure virale prouvée :
1. **Titre accrocheur** : Question/provoc/curéosité (60 caractères max)
2. **Introduction punchy** : Hook + problème + promesse (150 mots)
3. **Développement** : Histoire + données + exemples concrets
4. **Twist inattendu** : Élément surprise ou contre-intuitif
5. **Call-to-action** : Partage + engagement communautaire

Optimisations virales :
- **Psychologie** : FOMO, confirmation bias, storytelling
- **Format** : Listicles, how-to, controversies saines
- **Timing** : Publication heure optimale
- **SEO** : Mots-clés tendance + long-tail
- **Social proof** : Témoignages, statistiques impressionnantes

Métriques cibles :
- Lecture complète : >70%
- Partages : >50 par 1000 vues
- Commentaires : >10 par 1000 vues

Format : Article HTML avec balises SEO optimisées
```

---

### 🎬 Script vidéo court

**Prompt :**
```
Tu es un scénariste TikTok/YouTube Shorts professionnel. Crée un script vidéo viral de 15-30 secondes sur [SUJET_ENGAGEANT].

Concept vidéo :
- Hook initial : [QUESTION_PROVOCATRICE_OU_STAT_IMPRESSIONNANTE]
- Twist : [ÉLÉMENT_SURPRISE_OU_CONTRE_INTUITIF]
- Call-to-action : [ACTION_CONCRÈTE_POUR_LE_SPECTATEUR]

Structure temporelle :
0-3s : Hook visuel + accroche audio
3-10s : Développement + démonstration
10-13s : Twist ou révélation
13-15s : CTA + branding

Éléments visuels suggérés :
- Texte à l'écran : Mots-clés importants
- Transitions : Rapides et dynamiques
- Musique : Trend actuelle + license-free
- Effets : Minimalistes mais impactants

Optimisations plateforme :
- Thumbnail accrocheur : Visage + texte contrasté
- Hashtags stratégiques : [LISTE_5-10_HASHTAGS]
- Timing parfait : Rythme qui garde l'attention
- Son : Voice-over énergique ou musique tendance

Métriques de succès :
- View rate : >50% des vues complètes
- Engagement : >5% likes + commentaires
- Partage : >2% des vues

Format : Script détaillé + storyboard textuel
```

---

### 🎨 Description produit e-commerce

**Prompt :**
```
Tu es un copywriter e-commerce senior pour [MARQUE_LUXE/STANDARD]. Rédige la description produit parfaite pour [NOM_PRODUIT] dans la catégorie [CATÉGORIE].

Analyse produit :
- Caractéristiques techniques : [SPÉCIFICATIONS_DÉTAILLÉES]
- Bénéfices clients : [AVANTAGES_CONCRETS]
- Positionnement prix : [QUALITÉ/PRIX]
- Concurrents directs : [POINTS_DIFFÉRENCIATEURS]

Structure de description :
1. **Titre SEO optimisé** (50-60 caractères)
2. **Phrase d'accroche** : Bénéfice principal (20 mots max)
3. **Description détaillée** : Caractéristiques + avantages
4. **Points forts mis en avant** : Liste à puces
5. **Call-to-action** : Incitation à l'achat

Optimisations conversion :
- **Psychologie** : Preuve sociale, urgence, rareté
- **SEO** : Mots-clés longue traîne intégrés naturellement
- **Mobile** : Lecture fluide sur téléphone
- **Confiance** : Garanties, retours, certifications

Longueur optimale :
- Titre : 50-60 caractères
- Description : 150-300 mots
- Meta description : 150-160 caractères

Format : HTML avec balises sémantiques pour e-commerce
```

---

## 📚 ÉDUCATION & FORMATION

### 🧠 Explication concept complexe

**Prompt :**
```
Tu es un professeur universitaire en [DOMAINE] avec 20 ans d'expérience pédagogique. Explique le concept de [CONCEPT_COMPLEXE] à des [NIVEAU_ÉTUDIANTS - débutants/intermédiaires/avancés].

Contexte pédagogique :
- Prérequis des étudiants : [CONNAISSANCES_REQUISES]
- Objectif d'apprentissage : [COMPÉTENCE_À_MAÎTRISER]
- Temps disponible : [DURÉE_SESSION]
- Méthode d'évaluation : [QUIZ/PRÉSENTATION/PROJET]

Structure pédagogique :
1. **Introduction** : Analogie du quotidien (5 min)
2. **Concepts fondamentaux** : Définitions claires (10 min)
3. **Exemples concrets** : Applications pratiques (15 min)
4. **Démonstration visuelle** : Schémas/diagrammes (10 min)
5. **Cas d'usage réel** : Étude de cas (10 min)
6. **Conclusion** : Résumé + points clés (5 min)

Adaptations niveau :
- **Débutants** : Vocabulaire simple, analogies, répétitions
- **Intermédiaires** : Terminologie précise, exemples techniques
- **Avancés** : Mathématiques, implications théoriques

Supports pédagogiques :
- Slides avec visuels
- Exercices pratiques
- Ressources complémentaires
- Quiz d'auto-évaluation

Format : Support de cours complet + guide du formateur
```

---

### 📝 Plan de formation personnalisé

**Prompt :**
```
Tu es un conseiller en formation professionnelle certifié. Élaborer un plan de formation personnalisé pour [PROFESSIONNEL] souhaitant maîtriser [COMPÉTENCE_CIBLE].

Profil apprenant :
- Expérience actuelle : [ANNÉES_DANS_DOMAINE]
- Objectifs professionnels : [POSTE_VISÉ_OU_COMPÉTENCE]
- Contraintes temporelles : [HEURES_SEMAINE_DISPONIBLES]
- Style d'apprentissage : [VISUEL/AUDITIF/KINESTHÉSIQUE]
- Budget formation : [ENVELOPPE_DISPONIBLE]

Analyse des besoins :
1. **Évaluation initiale** : Compétences actuelles vs cibles
2. **Gap analysis** : Écarts à combler
3. **Priorisation** : Compétences critiques first
4. **Dépendances** : Prérequis logiques

Plan de formation structuré :
**Phase 1 : Fondamentaux** (Semaines 1-4)
- Objectifs spécifiques
- Ressources recommandées
- Méthodes d'apprentissage
- Évaluations formatives

**Phase 2 : Application pratique** (Semaines 5-8)
- Projets concrets
- Mentorat suggéré
- Challenges techniques
- Feedback continu

**Phase 3 : Maîtrise avancée** (Semaines 9-12)
- Optimisation performance
- Innovation et créativité
- Leadership technique
- Certification préparée

Ressources recommandées :
- Cours en ligne : [PLATEFORMES_SPÉCIFIQUES]
- Livres : [RECOMMANDATIONS_LITTÉRAIRES]
- Communautés : [FORUMS_ET_GROUPES]
- Outils pratiques : [LOGICIELS_ET_OUTILS]

Métriques de succès :
- Acquisition compétences : % maîtrisées
- Application terrain : Projets réussis
- Évolution carrière : Objectifs atteints
- Satisfaction personnelle : Niveau engagement
```

---

## 🏥 SANTÉ & BIEN-ÊTRE

### 💊 Conseils nutrition personnalisés

**Prompt :**
```
Tu es un nutritionniste-diététicien certifié avec spécialisation en nutrigenétique. Élabore un plan nutritionnel personnalisé pour [PATIENT] basé sur [OBJECTIF_PRINCIPAL].

Profil patient :
- Âge : [ÂGE] ans
- Sexe : [SEXE]
- Taille/Poids : [TAILLE]cm / [POIDS]kg
- Activité physique : [NIVEAU_ACTIVITÉ]
- Restrictions alimentaires : [ALLERGIES_INTOLÉRANCES]
- Pathologies : [MALADIES_CHRONIQUES]
- Médicaments : [TRAITEMENTS_EN_COURS]

Analyse personnalisée :
1. **Besoins caloriques** : Calcul BMR/TDEE précis
2. **Macronutriments** : Ratio Protéines/Glucides/Lipides optimal
3. **Micronutriments** : Vitamines et minéraux prioritaires
4. **Hydratation** : Apports journaliers recommandés

Plan alimentaire structuré :
**Petit-déjeuner** : Options équilibrées et pratiques
**Déjeuner** : Repas principal complet
**Collation** : Snacks sains et énergisants
**Dîner** : Repas léger et récupérateur

Recommandations complémentaires :
- Suppléments nutritionnels si nécessaires
- Timing des repas optimisé
- Adaptation week-end et occasions spéciales
- Suivi et ajustements mensuels

Éducation nutritionnelle :
- Principes fondamentaux expliqués
- Lecture d'étiquettes alimentaires
- Cours de cuisine santé suggérés
- Applications mobiles recommandées

Métriques de suivi :
- Évolution poids : Courbe réaliste
- Bien-être général : Énergie, sommeil, digestion
- Biomarqueurs : Analyses sanguines si pertinent
- Adhérence : % respect du plan

Format : Plan complet + guide du patient + suivi proposé
```

---

### 🧘 Plan méditation personnalisé

**Prompt :**
```
Tu es un instructeur de méditation certifié et thérapeute mindfulness. Crée un programme de méditation personnalisé de 30 jours pour [UTILISATEUR] souhaitant [OBJECTIF_PRINCIPAL].

Profil utilisateur :
- Expérience méditation : [DÉBUTANT/INTERMÉDIAIRE/AVANCÉ]
- Temps disponible/jour : [DURÉE_SESSION]
- Moment préféré : [MATIN/SOIR/PAUSE_DÉJEUNER]
- Environnement : [DOMICILE/TRANSPORT/BUREAU]
- Défis personnels : [STRESS/ANXIÉTÉ/INSOMNIE/AUTRE]

Analyse des besoins :
1. **État actuel** : Niveau stress, concentration, bien-être
2. **Objectifs SMART** : Spécifiques, Mesurables, Atteignables
3. **Préférences** : Style méditation (guidée/silence/nature)
4. **Contraintes** : Adaptations nécessaires

Programme structuré :

**Semaine 1-2 : Fondation**
- Jour 1-7 : Méditations courtes (5-10 min) focus respiration
- Techniques : Body scan, respiration 4-7-8
- Objectif : Créer l'habitude quotidienne

**Semaine 3-4 : Approfondissement**
- Jour 8-14 : Sessions 15-20 min avec visualisation
- Techniques : Loving-kindness, méditation marchée
- Objectif : Explorer émotions et sensations

**Semaine 5-6 : Intégration**
- Jour 15-21 : Pratiques thématiques ciblées
- Techniques : Méditation compassion, pleine conscience
- Objectif : Appliquer dans la vie quotidienne

**Semaine 7-8 : Maîtrise**
- Jour 22-30 : Sessions avancées 20-30 min
- Techniques : Méditation insight, pratiques combinées
- Objectif : Autonomie et sagesse intérieure

Supports fournis :
- Scripts guidés pour chaque session
- Applications recommandées (Headspace, Insight Timer)
- Journal de pratique quotidien
- Ressources complémentaires (livres, podcasts)

Suivi et ajustements :
- Points de contrôle hebdomadaires
- Adaptation selon progression
- Support motivationnel
- Extension programme si souhaité

Format : Programme complet + audio scripts + tracking journal
```

---

## 🏠 VIE QUOTIDIENNE

### 🛒 Liste courses optimisée

**Prompt :**
```
Tu es un chef cuisinier professionnel et nutritionniste. Crée une liste de courses optimisée pour [NOMBRE_PERSONNES] personnes pendant [DURÉE_PÉRIODE] jours avec un budget de [BUDGET_MAXIMUM]€.

Préférences alimentaires :
- Régime alimentaire : [VÉGÉTARIEN/VÉGAN/SANS_GLUTEN/AUTRE]
- Allergies/intolérances : [LISTE_RESTRICTIONS]
- Cuisine préférée : [ITALIENNE/ASIATIQUE/MÉDITERRANÉENNE/AUTRE]
- Niveau cuisine : [DÉBUTANT/INTERMÉDIAIRE/AVANCÉ]

Contraintes pratiques :
- Magasins disponibles : [SUPERMARCHÉ/MARCHÉ_LOCAL/DRIVE]
- Équipement cuisine : [BASIQUE/ÉQUIPÉ_PROFESSIONNEL]
- Temps préparation : [RAPIDE/<30MIN/NORMAL]
- Saisonnalité : [RESPECTER_SAISON_OU_PAS]

Optimisations recherchées :
1. **Nutrition** : Équilibre protides/glucides/lipides
2. **Budget** : Maximiser valeur nutritionnelle/€
3. **Diversité** : Varier plaisirs et textures
4. **Durabilité** : Produits locaux et de saison
5. **Praticité** : Facilité de conservation et préparation

Structure de la liste :
**Fruits & Légumes** : Saisonniers et colorés
**Protéines** : Viande/poisson/œufs/légumineuses
**Féculents** : Variété céréales/pommes de terre
**Produits laitiers** : Fromage/lait/yaourts
**Épicerie** : Huiles/condiments/épices
**Autre** : Boissons/snacks/boissons

Repas planifiés suggérés :
- Petit-déjeuner variés
- Déjeuners équilibrés
- Dîners légers
- Collations saines

Astuces pratiques :
- Équivalences et substitutions
- Conservation optimale
- Préparation en batch
- Réduction gaspillage

Format : Liste détaillée + recettes suggérées + budget détaillé
```

---

### 📅 Planification événements

**Prompt :**
```
Tu es un wedding planner professionnel avec 15 ans d'expérience. Organise l'événement [TYPE_ÉVÉNEMENT - mariage/anniversaire/événement corporate] pour [NOMBRE_INVITÉS] personnes avec un budget de [BUDGET_TOTAL]€.

Contexte événement :
- Date souhaitée : [DATE_PRÉFÉRÉE]
- Lieu : [INTÉRIEUR/EXTÉRIEUR + LIEU_SPÉCIFIQUE]
- Style : [ÉLÉGANT/MODERNE/CASUAL/THÉMATIQUE]
- Contraintes spéciales : [ALLERGIES/DIÉTÉTIQUES/ACCESSIBILITÉ]

Budget détaillé :
- Lieu et décoration : [MONTANT]€
- Traiteur et boissons : [MONTANT]€
- Animation et musique : [MONTANT]€
- Communication : [MONTANT]€
- imprévus (10%) : [MONTANT]€

Planning opérationnel :
**J-90** : Réservations fournisseurs, save-the-date
**J-60** : Confirmation invités, menu définitif
**J-30** : Timeline détaillée, décoration finalisée
**J-7** : Confirmations dernières minutes
**Jour J** : Coordination logistique

Fournisseurs recommandés :
- Lieu : [SUGGESTIONS_PAR_BUDGET]
- Traiteur : [OPTIONS_GASTRONOMIQUES]
- Photographe : [STYLES_PHOTOGRAPHIQUES]
- DJ/Animation : [AMBIANCES_MUSICALES]

Timeline événement :
- 15h : Accueil invités
- 16h : Cérémonie/animation d'ouverture
- 18h : Cocktail et networking
- 19h30 : Dîner officiel
- 22h : Soirée dansante
- 01h : Fin de soirée

Plans de secours :
- Météo défavorable
- Indisponibilité fournisseur
- Nombre d'invités différent
- Problèmes techniques

Format : Plan d'organisation complet + budget détaillé + contacts fournisseurs
```

---

## 💡 PROMPTS POWER-UPS (Techniques avancées)

### 🔄 Prompt itératif auto-améliorant

**Prompt :**
```
Tu es un prompt engineer expert. Améliore itérativement ce prompt initial jusqu'à atteindre l'excellence :

PROMPT INITIAL :
"[COLLER_LE_PROMPT_À_AMÉLIORER]"

CONTEXTE D'USAGE :
- Tâche cible : [OBJECTIF_PRINCIPAL]
- Audience : [PROFILS_UTILISATEURS]
- Contraintes : [LIMITATIONS_SPÉCIFIQUES]

ANALYSE INITIALE :
1. Identifier les faiblesses du prompt actuel
2. Évaluer la clarté des instructions
3. Vérifier la complétude des spécifications
4. Tester la robustesse face aux variations

ITÉRATION 1 : Amélioration structurelle
- Ajouter rôle spécifique et expertise
- Clarifier format de sortie attendu
- Inclure exemples concrets
- Définir contraintes explicites

ITÉRATION 2 : Optimisation contextuelle
- Enrichir le contexte fourni
- Ajouter variables personnalisables
- Inclure critères d'évaluation
- Prévoir cas limites

ITÉRATION 3 : Perfectionnement avancé
- Intégrer techniques psychologiques
- Optimiser pour engagement utilisateur
- Ajouter métriques de succès
- Prévoir itérations futures

VALIDATION FINALE :
- Test sur cas d'usage réels
- Comparaison avec benchmarks
- Mesure amélioration performance
- Documentation pour reproductibilité

Format : Prompt optimisé + explication améliorations + métriques attendues
```

---

### 🎭 Prompt persona multiple

**Prompt :**
```
Tu es simultanément [PERSONA_1], [PERSONA_2], et [PERSONA_3] - trois experts complémentaires travaillant en équipe pour résoudre [PROBLÈME_COMPLEXE].

**Persona 1 : [RÔLE_STRATÉGIQUE]**
- Expertise : [DOMAINE_SPÉCIALISÉ]
- Approche : [MÉTHODOLOGIE_PRINCIPALE]
- Points forts : [FORCES_ANALYTIQUES]

**Persona 2 : [RÔLE_OPÉRATIONNEL]**
- Expertise : [DOMAINE_PRATIQUE]
- Approche : [MÉTHODOLOGIE_CONCRÈTE]
- Points forts : [FORCES_EXÉCUTION]

**Persona 3 : [RÔLE_CRITIQUE]**
- Expertise : [DOMAINE_ÉVALUATION]
- Approche : [MÉTHODOLOGIE_RIGOUROUSE]
- Points forts : [FORCES_VALIDATION]

PROBLÉMATIQUE À RÉSOUDRE :
[DESCRIPTION_DÉTAILLÉE_DU_DÉFI]

PROCESSUS COLLABORATIF :
1. **Phase diagnostic** : Chaque persona analyse indépendamment
2. **Phase synthèse** : Identification consensus et divergences
3. **Phase recommandation** : Proposition solution intégrative
4. **Phase validation** : Test robustesse et faisabilité

FORMAT DE RÉPONSE :
- Analyse de chaque persona (séparément)
- Points d'accord et de désaccord
- Solution recommandée avec justification
- Plan d'implémentation pratique
- Métriques de succès proposées
```

---

### 📊 Prompt analyse comparative

**Prompt :**
```
Tu es un analyste comparatif expert. Compare objectivement [OPTION_A] vs [OPTION_B] dans le contexte de [USAGE_SPÉCIFIQUE].

CRITÈRES D'ANALYSE SYSTÉMATIQUES :

**1. Performance quantitative**
- Métriques mesurables : [KPIS_SPÉCIFIQUES]
- Benchmarks établis : [STANDARDS_INDUSTRIE]
- Évolutivité : [CAPACITÉ_À_GRANDIR]
- Coûts opérationnels : [ÉCONOMIE_RÉALISÉE]

**2. Qualité et fiabilité**
- Robustesse technique : [STABILITÉ_SYSTÈME]
- Qualité des outputs : [PRÉCISION_RÉSULTATS]
- Gestion d'erreurs : [RÉSILIENCE_PANNE]
- Maintenance requise : [EFFORT_SUPPORT]

**3. Expérience utilisateur**
- Facilité d'adoption : [COURBE_APPRENTISSAGE]
- Interface utilisateur : [ERGONOMIE_GÉNÉRALE]
- Personnalisation : [ADAPTATION_BESOINS]
- Support disponible : [QUALITÉ_ASSISTANCE]

**4. Avantages concurrentiels**
- Innovation technologique : [DIFFÉRENCIATEURS]
- Écosystème partenaire : [INTÉGRATIONS_DISPONIBLES]
- Roadmap produit : [VISION_FUTURE]
- Adoption marché : [PARTS_DE_MARCHÉ]

**5. Analyse coûts-bénéfices**
- ROI projet : [CALCUL_ÉCONOMIQUE]
- Time-to-value : [DÉLAI_RENTAABILITÉ]
- Risques identifiés : [FACTEURS_INCERTITUDE]
- Recommandation finale : [CHOIX_OPTIMAL]

FORMAT DE PRÉSENTATION :
- Matrice comparative détaillée
- Analyse SWOT pour chaque option
- Recommandation argumentée
- Plan de transition si applicable
```

---

## 🔧 Checklist d'utilisation

### ✅ Avant d'utiliser un prompt :
- [ ] Adapter les variables [ENTRE_PARENTHESES]
- [ ] Vérifier la cohérence avec votre contexte
- [ ] Tester sur un cas simple d'abord
- [ ] Préparer les informations nécessaires

### ✅ Pendant l'utilisation :
- [ ] Fournir suffisamment de contexte
- [ ] Être spécifique dans les demandes
- [ ] Indiquer le format souhaité
- [ ] Prévoir les contraintes importantes

### ✅ Après l'utilisation :
- [ ] Évaluer la qualité de la réponse
- [ ] Noter les points d'amélioration
- [ ] Ajuster le prompt pour la prochaine fois
- [ ] Sauvegarder les prompts qui fonctionnent

---

## 🎯 Conseils pour créer vos propres prompts

### Structure optimale :
1. **Rôle** : Définir l'expertise requise
2. **Tâche** : Décrire précisément l'objectif
3. **Contexte** : Fournir les informations pertinentes
4. **Contraintes** : Spécifier les limitations
5. **Format** : Indiquer la structure attendue

### Techniques avancées :
- **Few-shot** : Inclure 1-3 exemples
- **Chain of thought** : Demander le raisonnement étape par étape
- **Personas multiples** : Différentes perspectives
- **Variables dynamiques** : Adapter au contexte

### Optimisation continue :
- **Test A/B** : Comparer différentes versions
- **Métriques** : Mesurer la performance
- **Feedback** : Apprendre des résultats
- **Itération** : Améliorer progressivement

---

*Collection de prompts concrets mise à jour régulièrement. N'hésitez pas à les adapter à vos besoins spécifiques !*
