---
layout: page
---


# Introduction

In the digital realm, words spread faster than intentions. A single post can ignite tension between distant communities, leaving traces that reshape their emotional landscapes. This project tells the story of how online hostility unfolds, lingers, and transforms the language of those it touches. Focusing on Reddit communities from 2014 to 2017, the project explores how conflicts between subreddits reveal deeper patterns of collective emotion, examining how anger spreads and how communities recover. It also considers how repeated clashes may harden or exhaust communities over time. By tracing these emotional aftershocks, the project seeks to understand not just moments of division, but the fragile processes of linguistic healing that follow. Beyond individual disputes, it asks how local conflicts mirror broader societal shifts, from everyday tensions to global political events. The aim is to uncover what our digital language reveals about resilience, contagion, and the shared emotional life of online communities.

This project investigates the dynamics of conflict between communities on Reddit, considering language as a measurable indicator of social friction. We examine how verbal attacks between subreddits can function as linguistic weapons, how communities recover from them, and whether repeated exposure to conflict can create a snowball effect of negativity. By linking these digital battles to real-world political events related to the 2016 US presidential election, our aim is to reveal the profound connection between online discourse and the offline world.


# Our Analytical Approach

*TODO: Replace with actual methods used in the analysis*

{% include_relative figs/analytical_approach.html %}


# A Portrait of the Dataset

The following visualisations provide an overview of the language that shapes our digital landscape.


## Sunburst Plots

The sunburnst plot below reveals the most prevalent psychological and linguistic features across the entire network, offering insight into the shared emotional vocabulary of Reddit users.

{% include_relative figs/sunburst_LIWC.html %}


## Tracing the Contours of Conflicts

*TODO: rephrase "with our map and microscope in hand"*  
With our map and microscope in hand, we can now trace the flow of negativity itself. How does hostility manifest itself? How does it spread through the network over time?

The word clouds below illustrate the stark contrast between positive and negative interactions. One is a landscape of cohesion and reward. The other is a storm of anger and negation. This dichotomy is the fundamental emotional dynamic of inter-community conflict.


### Lexicon of Positivity

{% include_relative figs/positive_world_count.html %}


### Lexicon of Negativity

{% include_relative figs/negative_world_count.html %}


### The Pulse of Negativity Over Time

When does conflict flare up? The following timelines zoom from years down to days, revealing the rhythms and eruptions of online hostility. They allow us to identify long-term trends and pinpoint the days when the digital world held its breath.

*TODO: can't see side by side graphs entirely*  
{% include_relative figs/negativity_pulse.html %}


### Identifying the Verbel Arsenal

Not all negative language is created equal. Some words are more potent weapons than others. Using a Random Forest model, we analyzed through the linguistic features of hostile posts to identify the most powerful predictors of negative messages. The following chart reveals the most damaging elements in the verbal arsenal — the sharpest tools used in digital conflict.

{% include_relative figs/verbal_arsenal.html %}

Our analysis reveals that several linguistic characteristics are powerful indicators of negative messages. `VADER Negative` emerges as the best predictor, which makes sense since it is a sentiment analysis tool designed specifically to process informal social media language. The presence of capital letters and special characters suggests an emotional message. The most predictive LIWC features are:
- Negative emotions, such as anger and swear words;
- Cognitive processes, which suggest more elaborate and thoughtful messages;
- And a social dimension, which indicates complex relational interactions.


### Outgoing Interactions from `the_donald`

*TODO: maybe detail if it's based on the `POST_LABEL` / hyperlink ?*  
Below is plotted the linguistic characteristics evolution for negative outgoing interactions from `the_donald`.

{% include_relative figs/negative_LIWC_dashboard_the_donald.html %}

Analyzing the evolution of negativity characteristics in conflictual outgoing events from the subreddit `the_donald` reveals similar trends for certain features. Indeed, two maxima can be observed during the same periods for the features `Negemo`, `Anger`, `vader_neg`, `Affect`, and less obviously for `frac_alpha` and `Swear`. These peaks occurred during weeks 2016-06 and 2017-02.
