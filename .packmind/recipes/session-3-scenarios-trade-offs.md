Faciliter la troisième session d'une étude d'opportunité pour proposer 3 scénarios d'implémentation (Minimal/Équilibré/Complet), évaluer les trade-offs sur les dimensions valeur métier/IT, durée, budget, urbanisation SI, et analyser les risques via matrice avec actions de minimisation.

## When to Use

- Après Session 2 (Vision Statement et Benefits Roadmap validés)
- Besoin de proposer plusieurs options d'implémentation au COMEX
- Évaluation des trade-offs entre scope, temps, budget, valeur, urbanisation
- Construction d'options décisionnelles pour le dossier COMEX Produit
- Phase avant analyse des risques détaillés (Session 4)

## Context Validation Checkpoints

* [ ] Le Vision Statement et les axes de valeurs de Session 2 sont-ils validés ?
* [ ] Disposons-nous des contraintes budgétaires et temporelles de l'entreprise ?
* [ ] Les principes d'urbanisation du SI et la cible architecture sont-ils connus ?
* [ ] Les participants incluent-ils des architectes pour évaluer l'urbanisation SI ?
* [ ] Le format matrice de risques est-il défini (Impact x Probabilité) ?

## Recipe Steps

### Step 1: Scenario Framing (1h)

Définir collectivement les critères d'évaluation des 3 scénarios. Les dimensions à considérer sont : Valeur métier (axes Conquête, Efficacité opérationnelle, Réglementaire, Satisfaction clients), Valeur IT (Optimisation Run, Modernisation SI), Durée (timeline de livraison), Budget (estimation enveloppe), Urbanisation SI (cohérence architecture, dette technique, modernisation). Établir une échelle de notation pour chaque dimension (par exemple : Faible/Moyen/Fort ou 1-5). Documenter les hypothèses communes aux 3 scénarios.

```markdown
## Scenario Framing - Critères d'évaluation

### Dimensions d'évaluation
| Dimension | Échelle | Priorité |
|-----------|---------|----------|
| **Valeur Métier** | Faible / Moyen / Fort | Haute |
| - Conquête | 1-5 | - |
| - Efficacité opérationnelle | 1-5 | - |
| - Réglementaire | 1-5 | - |
| - Satisfaction clients | 1-5 | - |
| **Valeur IT** | Faible / Moyen / Fort | Haute |
| - Optimisation Run | 1-5 | - |
| - Modernisation SI | 1-5 | - |
| **Durée** | Mois | Haute |
| **Budget** | M€ | Haute |
| **Urbanisation SI** | Faible / Moyen / Fort | Moyenne |
| - Cohérence architecture | 1-5 | - |
| - Réduction dette technique | 1-5 | - |

### Hypothèses communes
- [Hypothèse 1 : API commune avec Programme B]
- [Hypothèse 2 : Équipe de 8-12 personnes disponibles]
```

### Step 2: Scénario Minimal (1h30)

Construire le scénario MVP (Minimum Viable Product) focalisé sur les fonctionnalités essentielles et les quick wins. Identifier le périmètre minimal répondant aux contraintes réglementaires critiques et aux irritants majeurs. Estimer la durée, le budget, et évaluer la valeur métier/IT ainsi que l'impact sur l'urbanisation SI. Documenter les fonctionnalités exclues et les limitations du scénario.

```markdown
## Scénario 1 : Minimal (MVP)

### Vue d'ensemble
- **Périmètre :** [3-4 actes métier prioritaires]
- **Durée :** 6 mois
- **Budget :** 3M€
- **Équipe :** 8 personnes

### Évaluation des dimensions
| Dimension | Score | Justification |
|-----------|-------|---------------|
| Valeur Métier | ⭐⭐ (Moyen) | Répond aux contraintes réglementaires + 1 irritant majeur |
| - Réglementaire | 5/5 | Conformité mars 2026 atteinte |
| - Satisfaction clients | 2/5 | 1 irritant résolu |
| Valeur IT | ⭐ (Faible) | Ajout fonctionnel, peu de modernisation |
| Urbanisation SI | ⭐ (Faible) | Patch sur existant, pas de refonte |

### Périmètre fonctionnel
✅ **Inclus :** Actes prioritaires, conformité
❌ **Exclus :** 60% des actes métier

### Risques majeurs
- 🔴 Dette technique augmentée
- 🟠 Satisfaction clients partielle
```

### Step 3: Scénario Équilibré (1h30)

Construire le scénario équilibré couvrant 50-70% du périmètre avec un bon ratio valeur/coût. Intégrer les fonctionnalités prioritaires, quelques améliorations SI, et adresser les principaux irritants. Estimer la durée, le budget, et évaluer toutes les dimensions. Ce scénario vise un équilibre entre gains business, modernisation technique, et contraintes ressources/temps.

```markdown
## Scénario 2 : Équilibré

### Vue d'ensemble
- **Périmètre :** [60% des actes métier]
- **Durée :** 9 mois
- **Budget :** 4.5M€
- **Équipe :** 10-12 personnes

### Évaluation des dimensions
| Dimension | Score | Justification |
|-----------|-------|---------------|
| Valeur Métier | ⭐⭐⭐⭐ (Fort) | 60% actes + irritants majeurs résolus |
| - Conquête | 3/5 | Nouveaux parcours clients |
| - Efficacité opérationnelle | 4/5 | Automatisation partielle |
| - Réglementaire | 5/5 | Conformité totale |
| - Satisfaction clients | 4/5 | 80% irritants résolus |
| Valeur IT | ⭐⭐⭐ (Moyen) | Refonte 2-3 API critiques |
| Urbanisation SI | ⭐⭐⭐ (Moyen) | Cohérence améliorée |

### Risques majeurs
- 🟡 Dépendances Programme B
- 🟡 Montée en compétence équipe
```

### Step 4: Scénario Complet (1h30)

Construire le scénario exhaustif couvrant 100% du périmètre avec transformation complète métier et SI. Intégrer toutes les fonctionnalités, refonte architecture, modernisation UI/API, réduction maximale de la dette technique. Estimer durée et budget réalistes. Évaluer impact maximal sur toutes les dimensions mais identifier aussi les contraintes et risques associés.

```markdown
## Scénario 3 : Complet (Transformation)

### Vue d'ensemble
- **Périmètre :** [100% des actes métier]
- **Durée :** 12-15 mois
- **Budget :** 6-7M€
- **Équipe :** 12-15 personnes

### Évaluation des dimensions
| Dimension | Score | Justification |
|-----------|-------|---------------|
| Valeur Métier | ⭐⭐⭐⭐⭐ (Très fort) | 100% + optimisations avancées |
| - Conquête | 5/5 | Nouveaux marchés accessibles |
| - Efficacité opérationnelle | 5/5 | Automatisation complète |
| Valeur IT | ⭐⭐⭐⭐⭐ (Très fort) | Modernisation complète |
| Urbanisation SI | ⭐⭐⭐⭐⭐ (Très fort) | Architecture cible atteinte |

### Risques majeurs
- 🔴 Durée longue (ROI différé)
- 🔴 Budget élevé (6-7M€)
- 🟠 Complexité gestion
```

### Step 5: Trade-offs & Risk Matrix (1h)

Comparer les 3 scénarios en utilisant une matrice de risques (Impact x Probabilité) associée à des actions de minimisation pour chaque risque identifié. Pour chaque scénario, lister les risques majeurs, évaluer leur impact (Faible/Moyen/Fort) et probabilité (Faible/Moyenne/Haute), puis proposer des actions de minimisation concrètes. Faciliter une discussion collective sur les trade-offs : quel scénario maximise la valeur tout en minimisant les risques ? Documenter les arguments pour et contre chaque option.

```markdown
## Trade-offs Analysis & Risk Matrix

### Matrice comparative
| Critère | Minimal | Équilibré | Complet |
|---------|---------|-----------|---------||
| Valeur Métier | ⭐⭐ | ⭐⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Valeur IT | ⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| Durée | 6 mois | 9 mois | 12-15 mois |
| Budget | 3M€ | 4.5M€ | 6-7M€ |
| Urbanisation SI | ⭐ | ⭐⭐⭐ | ⭐⭐⭐⭐⭐ |
| **Risque global** | 🟡 Moyen | 🟢 Faible | 🔴 Élevé |

### Matrice de risques - Scénario Équilibré
| Risque | Impact | Probabilité | Actions minimisation |
|--------|--------|-------------|----------------------|
| Dépendances Programme B | Moyen | Moyenne | Coordination hebdo, plan B |
| Montée compétence | Faible | Moyenne | Formation anticipée Q1 |

### Arguments décisionnels
**Pour Minimal :** ✅ Rapide (6 mois) ❌ Dette technique
**Pour Équilibré :** ✅ Ratio valeur/coût ⚠️ 40% backlog
**Pour Complet :** ✅ Transformation totale ❌ Durée/budget élevés
```

### Step 6: Validation & Wrap-up (30min)

Faire valider les 3 scénarios par tous les participants. Vérifier que les évaluations (valeur métier/IT, durée, budget, urbanisation) sont comprises et partagées. Confirmer que la matrice de risques et les actions de minimisation sont réalistes. Obtenir un consensus formel sur les scénarios présentés (pas encore sur le choix final, qui se fera en Session 5). Recueillir les feedbacks. Documenter les parking lot items. Présenter l'agenda de Session 4 (Risks & Mitigation détaillés).

```markdown
## Checklist Validation Session 3

□ 3 scénarios détaillés (Minimal / Équilibré / Complet)
□ Évaluation dimensions validée (Valeur Métier/IT, Durée, Budget, Urbanisation)
□ Matrice de risques par scénario créée
□ Actions de minimisation documentées
□ Trade-offs analysis partagée
□ Parking lot items capturés
□ Prochaine session planifiée (Session 4)
□ Relecture effectuée
□ Export Markdown → PowerPoint

**✅ Consensus formel obtenu :** □ Oui (sur les 3 scénarios)

📤 **Livrables pour COMEX Produit :**
- 3 scénarios détaillés
- Matrice comparative
- Matrice de risques
- Arguments décisionnels

⚠️ **Note :** Recommandation finale en Session 5
```
