# L'opportunité retenue : équiper les revendeurs avant le tournoi du 20 juin

<!-- agent: veille, orchestrateur · sujets: opportunité, déclenchement, tournoi, chaleur, pourquoi, signaux écartés, cycle suivant · source: données synthétiques, règles v1, exécution run-2026-06-01-0847 -->

## En bref
| | |
|---|---|
| Identifiant | OPP-2026-06-20-TOURNOI |
| Échéance | Grand tournoi de football, coup d'envoi, le 20 juin 2026 (SIG-TOURNOI-2026-06-20) |
| Fenêtre de commande des revendeurs | du 2 juin 2026 au 8 juin 2026 |
| Renfort de demande et ciblage | Pic de chaleur annoncé, Sud-Est, le 11 juin 2026 (SIG-CHALEUR-SE-2026-06-11) |
| Statut | retenue, le 1er juin 2026, par l'exécution run-2026-06-01-0847 |
| L'opération qui en découle | Opération Vague de chaleur — voir 40-offre/offre.md |

## Les signaux et leur rôle
Une opportunité repose sur un ou plusieurs signaux. Chacun y tient un rôle, parmi quatre : **échéance** (un seul par opportunité : il fixe la date), **renfort de demande**, **ciblage** (il désigne une zone ou un segment), **contrainte** (il freine : stock, coût, délai).
| Signal | Nature | Rôle | Ce qu'il apporte |
|---|---|---|---|
| SIG-TOURNOI-2026-06-20 · Grand tournoi de football, coup d'envoi | événement daté, certain | échéance | La fenêtre de commande du 2 juin 2026 au 8 juin 2026, l'envoi le 2 juin 2026, la fin de l'offre le 12 juin 2026 |
| SIG-CHALEUR-SE-2026-06-11 · Pic de chaleur annoncé, Sud-Est | prévision, confiance 60 %, réévaluée le 6 juin 2026 | renfort de demande, ciblage | Une demande plus forte de t-shirts légers, la priorité aux 50 revendeurs du Sud-Est, l'accroche de l'e-mail |
Le tournoi seul aurait suffi à déclencher une opération, plus modeste et sans zone prioritaire. La chaleur seule n'aurait rien déclenché : une prévision à 60 % ne fixe pas de date.

## Déclenchement
La règle (voir regle-de-declenchement.md), appliquée ici :
1. **Une échéance certaine induit une fenêtre de commande** : SIG-TOURNOI-2026-06-20, le 20 juin 2026 → les revendeurs commandent du 2 juin 2026 au 8 juin 2026 (enchaînement des délais : J−18 à J−12).
2. **Il reste assez de jours pour agir** : l'e-mail part le 2 juin 2026, 18 jours avant le coup d'envoi, à l'ouverture de la fenêtre.
3. **Un renfort de demande tombe entre l'ouverture de la fenêtre et l'échéance** : le pic de chaleur du 11 juin 2026 est entre le 2 juin 2026 et le 20 juin 2026 ; les clients finaux veulent leurs t-shirts pour la chaleur et pour le tournoi. Ce renfort est facultatif : il augmente l'intérêt de l'opportunité, il ne la conditionne pas.

## Ce qui dépend de chaque signal
| | Du tournoi | De la chaleur |
|---|---|---|
| La date d'envoi, la fin de l'offre, la fenêtre de commande | oui | non |
| La zone prioritaire (Sud-Est) et l'accroche de l'e-mail | non | oui |
| Le produit mis en avant (le t-shirt blanc léger) | en partie | oui |
| Les chiffres de la prévision (commandes, chiffre d'affaires, marge) | non | **non** — la règle de prévision n'utilise pas d'effet chaleur ; voir 50-prevision/regle-de-prevision.md |
Les hausses mesurées dans l'historique portent sur les ventes de t-shirts en général. Qu'elles s'appliquent au premium blanc, aux tailles L et XL, aux polos et au sport est une hypothèse métier, pas une mesure.

## Si la chaleur ne vient pas
La prévision est réévaluée le 6 juin 2026, c'est-à-dire **après l'envoi** du 2 juin 2026 : elle ne peut plus faire tomber l'opération. Ce qui change si le pic disparaît : la priorité Sud-Est n'a plus de raison, le réglage « Sud-Est seul » n'est plus proposé, l'accroche des relances change. Ce qui ne change pas : l'échéance, l'offre, la cible, les chiffres attendus. Perte chiffrée : aucune dans la prévision, puisqu'elle n'utilise pas la chaleur ; l'Analyse mesurera l'écart réel le 12 juin 2026.

## Les autres signaux, et pourquoi pas
47 signaux actifs, examinés le 1er juin 2026 — 2 retenus, qui forment une opportunité ; 1 reporté ; 44 écartés. Les motifs d'écart, avec leur effectif :
| Motif | Ce que ça veut dire | Signaux |
|---|---|---|
| pas de demande textile | ne fait pas commander de textile en volume aux revendeurs | 13 |
| déjà couvert | les revendeurs concernés sont déjà dans la cible de l'opération retenue | 13 |
| hors fenêtre | la fenêtre de commande qu'il induit est passée, ou trop loin pour agir maintenant | 10 |
| probabilité insuffisante | prévision trop incertaine, ou zone trop petite, pour justifier une opération | 4 |
| contrainte, pas une demande | pèse sur les coûts ou les délais ; il est transmis à Achats, il ne déclenche pas d'opération | 4 |
Trois cas nommés :
- **Fête de la musique**, le 21 juin 2026 : datée, mais elle ne fait pas commander de textile en volume aux revendeurs. Écartée.
- **Fin de saison des clubs, tournois amateurs**, le 27 juin 2026 : sa fenêtre de commande irait du 9 juin 2026 au 15 juin 2026, en plein pendant l'offre en cours et sur la même cible. La règle interdit deux opérations sur une même cible à moins de 15 jours. Reportée, prochain examen le 12 juin 2026, au bilan de l'Analyse.
- **La chaleur seule**, sans échéance : suivie, jamais déclenchée.
La liste complète est dans signaux-suivis.md.

## Le cycle suivant
Le 12 juin 2026, l'Analyse rend son bilan et la Veille réexamine SIG-FIN-SAISON-2026-06-27 avec ce bilan : quels métiers ont répondu, quels dormants sont revenus. C'est ce que la version tablette montrera après le salon.

## Comment le dire
« Le tournoi du 20 juin fixe l'échéance : vos revendeurs commandent du 2 au 8 juin. Un pic de chaleur est annoncé le 11, et sur les trois derniers épisodes les ventes de t-shirts ont monté de 19 à 37 %. 47 signaux suivis, une opportunité retenue, appuyée sur deux signaux. »
