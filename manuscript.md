---
title: Predicting Compressive Strength of Concrete using Machine learning
lang: en-US
date-meta: '2022-10-30'
author-meta:
- Andrew Bushnell
- Kanchan Kulhalli
- Vikram Gadge
header-includes: |-
  <!--
  Manubot generated metadata rendered from header-includes-template.html.
  Suggest improvements at https://github.com/manubot/manubot/blob/main/manubot/process/header-includes-template.html
  -->
  <meta name="dc.format" content="text/html" />
  <meta name="dc.title" content="Predicting Compressive Strength of Concrete using Machine learning" />
  <meta name="citation_title" content="Predicting Compressive Strength of Concrete using Machine learning" />
  <meta property="og:title" content="Predicting Compressive Strength of Concrete using Machine learning" />
  <meta property="twitter:title" content="Predicting Compressive Strength of Concrete using Machine learning" />
  <meta name="dc.date" content="2022-10-30" />
  <meta name="citation_publication_date" content="2022-10-30" />
  <meta name="dc.language" content="en-US" />
  <meta name="citation_language" content="en-US" />
  <meta name="dc.relation.ispartof" content="Manubot" />
  <meta name="dc.publisher" content="Manubot" />
  <meta name="citation_journal_title" content="Manubot" />
  <meta name="citation_technical_report_institution" content="Manubot" />
  <meta name="citation_author" content="Andrew Bushnell" />
  <meta name="citation_author_institution" content="Department of CEE, University of Illinois" />
  <meta name="citation_author" content="Kanchan Kulhalli" />
  <meta name="citation_author_institution" content="Department of CEE, University of Illinois" />
  <meta name="citation_author" content="Vikram Gadge" />
  <meta name="citation_author_institution" content="Department of CEE, University of Illinois" />
  <link rel="canonical" href="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/" />
  <meta property="og:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/" />
  <meta property="twitter:url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/" />
  <meta name="citation_fulltext_html_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/" />
  <meta name="citation_pdf_url" content="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/manuscript.pdf" />
  <link rel="alternate" type="application/pdf" href="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/manuscript.pdf" />
  <link rel="alternate" type="text/html" href="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/v/ab9718f0561ada0bfe9b43ffaf4ec5137bc41c9f/" />
  <meta name="manubot_html_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/v/ab9718f0561ada0bfe9b43ffaf4ec5137bc41c9f/" />
  <meta name="manubot_pdf_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/v/ab9718f0561ada0bfe9b43ffaf4ec5137bc41c9f/manuscript.pdf" />
  <meta property="og:type" content="article" />
  <meta property="twitter:card" content="summary_large_image" />
  <link rel="icon" type="image/png" sizes="192x192" href="https://manubot.org/favicon-192x192.png" />
  <link rel="mask-icon" href="https://manubot.org/safari-pinned-tab.svg" color="#ad1457" />
  <meta name="theme-color" content="#ad1457" />
  <!-- end Manubot generated metadata -->
bibliography:
- content/manual-references.json
manubot-output-bibliography: output/references.json
manubot-output-citekeys: output/citations.tsv
manubot-requests-cache-path: ci/cache/requests-cache
manubot-clear-requests-cache: false
...





<!--

<small><em>
This manuscript
([permalink](https://uiceds.github.io/cee-492-term-project-fall-2022-avk/v/ab9718f0561ada0bfe9b43ffaf4ec5137bc41c9f/))
was automatically generated
from [uiceds/cee-492-term-project-fall-2022-avk@ab9718f](https://github.com/uiceds/cee-492-term-project-fall-2022-avk/tree/ab9718f0561ada0bfe9b43ffaf4ec5137bc41c9f)
on October 30, 2022.
</em></small>
-->

## Authors



+ **Andrew Bushnell**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [andrewb7777](https://github.com/andrewb7777)<br>
  <small>
     Department of CEE, University of Illinois
  </small>

+ **Kanchan Kulhalli**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [Kanchan-uiuc](https://github.com/Kanchan-uiuc)<br>
  <small>
     Department of CEE, University of Illinois
  </small>

+ **Vikram Gadge**<br>
    · ![GitHub icon](images/github.svg){.inline_icon}
    [vgadge2](https://github.com/vgadge2)<br>
  <small>
     Department of CEE, University of Illinois
  </small>



# Abstract

Using a data set covering the concrete compressive strength of a variety of different mixture components, we are going to create a machine learning program that will be able to predict when concrete failures will occur, which components and the combinations of these components will work best based on strength requirements of certain structures, and predict maximum allowable loads that can be achieved based on the mixtures.

Using these future trends, we will we be able to reach certain conclusions on the future improvements, designs, and materials that should be used in certain structures that we will be able to present to individuals in the fields that use these structures. They then can use these recommendations in their future projects. We will be using the data set of "Concrete Compressive Strength" which was obtained using Kaggle.com [@{https://www.kaggle.com/datasets/sinamhd9/concrete-comprehensive-strength}]. The data comes in the form of an excel file and We will compile all of the data into specific tables and use them to create the future trends we stated above.  

We will be creating new tables and figures that will be of comparisons of when the concrete fails vs the concrete material, strength of concrete vs water to cement ratio, concrete composition vs concrete strength, max allowable loads vs concrete material, max allowable loads vs concrete permutations. In future we will be adding cost of components as new dimension and check out what’s the best and minimal combination to make it cost effective and compare the cost and strength graph.
 
We intend to use Julia to compile these new tables using machine learning tools that can be used to predict permutations, concrete to water ratios etc, that are not specifically included within the data set so we can accurately predict these unknown values that can then be used to run theoretical tests in real life construction project scenarios.

# Exploratory Data Analysis

The data set is composed of nine columns of data that state the following information: Fly Ash component, Water component, Superplasticizer, Coarse Aggregate, Age, and Concrete Compressive Strength. These columns have the following units of measurements: the first 7 columns have the units kg in m^3 mixture, and 8th column in days, 9th column in MPa megapascals. The excel data set has a total of 1030 rows of this data. We found a few discrepancies in the data set and we decided to clean the data before doing any exploratory analysis. The below section describes it in detail.

## Data Cleaning
The Dataset that we selected comprised of rows that were repeating multiple times. We could only learn about this when we began with asking questions and trying to code them out. So we go back and clean the data set by using "Unique" fuction, after which the rows reduced from 1030 to 1005.

The second challenge we were faced with was that the values of ingredients in the concrete were same for multiple rows but only the Concrete compressive strengths were varying i.e the input columns with same values generated different output. So we took a mean of those values and combined them into a single row.


## Description of the Dataset

Before we set out to ask questions, we generated the below table to get a deeper understanding of the columns in our dataset.

|   |               variable              |  min  |   mean  |  median | max    |
|:-:|:-----------------------------------:|:-----:|:-------:|:-------:|--------|
|   |                Symbol               |  Real | Float64 | Float64 |  Real  |
| 1 | :cement(kg per m3)                  | 102.0 | 276.873 | 259.95  | 540.0  |
| 2 | :blast_furnace_slag(kg per m3)      | 1.0   | 73.0007 | 20.0    | 359.4  |
| 3 | :fly_ash(kg per m3)                 | 1.0   | 55.6028 | 1.0     | 200.1  |
| 4 | :water(kg per m3)                   | 121.8 | 182.368 | 185.7   | 247.0  |
| 5 | :superplasticizer(kg per m3)        | 1.0   | 6.34415 | 6.0     | 32.2   |
| 6 | :coarse_aggregate(kg per m3)        | 801.0 | 974.597 | 968.0   | 1145.0 |
| 7 | :fine_aggregate(kg per m3)          | 594.0 | 773.081 | 780.0   | 992.6  |
| 8 | :age(days)                          | 1     | 46.1663 | 28.0    | 365    |
| 9 | :concrete_compressive_strength(MPa) | 2.33  | 35.119  | 33.73   | 82.6   |


Several studies independly have shown that concrete stregth development is determined not only by the water cement ratio, but that it is also influenced by the content of other concrete ingredients as well. Hence we tried to look into effects of various other ingredients on the compressive strength of concrete.In the below sections, we describe our columns in details and ask pertinent questions on our dataset.

### Water and Cement
The Abrams’ water-to-cement ratio (w/c) pronouncement of 1918 has been described as the most useful and signiﬁcant advancement in the history of concrete technology. His most important formulation was the inverse proportionality between the w/c ratio and the strength of concrete. The generally accepted Abrams rule is a formulation of the observation that an increase in the w/c decreases 

To check whether the Abrams' law holds true or false.
We are comparing the w/c ratio with the compressive strength of the concrete.

![Water-Cement Ratio vs Compressive strength of Concrete](https://github.com/uiceds/cee-492-term-project-fall-2022-avk/blob/main/content/images/WC_Plot.png)


### Blast Furnace Slag

### Fly Ash
In recent years, fly ash has become an increasing common component used in concrete mixtures. Fly ash is used to increase the workability of plastic concretes along with increase the strength and durability of regular concretes (Ondova, 2012). Fly ash can also replace a portion of the amount of cement mixture needed which in return reduces the cost while not decreasing the strength. Using our data set
### Coarse Aggregate and Fine aggregate

### Superplasticizer

### Age
<<<<<<< HEAD
By creating a histogram plot of Concrete Compressive Strength vs Age where age is the number of days after the concrete has been placed, we see that as concrete age increases the compressive strength increases until it reaches a peak at 28 days and then gradually decreases in strength as age increases. Looking online we see that concrete requires a curing time where once the concrete is placed it needs time to cure which is where the water content in the concrete mixture evaporates, leading to the concrete to settle and harden (Kim 1998). This in return leads to the strength to increase. Based on this information and looking at the data set, to have the concrete mixture to result in the strongest compressive strength we want our age to be around the 28 day mark. 
![Getting Started](images/Concrete%20Compressive%20Strength%20Vs%20Age.jpg)
=======

>>>>>>> 524d1b46f34774d156b912bc3c1a0e2ad51a01a9
### Concrete Compressive Strength




# Predictive Modeling


Using our data we can use machine learning to create predictive modeling code for solving for which combinations of concrete mixtures would be ideal to meet a certain strength requirement, based on different construction projects, and the find the minimum optimal cost. To do this we intend to first use the data available in our dataset to find out the unit costs of each component in our concrete. We then will look up research papers over the different strength requirements set in place at the State and Federal level for different construction projects, such as bridges and highways. We then will design a machine learning program that will take our data available and create rough estimations of what how much of each concrete component would need to be used to create the optimal combination. This would result in the creation of a  model of ideal solutions to meet the lowest price and still meet the strength requirements for certain projects. This would be very useful in the cocnstruction industry which would be able to use our machine learning program to evaluate which combination of concrete would best work to meet the requirements of their project while also saving them the most capital. Based on what we have discussed with the TA, this is a feasible idea since our data could be used to create combinations that are not currently in our dataset by using what we learned in class to create rough estimates of new combinations based on the current data. We intend to do this by creating something similar to the solver function in excel where we will have an objective function, such as minimize price or maximize strength, and set up constraints, such as have strength be greater than or equal to 25 MPa or have at least 20% cement. This would give us our end result of a new matrix of the ideal values for the combinations in the concrete.

# References
1) https://www.kaggle.com/datasets/sinamhd9/concrete-comprehensive-strength

2) Mahan Mark (2014), Statistical Analysis of Concrete Compressive Strengths for California Highway Bridges, https://doi.org/10.1061/(ASCE)CF.1943-5509.0000404

3) J.-K Kim, Y.-H Moon, S.-H Eo (1998), Compressive strength development of concrete with different curing time and temperature,Cement and Concrete Research, https://doi.org/10.1016/S0008-8846(98)00164-1.

4) M. Ondova, N. Stevulova, A. Estokova (2012),The Study of the Properties of Fly Ash Based Concrete Composites with Various Chemical Admixtures, https://doi.org/10.1016/j.proeng.2012.07.582.





## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
