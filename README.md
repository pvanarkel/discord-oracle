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
!roll 1d20+6
!roll 1d20-(2+6)
!roll 1d20-4+(1d4+3)
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
