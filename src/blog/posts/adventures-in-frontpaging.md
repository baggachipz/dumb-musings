---
layout: layouts/post.njk
title: Adventures in Frontpaging (on Hacker News)
description: Beware the hidden costs of a free static site paired with popularity!
date: 2023-10-10
---

## It all starts with one post.

A couple weeks ago, I wrote [the first post](/blog/posts/wordscapes-the-casino-in-your-pocket/) on my little blog site, simply because I'd diligently done some "research" work and thought it interesting to share with the aether. In order to do this as quickly and cheaply as possible, I spun up an [Eleventy](https://www.11ty.dev) site locally with a simple custom theme and began writing. It was a nifty little write-up, if I do say so myself. My wife liked it. So, out into the world it went, on a free static host package at [Netlify](https://www.netlify.com). I tooted about it on [Mastodon](https://vmst.io/@baggachipz/111116465453033500), which got no traction because I have exactly zero followers. I also posted it on [Lemmy](https://sh.itjust.works/c/technology@lemmy.world), and it was promptly removed by an admin. Finally, on a lark, I submitted it to [Hacker News](https://news.ycombinator.com/item?id=37642538). It got no upvotes all day and I went to bed without thinking of it. 

The next morning, it reached as high as #10 on the front page. I was shocked!

## Netlify, how could you?

Netlify has been kind of the "geek standard" for free static hosting and CDN for years; But, like any company who's venture-backed and profit driven, they tend to revise their [terms](https://www.netlify.com/legal/terms-of-use/) and chip away at the "free tier" which is designed to suck one into their ecosystem. I don't blame them for that, though it's a small tragedy every time I see it. In my case, I've hosted several small sites over the years on Netlify's free tier and enjoyed every minute of it.

But I've never hosted a site which experienced high traffic. My first inkling of trouble was the dreaded "You've got [sic] more room to grow!" email from Netlify:

<figure>
  <img src="/img/netlify-bandwidth-email.png" alt="Netlify email screenshot" />
  <figcaption>Wallet, we have a problem.</figcaption>
</figure>

Then I got another one of those emails. And then another. Woe be unto he who has three 3MB-sized images on their static site.

## Stop the bleeding!

I logged into my Netlify account, and was greeted by an outstanding invoice of $160.00. Not life-altering, but an unwelome expense. And it was clearly going to get worse if I didn't do something. So, having recently ported my domain from Google Domains to Cloudflare (Because Google sucks and is shutting down yet another useful product without explanation), I realized that Cloudflare also offers [free static hosting](https://www.cloudflare.com/developer-platform/pages/)... without bandwidth limits!

It didn't take much to publish the static site on Cloudflare and make the DNS switch away from Netlify. That happened without downtime or interruption; bless the internet.

## Lessons learned

First, optimize your assets. Those 3MB images are now less than 1MB each. I should have done that in the first place but was just lazy. Next, know your hosting plan. Free hosting is great, but those bandwidth costs over the free threshold are absurd. I guess that's how they get you. Finally, remember that you have options, and the current state of things will change. I'm sure Cloudflare's free option won't last forever, then it'll be time to move on to the next prospecting provider who's backed by venture capital and trying to lure in customers.

 > "Fool me once, shame on me. Fool me twice... uh, you can't fool me again."
 > 
 > *Sage American Philosopher*
