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

{% include_relative figs/the_donald_negative_LIWC_dashboard.html %}

Analyzing the evolution of negativity characteristics in conflictual outgoing events from the subreddit `the_donald` reveals similar trends for certain features. Indeed, two maxima can be observed during the same periods for the features `Negemo`, `Anger`, `vader_neg`, `Affect`, and less obviously for `frac_alpha` and `Swear`. These peaks occurred during weeks 2016-06 and 2017-02.


# Words as Weapons: How Do Inter-Subreddit Conflicts Affect Victims' Linguistic Recovery?


## Traces of Conflict: Influence of LIWC Characteristics on Post-Conflict Interaction Tones

<!-- How Does the Conflict LIWC Characteristics Impact the Afterward Interaction Tones of the Targeted Subreddit? -->

To study whether conflict changes the LIWC characteristics of a targeted subreddit, we computed the change in the subreddit's LIWC by comparing its mean LIWC after an incoming conflict during a 48-hour window with its mean LIWC before the conflict during a one-month window. Only situations without overlapping conflicts were chosen to study the effect of each conflict individually. Then, a t-test was applied to compare the obtained delta of LIWC to zero, and the variables most correlated with each change in LIWC were determined. 

{% include_relative figs/body_title_general.html %}


### `the_donald` Case

{% include_relative figs/the_donald_body_title.html %}

*TODO: add a transition to explain the next plots*  
Upon examining `the_donald` subreddit more closely, we observe some changes related to incoming conflicts. These changes can be explained by the composition of the subreddit and the characteristics of the conflicts. 

The table below shows the most correlated incoming features for each of the delta features. The incoming feature `frac_upper`, which corresponds to the proportion of capital letters in the incoming text, seems to be correlated with the most delta features, such as `delta_num_long_sentences` and `delta_frac_specials` (the proportion of special characters in the text). 

{% include_relative figs/the_donald_correlation.html %}


## The Rhythm of Recovery: How Communities Heal Their Linguistic Scars

<!-- How long does it take for the linguistic tone of a “victim” subreddit to return to its baseline after being targeted in a conflict? -->

When a community is targeted by a hostile post, its language doesn't immediately return to normal. The emotional shockwave reverberates through subsequent conversations, creating a linguistic recovery curve. This is the time it takes for a community's distinctive voice to return to its baseline after being disrupted by conflict. We used time-series analysis to track how key psychological markers in targeted subreddits evolved over 48-hour periods following an attack. The visualization below reveals the immediate impact and gradual healing process across different dimensions of language.

*TODO: maybe use a log axis or sth to see better the -0.0003 and -0.0001*  
{% include_relative figs/LIWC_delta_analysis.html %}

Our analysis reveals distinct patterns in how different psychological features respond to and recover from conflict. Social language and cognitive mechanisms demonstrate the most significant reductions following attacks, decreasing by -0.0003 and -0.0001, respectively. These findings suggest that communities respond to hostility by becoming less socially engaged and reducing their analytical thinking. This behavior is also observed in positive, negative, and neutral emotion words. Negative emotions show the largest increase, with rises in swear words, anger, sadness, and anxiety vocabulary.

*TODO: explain below plot*  
{% include_relative figs/LIWC_recovery_rate.html %}


### The Recovery Timeline: Fast Bounces and Lasting Scars

The recovery timeline reveals even more compelling insights. While most features recover relatively quickly (within 11.8-12.4 hours), many communities never fully return to baseline within the 48-hour window for certain linguistic features. Most strikingly:

*TODO: relevant to add the proportions ?*  
- Cognitive mechanisms never recover in 37.6% of cases
- Social language never recovers in  33.8%% of cases (4,548/14,698)  
- Positive emotion never recovers in  27.6%% of cases (3,318/14,698)

The recovery histogram below shows how long these linguistic disruptions typically persist across different psychological dimensions.

{% include_relative figs/recovery_histogram.html %}

Agreement, disagreement, and anxiety show the fastest recovery (11.6 hours), demonstrating resilience in these communication functions. However, the high rates of non-recovery for cognitive and social language functions suggest that attacks may cause lasting changes in how communities process information and interact socially.

While the immediate emotional spike of negativity and anxiety is short-lived, the most significant impact of a hostile post is the long-term reduction in social and analytical language use. This suggests that communities may not only be "hurt" in the short term but can be fundamentally altered, becoming less cohesive and less thoughtful in their discourse long after the initial attack has passed.


## The Contagion of Conflict: How Attacker Language Shapes Victim Response?

{% include_relative figs/attack_LIWC_correlation.html %}


## Analysis of Response to Conflict


## Random Forest Analysis


# Snowball Effect: ...


## Community Response Pattern


## Key Findings


## Implications


# Community Clusters: How do the linguistic profiles of online community clusters relate to and predict the propagation of conflict between communities?


# From Digital to Real World
*TODO: 2016 U.S.A. presidential election*