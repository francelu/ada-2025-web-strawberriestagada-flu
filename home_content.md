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

{% include_relative figs/negativity_pulse.html %}


### Identifying the Verbal Arsenal

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

Below is plotted the linguistic characteristics evolution for negative outgoing interactions from `the_donald`.

{% include_relative figs/the_donald_negative_LIWC_dashboard.html %}

{% include_relative figs/swear_bubble_pic.html %}

Analyzing the evolution of negativity characteristics in conflictual outgoing events from the subreddit `the_donald` reveals similar trends for certain features. Indeed, two maxima can be observed during the same periods for the features `Negemo`, `Anger`, `vader_neg`, `Affect`, and less obviously for `frac_alpha` and `Swear`. These peaks occurred during weeks 2016-06 and 2017-02.

<!-- To have title below picture too -->
<div style="clear: both;"></div>


# Words as Weapons: How Do Inter-Subreddit Conflicts Affect Victims' Linguistic Recovery?


## Traces of Conflict: Influence of LIWC Characteristics on Post-Conflict Interaction Tones

<!-- How Does the Conflict LIWC Characteristics Impact the Afterward Interaction Tones of the Targeted Subreddit? -->

<!-- Text reviewed -->
To study the effect of conflict on the LIWC characteristics of a targeted subreddit, we computed the change in the subreddit's LIWC by comparing its mean LIWC after an incoming conflict during a 48-hour window with its mean LIWC before the conflict during a one-month window. Only situations without overlapping conflicts were chosen in order to study the effect of each conflict individually. Then, we applied a t-test to compare the obtained delta of LIWC to zero and determined the variables most correlated with each change in LIWC. We conducted the analysis in both the hyperlinks in the titles and the hyperlinks in the body because we assumed that the underlying mechanism of their use differed in the two cases.


### General Conflict Analysis

<!-- Text reviewed -->
When analyzing the bodies of the posts, the conflicts significantly altered the targeted subreddit's `LIWC AuxVb` and `Time` by increasing their utilization while decreasing the proportion of `LIWC Home`. No significant changes were observed for the non-LIWC features. Therefore, it is difficult to draw conclusions about these influences. When analyzing the titles of the posts, only the `LIWC Inhib` increased significantly, and no changes were observed for the non-LIWC features.


#### Analysis on the Body of the Posts

{% include_relative figs/body_general_LIWC.html %}

{% include_relative figs/body_general_nonLIWC.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_general_LIWC.html %}

{% include_relative figs/title_general_nonLIWC.html %}


### `the_donald` Case

{% include_relative figs/the_donald_case_pic.html %}

<!-- Text reviewed -->
To delve deeper into the analysis of the real world, individual analyses were also carried out. Here is an example using the targeted subreddit, `the_donald`. When analyzing the LIWC features of the posts' bodies, `LIWC Function`, `Adverbs`, and `Negation` increased significantly, while `Social` and `Body` decreased. No significant changes were observed for the non-LIWC features. When analyzing the LIWC features of the post titles, the `Excl`, `Money`, and `Assent` features decreased. Upon examining `the_donald` subreddit more closely, we observe some changes related to incoming conflicts. These changes can be explained by the composition of the subreddit and the characteristics of the conflicts. 

<!-- To have title below picture too -->
<div style="clear: both;"></div>


#### Analysis on the Body of the Posts

{% include_relative figs/body_donald_LIWC.html %}

{% include_relative figs/body_donald_nonLIWC.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_donald_LIWC.html %}

{% include_relative figs/title_donald_nonLIWC.html %}


### Correlated Incoming Linguistic Features

<!-- Text reviewed -->
The tables below show the most correlated incoming features for each of the delta features. The incoming feature `frac_upper`, which corresponds to the proportion of capital letters in the incoming text, seems to be correlated with the most delta features, such as `delta_num_long_sentences` and `delta_frac_specials` (the proportion of special characters in the text). 


#### Analysis on the Body of the Posts

{% include_relative figs/body_donald_corr.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_donald_corr.html %}



## The Rhythm of Recovery: How Communities Heal Their Linguistic Scars

<!-- How long does it take for the linguistic tone of a “victim” subreddit to return to its baseline after being targeted in a conflict? -->

{% include_relative figs/rhythm_of_recovery_pic.html %}

When a community is targeted by a hostile post, its language doesn't immediately return to normal. The emotional shockwave reverberates through subsequent conversations, creating a linguistic recovery curve. This is the time it takes for a community's distinctive voice to return to its baseline after being disrupted by conflict. We used time-series analysis to track how key psychological markers in targeted subreddits evolved over 48-hour periods following an attack. The visualization below reveals the immediate impact and gradual healing process across different dimensions of language.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/recovery_bar_plot.html %}

Our analysis reveals distinct patterns in how different psychological features respond to and recover from conflict. Social language and cognitive mechanisms demonstrate the most significant reductions following attacks, decreasing by -0.0003 and -0.0001, respectively. These findings suggest that communities respond to hostility by becoming less socially engaged and reducing their analytical thinking. This behavior is also observed in positive, negative, and neutral emotion words. Negative emotions show the largest increase, with rises in swear words, anger, sadness, and anxiety vocabulary.


### The Recovery Timeline: Fast Bounces and Lasting Scars

The recovery timeline reveals even more compelling insights. While most features recover relatively quickly (within 11.8-12.4 hours), many communities never fully return to baseline within the 48-hour window for certain linguistic features. Most strikingly:

- Cognitive mechanisms never recover in 37.6% of cases
- Social language never recovers in  33.8%% of cases 
- Positive emotion never recovers in  27.6%% of cases 

The recovery histogram below shows how long these linguistic disruptions typically persist across different psychological dimensions.

{% include_relative figs/recovery_histogram.html %}

{% include_relative figs/recovery_timeline_pic.html %}

Agreement, disagreement, and anxiety show the fastest recovery (11.6 hours), demonstrating resilience in these communication functions. However, the high rates of non-recovery for cognitive and social language functions suggest that attacks may cause lasting changes in how communities process information and interact socially.

While the immediate emotional spike of negativity and anxiety is short-lived, the most significant impact of a hostile post is the long-term reduction in social and analytical language use. This suggests that communities may not only be "hurt" in the short term but can be fundamentally altered, becoming less cohesive and less thoughtful in their discourse long after the initial attack has passed.

<!-- To have text below picture too -->
<div style="clear: both;"></div>


## The Contagion of Conflict: How Attacker Language Shapes Victim Response?

{% include_relative figs/contagion_of_conflict_pic.html %}

When one community attacks another, the emotional tone of the assault itself may determine how deeply the target is wounded. We investigated whether specific linguistic features in hostile posts act as psychological triggers that create predictable patterns in how victim communities respond. We used correlation analysis across multiple time segments to trace how the emotional and cognitive composition of an attack influences subsequent linguistic shifts in the targeted community. The visualization below shows which attacker features have the strongest ripple effect.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/attack_LIWC_correlation.html %}

The data clearly shows patterns of emotional contagion and behavioral mirroring:

- Swear words in attacks trigger anger responses: the strongest correlation (r = 0.021) links attacker profanity to increased anger language in victim communities,
- Victims mirror profanity: target communities significantly increase their own swear word usage when attacked with profanity (r = 0.020),
- Sexual language escalates: attacks containing profanity also correlate with increased sexual language in responses (r = 0.019).

Interestingly, religious language in attacks correlates with increased social language in victim responses (r = 0.017). This suggests that communities may respond to religiously themed attacks by strengthening social bonds. Conversely, sadness in attacks correlates with reduced social language in targets (r = -0.016), indicating that emotionally vulnerable attacks may suppress community engagement.

{% include_relative figs/influential-attack.html %}

Our analysis reveals that swear is the most powerful linguistic trigger in attacks, with swear words in hostile posts having the strongest influence on victim responses. Although these correlations are statistically significant, the effect sizes are generally small. This suggests that, although attacker language influences victim responses, the relationship is subtle and mediated by many other factors. 


## Analysis of Response to Conflict

{% include_relative figs/response_to_conflict_pic.html %}

<!-- Text reviewed -->
This section examines how a subreddit under attack may respond to the attacking subreddit, considering the characteristics of the attacking hyperlinks' comments. The analyses performed here are similar to those performed for the general case, but are applied only to outgoing activities of the subreddit directed toward the attacker within 72 hours after the incoming conflict begins. 

<!-- Text reviewed -->
As in the conflict analysis, the plots below illustrate the changes in linguistic features of outgoing interactions from the targeted subreddit towards the source of the conflict. The significant increase in non-LIWC characteristics indicates longer texts containing more words, sentences, and special characters. Thus, the targeted subreddit responds to the source of the conflict with more intense comments than it does to a random hyperlink mention.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>


#### Analysis on the Body of the Posts

{% include_relative figs/body_conflict_response_LIWC.html %}

{% include_relative figs/body_conflict_response_nonLIWC.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_conflict_response_LIWC.html %}

{% include_relative figs/title_conflict_response_nonLIWC.html %}


## Random Forest Analysis

<!-- Text reviewed -->
To estimate the linguistic characteristics that impact the targeted subreddit the most, we used a Random Forest model to identify the features that best predict post-conflict linguistic changes. The tables below summarize the results obtained from this method. Due to the difficulty of fitting the data, not all linguistic feature deltas could be predicted. While it is difficult to draw conclusions from the results, the influence of certain conflict features is intriguing. For example, in the title analysis, the delta of the `LIWC Negate` feature was influenced by LIWC features such as `Dissent` or `frac_upper`, which could be considered aggressive.


#### Analysis on the Body of the Posts

{% include_relative figs/body_random_forest.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_random_forest.html %}


# Snowball Effect

{% include_relative figs/snowball_effect_pic.html %}

Online communities often interact through conflict, which can trigger cascading patterns of negativity. In this section, we will examine whether negative language from attacking subreddits influences the subsequent emotional and linguistic behaviors of targeted communities, producing a snowball effect of cumulative negativity. How do repeated inter-subreddit conflicts shape the linguistic and emotional tone (LIWC features) of targets over time, and do these patterns suggest a cumulative negativity ?

We use Granger causality tests to determine whether being attacked (receiving negative sentiment posts) causally influences a community's subsequent negative behavior. These tests examine whether knowledge of past values in one time series (attacks received) improves the prediction of another time series (negative behavior emitted).

<!-- To have text below picture too -->
<div style="clear: both;"></div>


## Community Response Pattern

The Granger causality heatmap below shows which communities have statistically significant causal relationships between being attacked and subsequently exhibiting negative behavior. Darker colors indicate stronger effects.

{% include_relative figs/granger_analysis.html %}


### Results

{% include_relative figs/community_response_pattern.html %}

{% include_relative figs/snowball_effect_results_pic.html %}

Based on the heatmap, we can conclude that attacks cause negative behavior in certain communities. Among them, `subredditdram` is the most vulnerable; attacks consistently lead to negative behavior for more than five hours. `politics` is highly reactive, with immediate and sustained negative responses, while `news` has a quick reaction, but of shorter duration. The plot shows that, in general, drama and politics communities are most vulnerable to attack. This the majority of communities show significant effects even 4-5 hours after the initial attack. Despite thematic differences, the pattern of negative responses to attacks appears to be a cross-cutting phenomenon with consistency across communities.

These results suggest that online attacks systematically create cycles of negativity that spread across different types of communities. Theses effects often persist for 4-5 hours, indicating that online conflicts can have influence on the tone of discussions long after the attack.

<!-- To have text below picture too -->
<div style="clear: both;"></div>


# Cluster Profiling

{% include_relative figs/cluster_profiling_pic.html %}

Online communities often form clusters based on shared common interests, behaviors, or emotional dynamics. These clusters can exhibit distinctive patterns in how their members use language, reflecting differences in emotional, cognitive, and social expression. How do the linguistic profiles of online community clusters, as captured through LIWC features, relate to and predict the propagation of conflict between communities? What are the distinctive LIWC profiles of different community clusters during periods of normal interaction?

In this part, subreddits are gathered in clusters of communities, made on the positive network (affection between subreddits) using the Louvain method and one the embedding (similarity of the subreddits respect to their posting users) using a k-mean algorithm. To simplify the analysis, only the 7 most virulent clusters are selected. Each cluster is assigned to each subreddit and a theme is manually assigned to each cluster as shown on below plot.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/cluster_profile.html %}

To analyze language patterns across clusters, LIWC features were first simplified into binary indicators showing whether a category appeared more or less than average. We then used chi-square tests to examine whether certain clusters were more likely to use specific types of language than would be expected by chance. To avoid false positives from running many tests, p-values were adjusted using false discovery rate correction. In the heatmap below, color intensity reflects the strength of association (Cramér’s V), while asterisks denote statistical significance after multiple-comparison correction.

{% include_relative figs/cross_cluster_conflict.html %}

The results reveal distinct linguistic profiles across clusters:

- `Cluster Relationships` is strongly associated with emotional and psychological language, including anxiety, sadness, anger, and overall negative emotion, alongside elevated cognitive mechanism terms. This suggests relationship-focused discussions are emotionally charged and introspective.

- `Cluster Complain About Reddit` shows a strong association with affective language, reflecting emotionally expressive and evaluative discourse centered on platform-related frustrations.

- `Cluster Cryptomania` is uniquely characterized by a heightened use of money-related language, consistent with a strong financial and investment-oriented focus.

- `Cluster Drama` is linked to both affective and sexual language, indicating emotionally intense and interpersonal narratives with sensational or provocative elements.

Together, these findings demonstrate that clusters differ not only in what topics they discuss, but also in how they express them linguistically, with each cluster exhibiting a distinct emotional and cognitive signature.


# From Digital to Real World - 2016 Presidential Election

{% include_relative figs/digital_real_intro_pic.html %}

*TODO: 2016 U.S.A. presidential election*  
To link Reddit conflict dynamics with real-world events, we first use Google Trends to track the public's interest in relevant topics over time, such as the United States presidential election, key candidates, and notable events. Peaks in search interest allow us to identify moments when global attention was heightened. We can then compare these moments with spikes in negative interactions between subreddit clusters.

<!-- To have text below picture too -->
<div style="clear: both;"></div>


## Global Events from Google Trends

We will analyze the topic of the "United States presidential election" using Google Trends data from January 1, 2014, to April 30, 2017.
In the next section, we will display the plots of the following people:
- `US_presidential_election`,
- `Donald_Trump`,
- `Trump_movie`,
- `Trump_vs_Clinton_movie`,
- and `UK_Brexit`.

{% include_relative figs/google_trends_2014-2017_detected_peak_per_topic.html %}

Using the maximum-interest dates detected for each topic, it is clear that several peaks correspond to major political events during the 2016 U.S. presidential cycle or other events that had a global impact:
- **`US_presidential_election` — Peak on November 6, 2016**  
    This peak occurred two days before the U.S. presidential election on November 8, 2016. Public attention was at its maximum as voters searched for polls, forecasts, and last-minute news. This peak is the largest in the entire dataset and aligns with the period's most intense political moment.
- **`Donald_Trump` — Peak on November 6, 2016**  
    This coincides with the pre-election surge that occurred before. As media coverage intensified, debates concluded, and final campaign events took place, searches for the eventual winner sharply increased.
- **`Trump_movie` — Peak on February 7, 2016**  
    This peak aligns with the February 2016 primary season, when media content about Trump surged, including documentaries, commentary videos, and satirical releases. This reflects the secondary cultural attention surrounding the election.
- **`Trump_vs_Clinton_movie` — Peak on September 25, 2016**  
    This week coincides with the first presidential debate between Donald Trump and Hillary Clinton on September 26, 2016. It was one of the most-watched political debates in U.S. history, which explains the spike in searches for related media content.
- **`UK_Brexit` — Peak on June 19, 2016**  
    This is the week immediately preceding the Brexit referendum on June 23, 2016. The outcome shocked global markets and sparked renewed interest in populism worldwide, generating significant cross-country attention that overlaps with U.S. political discourse.


## Linking Global Events to Reddit Activity

After identifying major political and global events using Google Trends, the next step is to examine whether these events correspond to changes in online dynamics. To accomplish this, we will turn to Reddit datasets, which offer extensive behavioral data on user interactions within political and non-political communities. Aligning the previously detected event dates with Reddit activity patterns, such as conflict scores, cross-community interactions, and posting volume, makes it possible to assess whether spikes in public attention and political tension translate into measurable fluctuations on Reddit. The Reddit data will be analyzed in the following sections with this goal in mind, allowing for a direct comparison between offline events and online reactions.


### Comparison with Google Trends Peaks

{% include_relative figs/google_comparison_pic.html %}

The goal now is to compare the activity of political subreddits with major events identified in Google Trends. By examining how Reddit discussions align with broader public interest, we can better understand the dynamics of political engagement online.

First, we filter the dataset to include only subreddits with known party labels. Then, we compute daily post counts for each party. Next, we identify the dates of peak activity for subreddits labeled as Republican or Democrat.

Finally, we compare these Reddit peaks with Google Trends peaks and visualize the results using a time series plot. In the plot, daily post counts are shown in color (red for Republican and blue for Democrat), and vertical dashed lines indicate corresponding Google Trends peaks. This allows for an intuitive assessment of their alignment.

<!-- To have text below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/political_activity_trends_peaks.html %}

From the comparison, we can see that Republican-labeled subreddits were more active than Democrat-labeled ones during the analyzed period. Additionally, Reddit activity peaks generally follow major events highlighted by Google Trends. For instance, both parties show increased activity around the U.S. presidential election on November 6, 2016, with Reddit peaks occurring shortly after (Republicans: November 9, 2016; Democrats: November 7, 2016). Another notable alignment occurred around the UK Brexit vote on June 19, 2016, reflecting heightened political discussion on Reddit in response to a globally significant event. Overall, these results suggest that Reddit activity partially mirrors broader public interest, as reflected in search trends, particularly during significant political events.


### Compute Cross-Sentiments Between the Groups

To measure negativity in interactions between political communities, we focus on cross-party interactions. This means we look at posts where a subreddit from one party engages with a subreddit from the other party, such as Republican → Democrat or Democrat → Republican. First, we map the target subreddit to its party label, keeping only interactions where both the source and target parties are known. From these interactions, we select only cross-party ones. For each direction, we calculate the total number of interactions and the number of negative interactions, which we define as those with a `LINK_SENTIMENT` value of -1, following our previously defined conflict metric, we then calculate a negativity rate. We also estimate 95% confidence intervals for these rates using a normal approximation. Finally, we visualize the results with a bar plot showing the negativity rates and their confidence intervals. This allows us to compare the intensity of negative sentiment across political communities.

{% include_relative figs/cross_party_negativity.html %}


*TODO: (Laura) t-test ?*


### Party Representation and Cross-Party Activity

We observe that Republican subreddits are very active in cross-party interactions. However, this raises the question of whether their higher activity is simply due to overrepresentation. To investigate this, we compared the number of subreddits and posts generated by each party. After excluding neutral subreddits, we counted the number of Democrat and Republican communities, as well as their total posts in cross-party interactions. This comparison allows us to determine if the observed differences in activity reflect genuine engagement patterns or if they are driven by the larger number of Republican subreddits.

{% include_relative figs/dem_rep_activity.html %}

The results show that although there are fewer Republican subreddits than Democrat subreddits, they generate more posts in cross-party interactions. This suggests that their increased activity is not due to overrepresentation, but rather, reflects a greater level of engagement in political discussions.


### Temporal Evolution of Cross-Party Negativity

Now, we analyze how negativity between political subreddits evolves over time. We do this by computing the quarterly negativity rate for cross-party interactions and excluding neutral communities. For each quarter, we calculate the proportion of interactions with a `LINK_SENTIMENT` of -1 for both Republican → Democrat and Democrat → Republican interactions.

We visualize the results as a line plot showing the quarterly negativity trends for each party. This allows us to observe how cross-party sentiment changes over time and identify periods with higher levels of negative engagement.

{% include_relative figs/cross_negativity_over_quarter.html %}

Overall, we observe that Republican subreddits display higher negativity rates toward Democrats than Democrats do toward Republicans. Throughout the observed period, this suggests that stronger negative sentiment consistently comes from Republican communities in cross-party interactions.


### LIWC Word Cloud of Party

We now visualize the language used in cross-party interactions by plotting LIWC-based word clouds. Specifically, we generate separate word clouds for posts from Republican subreddits directed at Democratic subreddits (Republican → Democratic) and for posts from Democratic subreddits directed at Republican subreddits (Democratic → Republican). This allows us to see which words and categories dominate the discourse between these two political communities.

{% include_relative figs/liwc_word_cloud_republican__to__democrat.html %}

{% include_relative figs/liwc_word_cloud_democrat__to__republican.html %}

Upon inspection, the LIWC word clouds do not reveal clear or relevant patterns that distinguish Republican and Democrat interactions. While some common words and categories appear, they do not offer significant insights beyond those observed in the negativity and activity analyses.