---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
### Spatio-Temporal Analysis of Drunkenness and Robbery in San Francisco

## Introduction
Over the past two months, we have been exploring crime data in San Francisco from the years 2003 to 2024. This [data](https://datasf.org/opendata/) have been combined from two distinct datasets. Clean data consists consists of crime incidents where each has a crime category, date and place of occurance.

During week 5 (our analysis is available [here](https://github.com/alonakonst/sda_crime_correlation/blob/main/week_5_crime_correlation.ipynb)) we have have noticed temporal correlation among selected group of crimes: weapon laws, robbery, drunkenness, assault and vandalism. By temporal correlation we mean pair wise-comparison of crime amount by hour of the week. In this report we start with overview of correlation of these group and proceed with focus on drunkenness and robbery spatio-temporal
relationship,

## Temporal Correlation
We begin with diving into plotting crime count of the crime group in question against hours of the week, as it can be seen in a graph below. Be aware, crime count is standardized. With drunkenness and robbery being preselected. We can clearly see that both tend to have similar pattern. Most of both crimes happen on Friday and Saturday nights. Sunday night is also peaking for drunkenness, but for robbery it is on a similar level as during weekdays. If remove drunkenness from the graph and add other crimes, we can see that they all four have similar pattern as robbery through out the week.

{% include crime_trends.html %}

However, we were wondering if this always the case through out the history of crime recordings, that five of these crimes are highly correlated. To answer that, we present a correlation matrix of Hour-By-Week pairwise comparison by possibility to choose a year of crime occurance. Moreover, on a bottom there is a time series of correlation coefficint of robbery and drunkenness through out the years.

The heatmap below visualizes the correlation between different crime categories based on their hour-of-the-week occurrence pattern. Each cell shows the Pearson correlation coefficient between two crime types, standardized over all 168 hours of the week (24 hours × 7 days). In this visualization, darker cells indicate stronger correlations, while brighter cells suggest weaker or no temporal alignment in crime activity.

A particularly striking pattern is the strong correlation between “robbery” and “drunkenness”, with a Pearson coefficient of 0.86. This implies that, overall, these two crimes tend to occur during similar hours of the week — likely concentrated around weekends or nightlife-related time slots.
When examining recent years individually, the correlation between robbery and drunkenness becomes noticeably weaker, indicating that this relationship may have changed over time, becoming weaker. Therefore, we chose to analyze the overall pattern across all years to better understand the deeper, long-term association between these two crime categories.


{% include crime_correlation_analysis.html %}

## Spatial Correlation
In San Francisco’s South of Market district, drunkenness and robbery—highly correlated crimes—peak, creating a notable hotspot. The block’s proximity to bars and nightlife fuels alcohol-related incidents, while its homeless population may contribute to opportunistic robberies. The mix of urban density, nightlife, and homelessness in this region calls for targeted solutions to address both root causes and immediate crime effects.

![Alt Text](/assets/map.jpeg)

## Conclusion


## Contributions

Alona s240400: Idea, Introduction, Temporal Correlation, Website formatting\
Paulo s242779: Idea, Temporal Correlation, Website formatting\
Felipe 244086: Spatial Correlation, Conclusion, Website formatting