# Ca$hfl00d

**Application de bureau de gestion financière personnelle en C++/Qt : transactions, comptes, budgets, recherche et filtrage, avec une base de données SQLite intégrée.**

![C++](https://img.shields.io/badge/C%2B%2B-17-00599C?logo=cplusplus&logoColor=white)
![Qt](https://img.shields.io/badge/Qt-Widgets-41CD52?logo=qt&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-QtSql-003B57?logo=sqlite&logoColor=white)
![Statut](https://img.shields.io/badge/Statut-en%20développement-orange)

Projet de groupe réalisé dans le cadre de l'**épreuve pratique Qt 2026-2027**. Rendu prévu le **11 décembre 2026 à 23h59**.

---

## Présentation

Ca$hfl00d aide à comprendre où va son argent. L'utilisateur enregistre ses opérations financières, les range par catégorie et par compte, fixe des plafonds de dépenses et suit l'évolution de ses budgets, le tout sans connexion Internet.

Vocabulaire utilisé dans le projet :

| Terme | Définition |
|---|---|
| **Transaction** | Une opération financière (revenu ou dépense) avec un montant, une date, une catégorie et une description |
| **Compte** | Un espace financier (Mobile money, Épargne, Portefeuille…) qui regroupe des transactions |
| **Budget** | Une limite de dépenses attribuée à une ou plusieurs catégories |

## Fonctionnalités

### Obligatoires
- [ ] **Transactions** : créer, modifier, supprimer et catégoriser
- [ ] **Comptes** : créer, modifier, réorganiser et supprimer
- [ ] **Budgets et catégories** : plafonds par catégorie, suivi et alertes de dépassement
- [ ] **Recherche et filtrage** des transactions (texte, date, montant, catégorie)
- [ ] **Réinitialisation** des données

### Bonus envisagés
- [ ] Tableau de bord avec graphiques (QtCharts)
- [ ] Thème clair / sombre
- [ ] Import / export CSV et JSON
- [ ] Catégories personnalisables avec couleurs
- [ ] Transactions récurrentes

> Les cases seront cochées au fur et à mesure de l'avancement.

## Technologies

- **C++** avec **Qt Widgets** pour l'interface
- **SQLite** via le module **QtSql** pour la base de données
- **QtCharts** pour les graphiques
- **Git** et GitHub pour le travail en équipe

## Organisation du code

```
cashfl00d-qt/
├── README.md
├── CMakeLists.txt          # fichier de projet (à confirmer en équipe : CMake ou .pro)
├── src/
│   ├── main.cpp
│   ├── models/             # Transaction, Compte, Budget, Categorie
│   ├── database/           # DatabaseManager et accès aux données (SQLite)
│   ├── ui/                 # fenêtres, dialogues et widgets
│   └── utils/              # fonctions utilitaires (formats, dates, montants)
└── docs/                   # rapport, diagrammes UML, captures d'écran
```

## Base de données

Tables prévues : `accounts`, `categories`, `transactions` (avec `account_id` et `category_id`) et `budgets`.

> Le schéma exact sera **figé en début de projet** par toute l'équipe, car chaque module en dépend.

## Compiler et lancer

**Prérequis :** Qt 6 (Widgets, Sql, Charts) et Qt Creator. La version exacte est à confirmer en équipe : tout le monde doit utiliser la même.

1. Cloner le dépôt :
   ```bash
   git clone https://github.com/<organisation-ou-pseudo>/cashfl00d-qt.git
   cd cashfl00d-qt
   ```
2. Ouvrir le fichier de projet dans **Qt Creator** (`CMakeLists.txt`).
3. Choisir un kit Qt 6, puis cliquer sur **Configurer le projet**.
4. Compiler et lancer avec **Ctrl + R**.

## Équipe

| Membre | Rôle | Responsabilités |
|---|---|---|
| Membre 1 — *à compléter* | Lead technique et données | Base SQLite, `DatabaseManager`, CRUD de base, réinitialisation, fenêtre principale |
| Membre 2 — *à compléter* | Transactions | Création, modification, suppression, catégorisation, recherche et filtrage |
| Membre 3 — *à compléter* | Comptes et budgets | Comptes et réorganisation, catégories, plafonds, suivi des budgets |
| Membre 4 — *à compléter* | Rapport, interface et bonus | Graphiques, thème, import/export, rapport (UML, manuel) |

## Travail en équipe avec Git

- La branche `main` doit **toujours compiler**. Personne n'y envoie de code qui ne fonctionne pas.
- Une **branche par fonctionnalité** : `feature/db-core`, `feature/transactions`, `feature/comptes-budgets`, `feature/rapport-bonus`.
- On met à jour sa branche avant de travailler (`git pull`), on fait de petits commits clairs, puis on fusionne par *pull request* relue par un autre membre.
- Un seul propriétaire par fichier d'interface (`.ui`) pour éviter les conflits.
- On ne versionne ni les dossiers de compilation (`build-*`), ni les exécutables.

## Planning

| Période | Étape |
|---|---|
| 23 – 25 novembre | Cadrage, schéma de la base, squelette du projet compilable |
| 26 novembre – 3 décembre | Fonctionnalités obligatoires, chacun sur sa branche |
| 4 – 7 décembre | Intégration, puis bonus |
| 8 – 9 décembre | Tests croisés, corrections, rapport |
| 10 décembre | Gel du code, archive, envoi |
| 11 décembre | Marge de sécurité (rendu avant 23h59) |

## Rendu

Archive `Groupe_XX.zip` contenant :
- le **rapport** : membres, fonctionnalités, diagrammes UML (cas d'utilisation, classes, séquence) et manuel d'utilisation ;
- le **dossier du projet Qt Creator** avec le code source complet, sans exécutables.

## Licence

Projet académique. Tous droits réservés à l'équipe.
