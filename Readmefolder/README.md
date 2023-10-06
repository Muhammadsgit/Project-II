
-Problem Statement

You are tasked with creating a regression model based on the Ames Housing Dataset. This model will predict the price of a house at sale.


- Executive Summary

It is usually assumed that the economoy of a country is dependent on the ecomonic condition of its citizen. World Development Statistics from [Gapminder](https://www.gapminder.org/about/) dataset provides us an excellent source to prove or disprove this notion of correlation between these two attributes. I aim to find evidence of correlation between GNI and population growth through examining trends embedded within the dataset.


- File Directory/table of contents

├── data         
│   ├── gni_per_cap_atlas_method_con2021.csv          
│   ├── population.csv       
│   └── pop_gni_merged.csv 

├── Code folder 

│   ├──  code V8.ipynb          
│   └── correlation V8.ipynb 

├── Presentation folder  
│   ├── A look at GNI and Population.pdf  



- Data  and Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|**{year}_pop**|*integer*|pop_gni_merged|The population of a country for a given year where 1800 <= year <= 2051
|**{year}_gni**|*integer*|pop_gni_merged|The Gross National Income of a country for a given year where 1800 <= year <= 2051|
|**country**|*integer*|gni_per_cap_atlas_method_con2021|The names of all the countries.
|**{year}**|*integer*|gni_per_cap_atlas_method_con2021|The Gross National Income of a country for the given year, where 1800 <= year <= 2051|
|**country**|*integer*|population|The names of all the countries.
|**{year}**|*integer*|population|The population of a country for the given year, where 1800 <= year <= 2100|


- Conclusions and Recommendations

Generally, it is thought that a country's population growth has a positive correlation with the economic well-being of its citizens. Gross National Income (GNI) is considered a metric of a country's economic well-being. Our findings show there was a positive correlation between population growth and GNI growth only until the mid-1990s. After the 1960s, this positive correlation turned negative, leading us to conclude that ***A positive population growth does not solely depend on increase in country's Gross National Income or vice versa***. Factors other than GNI likely influence population growth as well.

![image](concluding_graph.png) 


- Areas for Further Research/Study

Analyze the correlation between GNI and population growth before and after major economic events (e.g. recessions, financial crises) to understand impacts.


- Sources

Practical Statistics for Data Scientists by Peter Bruce, Andrew Bruce and Peter Gedeck

## Authors
- [Muhammad Affan Hassan](hassan.affan@gmail.com)
