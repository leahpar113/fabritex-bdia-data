# Corpus du RAG — étape 5, la validation

42 documents, générés depuis `pistes/donnees/*.json` par `Section5-demo/construire_data.py`. Relancer le script après toute régénération des données : les chiffres des documents sont ceux des données, pas des copies à la main.

## Ce que le corpus permet
Donner à l'orchestrateur et aux agents Achats, Marketing, Veille et Ventes tout ce qu'il faut pour :
- présenter l'opération à Camille, dans le **dossier** (un écran) comme dans la **conversation** (un fil) — les deux gabarits sont dans `60-presentation/` ;
- répondre à « pourquoi » avec les options, les critères signés et les sources ouvrables ;
- replanifier quand la remise change (10, 12, 15 %) : prévision, couverture de stock, e-mail réécrit ;
- appliquer les règles de décision : plafond, plancher, second regard, refus, annulation, échec d'un agent.

## Organisation
| Dossier | Agent principal | Contenu |
|---|---|---|
| `00-contexte/` | tous | le distributeur, Camille, l'équipe, le calendrier, les entrepôts, la saisonnalité des ventes, l'exécution |
| `10-opportunite/` | Veille, Orchestrateur | l'opportunité retenue et ses deux signaux, la règle de déclenchement, les 47 signaux suivis avec leur motif, les opérations passées |
| `20-cible/` | Ventes | les critères, le filtrage, les 185 revendeurs ciblés (CSV), les opposants, la base complète des 2 400 revendeurs (CSV), leur répartition, six portraits |
| `30-stock/` | Achats | la tension de stock, les stocks des deux références par taille, le catalogue complet (fiches et CSV), les stocks de tout le catalogue (MD + CSV), fournisseurs, prix |
| `40-offre/` | Marketing | l'offre, les deux e-mails avec le taux en variable |
| `50-prevision/` | Orchestrateur | la règle de prévision, les trois scénarios (MD + JSON), les règles de décision |
| `60-presentation/` | Orchestrateur, animateur | les deux gabarits, les règles de style, le script |

## Formats et indexation
- **Markdown** pour ce qui se lit : un sujet par fichier, un titre, un commentaire d'en-tête avec l'agent et les sujets, des sections de niveau 2 courtes. Indexer par section (un chunk par `##`) suffit ; chaque section se comprend seule.
- **CSV** (séparateur `;`, UTF-8) pour les tables longues : à charger dans une structure interrogeable, pas à vectoriser ligne par ligne.
- **JSON** pour ce qui se calcule : les scénarios de remise, les épisodes, le catalogue. À exposer comme outil de lecture plutôt qu'à vectoriser.
- `manifest.json` liste chaque document avec son agent, ses sujets et un résumé : utile pour filtrer la recherche par agent.

## Ce qui n'y est pas, volontairement
Les résultats de campagne (étape 6) : ils n'existent pas encore au moment de la validation. Le détail des 136 333 commandes : résumé mois par mois dans la saisonnalité et par gamme pour la cible ; la ligne à ligne n'apporterait rien à l'étape 5.

## Conventions
Prix hors taxes, délais en jours ouvrés, espaces insécables avant € et %, chiffres avec leur effectif. Le distributeur s'appelle « Fabritex » jusqu'à décision. Données synthétiques, règles v1, exécution run-2026-06-01-0847.
