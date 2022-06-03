# Phase 1 Project: Microsoft Movie Analysis

![Movie Studio](https://user-images.githubusercontent.com/105675055/171872770-14bb5453-3b7a-4d2d-b59c-6cb7c820d110.jpg)


## Project Overview

This project uses exploratory data analysis (EDA) to generate insights for Microsoft Corp. in their undertaking of the creation of a new movie studio. By analyzing film runtimes, genres, ratings, number of ratings, and box office revenues from an IMDb dataset and a box office dataset, I provide three recommendations to Microsoft to maximize the likelihood of success in their creation of new content for their studio.


## Business Problem

Microsoft has seen the success of other major tech companies with their creation of film and TV studios, and has decided to undertake their own venture. However, they have limited experience and knowledge on the minutiae of successful content creation. As such, I have been tasked with analyzing the most successful films to provide actioniable insights on what types of content are most likely to be succeed for Microsoft.


## Data

In this project I use a dataset from IMDb which contains information on film title, genre, runtime, year, average rating, and number of ratings. I also use a dataset of box office revenues, which contains information on film box office statistics, both foreign and domestic.


## Analysis



## Recommendations

This analysis leads to four recommendations for content creation in Microsoft's new movie studio:
- **If the studio's first short- or medium-term goal is exposure over profits, opt for adventure, action, and comedy films.** These films tend to gross the highest, but as mentioned in the analysis they are not necessarily the most profitable.
- **Take note of whether the film will be primarily targeted to foreign or domestic markets, and adjust film genre accordingly.** Favor the crime genre for films that will solely or primarily be targeted to domestic audiences. For films targeted to foreign audiences, favor the mystery genre. The crime genre ranked two spots higher in domestic box office revenues than in foreign revenues, while the mystery genre ranked two spots higher in foreign box office revenues than in domestic revenues.
- **Give priority to producing highly rated content for films that cater to foreign markets.** Domestic audiences are more forgiving at the box office for lower rated movies than foreign audiences tend to be. In theory one would expect that all content is produced with a high viewer rating in mind, but in practice studios generally know which content is more risky or experimental. Microsoft studios should save the experimental/risky films for domestic markets, in which the films may fare better if they do not garner high ratings.
- **Aim for a runtime range of 130 to 140 minutes for most films.** This is the local maximum of average IMDb rating in the range of films from 80 to 160 minutes (in 10 minute increments). With that said, the studio should also not be afraid to produce extended movies beyond 160 minutes if they are confident in the success of the film. Such situations could involve sequels to hit movies, film adaptations of popular novels, and movies with multiple A-list actors, for example.

## Next Steps and Remaining Questions

Further analysis could yield additional and/or more accurate insights for content creation:
Replace revenues with profits and see if the outcomes differ. In this analysis we used domestic and foreign box office revenues as a proxy for the generalized "success" of a film. However, this does not control for the expenses outlayed on a film. It may be that adventure films tend to gross the highest, but the additional costs for adventure films outweight the benefit, for example. One could envision horror films faring well profit-wise due to the typically low costs associated with horror films, despite low average revenues.
Segment runtimes vs. ratings by genre. We saw that, among all movies, 130 to 140 minutes tended to yield the highest average rating, along with movies beyond 160 minutes. But it's likely that this is not true for all genres. Some genres may be more conducive to a shorter runtime, while others fare better with longer runtimes. For example, one would expect most consumers to favor documentaries in the range of 60 to 90 minutes vs. 120 minutes plus, while the opposite may be true for adventure movies.
Analyze film success by release month, and further segment by genre. The datasets used in this analysis did not include release month, but other datasets do. Looking at datasets of revenues or profits per release month, segemented by genre, could tell us the release months most conducive to box office success for each genre.
Account for effects of inflation. As the gross revenues dataset did not account for the effects of inflation, more recent films will be more heavily weighted compared to older films. This could skew our results. One solution would be to use a dataset of annual inflation going back to our oldest film, and apply it to each row in our dataframe. Even better would be a dataset on annual box office inflation.
Why does average IMDb rating spike after a film runtime surpasses 160 minutes? One would expect the trendline to continue downward after 160 minutes, but instead we see the opposite. Is this simply an artifact of popular hit movies tending to be longer, or is something else going on in addition here?
What is it about adventure and action movies that make them the highest grossing film genres? Similar to the above, this could simply be an artifact of popular hit movies tending to come in the form of (expensive) adventure and action "epics". But it's possible that there are underlying characteristics of these genres that make them more popular among consumers, that we can then utilize to maximize the chance of success for Microsoft's content.
