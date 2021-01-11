# discord-oracle

Available commands:

```
!roll
!tarot
```

# bot usage

## `!roll`
All forms of diceroll notations should work properly, including adding or detracting dice with each other, adding or detracting numbers from dicerolls, or even adding or detracting sums within brackets. Below are some examples. <br>

```
Simple rolls
!roll 1d20+6
!roll 1d20-(2+6)
!roll 1d20-4+(1d4+3)

Advanced rolls
!roll 1d20x(N)
    exploding dice, will add extra dice on each roll above threshold N. If N is not defined, will default to maximum possible roll.
!roll 6d6^(N)
    highest N dicerolls will be kept, so 6d6^2 will keep the highest two dice.
!roll 6d6m(N)
    middle N dicerolls will be kept, so 6d6m2 will keep the middle two dice.
!roll 6d6v(N)
    lowest N dicerolls will be kept, so 6d6l2 wil keep the lowest two dice.
!roll 2d6r(N)
    will reroll any dice that are below threshold N. The reroll is possible to be below the threshold N.
!roll 2d6rr(N)
    will reroll any dice that are below threshold N. The reroll will be at the very minimum threshold N.
!roll 10d10s
    will sort the rolls in order, this will not change the result.
```

## `!tarot`
This bot can get a random card from a pre-defined set of images. 

You should DM the bot to push commands so people will not see whether you are excluding cards from the random set or not; but the output will always be to a channel defined in the configuration.

```
!tarot
```
Will get a single random card from the list defined in the configuration.

```
!tarot N
``` 
(example: `!tarot 21`) <br>
Will get the card with this specific number.

```
!tarot -N
```
(example: `!tarot -36`)<br>
Will get a random card from the list, but will exclude the number N.

```
!tarot -N,-N2,-N3
```
(example: `!tarot -4,-6,-56`) <br>
Will get a random card from the list, but will exclude the commaspaced numbers. (no spaces between commaspaced values, otherwise the results could be unpredictable, recorded as discord-oracle#1)


# notes
In the tarot command, it's possible to define excludes and specific numbers, like `!tarot 21,-5`, but since the bot only outputs one card at a time, they excludes will not do anything. This behaviour might change when the bot is changed to be able to output more cards simultaneously.