# Requirements breakdown:

We will have to break down the requirements into three types:

- functional requirements (needed for functionality)

- non-functional requirements (non-essiential but would be nice)

- domain requirements (requirements in terms of the market/genre)


## User Stories and task Cards:

Note: The numbers represent the user stories (requirements). The bullet points below are the task cards it has been split up into.

---

1. The game is for 2-6 players. Each player is assigned one of the game tokens. The tokens are: boot, smartphone, goblet, hatstand, cat and spoon. Each player takes a turn by rolling two dice to determine how they move around the board. At the outset, all players start on the board space labelled Go and move clockwise around the board. 
    
    - Game for two-6 players

    - assign each player a game token (boot, smartphone, goblet, hatstand, cat and spoon)

    - Be able to roll the dice

    - make all players start on go and move clockwise around the board

---

2. At the outset of the game, each player has £1,500 in cash. One player is designated the banker and is responsible for distributing the correct amount of cash to each player. The bank has a total of £50,000 cash. Players may not borrow additional money from the bank, but they can trade game items with the bank. 

    - Initialise each player start with 1,500 cash

    - make one player the banker

    - Initialise the bank to have a total of 50,000 cash

    - allow players to trade game items with the bank (trading system with the bank)

---

3. At the outset of the game, the two packs of cards labelled “pot luck” or “opportunity knocks” are shuffled and placed on the board. When cards are taken, they must be replaced at the bottom of the corresponding pile.

    - on start of game, shuffle the pot luck and opportunity knocks decks

    - when a card gets put back, place at the bottom of the deck. (just use a queue for storing "pot luck" and "opportunity knocks" decks)

---

4. For each turn, the player rolls the two dice. They move the number of spaces shown on the dice and arrive at a board space. Players move clockwise around the board.

    - each turn, the player rolls two dice.
        - move the player the total of the two die around the board (clockwise)

---

5.  If a player throws a double, then they take another turn. If a player throws another double at the third turn, then they “go to jail”. When a player goes to jail, they go directly and do not pass Go.

    - allow player to take another turn when a double is rolled.
        - On the third double, send the player to jail

---

6. Board spaces may consist of properties, a “pot luck” space, an “opportunity knocks” space, “free parking”, the jail/just visiting space or a space with specific instructions that must be followed by the player.

    - initialise board spaces and instructions that come with them


---

7. If a player lands on a “pot luck” or “opportunity knocks” space, they take a card for the top of the corresponding pile and carry out the instructions on the card. When this is complete, the card is replaced at the bottom of the corresponding pile. 

    - if landed on "pot luck" / opportunity knocks make the player perform the tasks on the card.

    - place card at bottom of deck (dequeue and enqueue)

---

8. Players make progress in the game by buying property as they move around the board. Players may not purchase property until they have completed one complete circuit of the board by passing the Go space. When a player passes Go, they receive £200 from the bank.

    - Preven players from buying properties unless they have passed "GO" once

    - Give the player 200 when they pass "GO"

---

9. All properties are initially the property of the bank. When a player purchases a property, the card is transferred from the bank to that player and the amount shown on the card is paid to the bank. 

    - All properties should be property bank initially

    - When player purchases property, transfer card from bank to player.
        - subtract amount paid for the property and add to the banks money

---

10. Once a player has made their move, if they land on a property that has not yet been purchased, they have the opportunity to buy that property. If they decide not to buy that property then the property is auctioned by the bank. Each player makes a bid to the bank. The bank sells the property to the highest bidder. If there are no bids, then the property remains unsold. All bidding players must have completed one circuit of the board. 

    - when player lands on property, property can be bought

    - if they do not buy, it is auctioned.
        - each player makes a bid
        - it is sold to the highest bidder
        - if no bids are made, do nothing

---

11. If a player lands on a property owned by another player, they must pay the player who owns the property the value of the rent shown on the card. 

    - when a player lands on a property owned by a player, pay the value on the card

---

12. If a player owns all of the properties in a colour coded group, but the properties are otherwise not developed further with houses and hotels, then the rent due is doubled. 

    - if player owns all poperties but they have no houses, players landing pay double

---

13. If a property is improved with houses or hotels, then the rent to be paid is as shown on the card. 

    - pay rent shown on card depending on the number of houses or hotels

---

14. All rents must be paid for in cash. If a player is unable to pay the rent for a property they have landed on, they must sell game assets to make good on the rent. If they are unable to pay the rent after selling all of their game assets, then they are bankrupt and must leave the game. Their game token is then removed from the board. 

    - If player cannot pay rent, they must sell game assets to get money.
        - be able to sell game assets

    - if they are unable to pay rent after selling all assets they are bankrupt and leave the game

---

15. Players may not borrow or lend money from each other, and may not borrow money from the bank. 


---

16. When a player has finished moving their token, and has completed any property purchase activity, they have the option to buy houses and hotels to improve their properties. Players are not permitted to improve their properties at any other time. 

    - After a turn, allow players to buy new houses

---

17. Houses and hotels may only be purchased for properties where a player owns all of the properties in a particular colour coded group.

    - limit players to only buy houses when all colours of the group are owned.

---

18. Houses and hotels are purchased for the amount shown on the game card. 

---

19. If a player needs to raise funds, they can sell a property back to the bank for its original value as shown on the game card. A property can only be sold when there are no houses or hotels on the property. A player may also sell houses and hotels back to the bank for the original purchase price. 

    - Limit properties to only be sold when all houses are sold on the property.

    - Once all houses ar esold have the option to sell the property.

---

20. Where a coloured set of properties is owned and developed by a player, there may never be a difference of more than 1 house between the properties in that set. If a player wishes to buy a hotel, that is the equivalent of 5 houses in cost. A player may have 4 houses on one set and a hotel on another in that set.

    - should be a difference no more than 1 houses on properties

    - hotels cost 5 times the cost of a house

---

21. The maximum development permitted on any one property is one hotel. 

---

22. If a player needs to raise funds, they may mortgage a property with the bank. The bank will pay the player one half of the value of the property as shown on the game card. No rents may be collected for that property whilst it is under mortgage.

    - Be able to morgage a property with the bank.

    - if morgaged no money should be taken if a player lands on it 

---

23. If a mortgaged property is then sold back to the bank, it is sold for one half of the property price as shown on the card. 

---

24. Where fines are to be paid, the proceeds accumulate on the free parking space in the centre of the board. When a player lands on free parking, they collect all of the funds currently on the free parking space. 

    - make fines go to a seperate place and accumulate

    - if free parking is landed on, all this accumulated money should be given to the player

---

25. If a player is sent to the jail, they may pay £50 to be released from jail. The £50 is added to the free parking fines. The player token is then moved to “just visiting” and the players turn ends. The player takes a normal turn in the next round. 

    - allow players to buy their way out of jail
        - money goes to free parking

    - make a seperate section for in jail and just visiting

---

26. If a player opts to stay in jail, they give up their turn for the next 2 rounds. Whilst in jail, a player may not collect any rents from other players. At the end of the next 2 rounds, the player token is moved to “just visiting” and the players turn ends. The player takes a normal turn in the next round. 

    - players should come out of jail after two turns (but cannot roll that turn)
        - on their following turn they can take a normal turn

---

27. If a player has a “get out of jail free” card, then they place the card at the bottom of the “pot luck” or “opportunity knocks” pile as appropriate, the player token is moved to “just visiting” and the players turn ends. The player takes a normal turn in the next round.

    - be able to hold cards that have special properties. (get out of jail cards)

    - when used place on the bottom of the appropriate deck pile.

---

## Functional requirements:

- A game player agent (AI):

    - agent should be able to take place of 1 or more players

- A means of uploading initial data:

    - A method to initialise data on the board layout

    - It would be useful to be loaded from the excel files. This would mean that it is easily changeable to anything watson games may want to change or replace.

- A means of monitoring the performance of the simulation

    - A system that allows **all** players to see the current worth of each player and what property assets they own.

- A means of being tested:

    - This will let us **show** the software is working properly.

## non-functional requirements:
    
- It should be for desktop pc's, ideally mac and windows. If this is difficult windows is prefered.

- Should be fun to play

- Should have a colourful and intuitive interface. (It should reflect the spirit and character of the original board game from watson games)

**Keeping the Integrity of the game**:

- In the game the bank has a total number of resources of £50,000
    
    - There is no reason to give it a limit
    
    - BUT... in the original board game the bank would issue IOUs

