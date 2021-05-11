---
layout: page
title: RE- Spatial-temporal and content analysis of Twitter Data
---


**Replication of**
# Spatial, temporal and content analysis of Twitter data

Original study *by* Wang, Z., X. Ye, and M. H. Tsou. 2016. Spatial, temporal, and content analysis of Twitter for wildfire hazards. *Natural Hazards* 83 (1):523–540. DOI:[10.1007/s11069-016-2329-6](https://doi.org/10.1007/s11069-016-2329-6).
and
First replication study by Holler, J. 2021 (in preparation). Hurricane Dorian vs Sharpie Pen: an empirical test of social amplification of risk on social media.

Replication Author: Brooke Laird


Replication Materials Available at: [brookelaird.github.io](brookelaird.github.io)

Created: `04 May 2021`
Revised: `10 May 2021`

## Abstract

Why study the spatial distribution of Twitter data?

Wang et al (2016) analyzed Twitter data for wildfires in California, finding that the social media data served as a useful tool in characterizing the trends of wildfires across space, and the ways that local community members and groups--specifically local media/news groups and government authorities--can use social media to spread news of disaster updates. While social media has always been a useful piece of data for studying the trends in populations, the increase in geotagged tweets (and other examples of social media data) as a geospatial tool helps with tracking trends that reflect dominant flows of information with a spatial dimension.

Holler (2021) is studying Twitter data for Hurricane Dorian on the Atlantic coast, finding that in spite of tending news and social media content regarding a false narrative of risk, original Tweets still clustered significantly along the real hurricane track, and only along the hurricane track.

Reproducing and replicating spatial research of these two studies, and API research and mapping more generally, continues to be relevant because the increase in studies involving the spatial distribution of twitter data helps to identify areas where API based research can be improved, and also areas where this research has lead to great advancements and new findings.

In his replication study, I will examine the spatial distribution of twitter data that contains the words "vaccine" "pfizer" and "moderna." I centered my analysis on the city of Atlanta, Georgia, and will use twitter data that is available for an 1,000 km buffer around the point, between the temporal window of May 5-May 9, 2021.  My classmates, Emma Brown and Hannah Rigdon, will be completing the same analysis but for different regions of the United States, in hopes of completing a full national map illustrating the spatial distribution of twitter data about Covid-19 vaccinations.


## Original Study Information

**summarize Wang et al (2016) similar to the Holler (2021) summary below**

Holler (2021) losely replicated the methods of Wang et al (2016) for the case of Hurricane Dorian's landfall on the U.S. mainland during the 2019 Atlantic Hurricane season. Data was based on Twitter Search API queries for ....

Holler modified Wang et al's methods by not searching for retweets for network analysis, focusing instead on original Tweet content with keywords hurricane, Dorian, or sharpiegate (a trending hashtag referring to the storm). Holler modified the methodology for normalizing tweet data by creating a normalized Tweet difference index and extended the methodology to test for spatial cluserting with the local Getis-Ord statistic. The study tested a hypothesis that false narratives of hurricane risk promulgated at the highest levels of the United States government would significantly distort the geographic distribution of Twitter activity related to the hurricane and its impacts, finding that original Twitter data still clustered only in the affected areas of the Atlantic coast in spite of false narratives about risk of a westward track through Alabama.

Wang et al (2016) conducted their study using the `tm` and `igraph` packages in `R 3.1.2`. Is it known what GIS software was used for spatial analysis?
The replication study by Holler (2021) used R, including the rtweet, rehydratoR, igraph, sf, and spdep packages for analysis.

## Materials and Procedure

Outline the data to be used in your replication study, including:

- twitter search parameters
- attach / link to files containing status_id's for the search results
- any data used to normalize the tweets
- methods for analysis / synthesis

## Replication Results

- ![temporal analysis graph](temporal.png)
This temporal analysis graph shows when tweets that contained our words of interest (vaccine, pfizer, moderna) were most trending during the 6 day window.

- ![content analysis graph](content.png)
A content analysis graph of the most popular words, and words that were linked together, demonstrate the language that was most frequently used in the tweets. An interesting finding here is the stronger linkage between vaccine and support, over vaccine and hesitancy. However, tweets that contained the word hesitancy do not indicate places where there was hesitancy, instead it shows that vaccine twitter language is more frequently using positive language (support). Furthermore, the links between vaccine and clinic show that twitter is a dominant way that individuals may be able to find out about vaccination opportunities near them.

- ![map of twitter activity](tweetmap.png)
Tweet locations normalized by population density help to illustrate where tweets were most dominant. Tweet locations still tended to be concentrated in urban areas, which may reflect a common demographic of twitter users (young, urban, educated) (Crawford 2014).

- ![hot spot analysis](hotspots.png)
This hot spot analysis map illustrates the clusters of tweets mentioning vaccinations for the buffer around the city of Atlanta, Georgia (not the entire United States). The cluster in southern Florida is interesting, as that is an area that has been a popular travel destination recently.

## Unplanned Deviations from the Protocol

There were few deviations from the replication of the Holler (2021) Hurricane Dorian lab. One change was the addition of a rehydration step to get my data back into R studio, which used the rehydratoR package tool. During the analysis, the only stop words that I used were the common stop words generated by twitter, however in the Dorian lab replication we had used a series of other stop words that made sense for the content.

## Discussion

Provide a summary and interpretation of your key findings in relation to your research question. Mention if findings confirm or contradict patterns observed by Wang et al (2016) or by Holler (2

## Conclusion

This reproduction of both Wang et al. and Holler is a useful tool for starting to use twitter data as a means for examining

## References

Include any referenced studies or materials in the [AAG Style of author-date referencing](https://www.tandf.co.uk//journals/authors/style/reference/tf_USChicagoB.pdf).

####  Report Template References & License

This template was developed by Peter Kedron and Joseph Holler with funding support from HEGS-2049837. This template is an adaptation of the ReScience Article Template Developed by N.P Rougier, released under a GPL version 3 license and available here: https://github.com/ReScience/template. Copyright © Nicolas Rougier and coauthors. It also draws inspiration from the pre-registration protocol of the Open Science Framework and the replication studies of Camerer et al. (2016, 2018). See https://osf.io/pfdyw/ and https://osf.io/bzm54/

Camerer, C. F., A. Dreber, E. Forsell, T.-H. Ho, J. Huber, M. Johannesson, M. Kirchler, J. Almenberg, A. Altmejd, T. Chan, E. Heikensten, F. Holzmeister, T. Imai, S. Isaksson, G. Nave, T. Pfeiffer, M. Razen, and H. Wu. 2016. Evaluating replicability of laboratory experiments in economics. Science 351 (6280):1433–1436. https://www.sciencemag.org/lookup/doi/10.1126/science.aaf0918.

Camerer, C. F., A. Dreber, F. Holzmeister, T.-H. Ho, J. Huber, M. Johannesson, M. Kirchler, G. Nave, B. A. Nosek, T. Pfeiffer, A. Altmejd, N. Buttrick, T. Chan, Y. Chen, E. Forsell, A. Gampa, E. Heikensten, L. Hummer, T. Imai, S. Isaksson, D. Manfredi, J. Rose, E.-J. Wagenmakers, and H. Wu. 2018. Evaluating the replicability of social science experiments in Nature and Science between 2010 and 2015. Nature Human Behaviour 2 (9):637–644. http://www.nature.com/articles/s41562-018-0399-z.