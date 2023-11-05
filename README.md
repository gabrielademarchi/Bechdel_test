# Cracking the Code of Cinema: A Data-Driven Dive into the Bechdel Test
Harnessing data to illuminate the on-screen female representation in film with Python  

So there we were, my sister and I, on a lazy Saturday afternoon, half looking for something to watch and half scrolling through social media, when we stumble upon the Bechdel Test on the depts of a reddit debate. You know, that test that checks if the women in a movie talk about something other than a men? Yes, that one. For those uninitiated, the Bechdel Test was a concept introduced in 1985 by Alison Bechdel, which evaluates women’s roles in movies under three criteria:

Are there at least two named female characters in the film?
Do they talk to each other?
Is their conversation about something other than a man?

As movie buffs with a knack for patterns, we were intrigued. How have movies stood the test of time in meeting this criteria? So, instead of settling down with the latest “binge-worthy” series, we opted for a different kind of Saturday entertainment. 
Armed with curiosity and an unhealthy amount of sweet popcorn, we embarked on a quest not just to pass the time, but to pass judgement on decades of cinematic storytelling. Because nothing says 'fun weekend' quite like charts and statistics, right?

Research Questions:
Our analysis was guided by four key questions:

1. The Evolution of the Bechdel Test: How have Bechdel Test scores evolved over time? Are films today more likely to pass the test than their predecessors?

2. Genre by Genre Breakdown: Do comedies laugh in the face of the Bechdel Test, or do dramas take it more seriously? We compared different genres to see how they stack up.

3. Directorial Deeds: Which directors have been championing female representation in the past decade, and who could use a nudge in the right direction?

4. Ratings vs. Representation: Is there a correlation between a movie's Bechdel Test score and its ratings? Do critics and audiences appreciate films that give women more substantial roles?

Understanding the Bechdel Rating
In the Bechdel Test, not all passes are created equal. The test comes with a rating system, a scale from 0 to 3, each number a stepping stone of representation: 
0 indicates the absence of two named female characters, 
1 suggests these characters do not engage in conversation. 
2 means the characters do converse, but their dialogue revolves around a man.
3 signifies a film where two women talk about something other than a man, reflecting a fuller representation of female characters.  

In our analysis, we've chosen to focus on films that achieve a score of "3" on the Bechdel Test. We felt that this score was more significant as it indicates a film where women are not only present, but are also more pivotal to the plot, having agency and narratives untethered from their male counterparts. 

Limitations: the Bechdel Test as a starting point, not a cure-all medicine
While the Bechdel Test offers a measure for female presence in film, it's not without its limitations. It doesn't account for the quality of female representation or the complexity of their roles. A film can pass the Bechdel Test and still portray women in a stereotypical or sexist manner. Conversely, a film might fail the test due to a setting that limits female presence, such as "The Name of the Rose," or because of a small cast, like in "Gravity."

The application of the test also has a degree of subjectivity. The definition of what constitutes a conversation, or whether the mere mention of a man disqualifies the exchange, can vary. This ambiguity can affect the consistency of the test's application.

Even though a film’s passing score is not a guarantee of a substantive female character representation, the Bechdel test can be a useful tool for identifying trends and sparking discussion. And our aim with this analysis is to do just that. 🙂

Data Collection & Preparation:
We found an great API at bechdeltest.com, which provided a comprehensive list of 10,136 movies, complete with their IMDb IDs, release years, and Bechdel ratings. To add depth to our analysis, we enriched this list with a dataset from Kaggle, which included additional details such as movie directors, genres, ratings, and more. We then merged the datasets to create a cohesive structure, using the IMDb ID as a common key between them. Finally, we cleaned the the data by keeping only the most relevant columns. 




Check Kaggle for the dataset.
Code in this post can be found in this GitHub repo.


Data Analysis:

Charting the Change: the Bechdel Test through the decades
How have Bechdel Test scores evolved over time? 

Our analysis began by mapping out the trajectory of the Bechdel test from the early 1900s to the present day. Starting from the 80s we see a significant rise in both in number of movies produced and the number of films passing the Bechdel Test. It's a positive trend, suggesting a growing awareness of the need for female representation on screen.

Delving into the era before the sixties, the data presented a near-even split, indicating a hit-or-miss approach to women’s roles in cinema during that period. This discovery sparked our curiosity, leading us to dig a little deeper. What we uncovered was both interesting and inspiring: during the silent film era, women were powerhouses in scriptwriting and film production. Women penned the outlines for about half of all films, and many were instrumental behind the scenes, taking on roles as producers, directors, and studio heads.

This led us to wonder: could the silent era's impressive Bechdel Test pass rates be attributed to these pioneering women? 
Regardless of the reason, this newfound knowledge about women's early influence in cinema was a delightful revelation. The more you know, right?



Genre Breakdown: The Good, The Bad, and The Data
How do different movie genres compare in terms of passing the Bechdel Test over the past decade?
Moving on to our genre analysis,  there's a general balance in Bechdel Test pass rates: most genres seem to give their female characters something to talk about besides the leading men. 
But let's talk about Westerns. They're the underachievers of the Bechdel world, with less than 20% making the cut. Most don't even tick the first box of having two women to name. 
Even when we look at newer Western movie, things still look quite grim for the genre. 
Take, the movie 'Brimstone', for example, a rare Western that is actually centred around a female protagonist. Despite its focus, the character's tongue is literally cut off early in the film. It's a stark metaphor for the genre's historical muffling of women's voices. With their testosterone-fueled narratives and a less-than-stellar record of female empowerment, Westerns often ride into the sunset of Bechdel oblivion.

Yet, this could be the perfect plot twist for a Netflix production. Imagine a Western where women aren't just part of the backdrop but are driving the action, embodying the untold strength of historical heroines. So here's a nugget of inspiration for any Netflix bigwig reading this: an all-female Western could be your next showstopper. How about we give those cowboy boots to the ladies for a change?



Director's Cut: The Leaders and the Laggards
How do movie directors with the most films over the past decade compare in terms of passing the Bechdel Test?

Turning the lens on directors, Paul Feig and Mike Flanagan stand out with a perfect track record. Feig's 'Bridesmaids' not only passes the Bechdel Test but does so with flying colours, offering a fresh narrative full of rich and incredibly funny female characters. Similarly, Flanagan's works, such as 'The Haunting of Hill House', provide a platform for women's stories to unfold.
On the other end of the spectrum, we have Clint Eastwood, Antoine Fuqua, and Ron Howard, who seem to be directing in a Bechdel desert. With scores as low as 0.20 and 0.00, it's a stark reminder of the genre biases that still exist. Their films, often steeped in gritty realism or historical contexts, tend to sideline the female voice. It's noteworthy that war movies, a genre these directors frequently visit, muster a Bechdel pass rate barely over 40%, having the second lowest pass rate after Westerns. This is not just just a missed opportunity; it's a narrative bottleneck that's begging for a rewrite.



Bechdel Rating vs. IMDb Rating Correlation 
Is there a correlation between a movie's Bechdel Test score and its ratings?

Finally, we looked into the dynamic between Bechdel ratings and IMDb ratings. The relationship here is a somewhat subtle one, with a slight negative trend that's statistically significant, which certainly piqued our interest. It's not the kind of dramatic revelation that would end a thriller, but it does invite some thoughtful speculation. Could it be that films with stronger female representation are receiving lower ratings from audiences and critics, perhaps without even realizing it? Or could this just be an unexpected twist in the vast narrative of film ratings? While the data isn't giving away all the answers, it's definitely food for thought—something to mull over and an invitation for further investigation. 



In the end, our data-driven dive into the Bechdel Test reveals a narrative that's still unfolding. It's a story of progress and plateaus, of genres and directors who champion female voices, and those who could use a little nudge from the muse of equality. As the credits roll on our analysis, we're left with both hope and a call to action. Because in the grand cinema of life, everyone deserves not just a seat but a voice in the story.


