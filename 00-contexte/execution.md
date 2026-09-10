# Identité de l'exécution et traçabilité

<!-- agent: orchestrateur · sujets: exécution, traçabilité, sources, rejeu · source: données synthétiques, règles v1, exécution run-2026-06-01-0847 -->

## L'exécution
- Identifiant : **run-2026-06-01-0847** · 08:47:12, le 1er juin 2026.
- Règles : version 1. Données : synthétiques, générées par les règles.
- Mode : « réel » quand les agents tournent sur la plateforme ; « rejeu » quand des réponses enregistrées sont rejouées, sans réseau. Le mode est affiché en permanence et dit au public.

## Les sources que le « pourquoi » ouvre
| Source | Ce qu'elle contient | Fichier du corpus |
|---|---|---|
| Stocks par taille au 1er juin 2026 | TS-165-BLA et TS-165-EU-BLA, par entrepôt et par taille | 30-stock/stocks-ts165.csv |
| Fiche fournisseur, avis de retard | Textil Nova, conteneur retardé ; Malhas do Douro | 30-stock/fournisseurs.md |
| Grille de prix 2026 | Prix revendeur HT des deux références, marge | 30-stock/grille-prix-2026.md |
| Règle de prévision | Conversion, panier, marge, élasticité | 50-prevision/regle-de-prevision.md |

## Ce que chaque chiffre porte
Chaque chiffre affiché est signé par l'agent qui l'a produit (Achats pour le stock, l'orchestrateur pour la demande et la marge, Ventes pour la cible, Marketing pour l'offre) et peut être suivi jusqu'à sa source.
