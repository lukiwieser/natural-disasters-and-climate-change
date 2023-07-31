# Deaths by Natural Disasters and Climate Change

Exploring the deaths by natural disasters since 1900, and possible relations to climate change.

Our whole process is documented in the jupyter notebook [main.ipynb](main.ipynb).

## Main Findings

### Natural disasters over time

![disasters-over-time](/docs/disasters-over-time.png)

Here we can see the occurrences and deaths of disasters over time for each decade.

The number of disasters is rising. However, this is likely subject to a reporting bias, since likey just more disasters are reported. The deaths by disasters are sinking, we see that fewer apocalyptic disasters where millions of people die occur. However this could also be likely due to humans being better prepared for natural disasters, and not diasters being less severe.

### Type of disaster

![disasters-by-type](/docs/deaths-by-type.png)

Different types of disasters kill different amounts of people. Droughts and floods are by far the deadliest. A possible bias here could be that deaths by droughts and floods can be strongly dependent on political decisions, so floods & droughts are not inherently more severe on their own.

### Disasters by region

![deaths-by-region](/docs/deaths-by-region.png)

Asia has by far the most deaths by disasters, total deaths as well as deaths by population.

We refer to the deaths per population as relative deaths.

### Disasters by country

![deaths-and-type-by-country](/docs/deaths-and-type-by-country.png)

Here we look at a small selection of countries that are different to each other e.g. in their region or how developed they are.

Usually, droughts are the deadliest disasters. However, France has nearly no deaths by droughts, but here heatwaves are the most deadly.

### Temperature over time

![temperature-by-region](/docs/temperature-by-region.png)

The temperature rises in all regions, with Europe being the most extreme.

We use temperature anomalies as a measurement for temperature since they are supposedly more representative. Temperature anomalies are simply the temperature, but corrected by a baseline, in our case by the Jan 1951 - Dec 1980 average temperature. 
Additionally, we smoothed the temperature with lowess.

### Correlation of natural disasters and temperature

![temperature-by-region](/docs/correlation-temperature-and-disaster-deaths.png)

Here we can see the correlation of _deaths by natural disasters_ with the _temperature_, foreach type of natural disaster.
For earthquakes the correlation is very small at `0.028`, for extreme temperature events it is relatively high at `0.8`.

However, when looking closer at specific disaster types in specific countries, e.g. heatwaves deaths in France, the correlation drops to `0.18`, and in Spain even to `-0.49`.
This kinda contradicts scientific evidence which suggests that heatwaves increase in severity. 
There is also the effect that when looking at the country level and disaster subtypes just very few recorded instances remain, and outlines are quite influential (thus the negative correlation in Spain).

So here more research is necessary to reach substantial conclusions.

### Summary

Since 1900 the number of recorded disasters rises, and the number of deaths by disaster is sinking.

When looking at the deaths from natural disasters there is a strong difference between different disaster types, and between different regions and countries.

There seems to be a correlation between some natural disaster types and rising temperatures, but further research is necessary for this area.

Overall everything should be taken with a grain of salt. Because there are quite some biases, like better reporting of natural disasters, better preparation for natural disasters, and too few instances to derive meaningful results. 

More details are available in our jupyter notebook [main.ipynb](main.ipynb). 

## Reproduce

One dataset that we use for our analysis, the *Emdat dataset*, is not allowed to be shared publicly. Thus for reproducing, it has to be manually downloaded.

First, create an account and download the dataset from the [Emdat website](https://public.emdat.be/).
Then put the dataset to the following location, with the exact filename:
`data/raw/disaster/emdat_public_2022_12_22_full.xlsx`

Finally, you can run the jupyter notebook [main.ipynb](main.ipynb) to reproduce our results. Don't forget to check if you have the correct python version as specific in the notebook.

## Credits

This project was created by students as part of a lecture at the [Technical University of Vienna](https://www.tuwien.at/).

Sebastian Fürndraht, Hannes Rokitte, Paul Schmitt, Lukas Wieser · 24.01.2023
