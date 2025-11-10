---
title: Bienvenue dans mon jardin numérique
---

# Bienvenue sur mon site Quartz

Ceci est un site Quartz propulsé par Obsidian. Vous pouvez ajouter vos propres fichiers Markdown dans le répertoire `content/` pour commencer à publier votre contenu.

## Fonctionnalités

- Support des liens wiki [[comme ceci]]
- Graphique de vos notes
- Recherche en texte intégral
- Et bien plus encore !

## Pour commencer

1. Ajoutez vos fichiers Markdown dans le répertoire `content/`
2. Utilisez la syntaxe Markdown et Obsidian
3. Visualisez vos changements en temps réel

Bon jardinage numérique ! 🌱

# 13.2.2.4 Calcul des puissances nominales

Lorsque les puissances des générateurs à combustion individuels ne sont pas connues et pour les recommandations, il est possible d'en faire une estimation selon la méthode suivante :

$$
\text { Pch }=\frac{1,2 * G V *(19-\text { Tbase })}{1000 * 0,95^{3}}
$$

Avec :

- Pch : puissance nominale du générateur pour le chauffage (kW)
- Tbase : température extérieure de base selon la zone climatique et l'altitude $\left({ }^{\circ} \mathrm{C}\right)$ (voir paragraphe 18.1)
- GV : déperditions à travers l'enveloppe et par renouvellement d'air (W/K)

Dans le cas de la réalisation d'un DPE à l'échelle de l'appartement, et lorsque celui-ci est alimenté par une installation

![](https://cdn.mathpix.com/cropped/2024_07_18_97732d9d6048f6ca5301g-093.jpg?height=45&width=1182&top_left_y=1685&top_left_x=251)

$$
\text { Pch }_{\text {immeuble }}=\frac{1,2 * G V_{\text {immeuble }} *(19-\text { Tbase })}{1000 * 0,95^{3}}
$$

Avec :

- $\mathrm{GV}_{\text {immeuble }}$ : déperditions à travers l'enveloppe et par renouvellement d'air pour l'immeuble $(\mathrm{W} / \mathrm{K})$ :

$$
G V_{\text {immeuble }}=G V_{\text {appartement }} * \frac{S h_{\text {immeuble }}}{\text { Sh }}
$$

- Tbase : température extérieure de base selon la zone climatique et l'altitude $\left({ }^{\circ} \mathrm{C}\right)$ (voir paragraphe 18.1)

Dans le cas de la réalisation d'un DPE à l'échelle de l'appartement à partir des données de l'immeuble (voir \$17.2.2), et lorsque le chauffage est individuel et géré de manière homogène, le calcul de la puissance nominale du générateur de chaque appartement Pch (kW) est :

$$
\text { Pch }=\frac{1,2 * \frac{G V}{N} *(19-\text { Tbase })}{1000 * 0,95^{3}}
$$

Avec :

- Pch : puissance nominale du générateur pour le chauffage (kW)
- Tbase : température extérieure de base selon la zone climatique et l'altitude $\left({ }^{\circ} \mathrm{C}\right)($ voir paragraphe 18.1)
- GV : déperditions à travers l'enveloppe et par renouvellement d'air (W/K)
- N : nombre de logements dans l'immeuble

Si le générateur n'alimente qu'une partie du logement, il est nécessaire de proratiser cette puissance Pch.

Dans le cas de 2 générateurs alimentant pour le premier une surface Sh1 et pour le second une surface Sh2 (Sh1 + Sh2 = Sh avec Sh la surface du logement) :

$$
\begin{aligned}
& \text { Pch } 1=\frac{\operatorname{Sh} 1}{\text { Shtot }} * \frac{1,2 * G V *(19-\text { Tbase })}{1000 * 0,95^{3}} \\
& \text { Pch } 2=\frac{\operatorname{Sh} 2}{\text { Shtot }} * \frac{1,2 * G V *(19-\text { Tbase })}{1000 * 0,95^{3}}
\end{aligned}
$$

Avec :

- Pch1 la puissance nominale du générateur pour le chauffage (kW) pour la surface Sh1
- Pch2 la puissance nominale du générateur pour le chauffage (kW) pour la surface Sh2

La puissance nécessaire pour la production d'eau chaude sanitaire (Pecs) dépend du type de production et donc du volume de stockage :

| Type de production d'ECS | Volume de stockage (L) | Puissance de dimensionnement (kW) |
| :---: | :---: | :---: |
| Instantanée | $\mathrm{Vs}=0$ | Pecs $=21$ |
| Semi-instantanée | $0<\mathrm{Vs} \leq 20$ | Pecs $=21-0,8 * V s$ |
| Semi-accumulation | $20<\mathrm{Vs} \leq 150$ | Pecs $=5-1,751 * \frac{V s-20}{65}$ |
| Accumulation | $150<\mathrm{Vs}$ | Pecs $=\frac{7,14 * V s+428}{1000}$ |

La puissance de dimensionnement du générateur est :

$$
P d i m=\max (P c h ; P e c s)
$$

La puissance nominale $\mathrm{Pn}(\mathrm{kW})$ des chaudières est déterminée à partir de Pdim :

|  | CHAUDIERES MURALES INSTALLEES <br> avant 2005 ou chaudières sur sol | CHAUDIERES MURALES INSTALLEES <br> à partir de 2006 |
| :---: | :---: | :---: |
| Pdim (kW) | Pn (kW) | PnW) |
| $\leq 5$ | 18 | 5 |
| $5<\leq 10$ | 18 | 10 |
| $10<\leq 13$ | 18 | 13 |
| $13<\leq 18$ | 18 | 24 |
| $18<\leq 24$ | 24 | 28 |
| $24<\leq 28$ | 28 | 32 |
| $28<\leq 32$ | 32 | 40 |
| $32<\leq 40$ | 40 |  |
| $40<$ | (Partie entière $\left.\left(\frac{\text { Pdim }}{5}\right)+1\right) * 5$ |  |

Dans le cas d'un logement chauffé avec n radiateurs gaz, la puissance de chaque radiateur gaz est $\mathrm{Pn}(\mathrm{kW}$ ) tel que :

$$
P n=\frac{P c h}{n}
$$
