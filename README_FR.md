# Dashboard Retail — Analyse Ventes, Profits & Segments | Power BI

> **$2,14M CA · $270K profit · Consumer = 50%+ des ventes · Technology = meilleure marge**  
> Superstore Dataset · ETL Power Query · DAX · Recommandations business actionnables

![Dashboard Retail](DASHBOARD.png)

🇬🇧 [English version available here](README.md)

---

## Problème Business

Une entreprise retail cherchait à comprendre ses leviers de croissance et ses
axes d'amélioration à partir de ses données de ventes historiques.

**4 questions posées par le management :**

| Question | Axe |
|---|---|
| Quelles sont les tendances ventes & profits dans le temps ? | Temporel |
| Quels segments clients sont les plus rentables ? | Client |
| Quelles régions et catégories contribuent le plus au CA ? | Géographique |
| Comment optimiser les coûts logistiques et les performances produits ? | Opérationnel |

---

## Insights Clés Extraits

| Insight | Détail |
|---|---|
| CA Total | **$2,14M** |
| Profit Total | **$270,63K** — marge globale 12,6% |
| Segment dominant | **Consumer** — plus de 50% des ventes |
| Régions leaders | **Est & Ouest** — concentrent la majorité du CA |
| Meilleure catégorie | **Technology** — marge bénéficiaire la plus élevée |
| Signal d'alerte | Écart croissant ventes/profits sur certaines années → coûts ou remises à surveiller |

---

## Recommandations Livrées

- **Rentabilité produit :** Surveiller les marges par référence et ajuster la politique de prix sur les produits déficitaires
- **Suivi mensuel :** Mettre en place un reporting mensuel des marges pour anticiper les baisses avant qu'elles deviennent critiques
- **Focus marketing :** Concentrer les investissements sur les segments Consumer et Technology — meilleur ROI démontré
- **Optimisation logistique :** Revoir les modes de livraison dans les régions à faible marge — coût shipping non compensé par le prix de vente

---

## Dashboard — Composants

![Dashboard](DASHBOARD.png)

| Visualisation | Contenu |
|---|---|
| Carte géographique | Ventes par région |
| Graphique temporel | Ventes & profits par année — détecte l'écart croissant |
| Répartition segments | Consumer · Corporate · Home Office |
| Top 5 produits | Classement par volume de ventes |
| Analyse CA | Par catégorie (Technology · Furniture · Office Supplies) et par segment |

---

## Mesures DAX

```dax
CA_Total        = SUM(Sales[Sales])
Profit_Total    = SUM(Sales[Profit])
Nb_Commandes    = DISTINCTCOUNT(Sales[Order ID])
Nb_Clients      = DISTINCTCOUNT(Sales[Customer ID])
Marge_%         = DIVIDE([Profit_Total], [CA_Total], 0)
```

---

## Pipeline ETL — Power Query

- Vérification doublons et valeurs manquantes
- Transformation des champs de dates
- Correction des types de données (dates · nombres · textes)
- Normalisation des champs géographiques

---

## Dataset

**Source :** Sample Superstore Dataset — [Kaggle](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)  
**Format :** CSV · Données fictives à des fins analytiques  
**Contenu :** Ventes · Profits · Quantités · Catégories · Segments clients · Régions · Modes de livraison

---

## Stack Technique

- **Power BI Desktop** — dashboard interactif
- **Power Query / M** — ETL et nettoyage
- **DAX** — 5 mesures calculées
- **CSV** — source de données

---

## Installation

```bash
git clone https://github.com/bouba02/Dashboard-Retail-Analyse-Ventes.git
```

Ouvrir le fichier `.pbix` dans Power BI Desktop.

---

## Auteur

**Boubacar Nikiema** — Data Analyst & Consultant BI

Spécialisé en dashboards retail & distribution, analytics commerciaux et pilotage
de la performance avec Power BI, SQL, Python et Excel. Basé au Maroc, j'interviens
auprès d'entreprises en Afrique et en Europe francophone.

[![LinkedIn](https://img.shields.io/badge/LinkedIn-boubacar--nikiema-blue?logo=linkedin)](https://linkedin.com/in/boubacar-nikiema)
[![YouTube](https://img.shields.io/badge/YouTube-BoubacarDataAnalyst-red?logo=youtube)](https://youtube.com/@BoubacarDataAnalyst)
[![Email](https://img.shields.io/badge/Email-nikiemaboubacar%40gmail.com-gray?logo=gmail)](mailto:nikiemaboubacar@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-data.ngroupmediadigital.com-green)](https://data.ngroupmediadigital.com)

---

*Données fictives — Sample Superstore Dataset (Kaggle) · Code : MIT License*
