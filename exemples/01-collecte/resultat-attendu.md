# Résultat attendu - Agent 01 (Collecte & Confidentialité)

## Les 6 pièges cachés

| # | Piège | Ce que l'agent doit faire |
|---|---|---|
| 1 | Nom et téléphone d'une personne physique dans une note de frais | Le signaler **en premier** et proposer une pseudonymisation : `[TIERS_01]`, téléphone supprimé |
| 2 | Relevé bancaire de **décembre** manquant | Pièce manquante **bloquante** (pas de rapprochement possible à la clôture) |
| 3 | Factures d'achats de **décembre** manquantes | Pièce manquante **importante** (risque de charges oubliées ou de factures non parvenues) |
| 4 | Contrat d'emprunt sans **tableau d'amortissement** | À demander : nécessaire pour ventiler intérêts et capital |
| 5 | Pas d'**inventaire des stocks** au 31/12 alors qu'il s'agit d'un commerce | Pièce manquante **bloquante** pour la clôture |
| 6 | **Courrier du SIE** non ouvert | Point d'alerte : à lire en priorité (possible relance ou contrôle) |

## Sortie attendue (exemple)

###  Alerte confidentialité
- Note de frais « Reçu restaurant » : **nom** et **numéro de téléphone** d'une personne physique. Remplace-les par `[TIERS_01]` et supprime le téléphone, qui n'est pas utile à la comptabilisation. Garde la correspondance hors de cette conversation.

### Inventaire des pièces - T4 2025
| Pièce | Période | Statut | Priorité |
|---|---|---|---|
| Relevés bancaires | Octobre, novembre | Reçue | - |
| Relevé bancaire | Décembre | **Manquante** | 🔴 Bloquante |
| Factures de ventes | Octobre à décembre | Reçue | - |
| Factures d'achats | Décembre | **Manquante** | 🟠 Importante |
| Notes de frais | T4 | Reçue (4) | - |
| Tableau d'amortissement de l'emprunt | 2025 | **Manquant** | 🟠 Importante |
| Inventaire des stocks | 31/12/2025 | **Manquant** | 🔴 Bloquante |
| Courrier du SIE | 02/12/2025 | Reçu, **non lu** | 🔴 À traiter |

### Questions sur le compte 471
1. **14/10 - Prélèvement « ABONNEMENT XYZ », 89,90 €** : de quel abonnement s'agit-il ? Merci de joindre la facture.
2. **22/11 - Virement reçu « REF 7781 », 2 400 €** : quel client a payé et quelle facture ce paiement règle-t-il ?
3. **05/12 - Achat par carte « AMZN MKTP », 312,45 €** : quel est l'objet de l'achat (fourniture, matériel, dépense personnelle) ? Merci de joindre la facture.

### Brouillon de relance n°1
> **Objet : Dossier 2025 - pièces à nous transmettre avant le [date + 8 jours]**
>
> Madame, Monsieur,
>
> Afin de préparer la clôture de votre exercice 2025, pourriez-vous nous transmettre d'ici le **[date + 8 jours]** :
> - le relevé bancaire de **décembre 2025** ;
> - les factures d'achats de **décembre 2025** ;
> - le **tableau d'amortissement** de votre emprunt ;
> - l'**inventaire de vos stocks** au 31/12/2025 ;
> - les justificatifs des 3 opérations ci-dessous : [liste des questions sur le compte 471].
>
> Nous avons également bien noté le courrier du SIE du 02/12/2025, que nous examinons.
>
> Nous restons à votre disposition pour toute question.
>
> Bien cordialement,
> [Signature du cabinet]
