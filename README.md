# International Market Prioritization — Education Data Analytics

**Projet academy | Analyse exploratoire des données EdStats (Banque mondiale)**

## Objectif métier

Identifier des marchés internationaux à approfondir pour une plateforme éducative à partir d’indicateurs démographiques, numériques et éducatifs. Cette étude est une **aide à la présélection**, et non une décision d’implantation.

## Méthodologie

1. Exploration des cinq fichiers EdStats et vérification de leur structure.
2. Nettoyage des données et exclusion des agrégats statistiques selon la disponibilité de la région.
3. Sélection de la période 2010–2015 et de trois indicateurs : accès à Internet (`IT.NET.USER.P2`), population d’âge secondaire (`SP.SEC.TOTL.IN`), dépenses publiques d’éducation en % du PIB (`SE.XPD.TOTL.GD.ZS`).
4. Étude des données manquantes et des corrélations ; comparaison sur les 103 entités disposant des trois indicateurs.
5. Transformation en rangs percentiles et score pondéré : **40 % Internet + 40 % population secondaire + 20 % dépenses éducatives**.
6. Analyse de sensibilité avec quatre scénarios de pondération.

## Principaux résultats

Le **Royaume-Uni** arrive en première position dans les quatre scénarios étudiés. **L’Allemagne, la France et les États-Unis** restent parmi les quatre premiers. Ces résultats sont relatifs à l’échantillon et aux hypothèses du modèle.

## Limites

- Données historiques (2010–2015), non représentatives à elles seules du marché actuel.
- 103 entités comparables sur 206 ; certains territoires sont inclus.
- Pondérations fondées sur des hypothèses métier.
- Concurrence, réglementation, demande EdTech réelle et pouvoir d’achat non modélisés.

## Organisation

```text
academy-market-intelligence/
├── README.md
├── pyproject.toml
├── notebooks/
│   └── edstats_market_analysis.ipynb
├── reports/
│   └── presentation_academy.pptx
├── figures/
│   └── README.md
└── data/
    └── README.md
```

## Reproduire l’analyse

1. Installer Python compatible avec la version déclarée dans `pyproject.toml`.
2. Installer les dépendances : `python -m pip install -e .`.
3. Télécharger les données **World Bank EdStats** depuis leur source officielle et placer les cinq fichiers CSV dans le répertoire attendu par le Notebook. Les données brutes ne sont pas redistribuées dans ce dépôt.
4. Ouvrir `notebooks/edstats_market_analysis.ipynb` avec Jupyter ou Google Colab. **Adapter les chemins de fichiers à son environnement** avant exécution.

> Le Notebook est le livrable final du projet de formation. Il est conservé sans modification de ses cellules ; l’exécution automatique dans un environnement neuf n’a pas été validée pour cette version GitHub.

## Livrables

- **Notebook** : exploration, préparation, analyse et classement.
- **Présentation** : synthèse des résultats et recommandations.
- **Environnement** : dépendances Python déclarées dans `pyproject.toml`.

## Source

Banque mondiale — [Education Statistics (EdStats)](https://databank.worldbank.org/source/education-statistics-%5E-all-indicators).
