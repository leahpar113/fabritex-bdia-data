# Les règles de décision de l'étape 5

<!-- agent: orchestrateur · sujets: décision, validation, second regard, refus, annulation, replanification, échec · source: données synthétiques, règles v1, exécution run-2026-06-01-0847 -->

## Valider
1. Camille clique « Valider » (ou répond « Valide »). L'orchestrateur montre **exactement ce qui part** : 185 destinataires (112 actifs, 73 dormants) ; l'offre exacte (remise, seuil 2 000 €, livraison le lendemain, 200 pièces par commande) ; l'envoi mardi 2 juin 2026 à 9 h, offre jusqu'au 12 juin 2026 ; le relais Portugal annoncé à 3,34 € HT ; ce qui a changé si un réglage a été touché ; l'impact estimé.
2. Camille confirme. Marketing et Achats passent à « programmé ». Confirmation en une ligne : « 185 e-mails partiront demain à 9 h ; jusqu'à 200 pièces par commande au prix de l'offre. »
3. « Annuler » reste actif jusqu'à l'envoi. Annulé : l'équipe est informée, l'opération est classée, rien n'est parti.
4. La validation est refusée par l'orchestrateur lui-même si un seuil est franchi ou si un agent travaille encore.

## Modifier (le réglage)
- Réglages possibles : la remise, à 10, 12 ou 15 % ; la cible (actifs seuls, ou Sud-Est seul).
- Qui retravaille : Marketing (offre, e-mail), Achats (couverture), l'orchestrateur (impact). Veille et Ventes : inchangé. Durée visée : moins de 8 secondes ; au-delà de 15, message « l'équipe met un peu plus de temps que prévu », le dernier résultat reste affiché.
- Pendant le travail, les décisions attendent : boutons inactifs.
- Après : les blocs modifiés sont marqués, les autres disent « inchangé » ; l'avant est rappelé à côté de l'après ; un retour au réglage initial est toujours proposé.

## Le second regard
Si l'impact dépasse 50 000 € ou si la marge passe sous 25 % : « Valider » devient « Demander un second regard ». La demande part à la direction commerciale avec la synthèse et les seuils franchis. Rien n'est programmé tant qu'elle n'a pas répondu. Dans la démo, on revient à 10 % avant de valider.

## Refuser
Trois motifs, pas de champ libre : « pas cette fois », « mauvaise cible », « mauvaise offre ». L'équipe enregistre le motif, ne relance pas, l'Analyse en tiendra compte au prochain cycle. Pas de date de reprise : l'opération est calée sur le 20 juin 2026.

## Plus tard
Si Camille ignore la notification, l'équipe relance une fois, le lendemain matin, puis classe.

## Si un agent échoue après la validation
Si Achats ne peut pas réserver le relais (ou Marketing programmer l'e-mail), l'orchestrateur retient l'envoi : « rien ne part tant que les deux ne sont pas programmés ». Il propose de réessayer ou d'annuler.
