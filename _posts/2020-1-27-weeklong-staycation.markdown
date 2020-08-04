---
layout: post
title:  "Week long staycation!!"
date:   2020-1-27 13:24:17 +0700
---

# What To do with all of this time?!

Work has been absolute madness the past few months. With the most recent Star Wars movie, all of the staff has had to work incredibly long hours. I have had almost zero time to myself. The small amount of time that i have had to myself has mainly been spent working out and playing Escape from Tarkov. I have been making decent progress in the gym but have been making NO progress at Tarkov. I guess my gaming skills peaked at age 16 :/. 

I have been maxed out on vacation hours for a few months so i have to make sure to take advantage of these hours. Most of my time that i have spent away from work is usually dedicated to traveling to see my family. Even though i love spending time with my family, traveling and navigating through Houston traffic can be rather hectic. This go around, i have decided to treat myself to a staycation!! 

Today i went and treated myself to a kickass office chair so that my back doesnt yell at me when i am at my desk for more than a few hours. I also spent 6 hours in my kitchen today preparing all of my necessary meals for the week. I am going to strictly monitor my calories during this week and make sure to be consistent with my 3 day a week full-body weight routine. Because i wil be away from work during this time, i will be able to have a consistent sleep schedule. I am curious to see how the updated sleep schedule will affect my performance in the gym as well as my general well-being.

# Time for code!

I have been navigating through a Coursera course dedicated to Java programming and my current project that i am working on is a [Caesar-Cipher](https://en.wikipedia.org/wiki/Caesar_cipher). The encoding part is pretty simple, as it is little more than parsing through a string and adding the "key" value to whatever the numeric 'char' value of the current letter is. To make sure that the code wraps properly, all i have to do is create a "shifted" alphabet:

`alphabet="ABCDEFGHIJKLMNOPQRSTUVWXYZ";
        shiftedAlphabet=alphabet.substring(key)+alphabet.substring(0,key);
        mainKey=key;`
        
This is relatively simple.

When it comes to actually DECRYPTING a caesar cipher, All you have to do is reverse the above code. This is ASSUMING that you know what the key is. If you DONT know what the key is, it get's a little trickier. The first step is finding the `max_index` value. This is the letter that occurs the most in the given string. From that, you can decipher to message:

`CaesarCipher cc=new CaesarCipher();
        int[] freqs=countLetters(encrypted);
        int maxInd=maxIndex(freqs);
        int key=maxInd-4;
        if(maxInd<4)
        {
            key=26-(4-maxInd);
        }
        return cc.encrypt(encrypted,26-key);`
        
        
        





Chaire,
MM
