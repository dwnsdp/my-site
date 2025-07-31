---
{"dg-publish":true,"permalink":"/the-ai-invasion/"}
---

AI is not as bad as you think but I still dislike it in the state it is currently in
[[The AI Invasion#The AI Invasion - Conclusion\|Skip to conclusion]]
# Electricity Usage
>[!note] Stats according to the [EPA via Arbor](https://www.arbor.eco/blog/ai-environmental-impact)
1 million messages sent to ChatGPT is equivalent to
> - 11,001 miles driven by an average gasoline-powered passenger vehicle
> - 4.3 acres of carbon absorbed by U.S. forests in one year
> - 349,258 smartphones charged

These are the stats I have seen quoted before. And while at first this may seem terrible, especially baring in mind it is messaged ~4 billion times a month. But it is worth noting that the average person who uses ChatGPT is likely to use other online services which are equal or worse.

*take all numbers with a massive grain of salt as large tech companies aren't exactly willing to share*

| Service                    | Energy per User per Day (Wh)                                                                                    | Notes                                                                                                                                         |
| -------------------------- | --------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------- |
| **HD Video Streaming**     | [~180–360 Wh](https://www.weforum.org/stories/2020/03/carbon-footprint-netflix-video-streaming-climate-change/) | 1 hr/day at 0.18–0.36 kWh/hr                                                                                                                  |
| **ChatGPT (GPT‑4o)**       | [~2.4 Wh](https://epoch.ai/gradient-updates/how-much-energy-does-chatgpt-use)                                   | 8 query/day, ~0.3 Wh each                                                                                                                     |
| **Cloud Storage (Google)** | [~84 Wh](https://techcrunch.com/2025/07/01/googles-data-center-energy-use-doubled-in-four-years/)               | This is google's cloud storage. But if you have an iPhone or an Android your photos are automatically backed up to some form of cloud storage |
This means streaming video is about 100 times worse than messaging chatgpt.
# Water Usage

I was always of the assumption that data centres simply dumped heat into water and then pumped it back where they found it. Unfortunately that is not the case. It is a lot cheaper to simply pump enough heat into the water to evaporate it.
This means that the water used goes around the world and is precipitated somewhere else.

This is fine when the water is being taken from deep under the Irish sea and precipitated somewhere above the pacific.

Unfortunately capitalist companies prefer to do things that are cheap. And a hint is that places with cheap water generally do not have cheap electricity and vice versa.

Okay so the water usage is a problem. But I have heard before that massive amounts of water are only used in the training.

Training GPT‑3 (I cannot find numbers for the newer models) likely used somewhere between [1 to 3 million litres](https://generative-ai-newsroom.com/the-often-overlooked-water-footprint-of-ai-models-46991e3094b6) of freshwater — roughly the amount a few households use in a year. Not nothing, but relatively small compared to the next bit.

Once deployed, GPT‑4o inference uses around [1.3 to 1.6 billion litres per year](https://arxiv.org/html/2505.09598v1) globally. That’s over 500 Olympic pools. Or the drinking water needs of over a million people.

This is because inference still generates heat, and cooling all those GPUs running all day takes a ridiculous amount of water.

With energy we discovered that video streaming is worse. What about with water usage?

~1095 (average time spent watching per year) * [~2-12L](https://www.mozillafoundation.org/en/blog/ai-internet-carbon-footprint/) = ~2,190-13,140 litres of water per year per person or ~0.4–2.6 trillion litres of water per year for 200 mil subscribers

Both of these things are of course terrible but this has not yet convinced me not to use AI. Rather it has convinced me to stop watching YouTube.
# Content theft
Those first two sections were hard sciences. This is not. This is more open to debate.
As such AI bros insist that this is not a problem.
[robots.txt](https://en.wikipedia.org/wiki/Robots.txt) is a standard such that you can control bots scraping your content. This means you can say, for instance, you do not want one of googles spiders to copy your data into a database so that it can be searched. You can also say in robots.txt; do not use my writing to train an AI
AI companies completely ignore this. In fact AI companies ignore any semblance of reason because who is going to sue them.
The thing is, this is not just lack of consent, which would be morally questionable. When a website has a large no trespassing sign that is a loud 'no'

> “The web is public.” But ‘public’ doesn’t mean ‘yours to take’.

# The AI Invasion - Conclusion
In terms of environmental impact it seems that whilst AI is bad there are a lot of worse things to tackle, like video streaming which uses 1.6k the amount. However this is not just waste. This is unnecessary waste. With shareholders shoving AI into everything crevice they can find like a house-flipper discovering beige paint, you cannot escape AI. AI companies want you to use AI for everything so they make money. This means contracts with governments. Annoying popups with AI generated answers using water on your behalf without consent. And Google recommends you use AI to ask what a shadow is. They want you to use AI for everything. But AI does have some legitimate use cases. As much as it cannot write professional code AI *can* do basic programming and is great at answering very specific technical questions. The question of course, is would it be able to do that if it was not built on stolen content.