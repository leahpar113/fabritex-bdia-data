# L'équipe d'agents et ce que chacun signe

<!-- agent: tous · sujets: agents, orchestrateur, rôles, statuts, réel, simulé · source: données synthétiques, règles v1, exécution run-2026-06-01-0847 -->

## Six rôles
| Agent | Ce qu'il fait | Ce qu'il signe à l'étape 5 |
|---|---|---|
| **Veille** | Suit les signaux (calendrier, météo, historique), en retient un, chiffre la corrélation | L'opportunité : échéance, fenêtre de commande, effet chaleur |
| **Ventes** | Applique les critères de ciblage à l'historique, forme les deux groupes | La cible : 185 revendeurs, 112 actifs, 73 dormants, les critères, une fiche |
| **Achats & Stock** | Vérifie la couverture de stock par taille et par entrepôt, chiffre les options, propose | Le point d'arbitrage : stocks, rupture, délais fournisseurs, options |
| **Marketing** | Construit l'offre sous contrainte de marge, rédige l'e-mail en deux versions | L'offre et l'e-mail, réécrits à chaque réglage |
| **Analyse** | En attente à l'étape 5 ; revient à la fin de l'offre avec les résultats | Rien avant le 12 juin |
| **Orchestrateur** | Coordonne, arbitre le conflit de stock, calcule l'impact, présente à Camille, programme l'envoi | La décision, la prévision, la synthèse, la confirmation |

## Les statuts affichés
- ✓ · a produit sa part ; **en cours** · retravaille après un réglage ; **inchangé** · n'a pas à retravailler ; **en attente** · n'intervient pas encore ; **programmé** · a programmé sa part après validation ; **échec** · n'a pas pu programmer.
- Pendant une replanification, seuls Achats, Marketing et l'orchestrateur travaillent ; Veille et Ventes restent « inchangé ». Les boutons de décision sont inactifs tant que quelqu'un travaille.
- Une replanification vise moins de 8 secondes. Au-delà de 15 secondes, l'écran dit « l'équipe met un peu plus de temps que prévu — le dernier résultat reste affiché ».

## Réel, chargé, simulé
- **Réel** pendant le direct : Achats, Marketing et l'orchestrateur, sur des données inventées pour la démonstration.
- **Chargé** : le travail de la Veille et de Ventes, fait le matin.
- **Simulé** : l'envoi des e-mails et le quota. La confirmation les montre, elle ne les exécute pas.
- L'indicateur de mode dit « réel » ou « rejeu » (sans réseau, des réponses enregistrées sont rejouées) ; l'animateur le dit au public.
- Sur validation, Marketing et Achats passent à « programmé ». Si l'un des deux échoue, la confirmation ne s'affiche pas : l'orchestrateur retient l'envoi et propose de réessayer ou d'annuler.
