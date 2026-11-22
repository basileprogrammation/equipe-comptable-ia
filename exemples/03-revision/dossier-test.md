# Dossier test - Agent 03 (Révision & Synthèse)

> Données fictives. Copie tout ce qui suit dans une conversation du Projet « 03 – Révision & Synthèse ».

---

Bonjour, dossier **[CLIENT_C]** (SARL, négoce de matériel). Exercice du **01/01/2025 au 31/12/2025**. Peux-tu me proposer les écritures de clôture, contrôler l'extrait de FEC et préparer la synthèse pour le rendez-vous de bilan avec le gérant, M. Paul Bernard ?

## 1. Balance avant écritures d'inventaire (en €)

| Poste | 2025 (avant inventaire) | 2024 (définitif) |
|---|---|---|
| 707 Ventes de marchandises | 596 000 | 560 000 |
| 607 Achats de marchandises | 360 000 | 322 000 |
| 6037 Variation de stock | à calculer | − 5 000 |
| 60 (hors 607) / 61 / 62 Autres achats et charges externes | 95 600 | 82 000 |
| 63 Impôts et taxes | 8 000 | 7 500 |
| 64 Charges de personnel | 110 000 | 98 000 |
| 681 Dotations aux amortissements | non passées | 12 000 |
| 66 Charges financières | 4 000 | 3 500 |

## 2. Informations de clôture
- Stock de marchandises : **80 000 €** au 01/01/2025, **95 000 €** au 31/12/2025 (inventaire physique).
- Facture d'électricité de décembre 2025 reçue le 12/01/2026 : **1 200 € HT** (TVA 240 €).
- Marchandises livrées le 28/12/2025, facturées le 05/01/2026 : **4 000 € HT** (TVA 800 €).
- Assurance payée le 01/10/2025 pour 12 mois : **2 400 €**.
- Dotation annuelle aux amortissements des immobilisations existantes : **12 000 €**.
- Véhicule utilitaire acquis le **01/07/2025** : **30 000 € HT**, amortissement linéaire sur 5 ans.
- Client [CLIENT_C-11] en redressement judiciaire : créance de **6 000 € TTC** (5 000 € HT). Risque de perte estimé à **50 %**.

## 3. Trésorerie et clients
| | 31/12/2025 | 31/12/2024 |
|---|---|---|
| Trésorerie | 18 000 € | 42 000 € |
| Créances clients (TTC) | 98 000 € | 70 000 € |
| Chiffre d'affaires TTC | 720 000 € | 672 000 € |

## 4. Extrait du FEC (journal des ventes, décembre)

```
JournalCode|JournalLib|EcritureNum|EcritureDate|CompteNum|CompteLib|CompAuxNum|CompAuxLib|PieceRef|PieceDate|EcritureLib|Debit|Credit|EcritureLet|DateLet|ValidDate
VE|Ventes|VE000123|20251215|411000|Clients|C011|[CLIENT_C-11]|F2025-311|20251215|Facture F2025-311|1200,00|0,00|||20251231
VE|Ventes|VE000123|20251215|707000|Ventes de marchandises|||F2025-311|20251215|Facture F2025-311|0,00|1000,00|||20251231
VE|Ventes|VE000123|20251215|445710|TVA collectée|||F2025-311|20251215|Facture F2025-311|0,00|200,00|||20251231
VE|Ventes|VE000124|20251218|411000|Clients|C014|[CLIENT_C-14]|F2025-312|20251218|Facture F2025-312|1500,00|0,00|||20251231
VE|Ventes|VE000124|20251218|707000|Ventes de marchandises|||F2025-312|20251218|Facture F2025-312|0,00|1250,00|||20251231
VE|Ventes|VE000124|20251218|445710|TVA collectée|||F2025-312|20251218|Facture F2025-312|0,00|250,00|||20251231
VE|Ventes|VE000126|20251220|411000|Clients|C002|[CLIENT_C-02]|F2025-314|20251220|Facture F2025-314|1200,00|0,00|||20251231
VE|Ventes|VE000126|20251220|707000|Ventes de marchandises|||F2025-314|20251220|Facture F2025-314|0,00|1000,00|||20251231
VE|Ventes|VE000126|20251220|445710|TVA collectée|||F2025-314|20251220|Facture F2025-314|0,00|20,00|||20251231
VE|Ventes|VE000127|20260103|411000|Clients|C005|[CLIENT_C-05]|F2025-315|20260103|Facture F2025-315|600,00|0,00|||20251231
VE|Ventes|VE000127|20260103|707000|Ventes de marchandises|||F2025-315|20260103|Facture F2025-315|0,00|500,00|||20251231
VE|Ventes|VE000127|20260103|445710|TVA collectée|||F2025-315|20260103|Facture F2025-315|0,00|100,00|||20251231
```
