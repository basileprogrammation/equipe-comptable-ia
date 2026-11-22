# Équipe comptable IA — 3 agents Claude

Trois agents IA spécialisés pour **assister un comptable junior** en cabinet, conçus pour **protéger les données des clients**.

| # | Agent | Rôle |
|---|-------|------|
| 01 | [Collecte & Confidentialité](agents/01-collecte-confidentialite.md) | Pseudonymisation, inventaire des pièces, pièces manquantes, compte 471, relances clients |
| 02 | [Banque & TVA](agents/02-banque-tva.md) | Rapprochement bancaire, lettrage, TVA collectée et déductible, autoliquidation, écarts |
| 03 | [Révision & Synthèse](agents/03-revision-synthese.md) | Cut-off, provisions, contrôle du FEC, SIG, trésorerie, points d'alerte client |

Le comptable garde la main : chaque agent **prépare et contrôle**, et l'humain **valide**.

## Installation (5 minutes)

1. Sur [claude.ai](https://claude.ai), crée un **Projet** pour chaque agent (par exemple « 01 – Collecte »).
2. Copie le contenu du fichier de l'agent dans les **instructions du projet**.
3. Remplis [`fiche-cabinet.md`](fiche-cabinet.md) et ajoute-le aux **fichiers du projet**.
4. Ouvre une conversation dans le projet et décris ta tâche. L'agent te pose les bonnes questions s'il lui manque des informations.

## Testé sur des dossiers fictifs

Le dossier [`exemples/`](exemples/) contient, pour chaque agent, un **faux dossier client** avec des **pièges volontaires** (données personnelles, écarts bancaires, erreurs de TVA, FEC non conforme…) et le **résultat attendu**, avec des calculs détaillés.

| Agent | Pièges à détecter |
|---|---|
| 01 — Collecte & Confidentialité | 6 : données personnelles, relevé manquant, inventaire absent… |
| 02 — Banque & TVA | 7 : écart de 90 €, double paiement, TVA sous-évaluée, autoliquidation oubliée… |
| 03 — Révision & Synthèse | 9 : cut-off, provision, prorata d'amortissement, FEC non conforme… |

[Tester les agents en 5 minutes](exemples/README.md)

## Confidentialité : les bons réflexes

- **Pseudonymise avant de coller** : remplace les noms, IBAN et coordonnées par des codes (`[CLIENT_A]`, `[IBAN_1]`…) et garde la table de correspondance hors de Claude.
- Ne transmets que les données nécessaires à la tâche.
- Vérifie les paramètres de confidentialité de ton offre Claude et la politique de ton cabinet avant tout usage sur des dossiers réels.
- Le secret professionnel reste sous ta responsabilité.

## Avertissement

Ces agents sont des **outils d'assistance**. Ils peuvent se tromper et ne remplacent ni le jugement du comptable ni la validation d'un expert-comptable. Aucune sortie ne doit être déposée ou envoyée sans relecture.

## Besoin d'agents sur mesure pour votre cabinet ?

Ces 3 agents sont une base générique. Je conçois des agents adaptés à **vos process, vos outils et vos règles de confidentialité** :

- **Diagnostic** : on identifie ensemble les tâches répétitives qui coûtent le plus de temps.
- **Conception** : des agents sur mesure (ton du cabinet, logiciel comptable, procédures internes), testés sur vos cas réels pseudonymisés.
- **Mise en place** : installation chez vous et formation de l'équipe.
- **Suivi** : ajustements et nouveaux agents selon vos besoins.

 Contact : [konanbeyegbin@gmail.com] · [https://www.linkedin.com/in/basile-konan-3b4869119/] 

## Auteur

Basile KONAN —(https://www.linkedin.com/in/basile-konan-3b4869119/)

📘 Commente **AGENT** sous mon post LinkedIn pour recevoir mon ebook sur les agents IA.

## Licence

[CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.fr) : libre de réutiliser et d'adapter, en citant l'auteur.
