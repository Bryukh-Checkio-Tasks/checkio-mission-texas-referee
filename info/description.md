> There are few things that are so unpardonably neglected in our country as poker. The upper class knows very little about poker. Now and
then you find ambassadors who have sort of a general knowledge of poker, but the ignorance of the people is fearful. Why, I have known
clergymen, good men, kind-hearted, liberal, sincere, and all that, who did not know the meaning of a "flush". It is enough to make one
ashamed of the species.<br>
> -- Mark Twain

[Texas hold'em](http://en.wikipedia.org/wiki/Texas_hold_'em) is a variation of the standard card game of poker.
Two cards (hole cards) are dealt face down to each player and then five community cards are placed face-up by the dealer.
And when all openings we need to define what is the combination a player have.

You are given a sequence of 7 cards and you should choose the best hand (5 cards) in it.
Card sequence are described as a string, where each card are defined by two character - rank and suit.
Cards separated by commas.

Card ranks (from highest to lower): Ace - "A", King - "K", Queen - "Q", "J" - Jack, 10 - "T" and from "9" to "2".

Card suits (from lowest to highest): Spades - "s", Clubs - "c", Diamonds - "d", Hearts - "h".

Texas holdem uses classical [poker hand list](http://en.wikipedia.org/wiki/List_of_poker_hands):
Straight flush, Four of a kind, Full house, Flush, Straight, Three of a kind, Two Pair, One Pair and High card.

Because of the presence of community cards in Texas hold 'em, different players' hands can often run very close in value.
As a result, it is common for kickers to be used to determine
the winning hand and also for two hands (or maybe more) to tie.
A kicker is a card which is part of the five-card poker hand,
but is not used in determining a hand's rank. For instance, in the hand A-A-A-K-Q, the king and queen are kickers.

But in our Texas holdem variation ties are impossible because suits are ordering and for
the same rank cards the highest are determined by the suit. So "Td" are higher than "Tc", but lower then "Jc".

Your goal is to choose the best hand with 5 cards and return them as a string, where cards are separated by commas and
ordering from the highest to lowest value.
For example: We have two pair by queens (heart and spades) and eights (diamonds and clubs) and nine heart as a kicker.
The result: "Qh,Qs,9h,8d,8c". Be careful with order.

**Input:** A list of cards as a string.

**Output:** The best hand as a string.


**How it is used:**
This concept can be useful for game development. And a good example of combinatorial optimisation process.

**Precondition:**

```
cards_quantity == 7
All cards correct and unique.
```