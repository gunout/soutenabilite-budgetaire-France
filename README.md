# 🇫🇷 Soutenabilité budgétaire — France

Simulateur de trajectoire de dette publique pour économistes. Modèle de Domar étendu, analyse stochastique Monte Carlo, CAPB, multiplicateur budgétaire et matrice de sensibilité.

[![Licence MIT](https://img.shields.io/badge/Licence-MIT-ED2939?style=for-the-badge)](LICENSE)
[![Made in France](https://img.shields.io/badge/Made_in-France-002395?style=for-the-badge&labelColor=FFFFFF&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCA5MDAgNjAwIj48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjYwMCIgZmlsbD0iIzAwMjM5NSIvPjxyZWN0IHdpZHRoPSI5MDAiIGhlaWdodD0iNDAwIiB5PSIxMDAiIGZpbGw9IiNmZmYiLz48cmVjdCB3aWR0aD0iOTAwIiBoZWlnaHQ9IjIwMCIgeT0iNDAwIiBmaWxsPSIjZWQyOTM5Ii8+PC9zdmc+)](https://github.com/gunout)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat-square&logo=html5&logoColor=white)](https://github.com/gunout/soutenabilite-budgetaire-France)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)](https://github.com/gunout/soutenabilite-budgetaire-France)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.4-FF6384?style=flat-square&logo=chartdotjs&logoColor=white)](https://www.chartjs.org/)
[![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-en_ligne-222?style=flat-square&logo=githubpages&logoColor=white)](https://gunout.github.io/soutenabilite-budgetaire-France/)

---

## 📑 Sommaire

- [Aperçu](#-aperçu)
- [Fonctionnalités](#-fonctionnalités)
- [Démo](#-démo)
- [Installation](#-installation)
- [Déploiement GitHub Pages](#-déploiement-github-pages)
- [Méthodologie](#-méthodologie)
- [Scénarios prédéfinis](#-scénarios-prédéfinis)
- [Structure du projet](#-structure-du-projet)
- [Exports](#-exports)
- [Limitations](#-limitations)
- [Références](#-références)
- [Licence](#-licence)

---

## 🔎 Aperçu

Un fichier HTML unique, sans build ni dépendance npm, qui implémente un **simulateur de soutenabilité budgétaire** pour la France. L'outil modélise la trajectoire de la dette publique selon l'**équation de Domar étendue** et fournit une analyse stratégique complète destinée aux économistes, étudiants en politique économique et analystes budgétaires.

L'application est **100 % côté client** : aucune donnée n'est envoyée à un serveur, aucun compte n'est requis, aucune dépendance externe n'est installée.

> ⚠️ **Outil académique et pédagogique** — Ne constitue pas un conseil en investissement ni une prévision officielle.

---

## ✨ Fonctionnalités

### 📐 Modèle macroéconomique

- **Équation de Domar discrète** : Δb = [(r−g)/(1+g)]·b − pb/(1+g)
- **Solde primaire corrigé du cycle (CAPB)** : décomposition cyclique via élasticité recettes/PIB et output gap
- **Output gap endogène** : fermeture progressive avec vitesse paramétrable
- **Taux effectif endogène** : transmission progressive depuis la maturité moyenne
- **Prime de risque conditionnelle** : endogène, croissante au-delà de 100 % de dette/PIB
- **Multiplicateur budgétaire** : paramétrable de 0 à 2

### 🎲 Analyse stochastique

- **Monte Carlo** : jusqu'à 5 000 simulations avec chocs gaussiens sur croissance et taux
- **Fan chart** : bandes P10–P25–P50–P75–P90
- **Stress test** : impact d'un choc de +100 pb sur le taux d'intérêt

### 📊 Analyses avancées

- **Analyse de sensibilité** (tornado) sur 11 paramètres
- **Matrice pb\* × (r−g)** : heatmap du solde stabilisant sur 5 niveaux de dette
- **Comparaison de 6 scénarios** superposés
- **Références historiques** : France 1980 → 2025 vs projection

### 🎯 Scénarios prédéfinis

- 📊 Statu quo tendanciel
- ⚖️ Consolidation modérée
- 🔻 Austérité forte
- 📈 Réformes structurelles
- 🔥 Choc inflationniste
- 🇪🇺 Retour Maastricht 60 %
- ⚠️ Stagflation
- 🏦 Choc de taux BCE
- 🎯 Consolidation ambitieuse
- 💰 Restructuration partielle

### 📌 Indicateurs calculés

- Solde primaire stabilisant pb\*
- Effort de stabilisation (points de PIB et Md€/an)
- Effort de retour à Maastricht 60 %
- Charge d'intérêts moyenne et en % du PIB
- Effet boule de neige
- Dette par habitant
- CAPB (solde primaire corrigé du cycle)

### 📥 Exports

- **CSV** (séparateur `;`, compatible Excel FR)
- **JSON** (paramètres + trajectoire + Monte Carlo)
- **Excel** (.xls)
- **PNG** (graphiques)

---

## 🚀 Démo

### 🌐 Application en ligne

👉 [**https://gunout.github.io/soutenabilite-budgetaire-France/**](https://gunout.github.io/soutenabilite-budgetaire-France/)

Aucune installation, aucune inscription. Ouvrez le lien dans un navigateur moderne.

---

## 📦 Installation

### Utilisation directe (recommandée)

```bash
git clone https://github.com/gunout/soutenabilite-budgetaire-France.git
cd soutenabilite-budgetaire-France
# Ouvrez index.html dans votre navigateur
```

Aucune dépendance, aucun `npm install`, aucun build.

### Serveur local (optionnel)

```bash
# Python 3
python -m http.server 8000

# ou Node.js
npx serve .
```

Puis ouvrez `http://localhost:8000/index.html`.

---

## 🌐 Déploiement GitHub Pages

L'application est **déjà déployée** à l'adresse :

**🔗 [https://gunout.github.io/soutenabilite-budgetaire-France/](https://gunout.github.io/soutenabilite-budgetaire-France/)**

### Déployer sur votre propre fork

1. **Forkez** le dépôt sur GitHub
2. Le fichier `index.html` doit être **à la racine** du dépôt (c'est déjà le cas)
3. Allez dans **Settings → Pages**
4. Sous **Build and deployment** :
   - **Source** : `Deploy from a branch`
   - **Branch** : `main` / `(root)`
5. Cliquez sur **Save**
6. Attendez 1–2 minutes

Votre site sera accessible à :
`https://<votre-compte>.github.io/<votre-repo>/`

> 💡 **Astuce** : Le fichier `index.html` étant à la racine, l'URL est automatiquement raccourcie à `https://<compte>.github.io/<repo>/` (sans `/index.html`).

### Ajouter un fichier `.nojekyll`

Pour éviter tout traitement Jekyll inutile et accélérer le déploiement :

```bash
touch .nojekyll
git add .nojekyll
git commit -m "chore: add .nojekyll"
git push
```

---

## 📐 Méthodologie

### Équation de Domar

Le simulateur résout l'équation de Domar discrète :

```
Δb_t = [(r_t − g_t) / (1 + g_t)] · b_{t−1} − pb_t / (1 + g_t)
```

Où :
- `b` = dette/PIB
- `r` = taux d'intérêt effectif
- `g` = croissance nominale (croissance réelle + inflation)
- `pb` = solde primaire (% PIB)

### Solde primaire stabilisant

```
pb* = [(r − g) / (1 + g)] · b
```

### Effort de retour à Maastricht 60 %

Formule analytique avec `a = (1+r)/(1+g)` :

```
pb_requis = (a^N · b_0 − 60) · (1+g) · (a−1) / (a^N − 1)
```

### CAPB (Solde primaire corrigé du cycle)

```
CAPB = pb − ε · gap · (recettes/PIB)
```

Où `ε` = élasticité des recettes au PIB.

---

## 📋 Scénarios prédéfinis

| Scénario | g* | π | i | Recettes | Dépenses |
|---|---|---|---|---|---|
| Statu quo | 1.2 | 1.8 | 3.2 | 51.4 | 55.9 |
| Consolidation modérée | 1.2 | 1.8 | 3.2 | 52.4 | 55.9 |
| Austérité forte | 0.9 | 1.5 | 3.0 | 51.4 | 52.9 |
| Réformes structurelles | 2.2 | 1.8 | 3.2 | 51.4 | 55.9 |
| Choc inflationniste | 1.0 | 3.8 | 3.2 | 51.4 | 55.9 |
| Maastricht 60 % | 1.5 | 1.8 | 3.0 | 53.0 | 53.5 |
| Stagflation | 0.4 | 4.5 | 4.5 | 51.4 | 56.9 |
| Choc BCE | 1.0 | 1.5 | 5.2 | 51.4 | 55.9 |
| Consolidation ambitieuse | 1.4 | 1.8 | 3.0 | 53.5 | 52.5 |
| Restructuration | 1.5 | 2.0 | 2.5 | 51.4 | 55.9 |

---

## 📁 Structure du projet

```text
.
├── index.html      # Application complète (HTML + CSS + JS inline)
├── README.md       # Ce fichier
├── LICENSE         # MIT
└── .nojekyll       # (optionnel) désactive Jekyll sur GitHub Pages
```

L'application est volontairement monolithique pour faciliter le déploiement et l'audit.

---

## 📥 Exports

| Format | Contenu |
|---|---|
| **CSV** | Trajectoire annuelle complète (15 colonnes) |
| **JSON** | Paramètres + trajectoire + quantiles Monte Carlo |
| **Excel** | Tableau détaillé (.xls) |
| **PNG** | Graphique principal |

---

## ⚠️ Limitations

- **Calibration statique** : les paramètres sont fixes sur l'horizon (pas de réaction endogène de la politique budgétaire)
- **Pas de boucle prix-salaires** : l'inflation est exogène
- **Modèle fermé** : pas de secteur extérieur, pas de taux de change
- **Monte Carlo gaussien** : pas de queues épaisses ni de sauts
- **Représentatif** : pas d'hétérogénéité des agents

---

## 📚 Références

- **Domar, E. D.** (1944), *The "Burden of the Debt" and the National Income*, American Economic Review
- **Blanchard, O.** (2019), *Public Debt and Low Interest Rates*, American Economic Review
- **FMI** (2022), *Staff Guidance Note on the Sovereign Risk and Debt Sustainability Framework*
- **INSEE** — Comptes nationaux, dette publique
- **Eurostat** — Procédure concernant les déficits excessifs
- **OFCE** — *Debtwatch*, simulation de soutenabilité
- **Sénat** — Rapport sur le débat d'orientation budgétaire (2023)

---

## 📄 Licence

Ce projet est distribué sous licence **MIT** — voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

## 🙏 Remerciements

- **INSEE** — comptes nationaux et dette publique
- **Eurostat** — statistiques européennes
- **OFCE** — recherches sur la soutenabilité
- **FMI / OCDE** — cadres méthodologiques DSA

---

<div align="center">

**📊 Outil académique — Ne constitue pas un conseil en investissement**

Fait pour la communauté économique open source.

</div>

--- 

