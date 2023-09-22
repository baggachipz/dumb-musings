---
layout: layouts/post.njk
title: The Casino in Your Pocket
description: One example of Wordscapes being a money funnel without you even realizing it.
date: 2023-09-15
---

_A very rough statistical analysis of a casino trick used by games on your phone (n=28)._

tl;dr: It's all rigged! [_Clutches pearls, faints_]

## Introduction to the Game


[Wordscapes](https://en.wikipedia.org/wiki/Wordscapes) is a well-known simple, addictive, and fun word-based game on mobile devices. The base game is very simple: Use a set of available letters to compose proper words to solve a crossword-like puzzle. It has a thriving community of players which can congregate in teams and compete in tournaments.

## The Setup

Like any modern mobile game worth its monetization, the game offers awards, hints, and other decorations to enhance the game experience. They're occasionally gifted for free (and ostensibly at random), but of course are also available for purchase with their in-game currency, coins. Coins are slowly earned by playng the main game. Also  unsurprisingly, coins are available for purchase with real money from your phone. The game frequently pushes ads in your face to buy coins, lest you accidentally forget they're available.

In-app game microtransactions are an [absolutely gigantic industry](https://medium.com/shopify-gaming/mobile-gaming-is-a-50b-industry-but-only-5-of-players-are-spending-money-f7f3375dd959), so a mobile game with real-money purchases truly has only one mission -- to convince you to spend your money on in-game currency. Wordscapes regularly rolls out new bells and whistles to engage the player and unlock new in-game decorations. 

## Mt. Fortune - Welcome to the Gaming Floor

The newest iteration in this monetization/reward system is called "Mt. Fortune", an mini-game of chance<sup>*</sup> where the player ascends a "mountain" of 25 steps. At each step, four cards are presented to the player. 

<figure>
  <img src="/img/mt-fortune-1.png" alt="Mt. Fortune layout" />
  <figcaption>The layout of the Mt. Fortune interface.</figcaption>
</figure>

<figure>
  <img src="/img/mt-fortune-2.png" alt="Mt. Fortune card reveal" />
  <figcaption>After you choose a card, all four are revealed.</figcaption>
</figure>

Three of the cards contain a reward, and one of them contains a "rock", halting your progress. The player is free to exit with their rewards after any step, unless they reveal a rock. They are then presented with an ultimatum: Abandon all your collected rewards, or pay coins to continue on. Each time this happens, the number of coins required to continue increases, to an upper threshold of 1200.

<figure>
  <img src="/img/mt-fortune-3.png" alt="Mt. Fortune ultimatum" />
  <figcaption>The decision. Pay and continue, or lose it all?</figcaption>
</figure>

It's a very effective means of investing the player into the process, extracting their in-game currency in order to continue enhancing their experience.

## Something's Not Right

Given that one is presented with four cards, one being a hazard, the assumption would be that on any non-"basecamp" step (steps divisible by 5 have no rock hazard) would confer a 25% chance of getting a rock and forcing you to pay to continue. As you will see below, this is very much not the case. After noticing some general patterns of rock appearance, my curiosity was piqued.

## The Scam, Visualized

To test this, I created a [spreadsheet](/img/mt-fortune.xlsx). For 28 consecutive days, I played the game in full; paying to continue when a rock appeard, until I reached the end. (This cost me a lot of coins!) To control for selection bias, I randomized (`RANDBETWEEN(1,4)`) the card to choose and recorded the result of my choice for each step: rock or no rock. The result of which card I chose didn't really affect whether it was a rock:

<figure class="chart">
  <img src="/img/mt-fortune-by-card.png" alt="Mt. Fortune card distribution" />
  <figcaption>Which card you choose does not seem to affect whether a rock appears or not.</figcaption>
</figure>

Also, when looking at each day's play, the number of rocks wasn't constant but was pretty consistent. It's interesting to know that in every case, the percentage of cards which exposed a rock was _at least_ 25%, sometimes as high as 45%! (Remember, "basecamp" cards at positions 5,10,15,20, and 25 can't have rocks):

<figure class="chart">
  <img src="/img/mt-fortune-by-date.png" alt="Mt. Fortune rocks by day" />
  <figcaption>Some days, the game likes giving you more rocks than others. But never fewer!</figcaption>
</figure>

But the truly telling chart is the position in which rocks tend to appear:

<figure class="chart">
  <img src="/img/mt-fortune-by-level.png" alt="Mt. Fortune rock distribution by position" />
  <figcaption>Rocks sure do love to appear right before and after those basecamp stations!</figcaption>
</figure>

Whoa. Nothing creates a sense of urgency like snatching away your rewards right before or after a basecamp, and the stakes sure do get high near the end. It should also be noted that the farther you ascend up the steps, the "better" the rewards get. As you get up the mountain, you're virtually guaranteed to have your haul held hostage. Nobody said this would be easy!

According to me, it would seem that the "safest" strategy to reap rewards with the lowest risk of spending coins would be to play through step 8 and then cash out. Or, you can plow on, flinging worthless in-game currency to the tune of 70,000 coins. It's for science, right?

## Conclusion

I'm sure this doesn't come as much of a surprise to anybody that the game is rigged in the house's favor. The choice presented to the player is entirely an illusion, masked as a game of chance. In a casino, any rational adult expects this. For games which allow real-money purchases in the hands of players of any age? Well, we can discuss the morality of that another day. In the meantime, I'll be killing my time with mindless word puzzles.
