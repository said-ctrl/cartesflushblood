# 1.  **Site de jeux de cartes**:
[![d6IJzyF.md.png](https://iili.io/d6IJzyF.md.png)](https://freeimage.host/i/d6IJzyF)
  
1. page index avec navbar et un text de présentation et une image

5. footer en fin de page 
6. nav bar et footer sur 3 pages
7. accueil
8. les cartes
9. jeux
10. 
11. dans la page les cartes j'affiche toutes les cartes par la suite je vais faire en sorte d'afficher de 16 ou 10 cartes

[![d6IHELx.md.png](https://iili.io/d6IHELx.md.png)](https://freeimage.host/i/d6IHELx)

12. 2.  **response => response.json()**  : Convertit la réponse en format JSON.
13.  **cardsData => { … }**  : Traite les données des cartes.
14.  **const container = document.getElementById(‘cards-contain’)**  : Sélectionne l’élément HTML où les cartes seront affichées.
15.  **const displayedCards = new Set()**  : Crée un ensemble pour suivre les cartes déjà affichées.
16.  **cardsData.forEach(card => { … })**  : Parcourt chaque carte dans les données.
17.  **if (!displayedCards.has(card.image_url)) { … }**  : Vérifie si la carte n’a pas déjà été affichée.
18.  **const cardElement = document.createElement(‘div’)**  : Crée un nouvel élément div pour la carte.
19.  **cardElement.className = ‘card’**  : Ajoute la classe ‘card’ à l’élément.
20.  **cardElement.innerHTML =  `...`**  : Ajoute le contenu HTML de la carte.
21.  **container.appendChild(cardElement)**  : Ajoute la carte au conteneur.
22.  **displayedCards.add(card.unique_id)**  : Ajoute l’ID unique de la carte à l’ensemble des cartes affichées.
23.  **.catch(error => console.error(‘Erreur lors du chargement des données JSON:’, error))**  : Gère les erreurs de chargement des données JSON.
24. 
25. 
    

26.  **Démarrage et Rejouer le Jeu**:

    
    -   Lorsque le bouton “Démarrer le jeu” est cliqué, le jeu commence en tirant 5 cartes uniques pour le joueur et l’adversaire.
    -   Le bouton “Rejouer” permet de redémarrer le jeu avec de nouvelles cartes et réinitialise les scores.
27.  **Affichage des Cartes**:
[![d6zmgRa.md.png](https://iili.io/d6zmgRa.md.png)](https://freeimage.host/i/d6zmgRa)[


    
    -   Les cartes tirées sont affichées dans les sections “Vos Cartes” et “Cartes Adversaire”.
    -   Les cartes du joueur ont un bouton “Jouer cette carte” pour lancer un duel.
28.  **Jouer une Carte**:

[![d6zmIcX.md.png](https://iili.io/d6zmIcX.md.png)](https://freeimage.host/i/d6zmIcX)

    
    -   Lorsque le joueur joue une carte, elle est comparée à la première carte de l’adversaire.
    -   Les scores sont mis à jour en fonction des résultats du duel (victoire, défaite ou égalité).
20.  **Mise à Jour des Scores**:
[![d6zb0va.md.png](https://iili.io/d6zb0va.md.png)](https://freeimage.host/i/d6zb0va)
    -   Les scores du joueur et de l’adversaire sont affichés et mis à jour après chaque duel.
    - 
VOICI LES FONCTIONS UTILIS2 POUR LE JEUX DE DUEL 
[![d6zDNmx.md.png](https://iili.io/d6zDNmx.md.png)](https://freeimage.host/i/d6zDNmx)

  
let opponentHand = []; : Tableau pour les cartes de l’adversaire.
let playerScore = 0; : Score du joueur.
let opponentScore = 0; : Score de l’adversaire.
Chargement des données JSON :
fetch('cards.json') : Récupère les données des cartes.
response => response.json() : Convertit la réponse en JSON.
cardsData => { ... } : Traite les données des cartes.
const startGameButton = document.getElementById('start-game'); : Sélectionne le bouton de démarrage.
const replayGameButton = document.getElementById('replay-game'); : Sélectionne le bouton de rejouer.
Événements des boutons :
startGameButton.addEventListener('click', () => { ... }); : Démarre le jeu.
replayGameButton.addEventListener('click', () => { ... }); : Relance le jeu.
Fonctions :
drawUniqueCards(cardsData, numberOfCards) : Tire un nombre unique de cartes.
displayHand(hand, elementId, isPlayer) : Affiche les cartes dans le conteneur spécifié.
playCard(playerCardIndex) : Joue une carte et compare les scores.
updateScores() : Met à jour les scores affichés

