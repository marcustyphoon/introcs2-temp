# Lab 3.03 - War (Card Game)

1) Create a program that lets a user play the card game ['War'](http://www.pagat.com/war/war.html).

Your game should:

* Start with a given shuffled deck variable (shuffle function comes from python's random library, more details below)
* Ask for player1 and player2's names.
* Have a function `player_turn`, with the contract shown below:

```python
#player_turn: takes in a player name, player_name, and draws/removes a card from the deck, prints "user drew card x", and returns the value
#input: player_name, string
#output: string
```
* Have a function `compare_scores` that takes in the two strings representing the cards drawn and compares the card values. Make sure to write the contract for `compare_scores`!
* For simplicty Jacks will be represented as 11, Queens will be represented as 12, Kings will be represented as 13, and Aces will be represented as 14
* For simplicty the suit does not matter
* Include a while loop that keeps the game running until there are no cards in the deck.
* Keep track of the score.
* Declare the name of the winner and final score at the end of the game.

### Deck Shuffling

While seemingly simple-- shuffling a deck is a somewhat complicated problem. Luckily, Python's random library has a built in shuffle algorithm. Feel free to read the documentation, but we have provided a simple wrapper function that will return to you a shuffled deck of cards.

```python

import random

# shuffled_deck: will returna shuffled deck to the user
#input:
#output: a list representing a shuffled deck
def shuffled_deck():
	basic_deck = range(2, 15) * 4
	random.shuffle(basic_deck)
	return basic_deck
```

###Bonus!
Instead of closing the program when the deck is empty, create a way for the user to play again.