---
layout: post
title:  "Mastermind"
date:   2020-4-16 21:28:15 +0700
---

# My first game

My first game that was assigned to me via The Odin Project is [Mastermind](https://en.wikipedia.org/wiki/Mastermind_(board_game)). The game will be written in ruby and will be executed via the command line. A sequence of four begs is randomly picked from a variation of six colors. Tha player has 10 chances to guess the correct sequence of correct pegs before they lose. After each attempted guess, the computer returns a "key" which provides feedback on the accurracy of the players guess. If the player has the right color in the wrong place, a white key means the right peg in the wrong spot, and a black peg means the right code in the right spot. 

## More appreciation for ruby

One of the functions that i needed to write was to randomly pick 5 colors for the pegs. In Java or C++ this would require creating a random class, importing a library, randomly generating an integer, use that integer to access the array in which the colors are stored.
```
Random random = new Random();
for(Array[] currentArray : arrayList){
    String chosenString = currentArray[random.nextInt(currentArray.lenght)];
    System.out.println(chosenString);
}
```
The kind folk(s) who created ruby have simplified this with the [Array.sample](https://www.geeksforgeeks.org/ruby-array-sample-function/) function. This changes a rather clunkly block of code to something more elegant and legible:

```
def initialize()
        @pegs=Array.new
        (0...4).each do |n|
            @pegs[n]=["R","G","B","P","Y","W"].sample
        end
    end
```

## REGEX

Part of this project required the use of regular expression. It is used in this project to verify valid inputs from the user as well as to check to see if the user's guess was accurate. I completed several tutorials on regex and the one-step expressions are easy enough to create and understand. Troubles arise when you have to create more complicated expressions. I had to do several google searches for creating regex statements when i stumbled across this [regex generator](https://regexr.com/). This site has been a very valuable tool that i plan to use in the future. 

Here is one example of the regex that i had to use in this project:
```
if selection.match(/(^([RGBYPW] ){3})[RGBYPW]$/)
                good_selection=true
            end
```

The above regex expression, `/(^([RGBYPW] ){3})[RGBYPW]$/` basically means that it requires that the string start with 3 occurences of either R,G,B,Y,P,W and ends with one occurence of R,G,B,Y,P,W

Even though i was intimidated by regex in the beginning, being somewhat proficient with it allows me to replace several lines of conditionals with one regex statement.

# Future of this project

I want to figure out a way to deploy this within my portfolio website. I will have to do some research and a lot of googling... But such is the life of a programmer


## In other news

I am actually rather enjoying quarantine. Aside from grinding out code for hours a day, i have been able to spend a lot of time outside, away from people of course. I have also been able to spend a lot more time focusing on myself.


Chaire,
MM


