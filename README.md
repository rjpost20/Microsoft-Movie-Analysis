# Phase 1 Project: *Microsoft Movie Analysis*

![Movie Studio](https://user-images.githubusercontent.com/105675055/171872770-14bb5453-3b7a-4d2d-b59c-6cb7c820d110.jpg)

<br>

## Project Overview

This project uses exploratory data analysis (EDA) to generate insights for Microsoft Corp. in their undertaking of the creation of a new movie studio. By analyzing film runtimes, genres, ratings, number of ratings, and box office revenues from an IMDb dataset and a box office dataset, I provide three recommendations to Microsoft to maximize the likelihood of success in their creation of new content for their studio.

<br>

## Business Problem

Microsoft has seen the success of other major tech companies with their creation of film and TV studios, and has decided to undertake their own venture. However, they have limited experience and knowledge on the minutiae of successful content creation. As such, I have been tasked with analyzing the most successful films to provide actioniable insights on what types of content are most likely to be succeed for Microsoft.

<br>

## Data

In this project I use a dataset from IMDb which contains information on film title, genre, runtime, year, average rating, and number of ratings. I also use a dataset of box office revenues, which contains information on film box office statistics, both foreign and domestic.

<br>

## Analysis

### Box office revenues by genre

My first analysis examines the highest grossing movie genres, domestic and foreign.

We can see that adventure and action stand out amongst the pack as the highest grossing film genres in both domestic and foreign markets. While we may be tempted to suggest that the film studios should prioritize these genres, we have to be cautious of the effect of outliers. Many of the highest grossing films of all time, such as Avatar, Avengers, and Spider-Man, tend to be adventure and/or action films, but this does not necessarily mean that the average adventure and/or action film will perform well.

Another insight we can obtain from this analysis is that domestic markets tend to prefer crime films (at 6th highest grossing) compared to foreign markets (where crime is 8th highest grossing). We also see that foreign markets tend to favor mystery films (at 5th highest grossing) compared to domestic markets (7th highest grossing).

<img width="990" alt="Domestic Revenues by Genre" src="https://user-images.githubusercontent.com/105675055/171882367-2da037fa-2ba8-4c15-a489-bc11c8bd01b8.png">

<img width="990" alt="Foreign Revenues by Genre" src="https://user-images.githubusercontent.com/105675055/171882582-6dc2e2d2-e3bc-41f2-922f-a9005332832e.png">

<br>

### Box office revenues by IMDb rating

My second analysis examines box office revenues, domestic and foreign, by IMDb rating.

We can see that there is a positive correlation between average IMDb rating and domestic box office revenues. We can also see that there is an even stronger correlation between average IMDb rating and foreign box office revenues. We would expect the average IMDb rating for a film to correlate with its revenues, but we might not expect the correlation to be stronger in foreign markets than in domestic markets.

<img width="990" alt="Domestic Revenues by Rating" src="https://user-images.githubusercontent.com/105675055/171882780-c49e0580-a9b7-4128-a8ff-90e69ff80bc7.png">

<img width="990" alt="Screen Shot 2022-06-03 at 11 16 33 AM" src="https://user-images.githubusercontent.com/105675055/171882836-60ac4893-3259-4042-888b-e6b835063220.png">

<br>

### Average IMDb rating by Runtime

My third and final analysis examines average IMDb rating by runtime, segmented into 10 minute bins.

There is a clear upward trend in average IMDb rating until a film reaches 130 to 140 minutes, and then the rating drops off. However, surpassing 160 minutes, the average rating increases rapidly, surpassing the previous global maximum. Similar to our first analysis, we should be cautious with concluding that films should be longer than 160 minutes. While the effect of outliers will not be as strong here (ratings involve a 10 point scale, while revenues can reach into the billions), it's possible that film studios only tend to produce such extended films when they are especially confident of their success.

<img width="990" alt="Screen Shot 2022-06-03 at 11 16 53 AM" src="https://user-images.githubusercontent.com/105675055/171882879-35f0cac2-f5a7-4c93-bf00-dc117da90a08.png">

<br>

## Recommendations

This analysis leads to four recommendations for content creation in Microsoft's new movie studio:
- **If the studio's first short- or medium-term goal is exposure over profits, opt for adventure, action, and comedy films.** These films tend to gross the highest, but as mentioned in the analysis they are not necessarily the most profitable.
- **Take note of whether the film will be primarily targeted to foreign or domestic markets, and adjust film genre accordingly.** Favor the crime genre for films that will solely or primarily be targeted to domestic audiences. For films targeted to foreign audiences, favor the mystery genre. The crime genre ranked two spots higher in domestic box office revenues than in foreign revenues, while the mystery genre ranked two spots higher in foreign box office revenues than in domestic revenues.
- **Give priority to producing highly rated content for films that cater to foreign markets.** Domestic audiences are more forgiving at the box office for lower rated movies than foreign audiences tend to be. In theory one would expect that all content is produced with a high viewer rating in mind, but in practice studios generally know which content is more risky or experimental. Microsoft studios should save the experimental/risky films for domestic markets, in which the films may fare better if they do not garner high ratings.
- **Aim for a runtime range of 130 to 140 minutes for most films.** This is the local maximum of average IMDb rating in the range of films from 80 to 160 minutes (in 10 minute increments). With that said, the studio should also not be afraid to produce extended movies beyond 160 minutes if they are confident in the success of the film. Such situations could involve sequels to hit movies, film adaptations of popular novels, and movies with multiple A-list actors, for example.

<br>

## Next Steps and Remaining Questions

Further analysis could yield additional and/or more accurate insights for content creation:
- **Replace revenues with profits and see if the outcomes differ.** In this analysis we used domestic and foreign box office revenues as a proxy for the generalized "success" of a film. However, this does not control for the expenses outlayed on a film. It may be that adventure films tend to gross the highest, but the additional costs for adventure films outweight the benefit, for example. One could envision horror films faring well profit-wise due to the typically low costs associated with horror films, despite low average revenues.
- **Segment runtimes vs. ratings by genre.** We saw that, among all movies, 130 to 140 minutes tended to yield the highest average rating, along with movies beyond 160 minutes. But it's likely that this is not true for all genres. Some genres may be more conducive to a shorter runtime, while others fare better with longer runtimes. For example, one would expect most consumers to favor documentaries in the range of 60 to 90 minutes vs. 120 minutes plus, while the opposite may be true for adventure movies.
- **Analyze film success by release month, and further segment by genre.** The datasets used in this analysis did not include release month, but other datasets do. Looking at datasets of revenues or profits per release month, segemented by genre, could tell us the release months most conducive to box office success for each genre.
- **Account for effects of inflation.** As the gross revenues dataset did not account for the effects of inflation, more recent films will be more heavily weighted compared to older films. This could skew our results. One solution would be to use a dataset of annual inflation going back to our oldest film, and apply it to each row in our dataframe. Even better would be a dataset on annual box office inflation.
- **Why does average IMDb rating spike after a film runtime surpasses 160 minutes?** One would expect the trendline to continue downward after 160 minutes, but instead we see the opposite. Is this simply an artifact of popular hit movies tending to be longer, or is something else going on in addition here?
- **What is it about adventure and action movies that make them the highest grossing film genres?** Similar to the above, this could simply be an artifact of popular hit movies tending to come in the form of (expensive) adventure and action "epics". But it's possible that there are underlying characteristics of these genres that make them more popular among consumers, that we can then utilize to maximize the chance of success for Microsoft's content.
