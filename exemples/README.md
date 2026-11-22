# Exemples : tester les 3 agents en 5 minutes

Chaque agent a un **faux dossier client** (données 100 % fictives) avec des **pièges volontaires**, et le **résultat attendu** pour vérifier que l'agent les détecte.

| Agent | Dossier test | Résultat attendu | Pièges cachés |
|---|---|---|---|
| 01 — Collecte & Confidentialité | [dossier-test](01-collecte/dossier-test.md) | [resultat-attendu](01-collecte/resultat-attendu.md) | 6 |
| 02 — Banque & TVA | [dossier-test](02-banque-tva/dossier-test.md) | [resultat-attendu](02-banque-tva/resultat-attendu.md) | 7 |
| 03 — Révision & Synthèse | [dossier-test](03-revision/dossier-test.md) | [resultat-attendu](03-revision/resultat-attendu.md) | 9 |

## Comment tester

1. Crée le Projet Claude de l'agent (voir le [README principal](../README.md)).
2. Ouvre une nouvelle conversation dans le projet.
3. Copie-colle **tout le contenu** du `dossier-test.md` de l'agent.
4. Compare la réponse avec `resultat-attendu.md` : chaque piège est numéroté.

## Grille d'évaluation

Pour chaque agent, coche :

- [ ] Tous les pièges sont détectés.
- [ ] Les montants calculés sont justes, et les calculs sont montrés.
- [ ] Aucun chiffre n'est inventé : les données manquantes sont signalées.
- [ ] Les données personnelles sont signalées **avant** l'analyse.
- [ ] Les points à valider par le comptable sont listés.
- [ ] La sortie est directement exploitable (tableaux, brouillon de relance, etc.).

> La formulation peut varier d'un essai à l'autre : c'est normal avec une IA. Ce qui compte, ce sont les **pièges détectés** et les **montants**.

## Ce que ces tests montrent

- **Confidentialité** : chaque dossier contient au moins une donnée personnelle (nom, téléphone, IBAN) que l'agent doit signaler en premier.
- **Fiabilité** : les écarts sont construits pour que le bon montant soit vérifiable à la main.
- **Humain dans la boucle** : l'agent propose, et le comptable valide.
