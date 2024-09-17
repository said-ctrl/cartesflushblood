projet jeux de cartes Flesh and blood

Explication des Fonctions JavaScript




Chargement des Données:

fetch('cards.json'): Charge les données des cartes à partir d’un fichier JSON.

then(response => response.json()): Convertit la réponse en JSON.

then(cardsData => { ... }): Traite les données des cartes.

Démarrage et Rejouer le Jeu:

startGameButton.addEventListener('click', () => { ... }): Démarre le jeu en tirant 5 cartes uniques pour le joueur et l’adversaire.

replayGameButton.addEventListener('click', () => { ... }): Redémarre le jeu avec de nouvelles cartes et réinitialise les scores.

Tirer des Cartes Uniques:

drawUniqueCards(cardsData, numberOfCards): Tire un nombre spécifié de cartes uniques à partir des données des cartes.

Afficher les Cartes:

displayHand(hand, elementId, isPlayer): Affiche les cartes dans l’élément spécifié. Si isPlayer est vrai, ajoute un bouton pour jouer la carte.
Variables Globales:

playerHand, opponentHand: Listes des cartes pour le joueur et l’adversaire.

playerScore, opponentScore: Scores du joueur et de l’adversaire.

Jouer une Carte:

playCard(playerCardIndex): Joue une carte du joueur contre la première carte de l’adversaire, met à jour les scores et affiche le résultat du duel.

Mettre à Jour les Scores:

updateScores(): Met à jour les scores affichés pour le joueur et l’adversaire.

-->



### Styles généraux

-   **body**  : Définit la police à ‘Arial’, la couleur de fond à un gris foncé (#1a1a1a), la couleur du texte à un gris clair (#e0e0e0), et supprime les marges et les paddings par défaut. Utilise Flexbox pour centrer les éléments verticalement et horizontalement.
-   **nav**  : Définit la largeur à 100%, la couleur de fond à un gris foncé (#333), la couleur du texte à blanc (#fff), et ajoute du padding en haut et en bas. Centre le texte et ajoute une ombre portée.
-   **nav a**  : Définit la couleur du texte à un gris clair (#e0e0e0), ajoute des marges latérales, supprime la décoration de texte et rend le texte en gras.

### Titres et conteneurs

-   **h1**  : Définit la couleur du texte à un orange vif (#ff4500), ajoute une marge en haut, et ajoute une ombre portée au texte.
-   **.game-container**  : Utilise Flexbox pour centrer les éléments verticalement et horizontalement, et ajoute une marge.
-   **.player-hand, .opponent-hand**  : Utilise Flexbox pour centrer les éléments horizontalement et permet le retour à la ligne, ajoute une marge.

### Cartes et boutons

-   **.card**  : Définit la couleur de fond à un gris foncé (#2e2e2e), ajoute des coins arrondis, une ombre portée, une marge, et une transition pour l’effet de survol. Ajoute une bordure orange (#ff4500).
-   **.card:hover**  : Agrandit légèrement la carte au survol.
-   **.card img**  : Définit la largeur à 100% et ajoute une bordure en bas.
-   **.card h2**  : Définit la taille de la police, ajoute une marge et définit la couleur du texte à orange.
-   **.card p**  : Définit la taille de la police, ajoute une marge et définit la couleur du texte à gris clair.

### Boutons et pied de page

-   **button**  : Définit la couleur de fond à orange, la couleur du texte à blanc, supprime les bordures, ajoute du padding et des marges, arrondit les coins, change le curseur au survol, et ajoute une transition pour l’effet de survol.
-   **button:hover**  : Change la couleur de fond à un orange plus clair.
-   **footer**  : Définit la largeur à 100%, la couleur de fond à un gris foncé, la couleur du texte à blanc, centre le texte, ajoute du padding, et fixe le pied de page en bas de la page.

### Conteneur d’images

-   **.container**  : Centre le texte et ajoute une marge en haut.
-   **.container img**  : Définit la largeur maximale à 100% et ajuste la hauteur automatiquement.
-   **.container h2**  : Ajoute une marge en haut.

### Conclusion

Ce CSS semble être conçu pour une page de jeu qui affiche des cartes. Les classes comme  `.game-container`,  `.player-hand`,  `.opponent-hand`, et  `.card`  indiquent qu’il s’agit probablement d’une interface de j