# Session 1 : Opening & Business Context
## Étude d'Opportunité : Dossier de Pièces Justificatives (DPJ)

**Date** : 22 décembre 2024  
**Durée** : 6 heures  
**Participants** : Squad Acquisition, PU (Pôle Utilisateur), Architectes  
**Facilitateur** : Claude (Packmind)  
**Version** : 1.0

---

## Table des matières

1. [Checklist de validation](#checklist-validation)
2. [Volumétrie DPJ](#volumétrie-dpj)
3. [Swimlane Diagram - Processus As-Is](#swimlane-diagram)
4. [Scope & Boundaries](#scope-boundaries)
5. [Les 6 Problèmes Majeurs](#6-problèmes-majeurs)
6. [Livrables Session 1](#livrables-session-1)
7. [Prochaine Session](#prochaine-session)

---

## <a name="checklist-validation"></a>✅ Checklist Validation Session 1

- [x] Swimlane Diagram validé par tous
- [x] Volumétrie confirmée (10/10 questions répondues)
- [x] 6 problèmes validés collectivement
- [x] Périmètre et contraintes documentés
- [x] Parking lot items capturés
- [x] Prochaine session planifiée (Session 2 : Opportunity & Strategy)

**✅ Session 1 validée collectivement**

---

## <a name="volumétrie-dpj"></a>📊 1. Volumétrie DPJ

### Synthèse des indicateurs clés

| Indicateur | Valeur | Impact Business |
|------------|--------|-----------------|
| **Dossiers créés/mois** | 150 000 | 🔴 Volume critique |
| **Documents/dossier (moyenne)** | 6 | **Total : 900 000 documents/mois** |
| **Types d'actes bancaires** | 200 | 🟠 Complexité élevée |
| **Répartition clients** | 80% PP / 20% PM | Focus Personnes Physiques |
| **Validation manuelle** | 99% | 🔴 **Charge conseillers massive** |
| **Validation automatique (RAD/LAD)** | 1% | 🟢 **Potentiel d'amélioration énorme** |
| **Taux de rejet documents** | 20% | 🔴 **450 000 documents rejetés/mois** |
| **Taux de certification** | 25% | 🔴 **Très faible** |
| **Taux de reproposabilité (objectif)** | 20% | 🟢 **337 500 documents réutilisables/mois** |
| **Nombre de conseillers** | 40 000 | Adoption critique |
| **Base clients** | 21 000 000 | Base massive |

### 🚨 Chiffres clés alarmants

- **2,25 millions de documents/mois** à traiter
- **99% de validation manuelle** = goulot d'étranglement conseillers
- **450 000 documents rejetés/mois** (20%) = irritant client majeur + risque conformité
- **Taux de certification 25%** = risques d'amendes réglementaires
- **Temps très variable** (minutes → 6 mois selon actes) = besoin de pilotage

---

## <a name="swimlane-diagram"></a>🏊 2. Swimlane Diagram - Processus As-Is

### Vue d'ensemble du processus DPJ

┌────────────────┬────────────────┬────────────────┬────────────────┬────────────────┬────────────────┐ │ PARCOURS │ SYSTÈME DPJ │ GED CATS │ STOCKAGE │ CLIENT │ CONSEILLER │ │ PRODUIT │ │ │ DOCUMENTS │ │ AGENCE │ ├────────────────┼────────────────┼────────────────┼────────────────┼────────────────┼────────────────┤ │ [Création acte │ │ │ │ │ │ │ bancaire] │ │ │ │ │ │ │ ↓ │ │ │ │ │ │ │ [Définition │ │ │ │ │ │ │ liste docs │ │ │ │ │ │ │ avec règles │ │ │ │ │ │ │ ET/OU] │ │ │ │ │ │ │ ↓ │ │ │ │ │ │ │ [Création │ │ │ │ │ │ │ dossier]──────┼───────────────→│ │ │ │ │ │ │ [Dossier créé] │ │ │ │ │ │ │ ↓ │ │ │ │ │ │ │ [REPROPOSABI- │ │ │ │ │ │ │ LITÉ] │ │ │ │ │ │ │ │ │ │ │ │ │ │ │ ├────────┼───────────────→│ │ │ │ │ │ │ │ [Recherche docs│ │ │ │ │ │ │ │ client valides│ │ │ │ │ │ │ │ en GED] │ │ │ │ │ │ │ │ │ │ │ │ │ │ │ ├────────┼────────────────┼───────────────→│ │ │ │ │ │ │ │ [Recherche docs│ │ │ │ │ │ │ │ en attente │ │ │ │ │ │ │ │ GED] │ │ │ │ │ │ │ │ │ │ │ │ │ │ │←───────┼────────────────┼────────┘ │ │ │ │ │ [Docs repro- │ │ │ │ │ │ │ posés trouvés]│ │ │ │ │ │ │ ↓ │ │ │ │ │ │ │ [Notification │ │ │ │ │ │ │ client] │ │ │ │ │ │ │ │────────┼────────────────┼────────────────┼───────────────→│ │ │ │ │ │ │ [Consultation │ │ │ │ │ │ │ liste docs │ │ │ │ │ │ │ manquants] │ │ │ │ │ │ │ ↓ │ │ │ │ │ │ │ [Dépôt docs] │ │ │ │ │ │ │ • Portail │ │ │ │ │ │ │ • App mobile │ │ │ │ │ │ │ • En agence │ │ │ │ │ │ │ │ │ │ │ │ [Stockage]←────┼────────────────┼────────────────┼───────┘ │ │ │ │ ↓ │ │ │ │ │ │ │ [Statut: │ │ │ │ │ │ │ Déposé] │ │ │ │ │ │ │ │ │ │ │ │ │ │ │ ├────────┼────────────────┼────────────────┼────────────────┼───────────────→│ │ │ │ │ │ │ │ [Consultation │ │ │ │ │ │ │ │ dossier + │ │ │ │ │ │ │ │ docs repro- │ │ │ │ │ │ │ │ posés] │ │ │ │ │ │ │ │ ↓ │ │ │ │ │ │ │ │ [Validation │ │ │ │ │ │ │ │ docs repro- │ │ │ │ │ │ │ │ posés] │ │ │ │ │ │ │ │ ↓ │ │ │ │ │ │ │ │ [Validation │ │ │ │ │ │ │ │ docs déposés] │ │ │ │ │ │ │ │ │ │ │ │ ├────────┴────────────────┴────────────────┴────────────────┴────────┘ │ │ │ ↓ │ │ │ [RAD/LAD si type doc compatible] │ │ │ │ │ │ │ ├──→ [Reconnaissance type document] │ │ │ │ │ │ │ ├──→ [Extraction données (LAD)] │ │ │ │ │ │ │ └──→ [Comparaison données parcours] │ │ │ ↓ │ │ │ [Si OK: Validation auto] │ │ │ [Si KO: Statut Rejeté] │ │ │ ↓ │ │ │ [Statut: Validé] │ │ │ ↓ │ │ │ [Transfert GED CATS] │ │ │ ↓ │ │ │ [Statut: En GED] │ └────────────────┴──────────────────────────────────────────────────────────────────────────────────┘


### Workflow des statuts documents

Déposé → (Issue reproposabilité) → En traitement → Validé/Rejeté → En GED


### Points clés du processus

- **Reproposabilité** : Recherche automatique dans GED CATS + Documents en attente AVANT notification client
- **Validation manuelle** : Conseiller valide docs reproposés + docs déposés (invisible au client)
- **Validation automatique** : RAD/LAD si type document compatible (reconnaissance + extraction + comparaison)
- **Deux chemins possibles** : Validation conseiller OU validation automatique RAD/LAD

---

## <a name="scope-boundaries"></a>✅ 3. Scope & Boundaries

### In Scope (Périmètre INCLUS)

**Processus :**
- Recueil de pièces justificatives pour **200 types d'actes bancaires**
- Processus KYC (Know Your Customer)
- Workflow de validation documents (manuel + automatique RAD/LAD)
- **Reproposabilité des documents** (GED CATS + Documents en attente)
- Transfert vers GED métier CATS

**Utilisateurs/Acteurs :**
- Parcours produits (créateurs de dossiers)
- **Clients Personnes Physiques (80%)** et Personnes Morales (20%)
  - EI, PME, Entreprises, Grandes Entreprises
- **40 000 conseillers** en agence
- Systèmes RAD/LAD/GED CATS

**Canaux de dépôt :**
- Portail client (selfcare)
- Application mobile
- En agence avec conseiller

**Fonctionnalités principales :**
- Définition documents attendus avec **règles ET/OU**
- Affichage documents requis (multi-canal)
- Dépôt documents (multi-canal)
- Validation manuelle par conseiller
- Validation automatique par RAD/LAD
- **Reproposabilité documents** (objectif : 20% des docs)
- Workflow statuts : Déposé → (Reproposé) → En traitement → Validé/Rejeté → En GED
- Transfert GED CATS

---

### Out of Scope (Périmètre EXCLU)

- ❌ **Refonte du socle GED** (dépendance externe)
- ❌ **Refonte du socle RAD/LAD** (dépendance externe)
- ❌ **Évolutions du paramétrage des types de documents**

**Note** : Ces sujets sont **en dépendance** du Dossier de PJ mais hors périmètre de cette étude.

---

### Contraintes

#### Réglementaires
- 🔴 **RGPD** : Validation automatique + réutilisation documents
- 🔴 **Conformité juridique** : Validation automatique des documents (études à mener)

#### Planning
- 🔴 **6 mois** : PMV imposé par **Programme 15C** (deadline critique)
- 🟠 **12 mois** : Produit complet avec RAD/LAD + Intégration Parcours Crédits Habitat
- 🟠 **Début 2027** : Décommissionnement DNC (migration obligatoire)

#### Budget
- ⚠️ **À estimer en fin de cadrage** (selon complexité fonctionnelle et architecture)

#### Dépendances critiques

| Dépendance | Impact | Maîtrise |
|------------|--------|----------|
| **Programme 15C** | PMV 6 mois obligatoire | ❌ Contrainte externe |
| **Refonte GED** | Fonctionnalités restreintes si non livrée | ❌ Hors Squad Acquisition |
| **Refonte RAD/LAD** | Validation manuelle uniquement (99%) | ❌ Hors Squad Acquisition |
| **Migration DNC** | 200 parcours à accompagner avant 2027 | ✅ Squad Acquisition |

---

## <a name="6-problèmes-majeurs"></a>🎯 4. Les 6 Problèmes Majeurs

### P1 : Surcharge validation manuelle conseillers

**Impact** : Opérationnel / Financier  
**Fréquence** : Quotidien  
**Acteurs concernés** : 40 000 conseillers

**Symptômes :**
- 99% de validation manuelle
- 2,25 millions de documents/mois à traiter manuellement
- Surcharge de travail conseillers
- Goulot d'étranglement opérationnel

**Analyse des causes racines (5 Whys) :**
1. Pourquoi 99% manuel ? → RAD/LAD sous-utilisé (1% seulement)
2. Pourquoi RAD/LAD sous-utilisé ? → Restrictions juridiques limitant la validation automatique
3. Pourquoi restrictions juridiques ? → Conformité juridique non validée pour validation auto
4. Pourquoi non validée ? → Études juridiques non menées
5. **Cause racine** : **Absence d'études juridiques pour lever les restrictions et permettre l'automatisation**

---

### P2 : Taux de certification documents très faible (25%)

**Impact** : Métier / Réglementaire / Financier  
**Fréquence** : Quotidien  
**Acteurs concernés** : Clients + Conseillers + Direction des Risques

**Symptômes :**
- 20% de taux de rejet documents (450 000 documents rejetés/mois)
- Seulement 25% de taux de certification
- Retards dans la réalisation des actes bancaires
- Risques de non-conformité des actes bancaires
- Risques d'amendes réglementaires

**Analyse des causes racines (5 Whys) :**
1. Pourquoi 25% certification seulement ? → Taux de rejet élevé (20%)
2. Pourquoi taux de rejet élevé ? → Qualité des documents déposés insuffisante
3. Pourquoi qualité insuffisante ? → Manque de guidage client ET conseiller
4. Pourquoi manque de guidage ? → Absence d'exemples de documents avec données/mentions à vérifier
5. **Cause racine** : **Pas de référentiel d'exemples de documents annotés avec critères de validation**

---

### P3 : Absence de reproposabilité des documents

**Impact** : Efficacité opérationnelle / Satisfaction clients  
**Fréquence** : Quotidien  
**Acteurs concernés** : Clients + Conseillers + Système DPJ

**Symptômes :**
- Clients ne souhaitent pas transmettre des documents fournis antérieurement et encore valides
- Expérience client dégradée (friction)
- Conseiller doit revalider des documents déjà validés antérieurement

**Analyse des causes racines (5 Whys) :**
1. Pourquoi redemander docs ? → Reproposabilité inexistante
2. Pourquoi reproposabilité inexistante ? → Fonctionnalité non implémentée dans SI actuel
3. Pourquoi non implémentée ? → Règles de reproposabilité non définies
4. Pourquoi règles non définies ? → Pas de validation juridique des cas d'usage
5. **Cause racine** : **Absence de référentiel juridique définissant les règles de reproposabilité des documents par cas d'usage (quels documents, pour quels actes, avec quelle durée de validité)**

**Objectif** : Atteindre 20% de taux de reproposabilité (337 500 documents/mois réutilisables)

---

### P4 : Deadline Programme 15C (PMV 6 mois)

**Impact** : Stratégique / Réglementaire  
**Fréquence** : Unique (contrainte temporelle)  
**Acteurs concernés** : Direction / PU (Pôle Utilisateur) / Équipes développement

**Symptômes :**
- Contrainte temporelle forte (6 mois)
- Obligation de livrer un PMV (Produit Minimum Viable) fonctionnel
- Impact sur le scope et la priorisation des fonctionnalités

**Analyse des causes racines :**
1. Pourquoi 6 mois ? → Engagement Programme 15C
2. Pourquoi cet engagement ? → Dépendances stratégiques inter-programmes
3. **Cause racine** : **Contrainte externe Programme 15C imposant un PMV à 6 mois**

---

### P5 : Dépendances externes critiques (GED + RAD/LAD)

**Impact** : Technique / Fonctionnel  
**Fréquence** : Permanent  
**Acteurs concernés** : Squad Acquisition + Équipes GED/RAD/LAD + Architectes

**Symptômes :**
- Fonctionnalités DPJ restreintes si socles GED/RAD/LAD non livrés
- Risque de livrables incomplets
- Dépendances non maîtrisées par Squad Acquisition

**Analyse des causes racines (5 Whys) :**
1. Pourquoi dépendances critiques ? → DPJ s'appuie sur socles GED et RAD/LAD
2. Pourquoi s'appuie sur ces socles ? → Architecture distribuée
3. Pourquoi architecture distribuée ? → Réutilisation de socles transverses
4. Pourquoi critiques ? → Refontes GED et RAD/LAD en cours, hors périmètre DPJ
5. **Cause racine** : **Architecture distribuée avec dépendances sur programmes externes (refontes GED et RAD/LAD hors maîtrise Squad Acquisition)**

---

### P6 : Migration DNC et intégration 200 parcours produits

**Impact** : Technique / Opérationnel / Stratégique  
**Fréquence** : Unique (contrainte temporelle - décommissionnement DNC début 2027)  
**Acteurs concernés** : Squad Acquisition + Équipes parcours produits + Architectes + PU

**Symptômes :**
- Migration obligatoire des parcours utilisant DNC (Dossier Numérique Client - ancêtre de DPJ)
- Décommissionnement DNC prévu début 2027
- 200 parcours produits hétérogènes à accompagner
- DPJ devient standard d'entreprise (obligation d'adoption)
- Besoin de définir règles de gestion spécifiques par parcours

**Analyse des causes racines (5 Whys) :**
1. Pourquoi migration obligatoire ? → Décommissionnement DNC début 2027
2. Pourquoi décommissionner DNC ? → Obsolescence technique et fonctionnelle
3. Pourquoi 200 parcours à accompagner ? → DPJ devient standard d'entreprise
4. Pourquoi difficile ? → Hétérogénéité parcours + absence de règles de gestion communes
5. **Cause racine** : **Dette technique historique (DNC obsolète à migrer avant 2027) + DPJ devenant standard d'entreprise nécessitant migration DNC et accompagnement de 200 parcours hétérogènes pour définir leurs règles de gestion**

---

## <a name="livrables-session-1"></a>📤 5. Livrables Session 1

| Livrable | Statut | Description |
|----------|--------|-------------|
| **Swimlane Diagram** | ✅ Validé | Processus As-Is avec reproposabilité, workflow validation manuel/auto |
| **Volumétrie complète** | ✅ Validé | 2,25M docs/mois, 40k conseillers, 21M clients, 200 types d'actes |
| **Scope & Boundaries** | ✅ Validé | Périmètre In/Out, contraintes réglementaires/planning/budget, dépendances |
| **6 Problèmes majeurs** | ✅ Validé | Causes racines documentées (5 Whys), impacts business quantifiés |

---

## <a name="prochaine-session"></a>🚀 6. Prochaine Session

### Session 2 : Opportunity & Strategy (6 heures)

**Objectifs :**
- Transformer les 6 problèmes en vision stratégique
- Créer la roadmap de bénéfices sur 2 ans
- Aligner avec la stratégie d'entreprise

**Livrables attendus :**
1. **Problem Deep Dive** : 6 problèmes détaillés en Lean Canvas
2. **Vision Statement** structuré (2 thèmes) :
   - Thème 1 : Valeur apportée Métier (4 axes)
   - Thème 2 : Valeur apportée SI (2 axes)
3. **Benefits Realization Roadmap** : Roadmap 2 ans par acteur/produit
4. **Strategy Alignment** : Prérequis, OKRs, contraintes programmes

---

## 📝 Notes & Parking Lot

### Décisions prises
- ✅ DPJ devient standard d'entreprise
- ✅ Migration DNC obligatoire avant 2027
- ✅ Reproposabilité = fonctionnalité prioritaire (20% objectif)
- ✅ PMV 6 mois imposé par Programme 15C

### Points à approfondir en Session 2
- [ ] Études juridiques pour lever restrictions RAD/LAD
- [ ] Référentiel d'exemples de documents annotés
- [ ] Référentiel juridique de reproposabilité
- [ ] Coordination avec refontes GED et RAD/LAD
- [ ] Plan d'accompagnement 200 parcours

---

**Document généré avec Packmind - Package "etude-opportunite"**  
**Conformité** : Standard "Qualité de Documentation d'Ateliers"

---

## Annexes

### Glossaire

- **DPJ** : Dossier de Pièces Justificatives
- **DNC** : Dossier Numérique Client (ancêtre de DPJ, à décommissionner 2027)
- **RAD** : Reconnaissance Automatique de Documents
- **LAD** : Lecture Automatique de Documents
- **GED CATS** : Gestion Électronique de Documents (GED métier)
- **PP** : Personne Physique
- **PM** : Personne Morale (EI, PME, Entreprises, Grandes Entreprises)
- **PU** : Pôle Utilisateur (MOA déléguée)
- **PMV** : Produit Minimum Viable
- **KYC** : Know Your Customer

### Contacts

- **Squad Acquisition** : Équipe responsable du Dossier de PJ
- **PU** : Pôle Utilisateur (experts métier)
- **Programme 15C** : Programme imposant deadline PMV 6 mois

---

*Fin du document Session 1*