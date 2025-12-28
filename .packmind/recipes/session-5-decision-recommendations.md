Synthétiser les 4 jours d'étude pour formaliser une recommandation GO/NoGO validée, un Business Case complet (Investment/ROI/Payback/NPV) et un Executive Summary de 3 pages pour le COMEX Produit.

## When to Use

- Après avoir complété les Sessions 1 à 4 de l'Étude d'Opportunité
- Quand il faut consolider les analyses (contexte, opportunité, scénarios, risques) pour prendre une décision formelle
- Avant de présenter au COMEX Produit une recommandation stratégique sur le lancement du projet
- Quand le Business Case doit être finalisé avec Investment, ROI, Payback et NPV
- Pour préparer un Executive Summary synthétique (3 pages) destiné à la direction

## Context Validation Checkpoints

* [ ] Les 4 sessions précédentes sont-elles complètes et validées (Contexte, Opportunité, Scénarios, Risques) ?
* [ ] Les données financières nécessaires au Business Case sont-elles disponibles (investissements, bénéfices, coûts récurrents) ?
* [ ] Les critères de validation GO/NoGO sont-ils définis et partagés (Business + IT + Risques + Budget) ?
* [ ] Le format et la durée de présentation au COMEX Produit sont-ils confirmés (15-20 min + 10 min Q&A) ?
* [ ] Les parties prenantes décisionnaires sont-elles identifiées et disponibles pour valider la recommandation ?

## Recipe Steps

### Step 1: Synthèse des 4 sessions précédentes

Consolider les livrables des Sessions 1 à 4 (Swimlane, Problem Canvas, Vision Statement, Scénarios, Matrice des risques) dans un document de synthèse structuré. Identifier les points clés qui justifient la recommandation.

```markdown
# Synthèse de l'Étude d'Opportunité DPJ

## Session 1 - Contexte Métier
- **Processus As-Is**: [Résumé du Swimlane Diagram]
- **Problématique**: [Pain Points identifiés]
- **Sponsors**: [Liste et engagement]

## Session 2 - Opportunité & Stratégie
- **Problem Canvas**: [Top 3 problèmes et solutions]
- **Vision Statement**:
  - Métier: [4 axes]
  - SI: [2 axes]
- **Benefits Roadmap**: [Jalons clés sur 2 ans]

## Session 3 - Scénarios
- **Scénario retenu**: [Minimal/Équilibré/Complet]
- **Justification**: [Critères de choix]

## Session 4 - Risques
- **Risques critiques**: [Top 5]
- **Stratégies de mitigation**: [Actions prioritaires]
```

### Step 2: Élaboration du Business Case complet

Calculer les 4 indicateurs financiers (Investment, ROI, Payback, NPV) en agrégeant les données du scénario retenu. Documenter les hypothèses de calcul et les sources de données pour assurer la traçabilité.

```markdown
# Business Case - Projet DPJ

## Investissement Total
| Catégorie | Montant (€) | Détail |
|-----------|-------------|--------|
| Développement | [montant] | [sprints × coût] |
| Infrastructure | [montant] | [licences + hébergement] |
| Change Management | [montant] | [formation] |
| Contingence (15%) | [montant] | [buffer risques] |
| **TOTAL** | **[montant]** | |

## Indicateurs Financiers
- **ROI**: [(Bénéfices - Investment) / Investment × 100] = **[X]%**
- **Payback**: **[X] mois**
- **NPV** (taux 5%): **[montant] €**
```

### Step 3: Validation GO/NoGO par points de contrôle

Évaluer le projet sur 4 dimensions (Business + IT + Risques + Budget) avec des critères binaires (✅ Validé / ❌ Bloquant / ⚠️ Attention). Toutes les dimensions doivent être au vert pour une recommandation GO.

```markdown
# Matrice de Décision GO/NoGO

## Point de Contrôle 1 - Business
| Critère | Statut | Commentaire |
|---------|--------|-------------|
| ROI > 20% | [✅/❌/⚠️] | [valeur] |
| Alignement stratégique | [✅/❌/⚠️] | [validation] |
| Sponsors engagés | [✅/❌/⚠️] | [niveau] |

## Point de Contrôle 2 - IT
| Critère | Statut | Commentaire |
| Faisabilité technique | [✅/❌/⚠️] | [validation Architecture] |
| Cohérence urbanisation | [✅/❌/⚠️] | [intégration] |

## Point de Contrôle 3 - Risques
| Critère | Statut | Commentaire |
| Aucun risque critique | [✅/❌/⚠️] | [top 5 sous contrôle] |
| Conformité RGPD | [✅/❌/⚠️] | [DPO OK] |

## Point de Contrôle 4 - Budget
| Critère | Statut | Commentaire |
| Budget disponible | [✅/❌/⚠️] | [enveloppe confirmée] |
| Payback < 18 mois | [✅/❌/⚠️] | [délai ROI] |
```

### Step 4: Rédaction de l'Executive Summary (3 pages)

Rédiger un document de synthèse de 3 pages structuré en 5 sections (Contexte + Enjeux + Solution retenue + Business Case + Next Steps) pour présentation au COMEX Produit. Appliquer le standard 'Qualité de Documentation d'Ateliers'.

```markdown
# Executive Summary - Étude d'Opportunité DPJ

## 1. Contexte
**Situation actuelle**: [Description processus As-Is et problématique]
**Sponsors**: [Direction Métier + SI]

## 2. Enjeux
**Enjeux Métier**: [3 enjeux quantifiés]
**Enjeux SI**: [Modernisation, Conformité]

## 3. Solution Retenue
**Scénario**: [Minimal/Équilibré/Complet]
**Durée & Budget**: [X mois / X M€]

## 4. Business Case
| Indicateur | Valeur | Objectif |
| ROI | [X]% | > 20% ✅ |
| Payback | [X] mois | < 18 mois ✅ |

## 5. Next Steps
**Recommandation**: **[GO / NoGO]**
**Feuille de route**: [3 phases]
```

### Step 5: Préparation de la présentation COMEX Produit

Préparer une présentation PowerPoint de 15-20 minutes (max 10 slides) en exportant l'Executive Summary. Anticiper les questions probables (risques, budget, délais) et préparer les réponses avec les données de support.

```markdown
# Slides COMEX Produit (10 slides max)

1. Page de garde
2. Contexte & Problématique
3. Enjeux Métier & SI
4. Solution Retenue (1-2 slides)
5. Business Case (Investment/ROI/Payback/NPV)
6. Risques & Mitigation (Top 5)
7. Feuille de Route
8. Recommandation GO/NoGO
9. Next Steps
10. Annexes (backup Q&A)

## Questions Anticipées
**Q: Pourquoi ce scénario ?**
→ [Trade-offs Session 3]

**Q: Risques SSI maîtrisés ?**
→ [Validation Référent Sécurité]
```

### Step 6: Validation collective et décision finale

Organiser une session de validation de 2 heures avec les parties prenantes clés (Direction Métier, DSI, sponsors, Risk Owners). Présenter l'Executive Summary, le Business Case et la recommandation GO/NoGO. Recueillir le consensus formel.

```markdown
# Checklist Validation Session 5

## Avant (J-2)
- [ ] Executive Summary relu (standard qualité)
- [ ] PowerPoint exporté
- [ ] Business Case vérifié
- [ ] Participants confirmés

## Pendant (2h)
- [ ] 00:00-00:15 - Rappel contexte
- [ ] 00:15-00:45 - Executive Summary + Business Case
- [ ] 00:45-01:15 - Matrice GO/NoGO
- [ ] 01:15-01:30 - Recommandation
- [ ] 01:30-01:50 - Q&A
- [ ] 01:50-02:00 - Vote et décision

## Après (J+1)
- [ ] Compte-rendu diffusé
- [ ] Si GO: Brief équipe + lancement cadrage
```
