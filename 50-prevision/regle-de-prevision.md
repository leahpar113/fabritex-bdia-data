# La règle de prévision

<!-- agent: orchestrateur · sujets: prévision, règle, conversion, marge, élasticité, demande · source: données synthétiques, règles v1, exécution run-2026-06-01-0847 -->

## La règle
18 % des ciblés commandent, panier moyen × 1.0 après remise ; marge = taux de marque de l'assortiment après remise, moins 3.5 points de coûts logistiques.
- **Conversion** : 18 % des 185 revendeurs ciblés commandent à 12 %.
- **Élasticité** : +6 % de commandes par point de remise — chaque point de remise en plus (ou en moins) change le nombre de commandes de 6 %.
- **Panier** : le panier moyen de la cible (1 612 €) après remise.
- **Marge** : le taux de marque de l'assortiment après remise, moins 3,5 points de coûts logistiques.
- **Demande en pièces** : commandes × 130 pièces de blanc par commande — c'est ce qui sert à la couverture de stock.

## Les seuils qu'elle contrôle
- Plafond de validation seule : 50 000 € de chiffre d'affaires estimé.
- Plancher de marge : 25 %.
Quand l'un des deux est franchi, l'orchestrateur le dit dans le bloc « impact », et la validation seule devient impossible.
