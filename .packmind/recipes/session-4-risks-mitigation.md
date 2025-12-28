Faciliter la quatrième session d'une étude d'opportunité pour identifier tous les risques de transformation (30-40), évaluer sur matrice 4x4 (Potentialité x Impact), identifier 5-7 risques critiques avec risk owners, et définir stratégies de mitigation (Avoid/Mitigate/Transfer/Accept) validées par référent sécurité.

## When to Use

- Après Session 3 (3 scénarios d'implémentation définis)
- Besoin d'identifier et évaluer risques transformation avant décision COMEX
- Évaluation risques de fabrication sur matrice 4x4
- Préparation Risk Summary pour dossier COMEX Produit
- Phase avant synthèse et recommandation finale (Session 5)

## Context Validation Checkpoints

* [ ] Les 3 scénarios de Session 3 sont-ils validés par tous les participants ?
* [ ] Le référent sécurité du produit est-il présent pour évaluer risques SSI ?
* [ ] Disposons-nous des éléments de conformité RGPD et réglementaire ?
* [ ] La matrice 4x4 (Potentialité x Impact) est-elle définie et comprise ?
* [ ] Les participants incluent-ils experts métier (ARM), juridique, conformité ?

## Recipe Steps

### Step 1: Risk Brainstorm (1h30)

Animer un brainstorming exhaustif pour identifier TOUS les risques liés à la transformation (objectif 30-40 risques). Catégoriser chaque risque selon 4 types : Métier (ARM) incluant risques opérationnels évalués en FCI pour DORA, SSI (technique) couvrant sécurité/infrastructure/architecture, Juridique et conformité (réglementaire) incluant obligations légales et deadlines, RGPD couvrant protection données personnelles et privacy. Utiliser la technique du brainstorming libre puis regrouper par catégorie. Documenter chaque risque avec une description claire.

```markdown
## Risk Brainstorm - Identification exhaustive

### Catégorie 1 : Risques Métier (ARM)
🔹 **R-M1 :** Résistance au changement des utilisateurs métier
🔹 **R-M2 :** Processus métier non stabilisé (impact FCI DORA)
🔹 **R-M3 :** Perte de connaissance métier (départ experts)
🔹 **R-M4 :** Volumétrie sous-estimée (80k → 100k dossiers/mois)
[... continuer jusqu'à 8-10 risques métier]

### Catégorie 2 : Risques SSI (Technique)
🔹 **R-T1 :** Complexité technique architecture sous-estimée
🔹 **R-T2 :** Dépendances fournisseurs externes (API tierce)
🔹 **R-T3 :** Performance dégradée sous charge
[... continuer jusqu'à 10-12 risques techniques]

### Catégorie 3 : Risques Juridique et Conformité
🔹 **R-J1 :** Non-conformité réglementaire mars 2026 (deadline)
🔹 **R-J2 :** Interprétation erronée textes réglementaires
[... continuer jusqu'à 5-8 risques juridiques]

### Catégorie 4 : Risques RGPD
🔹 **R-G1 :** Traitement données personnelles non conforme
🔹 **R-G2 :** Absence consentement explicite utilisateurs
🔹 **R-G3 :** Fuite de données / Data breach
[... continuer jusqu'à 5-8 risques RGPD]

**Total identifié :** 30-40 risques
```

### Step 2: Risk Assessment avec Matrice 4x4 (2h)

Évaluer chaque risque identifié sur une matrice 4x4. Axe horizontal : Potentialité d'occurrence (Très faible / Faible / Moyenne / Haute). Axe vertical : Impact (Faible / Moyen / Fort / Très fort). Pour chaque risque, faciliter une discussion collective pour déterminer sa position dans la matrice. Focus sur les risques de fabrication (liés à la réalisation du projet). Documenter la justification de chaque évaluation.

```markdown
## Risk Assessment - Matrice 4x4

| Risque | Catégorie | Potentialité | Impact | Zone | Justification |
|--------|-----------|--------------|--------|------|---------------|
| R-M1 | Métier | Moyenne | Fort | 🟠 ÉLEVÉ | Changement culturel important |
| R-M2 | Métier (FCI DORA) | Faible | Très fort | 🔴 CRITIQUE | Impact processus critique |
| R-T1 | SSI | Moyenne | Fort | 🟠 ÉLEVÉ | Architecture complexe |
| R-T2 | SSI | Haute | Très fort | 🔴 CRITIQUE | Dépendance fournisseur critique |
| R-J1 | Juridique | Faible | Très fort | 🔴 CRITIQUE | Deadline réglementaire impérative |
| R-G1 | RGPD | Moyenne | Moyen | 🟡 MODÉRÉ | Processus RGPD existants |
| R-G3 | RGPD | Faible | Très fort | 🔴 CRITIQUE | Impact réputation + CNIL |

**Zones de risque :**
- 🔴 **CRITIQUE** : Potentialité Faible-Moyenne x Impact Très fort
- 🟠 **ÉLEVÉ** : Potentialité Moyenne-Haute x Impact Fort
- 🟡 **MODÉRÉ** : Autres combinaisons
- 🟢 **FAIBLE** : Potentialité Très faible x Impact Faible-Moyen
```

### Step 3: Risk Prioritization & Risk Owners (1h)

Identifier les 5-7 risques critiques de fabrication (zone rouge/orange de la matrice 4x4) qui nécessitent une attention prioritaire. Pour chaque risque critique, assigner un Risk Owner (responsable du suivi et de la mitigation du risque). Impliquer le référent sécurité produit pour validation des risques SSI. Documenter les responsabilités de chaque risk owner.

```markdown
## Risques Critiques - Top 5-7

### 🔴 CRITIQUE - Priorité 1

#### R-T2 : Dépendance fournisseur externe (API tierce)
- **Catégorie :** SSI (Technique)
- **Potentialité :** Haute
- **Impact :** Très fort
- **Risk Owner :** [Nom Architecte Technique]
- **Référent Sécurité :** [Nom - validé ✅]
- **Description :** API critique fournie par Partenaire X, SLA non garanti
- **Impact si réalisé :** Blocage complet processus métier, 80k dossiers/mois

#### R-J1 : Non-conformité réglementaire mars 2026
- **Catégorie :** Juridique et Conformité
- **Potentialité :** Faible
- **Impact :** Très fort
- **Risk Owner :** [Nom Responsable Conformité]
- **Impact si réalisé :** Amende ACPR, suspension activité

#### R-G3 : Fuite de données / Data breach
- **Catégorie :** RGPD
- **Potentialité :** Faible
- **Impact :** Très fort
- **Risk Owner :** [Nom DPO]
- **Référent Sécurité :** [Nom - validé ✅]
- **Impact si réalisé :** Amende CNIL (4% CA), impact réputation

**Total risques critiques :** 5-7
**Risk Owners assignés :** 5-7
**Validation référent sécurité :** ✅ Risques SSI validés
```

### Step 4: Mitigation Strategies (1h30)

Pour chaque risque critique, définir une stratégie de mitigation parmi les 4 options : Avoid (éviter le risque en changeant l'approche), Mitigate (réduire probabilité ou impact), Transfer (transférer à un tiers, assurance, fournisseur), Accept (accepter le risque résiduel avec plan de contingence). Documenter des actions concrètes de mitigation avec timeline, budget estimé si applicable, et responsable d'exécution. Valider les stratégies SSI avec le référent sécurité produit.

```markdown
## Mitigation Strategies - Risques Critiques

### R-T2 : Dépendance fournisseur externe (API tierce)
**Stratégie :** 🔄 **MITIGATE** + 🛡️ **TRANSFER**

**Actions de mitigation :**
1. **Mitigate :** Développer API wrapper interne (abstraction)
   - Responsable : Architecte Technique
   - Timeline : Q1 2025
   - Budget : 50k€
   - Réduction impact : Fort → Moyen

2. **Transfer :** Négocier SLA 99.9% avec pénalités contractuelles
   - Responsable : Achat / Juridique
   - Timeline : Q4 2024

3. **Mitigate :** Plan B : API alternative identifiée
   - Responsable : Architecte Technique
   - Timeline : Q2 2025
   - Budget : POC 20k€

**Risque résiduel après mitigation :** 🟡 MODÉRÉ
**Validation référent sécurité :** ✅ Approuvé

---

## Synthèse Stratégies par Type

| Stratégie | Nombre risques | Budget total | Timeline |
|-----------|----------------|--------------|----------|
| 🚫 **AVOID** | 1 | Inclus | Immédiat |
| 🔄 **MITIGATE** | 7 | ~250k€ | Q4 2024 - Q2 2025 |
| 🛡️ **TRANSFER** | 2 | ~15k€/an | Q4 2024 |
| ✅ **ACCEPT** | 0 | - | - |

**Validation finale référent sécurité :** ✅ Toutes stratégies SSI/RGPD approuvées
```

### Step 5: Validation & Wrap-up (1h)

Faire valider l'ensemble des livrables de Session 4 par tous les participants : Risk Brainstorm complet (30-40 risques), Matrice 4x4 avec évaluation, 5-7 risques critiques avec risk owners assignés, Stratégies de mitigation (Avoid/Mitigate/Transfer/Accept) validées par référent sécurité. Obtenir un consensus formel via vote collectif. Présenter les éléments pour le Risk Summary du dossier COMEX. Recueillir feedbacks. Documenter parking lot items. Présenter agenda Session 5 (Decision & Recommendations).

```markdown
## Checklist Validation Session 4

□ Risk Brainstorm : 30-40 risques identifiés (4 catégories)
□ Risques catégorisés : Métier (ARM), SSI, Juridique, RGPD
□ Matrice 4x4 créée (Potentialité x Impact)
□ 5-7 risques critiques de fabrication identifiés
□ Risk Owners assignés à tous les risques critiques
□ Référent sécurité a validé risques SSI et RGPD
□ Stratégies mitigation définies (Avoid/Mitigate/Transfer/Accept)
□ Budget mitigation estimé : ~250k€
□ Parking lot items capturés
□ Prochaine session planifiée (Session 5)
□ Relecture effectuée
□ Export Markdown → PowerPoint

**✅ Consensus formel obtenu :** □ Oui (vote unanime/majorité)

📤 **Livrables pour COMEX Produit (Risk Summary) :**
- Risk Brainstorm complet (30-40 risques)
- Matrice 4x4 avec évaluation
- Top 5-7 risques critiques détaillés
- Stratégies de mitigation par risque
- Budget mitigation global
- Risk Owners assignés

**Validation référent sécurité :** ✅ [Nom] - Approuvé le [Date]
```
