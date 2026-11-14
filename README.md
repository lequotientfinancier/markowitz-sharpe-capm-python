# De Markowitz au CAPM — Travaux pratiques en Python

**Le Quotient Financier** · [lequotientfinancier.fr](https://lequotientfinancier.fr)

Quatre notebooks Jupyter pour comprendre, en le programmant, comment la gestion de portefeuille est passée
de la théorie de Markowitz (1952) au modèle de Sharpe (1963), aux modèles multifactoriels, puis au CAPM (1964).
Chaque notebook est à la fois un cours (textes et formules entre les cellules) et un TP (exercices à compléter).

| Notebook | Contenu |
|---|---|
| `01_markowitz` | Estimation des paramètres, incertitude sur les rendements espérés (Merton, Jorion), résolution pas à pas (deux titres, formule fermée, lagrangien), optimisation sans vente à découvert, coût du calcul, sensibilité et « maximiseur d'erreurs » (Michaud) |
| `02_modele_de_sharpe` | Alpha, bêta et risque propre, matrice de covariance de Sharpe, algorithme diagonal, Sherman-Morrison, règle de tri d'Elton-Gruber-Padberg, temps de calcul, sensibilité, test hors échantillon face au 1/N |
| `03_modeles_multifactoriels` | Facteurs sectoriels, formule de Woodbury, analyse en composantes principales, rétrécissement de Ledoit-Wolf, expérience contrôlée sur 100 titres simulés, test hors échantillon |
| `04_capm` | Théorie et vocabulaire, alphas et bêtas de 30 titres, test de la droite de marché, hypothèses à l'épreuve (normalité, stabilité des bêtas, critique de Roll, emprunt et anomalie du faible bêta), arithmétique de la gestion active |

Chaque notebook existe en deux versions :

- `*_etudiant.ipynb` : les cellules marquées `À COMPLÉTER` sont à remplir, dans l'ordre ;
- `*_corrige.ipynb` : la version complète, avec des commentaires de corrigé.

## Lancer les notebooks

**Sur votre ordinateur**

```bash
pip install -r requirements.txt
jupyter lab
```

**Sans rien installer** : ouvrez un notebook dans [Google Colab](https://colab.research.google.com)
(menu *Fichier › Importer un notebook*, onglet GitHub, puis collez l'adresse de ce dépôt).

## Les données

Les cours sont téléchargés gratuitement sur Yahoo Finance avec la librairie `yfinance`, de 2015 à 2024,
puis enregistrés dans des fichiers CSV locaux (`donnees_prix.csv`, `donnees_prix_capm.csv`) réutilisés ensuite.
Le notebook 1 crée le fichier utilisé par les notebooks 2 et 3 ; le notebook 4 télécharge son propre univers de 30 titres.

Si le téléchargement échoue (pas d'accès internet, service indisponible), les notebooks basculent automatiquement
sur des **données simulées** et l'indiquent clairement. Ils restent alors exécutables, mais les chiffres ne décrivent
plus les vrais titres.

## Pour aller plus loin

Les articles du Quotient Financier qui accompagnent ces notebooks :

- Markowitz et la diversification : *[lien à compléter]*
- Modèle de Sharpe : l'astuce de 1963 qui a rendu Markowitz calculable : *[lien à compléter]*
- Le CAPM : *[lien à compléter]*

## Références principales

- Markowitz, H. (1952), « Portfolio Selection », *Journal of Finance*.
- Sharpe, W. (1963), « A Simplified Model for Portfolio Analysis », *Management Science*.
- Sharpe, W. (1964), « Capital Asset Prices », *Journal of Finance*.
- Elton, E., Gruber, M. et Padberg, M. (1976), « Simple Criteria for Optimal Portfolio Selection », *Journal of Finance*.
- Roll, R. (1977), « A Critique of the Asset Pricing Theory's Tests », *Journal of Financial Economics*.
- Michaud, R. (1989), « The Markowitz Optimization Enigma », *Financial Analysts Journal*.
- Sharpe, W. (1991), « The Arithmetic of Active Management », *Financial Analysts Journal*.
- Ledoit, O. et Wolf, M. (2003), « Improved Estimation of the Covariance Matrix of Stock Returns », *Journal of Empirical Finance*.
- DeMiguel, V., Garlappi, L. et Uppal, R. (2009), « Optimal Versus Naive Diversification », *Review of Financial Studies*.
- Frazzini, A. et Pedersen, L. (2014), « Betting Against Beta », *Journal of Financial Economics*.

## Avertissement

Ces notebooks sont des supports pédagogiques. Ils illustrent des méthodes historiques et académiques
et ne constituent en aucun cas un conseil en investissement ni une recommandation d'achat ou de vente.
Les titres utilisés servent uniquement d'exemples.

## Licence

*À compléter.* Suggestion : CC BY 4.0 pour les textes et MIT pour le code, qui autorisent la réutilisation
à condition de citer la source.
