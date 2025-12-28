Faciliter la première session d'une étude d'opportunité pour cadrer le projet, analyser l'état actuel du processus, et identifier les 6 problèmes majeurs bloquants avec validation collective des participants.

## When to Use

- Démarrage d'une étude d'opportunité suite à une expression de besoin
- Besoin de cadrer un projet complexe impliquant plusieurs squads et produits
- Phase de découverte avant conception d'une transformation métier
- Alignement nécessaire entre MOA déléguée (experts PU), Product Owners, et parties prenantes techniques
- Workshop de cadrage hybride (présentiel/distanciel) avec 10-20 participants

## Context Validation Checkpoints

* [ ] Avons-nous tous les acteurs clés présents : porteur du besoin (expert PU ou PO), POs des produits impactés, architectes, et potentiellement directeur de programme ?
* [ ] Le processus actuel est-il documenté ou au moins connu des participants ?
* [ ] Disposons nous des données de volumétrie  ?
* [ ] L'environnement hybride des ateliers est-il configuré (Miro/Visio accessible en ligne, caméra/micro testés) ?
* [ ] Le temps alloué (6h) est-il confirmé avec tous les participants ?

## Recipe Steps

### Step 1: Welcome & Setup (30min)

Accueillir les participants, présenter les objectifs de l'étude d'opportunité et l'agenda de la journée. Expliquer le format hybride et les règles d'engagement (temps de parole, parking lot, validation collective). Faire un tour de table pour identifier les rôles et attentes de chacun.

```markdown
📋 Agenda Session 1
• Welcome & Introductions (30min)
• Business Context Analysis (2h30)
• Scope & Boundaries (1h)
• Problem Identification (1h30)
• Wrap-up & Validation (30min)

🎯 Objectifs
- Cadrer le projet
- Analyser l'état actuel (volumétrie, acteurs, flux)
- Identifier 6 problèmes majeurs
```

### Step 2: Business Context Analysis (2h30)

Faciliter l'analyse de l'état actuel du processus métier. Utiliser Miro, Visio ou papier pour créer un Swimlane Diagram montrant les acteurs, les étapes, les flux de données et les volumes. Poser des questions ouvertes pour faire émerger les irritants et les inefficacités. Documenter la volumétrie.

```markdown
🏊 Swimlane Diagram Template
┌─────────────┬──────────────┬──────────────┐
│ Acteur 1                   │ Acteur 2                    │ Acteur 3                    │
├─────────────┼──────────────┼──────────────┤
│ [Étape 1]                 │                                   │                                   │
│      ↓                        │                                   │                                   │
│ [Étape 2]      →       │  [Étape 3]                  │                                   │
│                                 │            ↓                    │                                   │
│                                 │      [Étape 4]         ───→ [Étape 5]              │
└─────────────┴──────────────┴──────────────┘

📊 Volumétrie à capturer
- Nombre d'utilisateurs/mois
- Temps moyen par étape
- Taux d'erreur/reprise
```

### Step 3: Scope & Boundaries (1h)

Délimiter clairement le périmètre de l'étude : quels produits sont impactés, quels processus sont inclus/exclus, quelles contraintes réglementaires s'appliquent. Identifier les dépendances avec d'autres initiatives en cours. Documenter les hypothèses et les non-goals explicitement.

```markdown
✅ In Scope
- Processus X, Y, Z
- Produits A, B impactés
- Actes métier prioritaires

❌ Out of Scope
- Migration infrastructure
- Refonte UI complète
- Processus connexe W

🚧 Contraintes
- Réglementaire: échéances
- Technique: compatibilité SI existant
- Budget: enveloppe prévisionnelle
```

### Step 4: Problem Identification (1h30)

Animer un brainstorming pour identifier tous les problèmes du processus actuel. Utiliser la technique des 5 Whys pour creuser les causes racines. Regrouper les problèmes similaires. Faire voter les participants pour sélectionner les 6 problèmes majeurs les plus bloquants. Documenter chaque problème avec son impact business.

```markdown
🎯 Template Problème
**P1: [Titre du problème]**
- Impact: [Métier/Opérationnel/Financier]
- Fréquence: [Quotidien/Hebdo/Mensuel]
- Acteurs concernés: [Liste]
- Symptômes: [Description]
- Cause racine (5 Whys): [...]  

Répéter pour P2, P3, P4, P5, P6
```

### Step 5: Validation Collective & Wrap-up (30min)

Faire valider les 6 problèmes identifiés par l'ensemble des participants. Vérifier que le Swimlane Diagram est compris par tous. Confirmer la volumétrie et le périmètre. Recueillir les feedbacks sur le format et le déroulement. Présenter l'agenda de la Session 2 (Opportunity & Strategy). Documenter les parking lot items pour traitement ultérieur.

```markdown
✅ Checklist Validation Session 1
□ Swimlane Diagram validé par tous
□ Volumétrie confirmée 
□ 6 problèmes validés collectivement
□ Périmètre et contraintes documentés
□ Parking lot items capturés
□ Prochaine session planifiée

📤 Livrables à partager
- Swimlane Diagram (Miro/Visio export)
- Liste des 6 problèmes détaillés
- Notes de périmètre et contraintes
```