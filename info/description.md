> There are few things that are so unpardonably neglected in our country as poker. The upper class knows very little about poker. Now and
then you find ambassadors who have sort of a general knowledge of poker, but the ignorance of the people is fearful. Why, I have known
clergymen, good men, kind-hearted, liberal, sincere, and all that, who did not know the meaning of a "flush". It is enough to make one
ashamed of the species.<br>
> -- Mark Twain

[Texas hold'em](http://en.wikipedia.org/wiki/Texas_hold_'em) is a variation of the standard card game of poker.
Two cards (hole cards) are dealt face down to each player then five community cards are placed face-up by the dealer.
Each player's hand is scored by the best five-card hand they can form from their two hole cards
and the five community cards.

For this mission you will be given a sequence of seven cards. Each card is a two-character string representing the rank and suit of the card (respectively). The 7-card sequence is a string of comma-separated cards (example: `"2d,5h,As,Js,2s,3s,5s"`).

The descending ranks are: "A" (Ace), "K" (King), "Q" (Queen), "J" (Jack), "T" (Ten), and "9" to "2".
The descending suits are "h" (hearts), "d" (diamonds), "c" (clubs), "s" (spades).

Your function should return the best five-card hand as string of comma-separated cards ordered by descending significance (example: `"As,Js,5s,3s,2s"`). A hand's value is based on the [classical poker hand hierarchy](http://en.wikipedia.org/wiki/List_of_poker_hands):  
1. Straight flush
2. Four of a kind
3. Full house
4. Flush
5. Straight
6. Three of a kind
7. Two Pair
8. One Pair
9. High card.  

Because of the presence of community cards in Texas Hold'em, different players' hands can often come very close in value.
As a result, it is common for kickers to be used to determine the winning hand for cases where two or more hands tie.
A kicker is a card which is part of the five-card poker hand, but is not used in determining a hand's rank. For instance,
in the hand A-A-A-K-Q, the king and queen are kickers.

In our version of Texas Hold'em cards of differing suits have different values. This means that there is only ever **one** best five-card hand to return. For example, given the following input:  
`"Qh,Qs,Qd,Kh,Kd,Ks,7c"`  
An *incorrect* return would be:  
`"Kh,Kd,Ks,Qh,Qs"` (wrong)  
because the `"Qd" > "Qs"`. The correct output would be:  
`"Kh,kd,ks,Qh,Qd"` (right)

Note: Be care full with order!  
If you are given:  
`"3s,Qh,Ac,3h,8c,3d,5h"`  
you should return:  
`"3h,3d,3s,Ac,Qh"`  
because the value of the three-of-a-kind is more important than the value of the ace and queen kickers.

**Input:** A list of cards as a string.

**Output:** The best hand as a string.


**How it is used:**
This concept is a good example of combinatorial optimisation process, and could come in handy should you make a poker game in Python.

**Precondition:**

```
cards_quantity == 7
All cards correct and unique.
```