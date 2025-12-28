## <a name="swimlane-diagram"></a>🏊 2. Swimlane Diagram - Processus As-Is

### Vue d'ensemble du processus DPJ

Le diagramme ci-dessous présente le flux de bout en bout du processus DPJ, depuis la création du dossier jusqu'au transfert en GED CATS.

#### Phase 1 : Création et Reproposabilité

| Acteur | Action | Description |
|--------|--------|-------------|
| **Parcours Produit** | Création acte bancaire | Initialisation d'un nouvel acte bancaire |
| **Parcours Produit** | Définition liste documents | Définition des documents attendus avec règles ET/OU (200 types d'actes) |
| **Parcours Produit** | Création dossier DPJ | Création du dossier de pièces justificatives |
| **Système DPJ** | Reproposabilité | Recherche automatique de documents existants AVANT notification client |
| **GED CATS** | Recherche documents valides | Recherche dans le patrimoine GED des documents du client encore valides |
| **Stockage Documents** | Recherche documents en attente | Recherche dans les documents en attente de mise en GED |
| **Système DPJ** | Documents reproposés trouvés | Récupération des documents trouvés (invisibles au client, visibles conseiller) |

#### Phase 2 : Notification et Dépôt Client

| Acteur | Action | Description |
|--------|--------|-------------|
| **Système DPJ** | Notification client | Notification au client de la liste des documents manquants uniquement |
| **Client** | Consultation liste | Consultation des documents requis (uniquement ceux manquants) |
| **Client** | Dépôt documents | Dépôt via Portail client, App mobile ou en Agence |
| **Système DPJ** | Stockage documents | Stockage avec statut "Déposé" |

#### Phase 3 : Validation

| Acteur | Action | Description |
|--------|--------|-------------|
| **Conseiller Agence** | Consultation dossier | Consultation du dossier complet : documents déposés + documents reproposés |
| **Conseiller Agence** | Validation documents reproposés | Validation manuelle des documents trouvés par reproposabilité |
| **Conseiller Agence** | Validation documents déposés | Validation manuelle des documents déposés par le client |
| **OU** | **OU** | **Deux chemins de validation possibles** |
| **Système RAD/LAD** | Validation automatique | Si type document compatible : Reconnaissance + Extraction + Comparaison |

#### Phase 4 : Traitement Automatique (RAD/LAD)

| Étape | Action | Description |
|-------|--------|-------------|
| **1** | Reconnaissance type document | Identification automatique du type de document (RAD) |
| **2** | Extraction données | Lecture automatique des données du document (LAD) |
| **3** | Comparaison données parcours | Comparaison avec les données saisies dans le parcours produit |
| **4** | Résultat | Si OK → Validation auto / Si KO → Statut Rejeté |

#### Phase 5 : Finalisation

| Acteur | Action | Description |
|--------|--------|-------------|
| **Système DPJ** | Statut "Validé" | Document validé (manuellement ou automatiquement) |
| **Système DPJ** | Transfert GED CATS | Transfert du document validé vers la GED métier |
| **Système DPJ** | Statut "En GED" | Document archivé en GED CATS |

### Workflow des statuts documents
Déposé → (Issue reproposabilité) → En traitement → Validé/Rejeté → En GED


### Points clés du processus

**🔑 Reproposabilité (invisible au client)**
- Recherche automatique dans GED CATS + Documents en attente AVANT notification client
- Documents reproposés visibles UNIQUEMENT par le conseiller
- Le client ne voit que les documents manquants

**🔑 Validation double chemin**
- **Chemin 1** : Validation manuelle par conseiller (99% actuellement)
- **Chemin 2** : Validation automatique RAD/LAD (1% actuellement)
- Si RAD/LAD possible pour le type de document → toujours exécuté

**🔑 Canaux de dépôt multi-canal**
- Portail client (selfcare)
- Application mobile
- En agence avec conseiller

**🔑 Règles ET/OU**
- Possibilité de définir des documents alternatifs (OU)
- Possibilité de définir des ensembles de documents obligatoires (ET)

### Vue synthétique du flux

## 🏊 Swimlane Diagram - Processus DPJ

| PARCOURS PRODUIT | SYSTÈME DPJ | GED CATS | STOCKAGE DOCUMENTS | CLIENT | CONSEILLER AGENCE |
|------------------|-------------|----------|-------------------|--------|-------------------|
| **Création acte bancaire** | | | | | |
| ↓ | | | | | |
| **Définition liste documents** (règles ET/OU) | | | | | |
| ↓ | | | | | |
| **Création dossier** → | | | | | |
| | **Dossier créé** | | | | |
| | ↓ | | | | |
| | **REPROPOSABILITÉ** | | | | |
| | ↓ Recherche → | **Recherche docs client valides** | | | |
| | ↓ Recherche → | | **Recherche docs en attente** | | |
| | ← Résultats | | | | |
| | **Docs reproposés trouvés** | | | | |
| | ↓ | | | | |
| | **Notification client** → | | | **Consultation liste manquants** | |
| | | | | ↓ | |
| | | | | **Dépôt documents** (Portail/App/Agence) | |
| | ← **Stockage** | | | | |
| | **Statut: Déposé** | | | | |
| | ↓ Notification → | | | | **Consultation dossier complet** |
| | | | | | ↓ |
| | | | | | **Validation docs reproposés** |
| | | | | | ↓ |
| | | | | | **Validation docs déposés** |
| | ← **Statut: Validé** | | | | |
| | ↓ | | | | |
| | **RAD/LAD** (si compatible) | | | | |
| | • Reconnaissance type | | | | |
| | • Extraction données | | | | |
| | • Comparaison parcours | | | | |
| | ↓ | | | | |
| | **Statut: Validé** | | | | |
| | ↓ | | | | |
| | **Transfert GED CATS** → | **Stockage** | | | |
| | **Statut: En GED** | | | | |
