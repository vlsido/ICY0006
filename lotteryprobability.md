# SuperEnalotto lottery

SuperEnalotto is an Italian lottery, it has been played since 3 December 1997. The jackpots are among the largest in the world, and the odds of winning one of the lowest in the world.

In order to win, a player has to match one of the following conditions:

Match all 6 numbers;

Match 5 numbers + the "Jolly" number;

Match 5 numbers;

Match 4 numbers;

Match 3 numbers;

Match 2 numbers.

The "Jolly" number gives an additional chance to those who have matched 5 numbers. If they also match the "Jolly" number, they'll win a higher "5+1" prize. 
The "Jolly" number only affects the second prizes and not the jackpot.

All numbers, including the "Jolly" number, are distinct integers in the range from 1 to 90.

There is also a possibility to pick the "SuperStar" number, which is an additional number which costs extra to play. The "SuperStar" number may be the same as another winning number.
Matching it can increase the prize money by up to 100-fold or pay out a fixed amount even if the player fails to match any of the six main numbers.

Winning conditions with the "SuperStar" number:

Match all 6 numbers + the "SuperStar" number;

Match 5 numbers + the "Jolly" number + the "SuperStar" number;

Match 5 numbers + the "SuperStar" number;

Match 4 numbers + the "SuperStar" number;

Match 3 numbers + the "SuperStar" number;

Match 2 numbers + the "SuperStar" number;

Match 1 number + the "SuperStar" number;

Match 0 numbers + the "SuperStar" number.

# Odds

## Formula

n! / k!*(n-k)!

where n is total amount of numbers (90 if none selected yet), k is how many we want to select

### Match all 6 numbers

To calculate the probabality of matching all 6 numbers we need to calculate the amount of possible combinations:

```
90! / 6!*(90-6)! = 622,614,630
```

Thus, the probability of matching all 6 numbers is 1 in 622,614,630

### Match 5 numbers + the "Jolly" number

We know that there are 90 numbers in total, so to match 5/6 numbers and the "Jolly" number, we do the following:

```
(1/622,614,630) * (6! / 5!*(6-5)!) * (83! / 82!*(83-82)!) * 1/83 = 1/103,769,105
```

some explanations

### Match 5 numbers

Same calculations as above, excluding the "Jolly" number probability

```
(1/622,614,630) * (6! / 5!*(6-5)!) * (83! / 82!*(83-82)!) = 1/1,250,230
```

### Match 4 numbers

Same logic, but now we also need to remember that we do not have a possibility to win the "Jolly" number

```
(1/622,614,630) * (6! / 4!*(6-4)!) * (84! / 82!*(84-82)!) = 1/11,907
```

### Match 3 numbers

Same logic

```
(1/622,614,630) * (6! / 3!*(6-3)!) * (84! / 81!*(84-81)!) = 1/327
```

### Match 2 numbers

Same logic

```
(1/622,614,630) * (6! / 2!*(6-2)!) * (84! / 80!*(84-80)!) = 1/22
```


## Winning odds with the "SuperStar" number

"SuperStar" number is any number in the range from 1 to 90, thus we do the just multiply our previous calculation by 1/90

All 6 numbers + the "SuperStar" number:

```
1/62261430 * 1/90 = 1/56,035,316,700 
```

5 numbers + the "Jolly" number + the "SuperStar" number

```
(1/622,614,630) * (6! / 5!*(6-5)!) * (83! / 82!*(83-82)!) * 1/83 * 1/90 = 1/9,339,219,450 
```

5 numbers + the "SuperStar" number

```
(1/622,614,630) * (6! / 5!*(6-5)!) * (83! / 82!*(83-82)!) * 1/90 = 1/112,520,716        
```

4 numbers + the "SuperStar" number

```
(1/622,614,630) * (6! / 4!*(6-4)!) * (84! / 82!*(84-82)!) * 1/90 = 1/1,071,626     
```

3 numbers + the "SuperStar" number

```
(1/622,614,630) * (6! / 3!*(6-3)!) * (84! / 81!*(84-81)!) * 1/90 = 1/29,404      
```

2 numbers + the "SuperStar" number

```
(1/622,614,630) * (6! / 2!*(6-2)!) * (84! / 80!*(84-80)!) * 1/90 = 1/1,936         
```

### Additional winning conditions

1 number + the "SuperStar" number

```
(1/622,614,630) * (6! / 1!*(6-1)!) * (84! / 79!*(84-79)!) * 1/90 = 1/303       
```

0 numbers + the "SuperStar" number

```
(1/622,614,630) * (6! / 0!*(6-0)!) * (84! / 78!*(84-78)!) * 1/90 = 1/138      
```

# Reference:
https://en.wikipedia.org/wiki/SuperEnalotto

https://www.superenalotto.net/en/odds
