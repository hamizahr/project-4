# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 4 - Predict Dengue Cases


### Problem Statement

To predict peak periods and locations to start the Wolbachia intervention with past data of dengue cases, temperature and weather patterns.

The dataset we used were: 
- meterological data (http://www.weather.gov.sg/climate-historical-daily/)
- dengue cases (https://data.gov.sg/dataset/weekly-number-of-dengue-and-dengue-haemorrhagic-fever-cases)
- outbreaksg (https://outbreak.sgcharts.com/data)

### Summary

We graduated from GA DSI program and managed to secure an interview with the NEA. We are given this assignment to present during the interview.

The assignment is about the dengue fever and how to prevent the spread of the breeding of the Aedes mosquitoes. Our tasks is to predict the locations and periods of when dengue cases could be high.


### Process

In the EDA, we identify the peak in dengue cases with is at the start of the year and mid year while temperature peaks in mid-year, rainfall peaks at end-year.

We formulate a linear combination of lagged temperature and lagged rainfall model.
We chose a single SMA of 15 period, at 𝛼 = 0.3 which we obtain the most optimal signal, to refine the signal we used a MAC signal as its easier to tell when the signal crosses above 0. It correlates well with when the peaks happen.

[![HYIJ70F.md.png](https://iili.io/HYIJ70F.md.png)](https://freeimage.host/i/HYIJ70F)

(lagged temperature and lagged rainfall model)

The cases were spread all over residential parts of singapore, we did k-means clustering to identify the different estates. From there we zoomed into the monthly dengue cases by the individual clusters.

[![HYIH0nS.md.png](https://iili.io/HYIH0nS.md.png)](https://freeimage.host/i/HYIH0nS) 

(Clusters in Singapore)

Start-of-year peak: North East cluster
Mid-year peak: North, North-East, East, North-South


### Recommendations

To counter the peaks we will need release the Wolabchia as we are expecting a peak to happen soon in January 2023 where the MAC signal will be a positive.

Locations to focus on will be in the North-East of Singapore, e.g. Sengkang West, Tampines, Siglap, Loyang, Serangoon Gardens, etc.


### Conclusion

As mentioned above, we have developed a model to predict the peak of dengue high-season.
We split the nation into several clusters using historical spatial trends. With this, the spatial clustering and temporal prediction works well together for the NEA officials to identify when and where to target the release of Wolbachia mosquitoes to combat the outbreak.

