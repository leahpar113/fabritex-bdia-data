# La règle de déclenchement d'une opportunité

<!-- agent: veille, orchestrateur · sujets: règle, déclenchement, signaux, rôles, statuts, motifs, fenêtre · source: données synthétiques, règles v1, exécution run-2026-06-01-0847 -->

## Le vocabulaire
- **Un signal** : une information suivie par la Veille. Trois natures : **événement daté** (certain, il ne change plus, connu longtemps à l'avance) ; **prévision** (probabiliste, avec un indice de confiance et une date de réévaluation) ; **tendance** (une série observée : ventes, prix, délais).
- **Une opportunité** : une possibilité d'action commerciale, appuyée sur un ou plusieurs signaux, chacun avec un rôle. C'est ce que la Veille propose.
- **Une opération** : l'action préparée à partir d'une opportunité — l'offre, la cible, l'e-mail, la prévision. C'est ce que Ventes, Marketing et l'Orchestrateur construisent, et ce que Camille valide. Elle est décrite dans 40-offre/ et 50-prevision/.

## Les rôles d'un signal dans une opportunité
| Rôle | Combien | Ce qu'il fait |
|---|---|---|
| échéance | exactement un | Fixe la date : il induit une fenêtre de commande |
| renfort de demande | zéro ou plusieurs | Augmente l'intérêt, sans conditionner l'opportunité |
| ciblage | zéro ou plusieurs | Désigne une zone ou un segment prioritaire |
| contrainte | zéro ou plusieurs | Freine : stock, coût, délai. Transmis à Achats |

## Les trois conditions
1. **Une échéance certaine induit une fenêtre de commande.** Seul un événement daté peut tenir le rôle d'échéance. La fenêtre va de J−18 à J−12 avant l'événement, en jours calendaires, d'après l'enchaînement des délais (voir 00-contexte/distributeur.md).
2. **Il reste assez de jours pour agir** : l'e-mail doit partir au plus tard à l'ouverture de la fenêtre.
3. **Un renfort, s'il y en a un, tombe entre l'ouverture de la fenêtre et l'échéance.** Le renfort est facultatif : une échéance seule suffit à déclencher, plus modestement.
Une prévision ne peut jamais tenir le rôle d'échéance.

## Ce que dit l'historique
Ce sont des mesures sur les ventes de t-shirts, tous produits, dans une fenêtre de mesure propre à chaque type de signal :
- tournoi majeur : fenêtre de mesure J−22 à J−8 ; deux tournois mesurés, +29 % et +27 % ;
- épisode de chaleur au-dessus de 32 °C : fenêtre de mesure J−18 à J−8 avant le pic ; trois épisodes, de +19 à +37 %.
Ces mesures justifient de retenir un signal. Elles n'entrent pas dans la prévision de l'opération, qui repose sur un taux de commande et un panier (voir 50-prevision/regle-de-prevision.md).

## Les décisions et leurs motifs
À chaque examen, chaque signal actif reçoit une décision : **retenu** (il entre dans une opportunité), **reporté** (avec une date de prochain examen), **écarté** (avec un motif). Les motifs :
| Motif | Ce que ça veut dire |
|---|---|
| hors fenêtre | la fenêtre de commande qu'il induit est passée, ou trop loin pour agir maintenant |
| pas de demande textile | ne fait pas commander de textile en volume aux revendeurs |
| probabilité insuffisante | prévision trop incertaine, ou zone trop petite, pour justifier une opération |
| déjà couvert | les revendeurs concernés sont déjà dans la cible de l'opération retenue |
| cible en collision | toucherait la même cible à moins de quinze jours d'une opération en cours |
| contrainte, pas une demande | pèse sur les coûts ou les délais ; il est transmis à Achats, il ne déclenche pas d'opération |
Règle de non-collision : pas deux opérations sur une même cible à moins de 15 jours ; le signal est reporté au bilan de l'opération en cours.

## Les conventions
Les fenêtres sont en jours calendaires avant la date de l'événement ou du pic. Les délais logistiques (livraison, marquage) sont en jours ouvrés. Chaque signal porte la date où il a été vu pour la première fois et la date de son dernier examen ; une opportunité porte l'exécution qui l'a créée.
