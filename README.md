#
Mapping and Tracking Covid-19 
**Dan Ovadia and Brett Holleman**

## Problem Statement 
The Covid-19 pandemic needs no introduction. We were tasked with mapping Covid-19 hotspots. One problem facing citizens and policymakers alike is how to analyze the situation based on the data available. The available data are more or less restricted to deaths, cases, and tests, positive or negative. Case numbers are broadly irrelevant as they reflect more than anything the number of tests being administered. Raws deaths, while headline-making, are not terrible meaningful outside of a per capita basis. Per capita deaths, in turn, should be viewed in the context of population density, since places like California are very populous but not very dense. 

## Approach 
When the outbreak began, case numbers were closely followed. Then people realized they were proxies for tests. Looking at raw deaths counts can be equally misleading when assessing the severity of the situation: 1,000 deaths in Spain (pop. 47m) reflects a substantially worse outbreak than the same number of deaths in India (pop. 1.4bn). Looking at deaths by population density is more meaningful. One way to visualize clusters of contagion is to look at county rather than state data. We used the New York Times county-level data to map deaths. While certain states were generally at risk, it was in fact specific counties in the areas outlying major urban areas and centers of population density that were accounting for most of the deaths. (This is obviously true for the New York City region, but also in Louisiana and Michigan.) Areas around dense areas are at greater risk than isolated areas. 

Further to this point, raw population density figures can be misleading. Spain, for example, has more deaths than France despite having a lower population density (93 vs. 114), and a considerably smaller population (47m vs. 67m). Alasdair Rae, a professor in urban studies and planning at the University of Sheffield, proposes an alternative metric he calls the "lived" population.$^1$ This is calculated by partitioning a region into 1 square kilometer parcels, discarding the squares that are uninhabited, and recalculating the density. The method gives Spain a whopping 737 people per square populous kilometer and France a corresponding figure of 194. Fortunately for our project, another group calculated these data at the state level for the US, which we employ in our dashboard.$^2$ 

[Link to dashboard](https://covid-hotspots-ga-dsi-la-11.herokuapp.com/) <br>
[Link to dashboard backup](https://peaceful-reaches-40141.herokuapp.com/)

## Conclusion and Next Steps
We conclude that by discounting for "lived" population density and total population, we can derive figures that are comparable across regions. In future, we would like to extend this to the county level, both to assess the current situation but, more importantly, to provide policy makers with an *ex ante* approximation of the risks a particular region faces. We see more work to do in three main areas. First, demographics have proven extremely predictive since Covid-19 is overwhelmingly a disease of the elderly. Although data are sparse and generally considered unreliable, many countries with very young populations seem to be faring well. India and Africa, with populations of over a billion people each, do not appear to suffering like the ageing countries in Europe. Second, availability of data on certain racial groups more prone to risk factors like diabetes could help contain the spread by proactively intervening in those neighborhoods.  Third, it is worth looking at temperature. For example, Australia has had 97 deaths, California around 2800, and Canada around 4400. (All three have populations of about 40m.) It was summer in Australia when the outbreak started, winter in Canada, and characteristically mild across California. All three places implemented lockdowns of some or another sort about the same time. Last, and most important, we would like to extend the granularity of our data to include density at the county level. A concrete goal would be to calculate the "lived" density at the county level. This would be valuable to policymakers by showing them which regions surrounding an outbreak would be most vulnerable. 


**Sources and Footnotes**
1. A. Rae, "There's a better way to measure population density". Retrieved on 10 May 2020 at https://www.citylab.com/life/2018/02/theres-a-better-way-to-measure-population-density/552815/. 
2. Babbitt, D., P. Garland & O. Johnson, "Lived population density and the spread of COVID-19". Retrieved on 10 May 2020 at https://arxiv.org/pdf/2005.01167. 
 
**Data Sources**
1. COVID-19 Data Repository. Center for Systems Science and Engineering (CSSE) at Johns Hopkins University
2. The [Covid-19 Dashboards](https://covid19dashboards.com) and associated Github pages
3. Coronavirus (Covid-19) Data in the United States. *The New York Times*
