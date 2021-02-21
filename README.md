# Topic-Modeling-the-Anti-Vaccine-Movement

Since the Covid-19 outbreak, talks of vaccine have occupied public discourse. When a vaccine for the pandemic finally rolled out, people rejoiced over the news. Yet, on the Internet scores of opinions swayed toward condemnation rather than approval.

The anti-vaccine movement dates back before the current pandemic. This particular crusade, though, poses threats that are of here and now. Therefore, I felt imperative to delve into understanding the movement.

More specifically, I wanted to know what goes on in the minds of anti-vaxxers to think and act the way they do? Could we achieve more nuanced understanding of their inner psychology? 

I started off this undertaking by heading over to where I could unearth a sleuth of opinions. And that is Twitter. 

I used Tweepy to help me interact with Twitter's API. From there, I procured more than four million tweets, all centered around "vaccination". 

Next was preprocessing the tweets to remove symbols not within the English lexicon. Those were special characters like emojis and hashtags. 

Preprocessing is a must to achieve structure. Otherwise, comprehensibility among the mass of informal and colloquial tweets would be difficult. 

Now came analysis. I put the tweets into Vader's SentimentIntensityAnalyzer. Scores of Positive, Neutral, and Negative corresponded to the tweets' sentiment leanings.

![Image](https://github.com/tengmelody/Topic-Modeling-the-Anti-Vaccine-Movement/blob/main/img/sentiment%20scores.png)

From there, I took only the negative tweets. I chose them because they seemed more likely to imply the anti-vaccine sentiment. 

I then put the negative tweets into Sklearn's Latent Dirichlet Allocation. This operation clustered the tweets into distinct categories based on term frequency. 

NMF was another clustering technique I could have utilized. But I chose to go with LDA because the results appeared more relevant to the context. 

With the categories finalized, I used the pyLDAvis library to generate a visual graph. The library creates a visualization that is interactive. On one side, it showed how prevalent each topic is and its relevancy to others. The other side ranked the terms most useful to interpret a topic. 

I started this project with the intention to understand the minds of anti-vaxxers. I wanted to know the factors that influence their thinkings. Yet Twitter, as a platform, offers a rather trivial and cursory way of expressing opinions. Instead of unearthing any insightful details on psychology, my findings felt more surface. The topics tended to lean more toward current event musings. 

To improve and deepen the insights of this project, I want to analyze other social media contents. 
