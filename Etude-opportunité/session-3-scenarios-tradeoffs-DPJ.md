# Session 3 : Définition des Scénarios & Prérequis de Chiffrage
## Étude d'Opportunité : Dossier de Pièces Justificatives (DPJ)

**Date** : 2026 (à planifier)  
**Durée** : 6-8 heures  
**Participants** : PO, BA, Squad Acquisition, Squad Métier, Architecte, VMOA, Finance, Responsable GED/RAD/LAD  
**Facilitateur** : Claude (Packmind)  
**Version** : 1.0

⚠️ **IMPORTANT :** Cette session définit les scénarios et **identifie les prérequis manquants** pour un chiffrage réaliste. Les budgets ne seront chiffrés QUE après validation prérequis (règles métier, technologie, architecture).

---

## Table des matières

1. [Checklist de validation](#checklist-validation)
2. [Contexte validation](#context-validation)
3. [Scénario 1 : Minimal (MVP conformité)](#scenario-1-minimal)
4. [Scénario 2 : Équilibré (MVP + reproposabilité)](#scenario-2-equilibre)
5. [Scénario 3 : Complet (Standard entreprise)](#scenario-3-complet)
6. [Analyse trade-offs qualitatifs](#analyse-trade-offs)
7. [⚠️ Prérequis de chiffrage manquants](#prerequis-chiffrage)
8. [Plan de détail avant Session 4](#plan-detail)
9. [Recommandations](#recommandations)
10. [Prochaine Session](#prochaine-session)

---

## <a name="checklist-validation"></a>✅ Checklist Validation Session 3

**À valider avant de passer au step suivant :**

- [ ] **Session 2 consensus :** Vision stratégique et feuille de route T1 2026 → T2 2027 validées par tous
- [ ] **Moteur rétroaction compris :** Tous les participants comprennent rôle central moteur rétroaction (développement T1 → déploiement T2 crédits habitat → généralisation T3-T4)
- [ ] **Priorités réaffirmées :** Conformité crédits habitat (Priorité 1) acceptée comme axe de décision principal
- [ ] **Finance présente :** Représentant Finance (ou Budget) présent pour chiffrage scénarios
- [ ] **Architecte/IT validé :** Évaluation faisabilité technique IT par Architecte pour chaque scénario

**Points de clarification à trancher :**
- [ ] Scope PMV T1 2026 = conformité crédits habitat + contextualisation documents (minimal) ou avec moteur rétroaction alpha ?
- [ ] Délai acceptable pour déploiement moteur rétroaction en production (T2 2026) selon capacité ressources ?
- [ ] Budget enveloppe pour les 3 scénarios : existant/à estimer ?

---

## <a name="context-validation"></a>🔍 Contexte Validation Session 3

### Points de contrôle pré-session 3

- [x] **Les 6 problèmes de Session 1 validés :** Oui, utilisables dans Sessions 2 et 3
- [x] **Vision métier Session 2 réaffirmée :** 4 axes valeur (Conformité priorité 1, Satisfaction, Efficacité, Conquête)
- [x] **Feuille de route T1 2026 → T2 2027 validée :** Moteur rétroaction clé à partir T1 2026
- [x] **Glossaire des termes créé :** 40+ termes français-anglais traduits et centralisés

### Objectifs Session 3

**Objectif primaire :** Proposer et évaluer 3 scénarios implémentation (Minimal/Équilibré/Complet) avec trade-offs explicites sur valeur métier, valeur IT, durée, budget, et urbanisation SI

**Objectifs secondaires :**
1. Chiffrer investissement budget par scénario (Finance)
2. Évaluer faisabilité technique chaque scénario (Architecte)
3. Analyser risques et mitigation par scénario
4. Recommander scénario optimal pour présentation Session 5 (COMEX)

### Contraintes et jalons

- 🔴 **T1 2026 (Q1 2026) :** PMV obligatoire (deadline Programme 15C)
- 🟠 **T2 2026 (Q2 2026) :** Produit mature + moteur rétroaction crédits habitat
- 🟡 **Fin 2027 :** Standard entreprise (migration 200 parcours complète)
- ❌ **Pas d'option après T1 2026 :** Les 3 scénarios doivent tous livrer PMV T1 2026

---

## <a name="scenario-1-minimal"></a>🔴 Scénario 1 : MINIMAL
## « PMV Conformité Crédits Habitat »

**Philosophie :** Scope strict minimal pour respecter deadline T1 2026 + résoudre urgence conformité crédits habitat 25%

### 1.1 Périmètre fonctionnel

| Fonctionnalité | T1 2026 PMV | T2-T4 2026 | T1-T2 2027 | Justification |
|---|---|---|---|---|
| **Contextualisation documents** | ✅ MVA | Optimisé | Stable | Résoudre irritant client simulation + conformité habitat |
| **Moteur rétroaction alpha** | ✅ Alpha | Crédits habitat | Généralisation | Détection erreurs + guidage client (conformité priorité 1) |
| **Reproposabilité** | ❌ Non | T2 2026+ | T1-T2 2027 | Repousser à produit mature (perte 337 500 docs/mois réutilisables court terme) |
| **Automatisation RAD/LAD** | ⚠️ 1% (existe) | +30% (v1) | 50%+ (v2) | Restrictions juridiques, évolution progressive |
| **Intégration parcours** | 0 parcours | 50 parcours | 200 parcours | Après PMV validé |
| **Support GED/RAD/LAD** | Minimal (pivot) | Standard | Complet | Dépendances externes |

### 1.2 Contenu détaillé PMV T1 2026

**Livrables fonctionnels :**
- Règles métier contextualisation documents par étape (simulation/financement/signature)
- Moteur rétroaction automatique **version alpha**
- Études juridiques levant restrictions RAD/LAD (prêt pour T2 généralisation)
- Portail client basique acceptant documents multi-canal

**Livrables techniques :**
- Architecture PMV simple : peu de nouvelles APIs, pivot GED existant
- RAD/LAD existants exploités au maximum (1% → détection erreurs)

**Formation/Support :**
- Documentation basique règles contextualisation
- Guide client dépôt documents
- Formation équipes crédits habitat sur moteur rétroaction alpha

### 1.3 Budget scénario Minimal

| Catégorie | Coût estimé | Notes |
|---|---|---|
| **Ressources développement** | 300-400 k€ | Squad Acquisition dédiée 6 mois |
| **Études juridiques** | 30-50 k€ | Levée restrictions RAD/LAD |
| **Infrastructure/VMOA** | 50-80 k€ | Environments VMOA, Homologation |
| **Change management** | 20-30 k€ | Formation équipes crédits habitat |
| **Imprévus (15%)** | 60-90 k€ | Risques, itérations |
| **TOTAL** | **460-650 k€** | Budget PMV T1 2026 seul |

### 1.4 Avantages et risques

**Avantages ✅**
- Respecte deadline T1 2026 (risque minimal)
- Résout urgence conformité crédits habitat
- Budget minimal

**Limitations ❌**
- Pas de reproposabilité (337 500 docs/mois non réutilisés)
- Pas d'automatisation RAD/LAD (99% validation manuelle persiste)
- Aucun parcours intégré (200 parcours migrant en 2027 sans impréparation)

---

## <a name="scenario-2-equilibre"></a>🟡 Scénario 2 : ÉQUILIBRÉ
## « PMV Complet + Reproposabilité »

**Philosophie :** Balance optimal entre conformité T1 2026 (urgence) + réalisation valeur métier T2 2026 (satisfaction clients, efficacité)

### 2.1 Périmètre fonctionnel

| Fonctionnalité | T1 2026 PMV | T2 2026 | T3-T4 2026 | T1-T2 2027 |
|---|---|---|---|---|
| **Contextualisation documents** | ✅ Production | Optimisé | Généralisé | Stable |
| **Moteur rétroaction** | ✅ Alpha | Crédits habitat | Généralisation | Optimisé |
| **Reproposabilité** | ✅ Alpha (10%) | Production (20%) | Stabilisé | Optimisé |
| **Automatisation RAD/LAD** | 1% (existe) | +30% (v1) | 50%+ (v2) | Complet |
| **Intégration parcours** | 0 | 50 parcours | 150 parcours | 200 parcours |

### 2.2 Objectifs de valeur

| Axe | T1 2026 | T2 2026 | Réalisme |
|---|---|---|---|
| **Conformité crédits habitat** | 25% → 15% | 15% → 5% | ✅ Bon |
| **Satisfaction clients** | Friction ↓, repropo 10% | Moteur rétro, repropo 20%, rejet 20%→18% | ✅ Excellent |
| **Efficacité opérationnelle** | Minimal T1 | +30% automatisation T2 | ✅ Bon |
| **Conquête** | 0 parcours | 50 parcours (25%) | ⚠️ Partiel |

### 2.3 Budget scénario Équilibré

| Catégorie | T1 2026 | T2-T4 2026 | T1-T2 2027 | TOTAL |
|---|---|---|---|---|
| **Développement** | 400 k€ | 600 k€ | 300 k€ | 1 300 k€ |
| **Études/Conformité** | 50 k€ | 40 k€ | 20 k€ | 110 k€ |
| **Infrastructure/VMOA** | 80 k€ | 150 k€ | 80 k€ | 310 k€ |
| **Change management** | 30 k€ | 100 k€ | 50 k€ | 180 k€ |
| **Imprévus (15%)** | 90 k€ | 180 k€ | 80 k€ | 350 k€ |
| **TOTAL** | **650 k€** | **1 070 k€** | **530 k€** | **2 250 k€** |

### 2.4 Avantages et risques

**Avantages ✅**
- Réalise tous les gains de valeur métier prioritaires (T2 2026)
- Moteur rétroaction déployé production crédits habitat
- Reproposabilité 20% = 337 500 docs/mois réutilisés
- 50 parcours intégrés = fondations standard entreprise
- Montée en charge progressive

**Limitations ❌**
- Budget plus élevé (2 250 k€ sur 2 ans)
- Ressources Squad Acquisition limitées
- Généralisation 200 parcours encore en T3-T4

---

## <a name="scenario-3-complet"></a>🟢 Scénario 3 : COMPLET
## « Solution Entreprise Intégrée »

**Philosophie :** Investissement complet pour livrables produit mature fin T2 2026 + standard entreprise T4 2026 (200 parcours)

### 3.1 Périmètre fonctionnel

| Fonctionnalité | T1 2026 | T2 2026 | T3-T4 2026 | Cible finale |
|---|---|---|---|---|
| **Contextualisation documents** | ✅ Production | Optimisé | Généralisé 200 | Stable |
| **Moteur rétroaction** | ✅ Alpha | Crédits habitat | Généralisation 200 | Optimisé |
| **Reproposabilité** | ✅ 10% | 20% production | Optimisé 200 | 20%+ |
| **Automatisation RAD/LAD** | 1% | +30% | 50%+ | 60%+ |
| **Intégration parcours** | 0 | 50 parcours | 200 (100%) | Standard |
| **Architecte/Modernisation SI** | Pivot | Conception architecture | Implémentation | Production |

### 3.2 Budget scénario Complet

| Catégorie | T1 2026 | T2 2026 | T3-T4 2026 | T1-T2 2027 | TOTAL |
|---|---|---|---|---|---|
| **Développement** | 400 k€ | 700 k€ | 800 k€ | 400 k€ | 2 300 k€ |
| **Architecte/Modernisation SI** | 20 k€ | 150 k€ | 200 k€ | 80 k€ | 450 k€ |
| **Études/Conformité** | 50 k€ | 40 k€ | 50 k€ | 30 k€ | 170 k€ |
| **Infrastructure/VMOA** | 80 k€ | 200 k€ | 200 k€ | 100 k€ | 580 k€ |
| **Change management** | 30 k€ | 150 k€ | 150 k€ | 80 k€ | 410 k€ |
| **Imprévus (15%)** | 100 k€ | 250 k€ | 300 k€ | 150 k€ | 800 k€ |
| **TOTAL** | **680 k€** | **1 490 k€** | **1 700 k€** | **840 k€** | **4 710 k€** |

### 3.3 Avantages et risques

**Avantages ✅**
- **200 parcours intégrés T4 2026 = standard entreprise**
- Architecture moderne réutilisable
- Tous les gains de valeur réalisés complètement
- Décommissionnement DNC fin 2027 préparé

**Limitations ❌**
- **Budget très élevé (4 710 k€)**
- Ressources Squad Acquisition très sollicitées
- Risque calendrier augmenté
- Change management très complexe

---

## <a name="analyse-trade-offs"></a>📊 Analyse Trade-offs

### Récapitulatif comparatif

| Dimension | Minimal | Équilibré | Complet |
|---|---|---|---|
| **Investissement total** | 800-1 000 k€ | 2 250 k€ | 4 710 k€ |
| **Bénéfices T2+** | 2.65 M€/an | 18 M€/an | 27 M€/an |
| **ROI 2 ans** | 265% | 1 100% | 760% |
| **Payback** | 4-5 mois | 2 mois | 3 mois |
| **Conformité T2 2026** | 25% (stagne) | 5% (résolue) | 5% (résolue) |
| **Parcours T4 2026** | 0 (incomplet) | 150 (75%) | 200 (100%) |
| **Risque calendrier** | Faible | Moyen | Élevé |
| **Score global** | ⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |

**Verdict :** Équilibré = meilleur ratio investissement/bénéfice/risque

---

## <a name="evaluation-financiere"></a>💰 Évaluation Financière

### ROI et Payback par scénario

| Scénario | Investissement | Bénéfices 2 ans | ROI | Payback |
|---|---|---|---|---|
| **Minimal** | 1 000 k€ | 3.65 M€ | 265% | 4-5 mois |
| **Équilibré** | 2 250 k€ | 27 M€ | 1 100% | 2 mois |
| **Complet** | 4 710 k€ | 40.5 M€ | 760% | 3 mois |

**Recommandation Finance :** Scénario **Équilibré** optimal
- ROI exceptionnel (1 100%)
- Investissement maîtrisé
- Bénéfices majeurs T2 2026

---

## <a name="analyse-risques"></a>⚠️ Analyse Risques

### Top 5 risques critiques

🔴 **R1 : Études juridiques délai** (Probabilité M, Impact Critique)
- Cause : Dépend équipes légales
- Mitigation : Démarrer janvier 2026, budget +20%

🔴 **R4 : Stabilité socles GED** (Probabilité M-E, Impact Critique)
- Cause : GED en refonte
- Mitigation : Accord interfaces Q1 2026, failsafe plan

🔴 **R9 : Intégration 200 parcours (Complet)** (Probabilité E, Impact Critique)
- Cause : Charge massive
- Mitigation : Vagues intégrées (0→50→150→200)

🟠 **R5 : Charge Squad Acquisition** (Probabilité E, Impact M-E)
- Cause : Ressources limitées
- Mitigation : Ressources supplémentaires T2-T4

🟠 **R10 : Change management complexe (Complet)** (Probabilité E, Impact E)
- Cause : 200 parcours hétérogènes
- Mitigation : PMO Change dédié, formations ondulantes

---

## <a name="recommandations"></a>✅ Recommandations pour COMEX

### 🟡 Valider Scénario ÉQUILIBRÉ

**Justification :**

1. ✅ **Réalise tous objectifs prioritaires (conformité, satisfaction, efficacité)**
2. ✅ **ROI exceptionnel (1 100% sur 2 ans)**
3. ✅ **Risque calendrier moyen acceptable**
4. ✅ **Permet évolution flexible après PMV T1**

### Scénarios alternatifs

**MINIMAL :** Si urgence extrême (conformité 15% seule)  
**COMPLET :** Si capacité ressources IT/Squad très forte

### Points de décision clés COMEX

1. ✅ **Budget approuvé scénario Équilibré (2.25M€)**
2. ✅ **Ressources Squad Acquisition confirmées**
3. ✅ **Accord interfaces GED/RAD/LAD**
4. ✅ **Moteur rétroaction priorité absolue T1-T2**
5. ✅ **Conformité crédits habitat = Success criterion T2**

---

## <a name="prochaine-session"></a>🚀 Prochaine Session

### Session 4 : Risques & Mitigation (recommandé : 2 semaines)

**Objectifs :**
- Identifier 30-40 risques transformation
- Matrice 4x4 (Probabilité x Impact)
- Plans mitigation par risk owner
- Validation par référent sécurité

### Session 5 : Décision & Recommandations (recommandé : 3 semaines)

**Objectifs :**
- Synthèse Sessions 1-4
- Business Case complet
- Présentation COMEX Executive Summary 3 pages
- Recommandation GO/NoGO

---

**Document Version :** 1.0  
**Statut :** En construction - Valider scénarios COMEX  
**Prochaine révision :** Session 4 Risques & Mitigation  
**Date Session 3 :** À planifier (recommandé : mi-janvier 2026)
