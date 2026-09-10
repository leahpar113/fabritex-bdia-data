# Gabarit A — le dossier (un seul écran)

<!-- agent: orchestrateur · sujets: dossier, écran, blocs, libellés, boutons, panneau pourquoi · source: données synthétiques, règles v1, exécution run-2026-06-01-0847 -->

## L'écran, de haut en bas
1. **Barre des agents** : [NOM] · CONSOLE — Veille ✓ · Ventes ✓ · Achats ✓ · Marketing ✓ · Analyse · en attente · Orchestrateur ✓ — mode · réel.
2. **Titre** : « Opération Vague de chaleur — prête à valider ». Sous-titre : « Tournoi le 20 juin, commandes revendeurs attendues du 2 au 8 · chaleur annoncée le 11 qui renforce la demande ».
3. **Rangée 1**
   - Calendrier — « Envoi mardi 9 h · offre jusqu'au 12 » — échéance : coup d'envoi du 20 juin · données au 1er juin · exécution 08:47.
   - Cible — « 185 revendeurs » — 112 actifs · 73 dormants · 235 éligibles, 11 opposants retirés · liens « 4 critères ▸ », « une fiche ▸ ».
   - Offre — « −12 % dès 2 000 € » — livraison le lendemain garantie, Milan J+2 · jusqu'à 200 pièces par commande · liens « Voir l'e-mail ▸ », « Régler la remise ▸ ».
4. **Point d'arbitrage · Achats + Orchestrateur** — « Le premium blanc ne couvre pas l'opération ; relais sur le même t-shirt fabriqué au Portugal. » Deux fiches côte à côte : TS-165-BLA (Bangladesh, 2 908 en stock, 4 290 demandés, rupture jour 6,8, L/XL jour 4,0, réappro 8 sem.) → puis → TS-165-EU-BLA (Portugal, 5 368 en stock, même produit, 3,34 € HT contre 3,05 € HT, réassort 2 sem., couvre 19,3 j en cumul). Liens « Pourquoi ▸ », « Les deux autres options ▸ ».
5. **Impact estimé · Orchestrateur** — « 33 commandes · 46 800 € · marge 25,3 % soit 11 840 € » — 18 % de la cible, panier moyen après remise · sous votre plafond de 50 000 € · au-dessus du plancher de marge de 25 %.
6. **Trois boutons** : « Valider l'envoi » (principal) · « Régler la remise » · « Refuser… ».

## Le panneau « pourquoi », quatre étages puis l'exécution
- **Décision · Orchestrateur** : Premium d'abord, fabrication Portugal en relais : même produit, +9 % annoncé dans l'e-mail.
- **Les trois options · Achats** : les trois options avec leur chiffre d'affaires et leur verdict (voir 30-stock/tension-stock-premium.md).
- **Critères** : couverture, demande, délai, marge, disponibilité — chacun signé.
- **Sources** : stocks par taille au 1er juin ▸ · fiche fournisseur, avis de retard ▸ · grille de prix 2026 ▸ · règle de prévision ▸ — chacune s'ouvre sur un extrait.
- **Exécution** : run-2026-06-01-0847 · 08:47:12 · règles v1 · données synthétiques.
Le même panneau sert à « Cible » (critères, filtrage, groupes, fiche), à « Offre » (l'e-mail en deux versions) et à « Impact » (la règle de prévision).

## Le panneau « Régler la remise »
Trois taux directement sélectionnables : 10 % · 12 % · 15 %. Sous les taux, la phrase d'écart (voir 50-prevision/scenarios-remise.md). Puis « Régler · cible » : actifs seuls, ou Sud-Est seul.

## L'écran après un réglage
- Titre : « Opération Vague de chaleur — mise à jour », sous-titre « Remise passée de 12 % à 10 % · replanifiée en 6 s ».
- Pendant le travail : titre « mise à jour en cours », barre de progression, agents « en cours », boutons inactifs, l'ancien résultat reste affiché.
- Après : Offre et Impact marqués « modifié », Cible « inchangé », l'avant rappelé (« avant : 33 · 46 800 € · 11 840 € — 1,6 point de marge de plus, 515 € de marge en moins »). Boutons : « Revenir à 12 % » · « Valider à 10 % » · « Refuser… ».
- À 15 % : Impact en couleur d'attention, « deux seuils franchis », « Valider — indisponible », « Demander un second regard ».

## Après validation
Aperçu (« Vous validez », liste de ce qui part) → « Confirmer l'envoi » → « Opération Vague de chaleur — programmée » avec la phrase de confirmation, agents Achats et Marketing « programmé », bouton « Annuler l'envoi », mention « envoi et quota simulés ».
