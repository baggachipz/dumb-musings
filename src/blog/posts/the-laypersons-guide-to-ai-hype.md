---
layout: layouts/post.njk
title: The Layperson's Guide to AI Hype
description: The so-called "AI" boom is mostly hype, here's why.
date: 2024-11-25
---

*tl;dr: AI is mostly hype and won't take everybody's job or end humanity.*

## AI here, AI there, AI everywhere
"AI" is a term you cannot escape if you follow any kind of tech news, or any news really. It's a constant drumbeat of breathless prognostications; of a future where all jobs are automated, people are obsolete, and perhaps the end of humanity as we know it while superintelligence enslaves or eradicates us. This is presented as a foregone conclusion. Companies and charlatans are getting rich by hopping on the bandwagon and embracing an "AI-first" business strategy.

The problem is, it's mostly bullshit. I'm constantly asked by people what it all means and what they can do. The truth is, this "AI" is an excellent means of prediction via probability. In the tech community, lots of people call it "fancy autocomplete". That is, given a set of input, the program can compare that input against thousands (or millions) of similar examples and spit out the most likely outcome. *That's it.*

## Everyday use
I'll give an example. Inspired by [*Silicon Valley*'s "Not Hotdog"](https://www.engadget.com/2017-05-15-not-hotdog-app-hbo-silicon-valley.html) app, I recognized a need in my everyday life. We had just procured some chickens for our backyard chicken coop, which I had proudly built with my own hands. However, I had a need: to keep out predators, a door to the coop should close automatically every night after the chickens roosted. Not content with simply putting the door on a timer, I feared that if one or more chickens didn't make it to the coop in time, they would be stranded outside and vulnerable to the horrors of the suburban nighttime landscape.

The idea was thus: When a chicken approaches the coop door, a motion sensor triggers a camera to take a picture. If the picture contains a chicken, open the coop door. If not, keep it closed. In order to build this, I used what was called "Machine Learning" at the time to feed a series of pictures of chickens into the training program, saying "this is a chicken". I then fed a series of predator animals to train the "not chicken" portion. This is time and processor-intensive, but the outcome was what's called a model. I could then use this model to accurately predict whether an entirely new picture of an animal was a chicken or not. It worked pretty well, and my cobbled-together [proof of concept code is here](https://github.com/baggachipz/cluckingham-palace), untouched for 6 years. Sadly, my gross inability to engineer the door hardware led to the project's demise. I caved and bought the door timer kit.

## More of the same, but fancier
All of this is to say that Machine Learning was the precursor upon which modern "AI" was built. The concept has existed for a while (in tech time), and recent advances in computing power have made this much better and generally applicable to other domains. ChatGPT is the most famous example right now. The engineers at OpenAI (which is ironically very closed) have ingested almost all of the text on the open web to build successively advanced models, which can take input and infer an answer. This answer can often seem uncanny, but the method remains very much the same as before. It's simply being done on a much higher, more intensive level of computing power and training set. (Please also understand that I'm not diminishing the incredibly hard work of legions of people, I simply mean to distill what's happening at a high level.)

Other applications of this advancement have been applied to additional domains. Feed it an absolute ton of images, then ask it to create something entirely new based on that set and model. For example, Captain America riding on a kangaroo. The model has lots of images containing Captain America, and lots of images of kangaroos. Merge those two together, apply the same kind of image blending/smoothing like Photoshop has had for years, *et voilà*: Captain America proudly mounted on his kangaroo steed.

<figure>
  <img src="/img/captain-america-kangaroo.png">
  <figcaption>Avenging down under.</figcaption>
</figure>

## Not as smart as you may think
However, you can see that these programs often get it hilariously wrong. When I prompted an [image generator](https://picsart.com/ai-image-generator/) to create that picture, it didn't realize that a kangaroo shouldn't have two heads. It simply tried to mash up a picture it found of Captain America, with some pictures of a kangaroo. This "AI" doesn't actually *understand* anything. It took the input, and tried its best (via probabilistic inference) to create the output from its vast collection of data (images). That is, given all the training data and the parsing of input, it decides that one outcome is the most likely to be correct. Some of the more advanced models have gotten very good at this through training on unimaginably large data sets. 

People mistake this for actual "intelligence"; true comprehension of the request and application of contextual reason to satisfy the requirements. These programs merely apply a brute-force method to statistically predict the output. All of this training and data ingestion [comes at a ridiculous cost](https://www.scientificamerican.com/article/the-ai-boom-could-use-a-shocking-amount-of-electricity/).

## Toto pulls back the curtain
Though this technology has gotten very good, cracks are beginning to form in the façade. Since these models rely on vast sets of training data, there is naturally an upper limit on the data available. [This is already starting to happen](https://apnews.com/article/ai-artificial-intelligence-training-data-running-out-9676145bac0d30ecce1513c20561b87d). Worse still, lots of the text now existing on the web is actually output from the very same AI programs. The result is a "snake eating its tail" scenario, where these models [actually get *worse*, not better](https://www.nytimes.com/interactive/2024/08/26/upshot/ai-synthetic-data.html). 

As a result, the AI boom will most likely collapse in spectacular fashion. This is not to say it is a failure. After the crash, good applications of the technology will rise from the ashes, and eventually what has been a punchline will be useful in the long run. But the actual application of the technology will never match the hype. This has been coined the [Gartner Hype Cycle](https://en.wikipedia.org/wiki/Gartner_hype_cycle), and we're in the midst of the hype peak, and very soon starting the rapid descent.

<figure class="chart">
  <img src="/img/gartner-hype-cycle.png">
  <figcaption>This is the part of the roller coaster where your stomach begins to float.</figcaption>
</figure>

This is far from the first time this cycle has played out. Previous examples include:
 * [Expert Systems](https://en.wikipedia.org/wiki/Expert_system) in the 80's
 * The World Wide Web and e-Commerce in the late 90's/early 2000s
 * Bitcoin and Cryptocurrency in the 2010's
 * NFT's
 * Self-driving cars (in progress)

... nor will it be the last time this happens.

## Don't believe the hype
"AI" in its current form will never reach the colloquial definition of "a super-intelligent mind which self-propagates and understands everything"; or in the industry parlance, Artifcial General Intelligence (AGI). It's not going to take your job, unless you write bullshit clickbait articles, or create derivative images, or videos making people say fake things. In which case, good riddance. Instead, it will become a useful assistant where its abilities are applicable. "Alexa, make a dinner reservation at Ruth's Chris at 7pm tomorrow" may finally be possible.

Until then, please stop assuming that the brilliant robot overlords are going to do anything but annoy us via the news wire.