# Gabarit B — la conversation (un fil de messages)

<!-- agent: orchestrateur · sujets: conversation, messages, fil, réponses proposées, boutons · source: données synthétiques, règles v1, exécution run-2026-06-01-0847 -->

## Principe
L'orchestrateur écrit à Camille. Chaque message porte une idée et le nom de l'agent qui l'a produite (« Orchestrateur · avec Achats »). Les chiffres sont en gras. Les réponses probables de Camille sont proposées en boutons ; le champ libre existe mais l'orchestrateur ne comprend que quelques formulations, et le dit.

## La séquence
1. **Ouverture** — « Bonjour Camille. L'équipe a préparé une opération pour vous — elle attend votre validation avant demain 9 h. Je vous la présente ? » Boutons : « Présente-la » · « Plus tard ».
2. **Avec la Veille** — le signal (voir 10-opportunite/opportunite-tournoi-20-juin.md, « Comment le dire »).
3. **Avec Ventes** — la cible (voir 20-cible/ciblage.md, « Comment le dire »).
4. **Avec Achats** — le point à trancher et l'arbitrage (voir 30-stock/tension-stock-premium.md, « Comment le dire »).
5. **Avec Marketing** — l'offre, une carte de quatre chiffres (commandes, chiffre d'affaires, marge, couverture premium), puis : « Sous 50 000 € : votre validation suffit. Je programme l'envoi pour demain 9 h ? »
Boutons après la présentation : « Valide » · « Pourquoi le Portugal ? » · « Et à 10 % ? » · « Et à 15 % ? » · « Voir la cible » · « Voir l'e-mail » · « Non, on arrête ».

## Les réponses à chaque question
- **Pourquoi le Portugal ?** → les trois options chiffrées, les critères, la liste des sources ; boutons « Montre les stocks », « La fiche fournisseur », « La grille de prix », « La règle de prévision », « Merci ».
- **Une source** → un extrait sous forme de petite table, signé « avec Achats ».
- **Voir la cible** → les quatre critères, le filtrage, une carte avec la fiche exemple.
- **Voir l'e-mail** → la version actifs, réécrite au taux en cours ; bouton « La version dormants ».
- **Et à 10 % ? / Et à 15 % ? / Reviens à 12 %** → message système « Achats et Marketing recalculent — stock, e-mail, impact » pendant 6 secondes, pastilles animées, puis la réponse (voir 50-prevision/scenarios-remise.md, « Comment le dire »). À 15 %, la réponse est en couleur d'attention et le bouton principal devient « Demande un second regard ».
- **Valide (à r %)** → « Vous validez : … » (la liste de ce qui part) « Je confirme et je programme ? » Boutons « Confirme » · « Attends ».
- **Confirme** → « C'est programmé. 185 e-mails partiront demain à 9 h ; jusqu'à 200 pièces par commande au prix de l'offre. Marketing et Achats sont passés à « programmé », le relais Portugal est réservé. Je reviendrai avec l'Analyse à la fin de l'offre, le 12 juin. » Bouton « Annule l'envoi ».
- **Non, on arrête** → « Entendu, je ne relance pas — l'opération est calée sur le 20 juin. Pour que la Veille apprenne : c'est plutôt… » Boutons : les trois motifs, et « Finalement non, on continue ».
- **Plus tard** → « D'accord. Je vous relance demain matin ; l'opération est calée sur le 20 juin, elle ne se reporte pas. »
- **Texte non compris** → « Je n'ai pas compris « … ». Je sais répondre à : pourquoi le Portugal, un autre taux de remise — 10, 12 ou 15 % —, la cible, l'e-mail, une source, valider, ou arrêter. »

## Règles du fil
Une idée par message. Le nom de l'agent en signature. Les seuils contrôlés dans l'action, pas seulement dans les boutons. Après une confirmation, le seul bouton est « Annule l'envoi ». Une négation (« ne valide pas ») est lue avant toute intention positive.
