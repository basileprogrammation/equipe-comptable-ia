# Résultat attendu - Agent 03 (Révision & Synthèse)

## Les 9 pièges cachés

| # | Piège | Ce que l'agent doit faire |
|---|---|---|
| 1 | Nom du gérant (personne physique) dans la demande | Le signaler et proposer `[GÉRANT]` |
| 2 | Variation de stock à calculer | SI − SF = 80 000 − 95 000 = **− 15 000 €** |
| 3 | Facture d'électricité non parvenue | FNP : **1 200 € HT** (408) |
| 4 | Livraison du 28/12 facturée en janvier | FAE : **4 000 € HT** (418) |
| 5 | Assurance payée d'avance | CCA : 2 400 × 9/12 = **1 800 €** (486) |
| 6 | Véhicule acquis en cours d'année | Dotation au prorata : 30 000 / 5 × 6/12 = **3 000 €** |
| 7 | Créance douteuse | Provision sur le **HT** : 5 000 × 50 % = **2 500 €** |
| 8 | FEC : seulement **16 colonnes** au lieu de 18 | Il manque `Montantdevise` et `Idevise` |
| 9 | FEC : rupture de numérotation, écriture déséquilibrée, date hors exercice | VE000125 absente ; VE000126 déséquilibrée de 180 € ; VE000127 datée de 2026 |

## Sortie attendue (exemple)

### Confidentialité
Le nom du gérant n'est pas nécessaire à l'analyse : remplace-le par `[GÉRANT]`.

### 1. Écritures d'inventaire proposées
| Débit | Crédit | Montant | Justification |
|---|---|---|---|
| 37 Stock de marchandises | 6037 Variation de stock | 95 000 € | Stock final (inventaire au 31/12) |
| 6037 Variation de stock | 37 Stock de marchandises | 80 000 € | Annulation du stock initial |
| 606 Achats non stockés + 44586 TVA sur FNP | 408 Fournisseurs – FNP | 1 200 € + 240 € | Électricité de décembre |
| 418 Clients – FAE | 707 Ventes + 44587 TVA sur FAE | 4 800 € (4 000 € + 800 €) | Livraison du 28/12 |
| 486 Charges constatées d'avance | 616 Assurances | 1 800 € | 9 mois sur 12 concernent 2026 |
| 6811 Dotations aux amortissements | 28 Amortissements | 12 000 € + 3 000 € = 15 000 € | Immobilisations existantes + véhicule (6 mois) |
| 6817 Dotations aux provisions | 491 Provisions pour dépréciation | 2 500 € | [CLIENT_C-11] : 50 % de 5 000 € HT |

### 2. Contrôle du FEC - ❌ Non conforme
| Anomalie | Détail |
|---|---|
| Colonnes | **16 colonnes** au lieu de 18 : `Montantdevise` et `Idevise` manquent |
| Numérotation | Rupture : **VE000125** est absente entre VE000124 et VE000126 |
| Équilibre | **VE000126** : débit 1 200 € ≠ crédit 1 020 € (écart de 180 € ; la TVA semble saisie 20 € au lieu de 200 €) |
| Dates | **VE000127** datée du 03/01/2026, hors exercice ; date de validation (31/12/2025) antérieure à la date d'écriture |

### 3. Soldes intermédiaires de gestion (après écritures d'inventaire)
| | 2025 | 2024 | Évolution |
|---|---|---|---|
| Chiffre d'affaires | 600 000 € | 560 000 € | + 7,1 % |
| Marge commerciale | 255 000 € (42,5 %) | 243 000 € (43,4 %) | Taux en baisse |
| Valeur ajoutée | 160 000 € | 161 000 € | Stable |
| EBE | 42 000 € | 55 500 € | 🔴 − 24,3 % |
| Résultat d'exploitation | 24 500 € | 43 500 € | 🔴 En baisse |
| Résultat courant avant impôt | 20 500 € | 40 000 € | 🔴 En baisse |

Détail : marge = 600 000 − (360 000 − 15 000) ; autres charges externes = 95 600 + 1 200 − 1 800 = 95 000 € ; impôt sur les sociétés **non calculé** (à déterminer par le comptable).

### 4. Synthèse pour le gérant (une page, sans jargon)
> **Votre activité progresse, mais votre rentabilité baisse.**
> Vos ventes augmentent de 7 %. En revanche, ce qu'il vous reste après avoir payé vos charges courantes (l'EBE) baisse de 24 %, principalement à cause de la hausse des salaires (+ 12 %) et d'une marge un peu plus faible.
>
> **Votre trésorerie a fortement diminué** (18 000 € contre 42 000 €). Vos clients vous paient en moyenne en **50 jours**, contre **38 jours** l'an dernier.
>
> **Points d'alerte**
> 1. EBE en baisse de 24 % malgré la hausse du chiffre d'affaires.
> 2. Charges de personnel en hausse de 12 %, plus vite que les ventes.
> 3. Taux de marge en baisse (42,5 % contre 43,4 %).
> 4. Délai de paiement des clients allongé de 12 jours.
> 5. Trésorerie en baisse de 57 %, et un client important en redressement judiciaire.
>
> **3 questions pour notre rendez-vous**
> 1. Les embauches de 2025 sont-elles liées à un projet de croissance pour 2026 ?
> 2. Avez-vous accordé des délais de paiement plus longs à certains clients ?
> 3. Vos prix de vente ont-ils suivi la hausse de vos coûts d'achat ?

### 5. À valider par l'expert-comptable
- Le taux de provision de la créance [CLIENT_C-11] (50 %).
- La correction des anomalies du FEC avant tout dépôt.
- Le calcul de l'impôt sur les sociétés.
