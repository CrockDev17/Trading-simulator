# CROCK Trading Simulator

Simulateur interactif de performance de trading avec projection Monte Carlo, développé en HTML, CSS et JavaScript.

## Fonctionnalités

- Paramétrage du capital initial
- Nombre de trades par mois et durée de simulation
- Winrate et ratio Risk/Reward
- Risque en pourcentage du capital par trade
- Frais fixes par transaction
- Simulation Monte Carlo (de 10 à 2 000 scénarios)
- Espérance mathématique par trade, exprimée en R
- Capital final moyen, médian, meilleur et pire scénario
- Drawdown moyen et proportion de scénarios terminant en gain
- Estimation de la fréquence des scénarios où le capital passe sous 50 % du capital initial
- Courbes moyenne, médiane, pire scénario et bande de percentiles 10–90

## Technologies

- HTML5
- CSS3
- JavaScript (vanilla)
- Canvas API pour le graphique

> Note : cette version est une application web côté navigateur. Elle ne nécessite pas Python ni de serveur backend.

## Lancer le projet en local

1. Télécharger ou cloner ce dépôt.
2. Ouvrir `index.html` dans un navigateur moderne.
3. Modifier les paramètres et cliquer sur **Lancer la simulation**.

Aucun package ni installation n'est nécessaire.

## Modèle et hypothèses

Chaque trade est simulé comme un tirage aléatoire indépendant selon un winrate constant. Le gain d'un trade gagnant est égal au montant risqué multiplié par le ratio Risk/Reward. Une perte retire le montant risqué. Le risque est recalculé sur le capital courant à chaque trade et les frais fixes sont ensuite déduits.

Le simulateur ne modélise pas les séries de résultats corrélées, l'évolution du winrate, les changements de volatilité, les spreads variables, le slippage, les gaps ou les contraintes propres à un broker ou à une prop firm. Les résultats Monte Carlo sont des scénarios aléatoires, pas des prévisions.

## Avertissement

Outil éducatif de simulation mathématique. Il ne constitue pas un conseil financier et ne garantit aucun résultat réel.
