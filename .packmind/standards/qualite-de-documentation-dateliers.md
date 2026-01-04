# Qualité de Documentation d'Ateliers

Assurer la qualité et la cohérence de tous les livrables produits lors des workshops (études d'opportunité, cadrages, ateliers décisionnels). Applicable à tous les types d'ateliers dans l'organisation, avec une priorité sur la langue française et l'utilisation de formats Markdown comme trame, exportables vers PowerPoint.

## Rules

* **Utiliser le français exclusivement** dans tous les livrables métier (questions, listes, descriptions, titres) - Pas de mélange français-anglais. Remplacer les termes anglais par des équivalents français : "attendees" → "participants", "deliverables" → "livrables", "stakeholders" → "parties prenantes", "milestone" → "jalon", etc.
* **Créer et maintenir un glossaire centralisé français-anglais** pour tous les termes métier et techniques utilisés dans l'étude
  - Format : Tableau Markdown avec colonnes Français / Anglais / Définition / Contexte
  - Emplacement : Fichier indépendant GLOSSAIRE-[NomProjet].md à la racine du projet
  - Mise à jour : Après chaque session, ajouter les nouveaux termes découverts
  - Validation : Relecteur métier responsable de validation traductions
  - Règles de traduction appliquées : Acronymes techniques (VMOA, RAD, LAD, RPA, etc.) conservés en anglais + traduction française parallèle fournie
* Utiliser l'infinitif pour tous les objectifs, livrables et actions dans les documents français
* Créer des templates Markdown (.md) comme trame d'atelier avant de générer les slides PowerPoint
* Désigner un relecteur pour valider grammaire, terminologie et mise en forme avant diffusion
* Utiliser une terminologie cohérente entre toutes les sessions (référencer le glossaire centralisé)
* Rédiger en français tous les livrables métier ; les annexes techniques peuvent utiliser l'anglais si approprié
* Inclure des checklists de validation dans tous les templates pour garantir la complétion avant diffusion
* Exporter les livrables finaux vers PowerPoint en utilisant le template organisation après validation Markdown
* Valider explicitement que toutes les questions d'un step ont reçu une réponse avant de passer au step suivant, sauf si l'absence de réponse est documentée comme "information non disponible"
* Utiliser des tableaux Markdown pour représenter les processus, flux et diagrammes Swimlane plutôt que de l'ASCII art, en structurant par phases logiques
* **RÈGLE CRITIQUE : Chiffrage scénarios uniquement sur base prérequis validés**
  - ❌ **INTERDIT** : Proposer budgets/ROI/payback sans base de règles métier + architecture technique + volumétrie confirmée
  - ✅ **OBLIGATOIRE** : Proposer analyse qualitative trade-offs (scope, durée, risque) même sans budget
  - ✅ **OBLIGATOIRE** : Lister exhaustivement tous prérequis manquants par domaine (règles métier, technologie, volumétrie, dépendances)
  - ✅ **OBLIGATOIRE** : Plan de détail 3-4 semaines pour affiner prérequis avant chiffrage fin
  - Format acceptable : "PLACEHOLDER indicatif (ordre de grandeur uniquement) : X-Y M€ à affiner après validation prérequis"
  - Sortie Session 3 réaliste : Scénario candidate retenu (soumis validation prérequis) + liste prérequis détaillée + plan affinage 3 semaines
