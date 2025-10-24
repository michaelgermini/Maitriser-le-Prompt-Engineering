# Chapitre 5 : Techniques de contrôle du style et du ton

## Ajuster le style (formel, créatif, humoristique…)

### Les dimensions du style

Le style d'un texte généré par IA peut être contrôlé à travers quatre dimensions principales :

#### 1. **Niveau de formalité**
Échelle allant du langage familier au discours académique.

#### 2. **Degré de créativité**
Du factuel et direct au poétique et imaginatif.

#### 3. **Complexité linguistique**
Du vocabulaire simple aux termes techniques spécialisés.

#### 4. **Ton émotionnel**
De l'objectif neutre à l'enthousiaste ou critique.

---

> **💡 Conseil** : Spécifiez toujours le style souhaité explicitement dans votre prompt pour éviter les surprises.

---

### Techniques de contrôle du style

#### 1. **Spécification directe**
```
Écris un article sur l'environnement avec un style [ADJECTIF].
```
- Journalistique
- Académique
- Conversationnel
- Poétique

#### 2. **Exemples de référence**
```
Voici un exemple du style souhaité :
[EXTRAIT_STYLISTIQUE]

Maintenant, écris [TÂCHE] dans le même style.
```

#### 3. **Contraintes stylistiques**
```
Utilise :
- Vocabulaire de niveau [NIVEAU]
- Phrases de longueur [LONGUEUR]
- Structures [TYPE] (actives/passives)
- Ton [DESCRIPTEUR]
```

### Matrice des styles

| Style | Formalité | Créativité | Complexité | Ton typique |
|-------|-----------|------------|------------|-------------|
| **Académique** | ⭐⭐⭐⭐⭐ | ⭐⭐ | ⭐⭐⭐⭐⭐ | Objectif, précis |
| **Journalistique** | ⭐⭐⭐⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐ | Factuel, engageant |
| **Commercial** | ⭐⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐ | Persuasif, positif |
| **Conversationnel** | ⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐ | Amical, accessible |
| **Technique** | ⭐⭐⭐⭐ | ⭐ | ⭐⭐⭐⭐⭐ | Précis, neutre |
| **Créatif** | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | Original, expressif |
| **Humoristique** | ⭐⭐ | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ | Léger, ironique |

### Exemples pratiques par style

#### Style académique
**Prompt :**
```
Tu es un professeur d'université. Écris une analyse critique de l'impact des réseaux sociaux sur la santé mentale des adolescents. Utilise un style académique avec citations théoriques, structure argumentative et conclusion nuancée. Cite au moins 3 études scientifiques récentes.
```

#### Style journalistique
**Prompt :**
```
En tant que journaliste d'investigation pour un grand quotidien, rédige un article de 800 mots sur la montée de l'IA dans les PME françaises. Style : factuel mais engageant, avec témoignages d'entrepreneurs, données chiffrées, et analyse des tendances. Structure pyramidale inversée.
```

#### Style commercial
**Prompt :**
```
Tu es un copywriter professionnel. Crée une page de vente pour un logiciel de gestion de projet. Ton : persuasif et confiant. Mets en avant les bénéfices clients, utilise des chiffres convaincants, crée l'urgence d'agir. Termine par un call-to-action fort.
```

#### Style conversationnel
**Prompt :**
```
Imagine que tu es mon ami expert en cuisine. Explique-moi comment réussir une pâte à crêpes parfaite. Style : amical et encourageant, comme si on discutait autour d'un café. Utilise des expressions familières et des anecdotes personnelles.
```

#### Style humoristique
**Prompt :**
```
Tu es un comédien stand-up. Fais un sketch de 3 minutes sur les difficultés d'utiliser l'IA au quotidien. Style : humoristique et absurde, avec des jeux de mots, de l'exagération, et une chute inattendue. Format : script de spectacle avec didascalies.
```

---

> **⚠️ Attention** : Un style trop spécifique peut limiter la créativité du modèle. Trouvez le bon équilibre entre contrainte et liberté.

---

## Maintenir la cohérence sur plusieurs réponses

### Le défi de la cohérence

Les LLM génèrent chaque réponse indépendamment, ce qui peut créer des incohérences lorsqu'une conversation se déroule sur plusieurs échanges.

### Techniques de maintien de cohérence

#### 1. **Contexte accumulé**
Incluez l'historique pertinent dans chaque prompt.

```
Historique de la conversation :
- Utilisateur : Je veux créer une application de recettes
- IA : Excellente idée ! Quel type de recettes ?

Maintenant, en tant qu'expert en développement mobile, propose une architecture technique pour cette app de recettes. Considère que l'utilisateur est débutant en programmation.
```

#### 2. **Variables de cohérence**
Définissez des variables qui doivent rester constantes.

```
PARAMÈTRES FIXES pour cette session :
- Public cible : Adolescents 13-17 ans
- Ton : Amical et pédagogique
- Niveau de langage : Accessible, éviter le jargon
- Longueur des réponses : 200-300 mots

Question de l'utilisateur : [QUESTION]
```

#### 3. **Personnage persistant**
Créez un personnage avec des traits constants.

```
Tu incarnes Marie Dubois, consultante en marketing digital depuis 15 ans. Tu as toujours :
- Un style direct et pragmatique
- Une préférence pour les stratégies data-driven
- Une aversion pour les "buzz words" marketing vides
- Une passion pour les études de cas concrets

Client : J'ai besoin d'une stratégie pour lancer mon produit.
Marie : Commençons par les données. Quel est votre marché cible exact ?
```

### Outils de cohérence

#### 1. **Prompts système persistants**
Utilisez le paramètre "system" dans les APIs pour définir un contexte permanent.

```python
messages = [
    {"role": "system", "content": "Tu es un coach sportif motivant spécialisé en running. Ton style est encourageant, scientifique mais accessible, et toujours positif."},
    {"role": "user", "content": "Je commence le running, par quoi commencer ?"}
]
```

#### 2. **Templates de réponse**
Définissez un format constant pour toutes les réponses.

```
FORMAT CONSTANT pour toutes les réponses :
1. **Accusé de réception** : Reformule la question pour confirmer compréhension
2. **Réponse principale** : Contenu demandé
3. **Recommandations** : 2-3 actions concrètes
4. **Question de suivi** : Pour approfondir la discussion

Question : [QUESTION_UTILISATEUR]
```

#### 3. **Mémorisation factuelle**
Créez une "mémoire" des faits importants.

```
FAITS ÉTABLIS dans cette conversation :
- L'utilisateur s'appelle Thomas
- Il travaille dans l'éducation
- Son budget projet est de 50K€
- La deadline est fin mars
- Il préfère les solutions open-source

Question : Quelle technologie recommandes-tu pour la base de données ?
```

### Gestion des incohérences

#### Détection d'incohérences
- **Contradictions factuelles** : Vérifiez les données précédentes
- **Changements de ton** : Assurez la stabilité stylistique
- **Évolution du contexte** : Adaptez sans perdre la continuité

#### Correction proactive
```
Avant de répondre, vérifie :
- Cohérence avec les informations précédentes
- Respect du ton établi
- Alignement avec les objectifs initiaux
- Mise à jour des contraintes si nécessaire
```

## Exemples pratiques

### Exemple 1 : Cohérence dans un tutoriel

**Contexte initial :**
```
Tu es un professeur de mathématiques pour lycée. Explique les fonctions quadratiques de manière progressive et interactive.
```

**Réponses successives :**
1. **Introduction** : "Bonjour ! Aujourd'hui nous allons découvrir les fonctions quadratiques..."
2. **Concept de base** : "Une fonction quadratique s'écrit f(x) = ax² + bx + c..."
3. **Exemple pratique** : "Prenons f(x) = x² + 2x - 3..."
4. **Application** : "Maintenant, appliquons cela à un problème concret..."

### Exemple 2 : Personnage cohérent dans une histoire

**Setup initial :**
```
Tu incarnes Élodie, une détective privée parisienne des années 1950. Tu es :
- Cynique mais juste
- Fumeuse de Gauloises
- Experte en arts martiaux
- Toujours habillée en tailleur Chanel
- Utilise un argot parisien daté mais compréhensible
```

**Interactions cohérentes :**
- **Client** : "J'ai perdu mon chat."
- **Élodie** : "Un chat perdu ? Pas vraiment dans mes cordes d'habitude, mais bon... Racontez-moi tout, et pas de cachotteries !"

- **Client** : "Il s'appelle Mistigri."
- **Élodie** : "Mistigri, hein ? Original. Vous l'avez vu pour la dernière fois où ?"

### Exemple 3 : Cohérence technique dans le développement

**Contexte projet :**
```
PROJET : Application e-commerce
STACK : React, Node.js, MongoDB
CONTRAINTES : Budget limité, équipe de 3 devs, deadline 3 mois
APPROCHE : MVP d'abord, puis itérations
```

**Prompts successifs maintiennent la cohérence :**
1. **Architecture** : "Propose l'architecture technique..."
2. **Base de données** : "Maintenant, le schéma de base de données..."
3. **API** : "Les endpoints de l'API REST..."
4. **Frontend** : "L'interface utilisateur..."

## Techniques avancées de contrôle stylistique

### 1. **Calibration par exemples**

#### Few-shot styling
```
Voici des exemples de mon style d'écriture :

Exemple 1 - Description technique :
"La fonction parseJSON() prend en entrée une chaîne de caractères au format JSON et retourne l'objet JavaScript correspondant, en gérant élégamment les erreurs de syntaxe."

Exemple 2 - Explication pédagogique :
"Imaginez que votre ordinateur est comme une cuisine : la RAM est le plan de travail où vous préparez vos ingrédients, tandis que le disque dur est le réfrigérateur où vous les stockez."

Maintenant, explique le concept de closure en JavaScript.
```

### 2. **Contraintes métriques**

#### Contrôle de la complexité
```
Écris un article avec ces métriques stylistiques :
- Niveau de lecture : CE2 (8-9 ans)
- Longueur moyenne des phrases : 12-15 mots
- Vocabulaire : 1500 mots les plus fréquents du français
- Ton : Enthousiaste et encourageant
```

#### Analyse automatique possible
- **Score Flesch** : Mesure de lisibilité
- **Indice Gulpease** : Adapté au français
- **Fréquence des mots** : Contrôle du vocabulaire

### 3. **Style adaptatif conditionnel**

```
Adapte ton style selon le contexte :

Si la question est simple :
- Style direct et concis
- Réponse en 2-3 phrases
- Vocabulaire courant

Si la question est complexe :
- Style structuré avec sections
- Exemples détaillés
- Explications progressives

Si c'est une erreur ou problème :
- Ton rassurant et solution-oriented
- Pas de blame, focus sur la résolution
- Étapes claires et numérotées

Question de l'utilisateur : [QUESTION]
```

## Exercices pratiques

### Exercice 1 : Transformation stylistique

**Mission :** Transformez un texte neutre en 4 styles différents.

**Texte de base :**
"L'intelligence artificielle est une technologie qui permet aux machines d'apprendre et de résoudre des problèmes complexes."

**Styles à appliquer :**
1. Style académique (thèse universitaire)
2. Style commercial (argument de vente)
3. Style humoristique (sketch comique)
4. Style poétique (haïku moderne)

### Exercice 2 : Cohérence conversationnelle

**Challenge :** Maintenez la cohérence dans une conversation de 5 échanges.

**Rôle :** Coach de vie professionnel
**Contexte :** Aider un client à changer d'emploi

**Échanges à générer :**
1. Introduction et première question
2. Analyse de la situation actuelle
3. Exploration des motivations
4. Proposition d'actions concrètes
5. Plan de suivi

### Exercice 3 : Création de personnage cohérent

**Mission :** Créez un personnage IA avec des traits distinctifs et générez une conversation cohérente.

**Éléments à définir :**
- **Background** : Profession, âge, origines
- **Personnalité** : Traits de caractère principaux
- **Style de communication** : Vocabulaire, expressions favorites
- **Domaines d'expertise** : Sujets maîtrisés
- **Limites** : Sujets à éviter ou gérer délicatement

### Exercice 4 : Calibration stylistique

**Expérience :** Testez l'impact des spécifications stylistiques sur la même tâche.

**Tâche :** Rédiger une critique de film

**Variables à tester :**
1. **Spécifications minimales** : "Fais une critique du film X"
2. **Spécifications détaillées** : Ton, longueur, aspects à couvrir
3. **Exemples fournis** : 2-3 exemples de critiques
4. **Métriques précises** : Score de lisibilité, nombre d'adjectifs, etc.

**Analyse :** Comparez les résultats et identifiez les facteurs les plus influents.

---

## Évaluation du chapitre

**Maîtrise du contrôle stylistique :**

**Styles de base :**
- [ ] 5 styles principaux maîtrisés
- [ ] Adaptation contextuelle réussie
- [ ] Exemples personnels créés

**Cohérence :**
- [ ] Techniques de maintien appliquées
- [ ] Gestion des conversations longues
- [ ] Personnages consistants développés

**Techniques avancées :**
- [ ] Calibration par exemples
- [ ] Contraintes métriques utilisées
- [ ] Style adaptatif implémenté

**Score global :** _____/20

**Portfolio stylistique :**
- [ ] 3 personnages originaux créés
- [ ] 5 exemples de transformations stylistiques
- [ ] 2 conversations cohérentes développées

**Application pratique :** Créez un assistant IA stylisé pour votre domaine professionnel.
