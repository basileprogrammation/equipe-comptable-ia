# Résultat attendu — Agent 02 (Banque & TVA)

## Les 7 pièges cachés

| # | Piège | Ce que l'agent doit faire |
|---|---|---|
| 1 | Nom d'un particulier et IBAN complet dans un libellé bancaire | Le signaler **en premier** et proposer `[TIERS_01]` / `[IBAN_1]` |
| 2 | Écart de rapprochement inexpliqué de **90 €** | Le calculer et le signaler, sans le « forcer » |
| 3 | Frais bancaires et virement reçu non comptabilisés | Proposer les écritures à passer |
| 4 | [FOURNISSEUR_03] payé **deux fois** | Signaler le doublon (fournisseur débiteur de 960 €) |
| 5 | [CLIENT_A-05] : règlement partiel | Reste dû : **400 €** |
| 6 | TVA collectée sous-évaluée de **200 €** | 40 000 × 20 % = 8 000 € et non 7 800 € |
| 7 | Autoliquidation de l'achat intracommunautaire non constatée | 5 000 × 20 % = **1 000 €** à constater en 4452 **et** en TVA déductible |

## Sortie attendue (exemple)

### ⚠️ Alerte confidentialité
Le libellé du virement du 28/03 contient un **nom de particulier** et un **IBAN complet**. Remplace-les par `[TIERS_01]` et `[IBAN_1]`.

### État de rapprochement au 31/03/2026
| Côté banque | Montant |
|---|---|
| Solde du relevé | 12 480,00 € |
| − Chèque n°4521 non encaissé | − 2 500,00 € |
| + Remise n°88 non créditée | + 3 005,00 € |
| **Solde bancaire rapproché** | **12 985,00 €** |

| Côté comptabilité | Montant |
|---|---|
| Solde du compte 512 | 11 320,00 € |
| − Frais bancaires à comptabiliser | − 45,00 € |
| + Virement reçu à comptabiliser | + 1 800,00 € |
| **Solde comptable rapproché** | **13 075,00 €** |

🔴 **Écart inexpliqué : 90,00 €** (le solde comptable est supérieur au solde bancaire).
Pistes : une écriture de 90 € en trop au débit du 512, ou une inversion de chiffres dans un montant (par exemple 1 845 saisi au lieu de 1 755). À rechercher dans les écritures de mars.

**Écritures proposées :**
- 627 Services bancaires / 512 Banque : **45,00 €**
- 512 Banque / 411 [TIERS_01] (ou 471 si le client n'est pas identifié) : **1 800,00 €**

### Lettrage
| Tiers | Statut | Action |
|---|---|---|
| [FOURNISSEUR_02] | ✅ Soldé (1 440 €) | Lettrer |
| [FOURNISSEUR_03] | 🔴 **Payé deux fois** : solde débiteur de 960 € | Demander un avoir ou un remboursement |
| [CLIENT_A-05] | 🟠 Reste dû : **400 €** | Relancer le client ou vérifier un éventuel escompte ou litige |

### Récapitulatif TVA — mars 2026
| | Attendu | Comptabilisé | Écart |
|---|---|---|---|
| TVA collectée (40 000 × 20 %) | 8 000,00 € | 7 800,00 € | 🔴 − 200,00 € |
| TVA autoliquidée (4452) : 5 000 × 20 % | 1 000,00 € | 0,00 € | 🔴 − 1 000,00 € |
| TVA déductible sur biens et services | 3 100,00 € + 1 000,00 € (autoliquidation) | 3 100,00 € | 🔴 − 1 000,00 € |

- TVA nette **avec les chiffres actuels** : 7 800 − 3 100 = **4 700,00 €**
- TVA nette **après corrections** : (8 000 + 1 000) − (3 100 + 1 000) = **4 900,00 €**
- L'autoliquidation est neutre sur le montant à payer, mais elle doit **figurer sur la CA3** (acquisitions intracommunautaires).

### À valider par le comptable
1. Rechercher la cause de l'écart de 90 €.
2. Rechercher la cause des 200 € de TVA collectée manquants (par exemple, une facture de 1 000 € HT saisie sans TVA).
3. Passer l'écriture d'autoliquidation (4452 / 44566 : 1 000 €).
4. Traiter le doublon de paiement de [FOURNISSEUR_03].
