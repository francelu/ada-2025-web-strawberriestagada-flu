---
layout: page
---


# Introduction

{% include_relative figs/intro_pic.html %}

<!-- Text reviewed -->
In the digital realm, words spread faster than intentions. A single post can ignite tension between distant communities, leaving traces that reshape their emotional landscapes. This project tells the story of how online hostility unfolds, lingers, and transforms the language of those affected by it. Focusing on Reddit communities from 2014 to 2017, the project examines how conflicts between subreddits reveal deeper patterns of collective emotion. It explores how anger spreads and how communities recover. It also considers how repeated clashes may harden or exhaust communities over time. By tracing these emotional aftershocks, the project seeks to understand not only moments of division, but also linguistic healing process. Beyond individual disputes, the project asks how local conflicts mirror broader societal shifts, from everyday tensions to global political events. Our goal is to reveal what our digital language reveals about resilience, contagion, and the shared emotional life of online communities.

<!-- Text reviewed -->
This project investigates the dynamics of conflict between Reddit communities, considering language as a measurable indicator of social friction. Specifically, we examine how verbal attacks between subreddits can function as linguistic weapons, how communities recover from them, and whether repeated exposure to conflict can create a snowball effect of negativity. By linking these digital battles to real-world political events related to the 2016 U.S. presidential election, we aim to reveal the profound connection between online discourse and the offline world.

<!-- To have text below picture too -->
<div style="clear: both;"></div>


# A Portrait of the Dataset

<!-- Text reviewed -->
The following visualizations provide an overview of the language that shapes our digital landscape.


## Sunburst Plot

<!-- Text reviewed -->
The Sunburnst plot below reveals the most prevalent psychological and linguistic features across the entire Redit network. It offers insight into the shared emotional vocabulary of Reddit users.

{% include_relative figs/sunburst_LIWC.html %}


## Tracing the Contours of Conflicts

<!-- Text reviewed -->
Now that we know what our data contains, we can trace the flow of negativity. How does hostility manifest itself? How does it spread through the network over time?

<!-- Text reviewed -->
The word clouds below illustrate the stark contrast between positive and negative interactions. One is a landscape of cohesion and reward. The other is a storm of anger and negation. This dichotomy is the fundamental emotional dynamic of intercommunity conflict.


### Lexicon of Positivity

{% include_relative figs/lexicon_positivity.html %}


### Lexicon of Negativity

{% include_relative figs/lexicon_negativity.html %}


### The Pulse of Negativity Over Time

<!-- Text reviewed -->
When do conflicts flare up? The following timelines zoom from years down to days, revealing the rhythms and eruptions of online hostility. They allow us to identify long-term trends and pinpoint the days when the digital world held its breath.

{% include_relative figs/negativity_pulse.html %}


### Identifying the Verbal Arsenal

{% include_relative figs/verbal_arsenal_pic.html %}

<!-- Text reviewed -->
Not all negative language is created equal. Some words are more potent weapons than others. Using a Random Forest model, we analyzed through the linguistic features of hostile posts to identify the most powerful predictors of negative messages. The following chart reveals the most damaging elements in the verbal arsenal — the sharpest tools used in digital conflict.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/verbal_arsenal.html %}

<!-- Text reviewed -->
Our analysis reveals that several linguistic characteristics are powerful indicators of negative messages. `VADER Negative` emerges as the best predictor, which makes sense since it is a sentiment analysis tool designed specifically to process informal social media language. The presence of capital letters and special characters suggests an emotional message. The most predictive LIWC features are:
- Negative emotions, such as anger and swear words;
- Cognitive processes, which suggest more thoughtful and elaborate messages;
- And a social dimension, which indicates complex relational interactions.


### Outgoing Interactions from `the_donald`

<!-- Text reviewed -->
The linguistic characteristics evolution of negative outgoing interactions from `the_donald` are plotted below.

{% include_relative figs/the_donald_negative_LIWC_dashboard.html %}

{% include_relative figs/swear_bubble_pic.html %}

<!-- Text reviewed -->
Analyzing the evolution of negative characteristics in conflict-related outgoing events from the subreddit the_donald reveals similar trends for certain features. Three peaks occurred during the same periods for the features `Negemo`, `vader_neg`, and `Affect`. Less obviously, peaks occurred for `Anger` and `Swear` as well. The first two peaks correspond to significant moments in Donald Trump’s 2016 campaign. The first peak occurred on February 22, 2016, during the Republican primary surge that month, and the second peak occurred on September 5, 2016, in relation to Labor Day, marking the start of the intensified general election campaign. The final peak occurred on January 19, 2017, the day before Trump's presidential inauguration.

<!-- To have title below picture too -->
<div style="clear: both;"></div>


# Words as Weapons: How Do Inter-Subreddit Conflicts Affect Victims' Linguistic Recovery?


## Traces of Conflict: Influence of LIWC Characteristics on Post-Conflict Interaction Tones

<!-- Text reviewed -->
To study the effect of conflict on the LIWC characteristics of a targeted subreddit, we computed the change in the subreddit's LIWC by comparing its mean LIWC after an incoming conflict during a 48-hour window with its mean LIWC before the conflict during a one-month window. Only situations without overlapping conflicts were chosen in order to study the effect of each conflict individually. Then, we applied a t-test to compare the obtained delta of LIWC to zero and determined the variables most correlated with each change in LIWC. We conducted the analysis in both the hyperlinks in the titles and the hyperlinks in the body because we assumed that the underlying mechanism of their use differed in the two cases.


### General Conflict Analysis

<!-- Text reviewed -->
When analyzing the bodies of the posts, the conflicts significantly altered the targeted subreddit's `LIWC_AuxVb` and `LIWC_Time` by increasing their utilization while decreasing the proportion of `LIWC_Home`. No significant changes were observed for the non-LIWC features. Therefore, it is difficult to draw conclusions about these influences. When analyzing the titles of the posts, only the `LIWC_Inhib` increased significantly, and no changes were observed for the non-LIWC features.


#### Analysis on the Body of the Posts

{% include_relative figs/body_general_LIWC.html %}

{% include_relative figs/body_general_nonLIWC.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_general_LIWC.html %}

{% include_relative figs/title_general_nonLIWC.html %}


### `the_donald` Case

<!-- Text reviewed -->
To ground the analysis in concrete cases, we conducted subreddit-level analyses. One example is the targeted subreddit, `the_donald`.


#### Analysis on the Body of the Posts

{% include_relative figs/body_donald_LIWC.html %}

{% include_relative figs/body_donald_nonLIWC.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_donald_LIWC.html %}

{% include_relative figs/title_donald_nonLIWC.html %}

{% include_relative figs/the_donald_case_pic.html %}

<!-- Text reviewed -->
Following incoming conflicts, the body of posts shows significant increases in function words, adverbs, and negations (`LIWC_Funct`, `LIWC_Adverbs`, `LIWC_Negate`), aw well as decreases in social and body-related terms (`LIWC_Social`, `LIWC_Body`). Together, these patterns reveal a shift toward a more argumentative and defensive writing style. Users rely more on grammatical structure and explicit negation to express opposition, and references to social relationships or concrete experiences become less common. This suggests that post-conflict discourse focuses less on interaction or shared experience and more on asserting positions and rejecting opposing viewpoints. No significant changes were observed for non-LIWC features.

<!-- Text reviewed -->
In contrast, changes in post titles are smaller and different. The decrease in exclusion words (`LIWC_Excl`) and assent words (`LIWC_Assent`) suggests that titles become more direct and less nuanced after conflicts. The drop in money-related terms (`LIWC_Money`) likely reflects a shift in topics rather than style. Overall, titles seem to focus on framing the post, while the detailed arguments appear in the body.

<!-- To have title below picture too -->
<div style="clear: both;"></div>


### Correlated Incoming Linguistic Features

<!-- Text reviewed -->
The tables below show the most correlated incoming features for each of the delta features.


#### Analysis on the Body of the Posts

{% include_relative figs/body_donald_corr.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_donald_corr.html %}

<!-- Text reviewed -->
In the body analysis, the incoming feature `frac_upper`, which corresponds to the proportion of capital letters in the text, appears to be correlated with the most delta features. These include delta_num_long_sentences and delta_frac_specials, which are the proportions of long sentences and special characters in the text, respectively. `frac_upper` indeed captures the intensity of the incoming conflict. High use of capital letters typically signals emphasis, urgency, or aggression. These messages are more likely to provoke stronger reactions in the targeted subreddit, resulting in longer posts, more sentences, and higher character and word counts as users respond with explanations, arguments, or counterattacks rather than brief replies. The high occurrence of positive correlations implies that capitalization may not be a causal driver itself, but rather a proxy for conflict severity that amplifies linguistic activity and stylistic expressiveness following the conflict.

<!-- Text reviewed -->
The analysis of titles reveals a markedly different mechanism. Unlike the body text, `frac_upper` does not play a dominant role, and no single linguistic feature clearly stands out in terms of influence. This is further supported by the lower overall correlation values, which indicate weaker and more diffuse associations between incoming features and LIWC changes in titles.


## The Rhythm of Recovery: How Communities Heal Their Linguistic Scars

{% include_relative figs/rhythm_of_recovery_pic.html %}

<!-- Text reviewed -->
After a community is targeted by a hostile post, it takes time for the community's language to return to normal. The emotional shockwave reverberates through subsequent conversations, creating a linguistic recovery curve. This is the amount of time it takes for a community's distinctive voice to return to its baseline after being disrupted by conflict. Using time-series analysis, we tracked how key psychological markers in targeted subreddits evolved over 48-hour periods following an attack. The visualization below reveals the immediate impact and gradual healing process across different dimensions of language.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/recovery_bar_plot.html %}

<!-- Text reviewed -->
Our analysis reveals distinct patterns in how different psychological features respond to and recover from conflict. Social language and cognitive mechanisms show the most significant reductions after attacks, decreasing by 0.0003 and 0.0001, respectively. These results imply that communities respond to hostility by becoming less socially engaged and reducing analytical thinking. This behavior is also observed in words expressing positive, negative, and neutral emotions. Negative emotions show the largest increase, reflected by rises in swear words, anger, sadness, and anxiety vocabulary.


### The Recovery Timeline: Fast Bounces and Lasting Scars

<!-- Text reviewed -->
The recovery timeline provides additional compelling insights. While most features recover relatively quickly within 11.8 to12.4 hours, many communities never fully return to baseline within the 48-hour window for certain linguistic features. Most strikingly:

<!-- Text reviewed -->
- Cognitive mechanisms never recover in 37.6% of cases,
- Social language never recovers in  33.8% of cases,
- And positive emotion never recovers in  27.6% of cases.

<!-- Text reviewed -->
The recovery histogram below shows how long these linguistic disruptions typically persist across various psychological dimensions.

{% include_relative figs/recovery_histogram.html %}

{% include_relative figs/recovery_timeline_pic.html %}

<!-- Text reviewed -->
Agreement, disagreement, and anxiety show the fastest recovery (11.6 hours), demonstrating resilience in these communication functions. However, the high rates of non-recovery for cognitive and social language functions suggest that attacks may cause lasting changes in how communities process information and interact socially. While the immediate emotional spike of negativity and anxiety is brief, the most significant consequence of a hostile post is the long-term reduction in social and analytical language use. This suggests that communities may not only be "hurt" in the short term but that an attack can fundamentally alter them, making them less cohesive and less thoughtful in their discourse long after the initial attack has passed.

<!-- To have text below picture too -->
<div style="clear: both;"></div>


## The Contagion of Conflict: How Attacker Language Shapes Victim Response?

{% include_relative figs/contagion_of_conflict_pic.html %}

<!-- Text reviewed -->
When one community attacks another, the emotional tone of the assault itself may determine how deeply the target is wounded. We investigated whether specific linguistic features in hostile posts act as psychological triggers that create predictable patterns in how victim communities respond. Using correlation analysis across multiple time segments, we traced how the emotional and cognitive composition of an attack influences subsequent linguistic shifts in the targeted community. The visualization below shows which features of the attackers have the strongest ripple effect.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/attack_LIWC_correlation.html %}

<!-- Text reviewed -->
The data clearly shows patterns of emotional contagion and behavioral mirroring:

<!-- Text reviewed -->
- Swear words used in attacks trigger anger responses: the strongest correlation (r = 0.021) links profanity used by attackers to an increase in angry language used by victim communities,
- Victims mirror profanity: target communities significantly increase their own swear word usage when attacked with profanity (r = 0.020),
- Sexual language escalates: attacks containing profanity also correlate with increased sexual language in responses (r = 0.019).

<!-- Text reviewed -->
Interestingly, religious language in attacks correlates with increased social language in victim responses (r = 0.017). This suggests that communities may respond to religiously themed attacks by strengthening social bonds. Conversely, sadness in attacks correlates with reduced social language in targets (r = -0.016), indicating that emotionally vulnerable attacks may suppress community engagement.

{% include_relative figs/influential-attack.html %}

<!-- Text reviewed -->
Our analysis reveals that swear is the most powerful linguistic trigger in attacks. Swear words in hostile posts have the strongest influence on victim responses. While these correlations are statistically significant, the effect sizes are generally small. This suggests that, although attacker language influences victim responses, the relationship is subtle and influenced by many other factors.


## Analysis of Response to Conflict

<!-- Text reviewed -->
This section examines how a subreddit under attack may respond to the attacking subreddit, considering the characteristics of the attacking hyperlinks' comments. The analyses performed here are similar to those performed for the general case, but are applied only to outgoing activities of the subreddit directed toward the attacker within 72 hours after the incoming conflict begins.

<!-- Text reviewed -->
As in the conflict analysis, the plots below illustrate the changes in linguistic features of outgoing interactions from the targeted subreddit towards the source of the conflict.


#### Analysis on the Body of the Posts

{% include_relative figs/body_conflict_response_LIWC.html %}

{% include_relative figs/body_conflict_response_nonLIWC.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_conflict_response_LIWC.html %}

{% include_relative figs/title_conflict_response_nonLIWC.html %}

{% include_relative figs/response_to_conflict_pic.html %}

<!-- Text reviewed -->
For the post bodies, LIWC changes were minimal, with only a decrease in `LIWC_Bio`, which is difficult to interpret. Non-LIWC features, however, show a general increase across all metrics (`num_chars`, `num_long_sentences`, `num_words`, etc.), suggesting that responses tend to be longer and more elaborate.

<!-- Text reviewed -->
For the post titles, the LIWC features show widespread increases. This includes function words, pronouns, verbs, present/future tense, adverbs, swear words, inclusive/exclusive terms, and more. In contrast, there were decreases in references to family, humans, causation, relative terms, and religion. Non-LIWC features mirror the body, showing an overall increase in length and complexity.

<!-- Text reviewed -->
Overall, these patterns suggest that when under attack, the subreddit responds with longer, more detailed, and linguistically richer posts in both the body and the title. Increases in function, pronoun, verb, and social/cognitive words indicate a shift toward active engagement, argumentation, and social signaling. Decreases in family, humans, and religious terms may reflect a narrowing of the content focus to conflict-related topics rather than general discussion.

<!-- To have text below picture too -->
<div style="clear: both;"></div>


## Random Forest Analysis

<!-- Text reviewed -->
To estimate the linguistic characteristics that impact the targeted subreddit the most, we used a Random Forest model to identify the features that best predict post-conflict linguistic changes. The tables below summarize the results obtained from this method. Due to the difficulty of fitting the data, not all linguistic feature deltas could be predicted.


#### Analysis on the Body of the Posts

{% include_relative figs/body_random_forest.html %}


#### Analysis on the Title of the Posts

{% include_relative figs/title_random_forest.html %}

<!-- Text reviewed -->
Analysing the body, the Random Forest analysis indicates that incoming stylistic and emotional cues seem to shape the subreddit's linguistic response. Capitalization (`frac_upper`), in particular, emerges as a strong predictor of increases in `LIWC_Certain`, suggesting that messages with high emphasis or intensity trigger more assertive responses. Incoming posts with numerical content (`frac_digits`) tend to trigger responses that mirror quantitative references or formatting, likely because users engage with facts, figures, or structured arguments.

<!-- Text reviewed -->
Analysing the titles, it is clear that the subreddit's responses are influenced by stylistic and structural cues. Capitalization (`frac_upper`) is linked to affective and syntactic features, and sentiment (`vader_compound`) is related to social and cognitive words and capitalization. This shows that the tone and emphasis of incoming titles influence how the subreddit frames its replies.


# Snowball Effect

{% include_relative figs/snowball_effect_pic.html %}

<!-- Text reviewed -->
Online communities often interact through conflict, which can trigger cascading patterns of negativity. In this section, we will examine whether negative language from attacking subreddits influences the subsequent emotional and linguistic behaviors of targeted communities, creating a snowball effect of cumulative negativity. How do repeated inter-subreddit conflicts shape the linguistic and emotional tone (LIWC features) of targets over time, and do these patterns suggest a cumulative negativity ?

<!-- Text reviewed -->
We use Granger causality tests to determine if being attacked (i.e., receiving negative sentiment posts) influences a community's subsequent negative behavior. These tests examine whether knowledge of past values in one time series improves the prediction of another time series. In this case, the first time series is attacks received, and the second is negative behavior emitted.

<!-- To have text below picture too -->
<div style="clear: both;"></div>


## Community Response Pattern

<!-- Text reviewed -->
The Granger causality heatmap below shows which communities have statistically significant causal relationships between being attacked and subsequently exhibiting negative behavior. Darker colors indicate stronger effects.

{% include_relative figs/granger_analysis.html %}


### Results

{% include_relative figs/community_response_pattern.html %}

{% include_relative figs/snowball_effect_results_pic.html %}

<!-- Text reviewed -->
Based on the heatmap, we can conclude that attacks cause negative behavior in certain communities. Among them, `subredditdram` is the most vulnerable; attacks consistently lead to negative behavior for more than five hours. `politics` is highly reactive, with immediate and sustained negative responses, while `news` has a quick reaction, but of shorter duration. The plot shows that, in general, drama and politics communities are most vulnerable to attack. Thus, the majority of communities show significant effects even 4-5 hours after the initial attack. Despite thematic differences, the pattern of negative responses to attacks appears to be a cross-cutting phenomenon with consistency across communities.

<!-- Text reviewed -->
These results suggest that online attacks systematically create cycles of negativity that spread across different types of communities. These effects often persist for 4-5 hours, indicating that online conflicts can have influence on the tone of discussions long after the attack.

<!-- To have text below picture too -->
<div style="clear: both;"></div>


# Cluster Profiling

{% include_relative figs/cluster_profiling_pic.html %}

<!-- Text reviewed -->
Online communities often form clusters based on shared common interests, behaviors, or emotional dynamics. These clusters can exhibit distinctive patterns in how their members use language, reflecting differences in emotional, cognitive, and social expression. How do the linguistic profiles of online community clusters, as captured through LIWC features, relate to and predict the propagation of conflict between communities? What are the distinctive LIWC profiles of different community clusters during periods of normal interaction?

<!-- Text reviewed -->
In this part, subreddits are gathered in clusters of communities, made on the positive network (affection between subreddits) using the Louvain method and one the embedding (similarity of the subreddits respect to their posting users) using a k-mean algorithm. To simplify the analysis, only the 7 most virulent clusters are selected. Each cluster is assigned to each subreddit and a theme is manually assigned to each cluster as shown in the below plot.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/cluster_profile.html %}

<!-- Text reviewed -->
To analyze language patterns across clusters, LIWC features were first simplified into binary indicators showing whether a category appeared more or less than average. We then used chi-square tests to examine whether certain clusters were more likely to use specific types of language than would be expected by chance. To avoid false positives from running many tests, p-values were adjusted using false discovery rate correction. In the heatmap below, color intensity reflects the strength of association (Cramér’s V), while asterisks denote statistical significance after multiple-comparison correction.

{% include_relative figs/cross_cluster_conflict.html %}

<!-- Text reviewed -->
The results reveal distinct linguistic profiles across clusters:

<!-- Text reviewed -->
- `Cluster Relationships` is strongly associated with emotional and psychological language, including anxiety, sadness, anger, and overall negative emotion, alongside elevated cognitive mechanism terms. This suggests relationship-focused discussions are emotionally charged and introspective.
- `Cluster Complain About Reddit` shows a strong association with affective language, reflecting emotionally expressive and evaluative discourse centered on platform-related frustrations.
- `Cluster Cryptomania` is uniquely characterized by a heightened use of money-related language, consistent with a strong financial and investment-oriented focus.
- `Cluster Drama` is linked to both affective and sexual language, indicating emotionally intense and interpersonal narratives with sensational or provocative elements.

<!-- Text reviewed -->
Together, these findings demonstrate that clusters differ not only in what topics they discuss, but also in how they express them linguistically, with each cluster exhibiting a distinct emotional and cognitive signature.


# From Digital to Real World - 2016 Presidential Election

{% include_relative figs/digital_real_intro_pic.html %}

<!-- Text reviewed -->
To link Reddit conflict dynamics with real-world events, we first use Google Trends to track the public's interest in relevant topics over time, such as the United States presidential election, key candidates, and notable events. Peaks in search interest allow us to identify moments when global attention was heightened. We can then compare these moments with spikes in negative interactions between subreddit clusters.

<!-- To have text below picture too -->
<div style="clear: both;"></div>


## Global Events from Google Trends

<!-- Text reviewed -->
We will analyze the topic of the "United States presidential election" using Google Trends data from January 1, 2014, to April 30, 2017.
In the next section, we will display the plots of the following people:

<!-- Text reviewed -->
- `US_presidential_election`,
- `Donald_Trump`,
- `Trump_movie`,
- `Trump_vs_Clinton_movie`,
- and `UK_Brexit`.

{% include_relative figs/google_trends_2014-2017_detected_peak_per_topic.html %}

<!-- Text reviewed -->
Using the maximum-interest dates detected for each topic, it is clear that several peaks correspond to major political events during the 2016 U.S. presidential cycle or other events that had a global impact:

<!-- Text reviewed -->
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

<!-- Text reviewed -->
After identifying major political and global events using Google Trends, the next step is to examine whether these events correspond to changes in online dynamics. To accomplish this, we will turn to Reddit datasets, which offer extensive behavioral data on user interactions within political and non-political communities. Aligning the previously detected event dates with Reddit activity patterns, such as conflict scores, cross-community interactions, and posting volume, makes it possible to assess whether spikes in public attention and political tension translate into measurable fluctuations on Reddit. The Reddit data will be analyzed in the following sections with this goal in mind, allowing for a direct comparison between offline events and online reactions.


### Comparison with Google Trends Peaks

{% include_relative figs/google_comparison_pic.html %}

<!-- Text reviewed -->
The goal now is to compare the activity of political subreddits with major events identified in Google Trends. By examining how Reddit discussions align with broader public interest, we can better understand the dynamics of political engagement online.

<!-- Text reviewed -->
First, we filter the dataset to include only subreddits with known party labels. Then, we compute daily post counts for each party. Next, we identify the dates of peak activity for subreddits labeled as Republican or Democrat.

<!-- Text reviewed -->
Finally, we compare these Reddit peaks with Google Trends peaks and visualize the results using a time series plot. In the plot, daily post counts are shown in color (red for Republican and blue for Democrat), and vertical dashed lines indicate corresponding Google Trends peaks. This allows for an intuitive assessment of their alignment.

<!-- To have graph below picture too -->
<div style="clear: both;"></div>

{% include_relative figs/political_activity_trends_peaks.html %}

<!-- Text reviewed -->
From the comparison, we can see that Republican-labeled subreddits were more active than Democrat-labeled ones during the analyzed period. Additionally, Reddit activity peaks generally follow major events highlighted by Google Trends. For instance, both parties show increased activity around the U.S. presidential election on November 6, 2016, with Reddit peaks occurring shortly after (Republicans: November 9, 2016; Democrats: November 7, 2016). Another notable alignment occurred around the UK Brexit vote on June 19, 2016, reflecting heightened political discussion on Reddit in response to a globally significant event. Overall, these results suggest that Reddit activity partially mirrors broader public interest, as reflected in search trends, particularly during significant political events.


### Compute Cross-Sentiments Between the Groups

<!-- Text reviewed -->
To measure negativity in interactions between political communities, we focus on cross-party interactions. This means we look at posts where a subreddit from one party engages with a subreddit from the other party, such as Republican → Democrat or Democrat → Republican. First, we map the target subreddit to its party label, keeping only interactions where both the source and target parties are known. From these interactions, we select only cross-party ones. For each direction, we calculate the total number of interactions and the number of negative interactions, which we define as those with a `LINK_SENTIMENT` value of -1, following our previously defined conflict metric, we then calculate a negativity rate. We also estimate 95% confidence intervals for these rates using a normal approximation. Finally, we visualize the results with a bar plot showing the negativity rates and their confidence intervals. This allows us to compare the intensity of negative sentiment across political communities.

{% include_relative figs/cross_party_negativity.html %}

<!-- Text reviewed -->
We can ask whether being affiliated with a political party makes a subreddit more or less negative, compared to neutral communities. To explore this, we compare the negativity rates (`LINK_SENTIMENT` = -1) of party-labeled subreddits with neutral ones using a t-test. Specifically, we compare Democrats vs. Neutral on Republican targets and Republicans vs. Neutral on Democrat targets. This allows us to test whether party affiliation is associated with stronger negative sentiment toward the opposing side.

<!-- Text reviewed -->
Negative rate comparison on Republicans (Neutral vs. Democrats):
- t-statistic: -0.1256
- p-value: 0.9002

<!-- Text reviewed -->
Negative rate comparison on Democrats (Neutral vs. Republican):
- t-statistic: -3.829
- p-value: 0.0001552

<!-- Text reviewed -->
The t-test results show that, for interactions targeting Republicans, there is no significant difference between Democrats and neutral subreddits in negativity (p = 0.90). In contrast, for interactions targeting Democrats, Republicans are significantly more negative than neutral subreddits (p < 0.001). This indicates that being neutral or Democrat does not affect negativity toward Republicans, while Republican subreddits tend to exhibit stronger negative sentiment toward Democrats compared to neutral communities.


#### Party Representation and Cross-Party Activity

<!-- Text reviewed -->
We observe that Republican subreddits are very active in cross-party interactions. However, this raises the question of whether their higher activity is simply due to overrepresentation. To investigate this, we compared the number of subreddits and posts generated by each party. After excluding neutral subreddits, we counted the number of Democrat and Republican communities, as well as their total posts in cross-party interactions. This comparison allows us to determine if the observed differences in activity reflect genuine engagement patterns or if they are driven by the larger number of Republican subreddits.

{% include_relative figs/dem_rep_activity.html %}

<!-- Text reviewed -->
The results show that although there are fewer Republican subreddits than Democrat subreddits, they generate more posts in cross-party interactions. This suggests that their increased activity is not due to overrepresentation, but rather, reflects a greater level of engagement in political discussions.


#### Temporal Evolution of Cross-Party Negativity

<!-- Text reviewed -->
Now, we analyze how negativity between political subreddits evolves over time. We do this by computing the quarterly negativity rate for cross-party interactions and excluding neutral communities. For each quarter, we calculate the proportion of interactions with a `LINK_SENTIMENT` of -1 for both Republican → Democrat and Democrat → Republican interactions. We visualize the results as a line plot showing the quarterly negativity trends for each party. This allows us to observe how cross-party sentiment changes over time and identify periods with higher levels of negative engagement.

{% include_relative figs/cross_negativity_over_quarter.html %}

<!-- Text reviewed -->
Overall, we observe that Republican subreddits display higher negativity rates toward Democrats than Democrats do toward Republicans. Throughout the observed period, this suggests that stronger negative sentiment consistently comes from Republican communities in cross-party interactions.


### Comparison with other non political clusters

<!-- Text reviewed -->
We extend our analysis to examine how non-political clusters interact with the political sphere. Specifically, we measure the negativity rates of posts originating from non-political clusters directed at political subreddits. To do this, we map each target subreddit to its party label and merge this information with the cluster assignments of the source subreddits. We then compute, for each non-political cluster, the fraction of negative interactions directed toward Democrats, Republicans, and neutral subreddits. By ranking clusters based on total activity toward the political sphere, we can identify which non-political communities are most engaged and which tend to be more negative. This allows us to assess the influence and sentiment patterns of non-political clusters in political discussions. We examine which non-political clusters show the highest negativity toward political subreddits. By computing the negativity rates for each non-political cluster toward Democrats, Republicans, and neutral subreddits, we can identify which communities are more negative in cross-cluster interactions.

<!-- Text reviewed -->
From the results, we can see that two clusters exhibit the highest negativity rates across the political sphere, with values exceeding 15% for both Democratic and Republican targets. The first cluster corresponds to our previously identified political cluster, containing the highest proportion of political subreddits. Because of this overlap, we consider it outside the scope of purely non-political clusters and exclude it from that part of the analysis. The second cluster contains subreddits like `campusreform`, `mensrights`, `circlebroke`, and `askstrawfeminists`, highlighting culture war and social critique topics.

<!-- Text reviewed -->
In contrast, other clusters show lower negativity, often below 12%. For instance, a cluster features `phones`, `techwar`, and `conspiracytheories`, indicating a focus on technology and conspiracy. Another cluster, with subreddits such as `politicalscience`, `interrail`, and `tunisia`, centers on geography, travel, and general knowledge. Yet another cluster, including `nonfictionbookclub`, `foreignpolicy`, and `debateacatholic`, is more oriented toward academic, religious, and literary topics. Overall, this indicates that certain non-political clusters are particularly more negative when interacting with political subreddits, often reflecting the themes of their communities.


### LIWC Word Cloud of Party

<!-- Text reviewed -->
We now visualize the language used in cross-party interactions by plotting LIWC-based word clouds. Specifically, we generate separate word clouds for posts from Republican subreddits directed at Democratic subreddits (Republican → Democratic) and for posts from Democratic subreddits directed at Republican subreddits (Democratic → Republican). This allows us to see which words and categories dominate the discourse between these two political communities.

{% include_relative figs/liwc_word_cloud_republican__to__democrat.html %}

{% include_relative figs/liwc_word_cloud_democrat__to__republican.html %}

<!-- Text reviewed -->
Upon inspection, the LIWC word clouds do not reveal clear or relevant patterns that distinguish Republican and Democrat interactions. While some common words and categories appear, they do not offer significant insights beyond those observed in the negativity and activity analyses.


# Contributions

<!-- Text reviewed -->
We are the strawberriestagada team. [Here](https://github.com/epfl-ada/ada-2025-project-strawberriestagada) is the link to our GitHub repository.

{% include_relative figs/strawberriestagada_pic.html %}

{% include_relative figs/end_gif.html %}
