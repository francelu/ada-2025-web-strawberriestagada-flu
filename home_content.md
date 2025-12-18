---
layout: page
---


# Introduction

{% include_relative figs/intro_pic.html %}

In the digital realm, words spread faster than intentions. A single post can ignite tension between distant communities, leaving traces that reshape their emotional landscapes. This project tells the story of how online hostility unfolds, lingers, and transforms the language of those it touches. Focusing on Reddit communities from 2014 to 2017, the project explores how conflicts between subreddits reveal deeper patterns of collective emotion, examining how anger spreads and how communities recover. It also considers how repeated clashes may harden or exhaust communities over time. By tracing these emotional aftershocks, the project seeks to understand not just moments of division, but the fragile processes of linguistic healing that follow. Beyond individual disputes, it asks how local conflicts mirror broader societal shifts, from everyday tensions to global political events. The aim is to uncover what our digital language reveals about resilience, contagion, and the shared emotional life of online communities.

This project investigates the dynamics of conflict between communities on Reddit, considering language as a measurable indicator of social friction. We examine how verbal attacks between subreddits can function as linguistic weapons, how communities recover from them, and whether repeated exposure to conflict can create a snowball effect of negativity. By linking these digital battles to real-world political events related to the 2016 US presidential election, our aim is to reveal the profound connection between online discourse and the offline world.


# A Portrait of the Dataset

The following visualisations provide an overview of the language that shapes our digital landscape.


## Sunburst Plot

The sunburnst plot below reveals the most prevalent psychological and linguistic features across the entire network, offering insight into the shared emotional vocabulary of Reddit users.

{% include_relative figs/sunburst_LIWC.html %}


## Tracing the Contours of Conflicts

Now that we know what our data contains, we can trace the flow of negativity. How does hostility manifest itself? How does it spread through the network over time?

The word clouds below illustrate the stark contrast between positive and negative interactions. One is a landscape of cohesion and reward. The other is a storm of anger and negation. This dichotomy is the fundamental emotional dynamic of inter-community conflict.


### Lexicon of Positivity

{% include_relative figs/lexicon_positivity.html %}


### Lexicon of Negativity

{% include_relative figs/lexicon_negativity.html %}


### The Pulse of Negativity Over Time

When does conflict flare up? The following timelines zoom from years down to days, revealing the rhythms and eruptions of online hostility. They allow us to identify long-term trends and pinpoint the days when the digital world held its breath.

*TODO: graphs are too narrow*  
{% include_relative figs/negativity_pulse.html %}


### Identifying the Verbel Arsenal

{% include_relative figs/verbal_arsenal_pic.html %}

Not all negative language is created equal. Some words are more potent weapons than others. Using a Random Forest model, we analyzed through the linguistic features of hostile posts to identify the most powerful predictors of negative messages. The following chart reveals the most damaging elements in the verbal arsenal — the sharpest tools used in digital conflict.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/verbal_arsenal.html %}

Our analysis reveals that several linguistic characteristics are powerful indicators of negative messages. `VADER Negative` emerges as the best predictor, which makes sense since it is a sentiment analysis tool designed specifically to process informal social media language. The presence of capital letters and special characters suggests an emotional message. The most predictive LIWC features are:
- Negative emotions, such as anger and swear words;
- Cognitive processes, which suggest more elaborate and thoughtful messages;
- And a social dimension, which indicates complex relational interactions.


### Outgoing Interactions from `the_donald`

*TODO: maybe detail if it's based on the `POST_LABEL` / hyperlink ?*  
Below is plotted the linguistic characteristics evolution for negative outgoing interactions from `the_donald`.

{% include_relative figs/the_donald_negative_LIWC_dashboard.html %}

{% include_relative figs/swear_bubble_pic.html %}

Analyzing the evolution of negativity characteristics in conflictual outgoing events from the subreddit `the_donald` reveals similar trends for certain features. Indeed, two maxima can be observed during the same periods for the features `Negemo`, `Anger`, `vader_neg`, `Affect`, and less obviously for `frac_alpha` and `Swear`. These peaks occurred during weeks 2016-06 and 2017-02.

<!-- To have title below picture too -->
<div style="clear: both;"></div>


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

{% include_relative figs/rhythm_of_recovery_pic.html %}

When a community is targeted by a hostile post, its language doesn't immediately return to normal. The emotional shockwave reverberates through subsequent conversations, creating a linguistic recovery curve. This is the time it takes for a community's distinctive voice to return to its baseline after being disrupted by conflict. We used time-series analysis to track how key psychological markers in targeted subreddits evolved over 48-hour periods following an attack. The visualization below reveals the immediate impact and gradual healing process across different dimensions of language.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

*TODO: maybe use a log axis or sth to see better the -0.0003 and -0.0001*  
*TODO: (huh - France) new graph Recovery_bar_plot.html mais fait beuguer quand j'essaie*

{% include_relative figs/recovery_bar_plot.html %}

Our analysis reveals distinct patterns in how different psychological features respond to and recover from conflict. Social language and cognitive mechanisms demonstrate the most significant reductions following attacks, decreasing by -0.0003 and -0.0001, respectively. These findings suggest that communities respond to hostility by becoming less socially engaged and reducing their analytical thinking. This behavior is also observed in positive, negative, and neutral emotion words. Negative emotions show the largest increase, with rises in swear words, anger, sadness, and anxiety vocabulary.



### The Recovery Timeline: Fast Bounces and Lasting Scars

The recovery timeline reveals even more compelling insights. While most features recover relatively quickly (within 11.8-12.4 hours), many communities never fully return to baseline within the 48-hour window for certain linguistic features. Most strikingly:

- Cognitive mechanisms never recover in 37.6% of cases
- Social language never recovers in  33.8%% of cases 
- Positive emotion never recovers in  27.6%% of cases 

The recovery histogram below shows how long these linguistic disruptions typically persist across different psychological dimensions.

{% include_relative figs/recovery_histogram.html %}

Agreement, disagreement, and anxiety show the fastest recovery (11.6 hours), demonstrating resilience in these communication functions. However, the high rates of non-recovery for cognitive and social language functions suggest that attacks may cause lasting changes in how communities process information and interact socially.

While the immediate emotional spike of negativity and anxiety is short-lived, the most significant impact of a hostile post is the long-term reduction in social and analytical language use. This suggests that communities may not only be "hurt" in the short term but can be fundamentally altered, becoming less cohesive and less thoughtful in their discourse long after the initial attack has passed.


## The Contagion of Conflict: How Attacker Language Shapes Victim Response?

When one community attacks another, the emotional tone of the assault itself may determine how deeply the target is wounded. We investigated whether specific linguistic features in hostile posts act as psychological triggers that create predictable patterns in how victim communities respond. We used correlation analysis across multiple time segments to trace how the emotional and cognitive composition of an attack influences subsequent linguistic shifts in the targeted community. The visualization below shows which attacker features have the strongest ripple effect.

{% include_relative figs/attack_LIWC_correlation.html %}

The data clearly shows patterns of emotional contagion and behavioral mirroring:

- Swear words in attacks trigger anger responses: the strongest correlation (r = 0.021) links attacker profanity to increased anger language in victim communities,
- Victims mirror profanity: target communities significantly increase their own swear word usage when attacked with profanity (r = 0.020),
- Sexual language escalates: attacks containing profanity also correlate with increased sexual language in responses (r = 0.019).

Interestingly, religious language in attacks correlates with increased social language in victim responses (r = 0.017). This suggests that communities may respond to religiously themed attacks by strengthening social bonds. Conversely, sadness in attacks correlates with reduced social language in targets (r = -0.016), indicating that emotionally vulnerable attacks may suppress community engagement.

{% include_relative figs/influential-attack.html %}

Our analysis reveals that swear is the most powerful linguistic trigger in attacks, with swear words in hostile posts having the strongest influence on victim responses.

Although these correlations are statistically significant, the effect sizes are generally small. This suggests that, although attacker language influences victim responses, the relationship is subtle and mediated by many other factors. 

## Analysis of Response to Conflict
*TODO: structure ?*

This section examines how a subreddit under attack may respond to the attacking subreddit, considering the characteristics of the attacking hyperlinks' comments. The analyses performed here are similar to those performed for the general case, but are applied only to outgoing subreddit activities directed toward the attacker within a 72-hour window after the incoming conflict. 

{% include_relative figs/body_title_conflict_response.html %}

*TODO: analyse or explain more !!!*


### Random Forest Analysis
*TODO: structure ?*

We use a random forest model to determine which characteristics of incoming conflicts best explain differences in targeted subreddits' linguistic responses.

{% include_relative figs/body_title_random_forest.html %}

## Snowball Effect


###  How do repeated inter-subreddit conflicts shape the linguistic and emotional tone of both attackers and targets over time, and do these patterns suggest a cumulative negativity ?


We use Granger causality tests to determine whether being attacked (receiving negative sentiment posts) causally influences a community's subsequent negative behavior. These tests examine whether knowledge of past values in one time series (attacks received) improves the prediction of another time series (negative behavior emitted).




#### Community Response Pattern
*TODO: structure ?*


The Granger causality heatmap below shows which communities have statistically significant causal relationships between being attacked and subsequently exhibiting negative behavior. Darker colors indicate stronger effects.


{% include_relative figs/granger_analysis.html %}


#### Results


{% include_relative figs/community_response_pattern.html %}


Based on the heatmap, we can conclude that attacks cause negative behavior in certain communities. Among them, `subredditdram` is the most vulnerable; attacks consistently lead to negative behavior for more than five hours. `politics` is highly reactive, with immediate and sustained negative responses, while `news` has a quick reaction, but of shorter duration. The plot shows that, in general, drama and politics communities are most vulnerable to attack. This the majority of communities show significant effects even 4-5 hours after the initial attack. Despite thematic differences, the pattern of negative responses to attacks appears to be a cross-cutting phenomenon with consistency across communities.


These results suggest that online attacks systematically create cycles of negativity that spread across different types of communities. Theses effects often persist for 4-5 hours, indicating that online conflicts can have influence on the tone of discussions long after the attack.


# Community Clusters: How do the linguistic profiles of online community clusters relate to and predict the propagation of conflict between communities?


*Je nommerais plutot cette partie cluster profiling car on ne prédit pas la propagation du conflict entre les communautés*


In this part, subreddits are gathered in clusters of communities, made on the positive network (affection between subreddits) using the Louvain method and one the embedding (similarity of the subreddits respect to their posting users) using a k-mean algorithm.

To simplify the analysis, only the 7 most virulent clusters are selected. Each cluster is assigned to each subreddit and a theme is manually assigned to each cluster as shown on below plot.

{% include_relative figs/cluster_profile.html %}

To analyze language patterns across clusters, LIWC features were first simplified into binary indicators showing whether a category appeared more or less than average. We then used chi-square tests to examine whether certain clusters were more likely to use specific types of language than would be expected by chance. To avoid false positives from running many tests, p-values were adjusted using false discovery rate correction.

In the heatmap, color intensity reflects the strength of association (Cramér’s V), while asterisks denote statistical significance after multiple-comparison correction.


{% include_relative figs/cross_cluster_conflict.html %}

The results reveal distinct linguistic profiles across clusters:

- `Cluster Relationships` is strongly associated with emotional and psychological language, including anxiety, sadness, anger, and overall negative emotion, alongside elevated cognitive mechanism terms. This suggests relationship-focused discussions are emotionally charged and introspective.

- `Cluster Complain About Reddit` shows a strong association with affective language, reflecting emotionally expressive and evaluative discourse centered on platform-related frustrations.

- `Cluster Cryptomania` is uniquely characterized by a heightened use of money-related language, consistent with a strong financial and investment-oriented focus.

- `Cluster Drama` is linked to both affective and sexual language, indicating emotionally intense and interpersonal narratives with sensational or provocative elements.

Together, these findings demonstrate that clusters differ not only in what topics they discuss, but also in how they express them linguistically, with each cluster exhibiting a distinct emotional and cognitive signature.



# From Digital to Real World
*TODO: 2016 U.S.A. presidential election*

{% include_relative figs/google_trends_us_presidential_election_topics_(2014-2017).html %}

{% include_relative figs/google_trends_2014-2017_detected_peak_per_topic.html %}

{% include_relative figs/political_activity_trends_peaks.html %}

{% include_relative figs/cross_party_negativity.html %}

{% include_relative figs/dem_rep_activity.html %}

{% include_relative figs/cross_negativity_over_quarter.html %}

{% include_relative figs/liwc_word_cloud_republican__to__democrat.html %}

{% include_relative figs/liwc_word_cloud_democrat__to__republican.html %}
