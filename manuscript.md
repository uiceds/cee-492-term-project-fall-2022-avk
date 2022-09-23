---
title: Predicting Compressive strength of Concrete using Machine learning
lang: en-US
date-meta: '2022-09-23'
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
  <meta name="dc.title" content="Predicting Compressive strength of Concrete using Machine learning" />
  <meta name="citation_title" content="Predicting Compressive strength of Concrete using Machine learning" />
  <meta property="og:title" content="Predicting Compressive strength of Concrete using Machine learning" />
  <meta property="twitter:title" content="Predicting Compressive strength of Concrete using Machine learning" />
  <meta name="dc.date" content="2022-09-23" />
  <meta name="citation_publication_date" content="2022-09-23" />
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
  <link rel="alternate" type="text/html" href="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/v/fa7fcd996c4052d7e5233033d5bdcee85eb932cd/" />
  <meta name="manubot_html_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/v/fa7fcd996c4052d7e5233033d5bdcee85eb932cd/" />
  <meta name="manubot_pdf_url_versioned" content="https://uiceds.github.io/cee-492-term-project-fall-2022-avk/v/fa7fcd996c4052d7e5233033d5bdcee85eb932cd/manuscript.pdf" />
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






<small><em>
This manuscript
([permalink](https://uiceds.github.io/cee-492-term-project-fall-2022-avk/v/fa7fcd996c4052d7e5233033d5bdcee85eb932cd/))
was automatically generated
from [uiceds/cee-492-term-project-fall-2022-avk@fa7fcd9](https://github.com/uiceds/cee-492-term-project-fall-2022-avk/tree/fa7fcd996c4052d7e5233033d5bdcee85eb932cd)
on September 23, 2022.
</em></small>

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



Using a data set covering the concrete compressive strength of a variety of different mixture components, we are going to create a machine learning program that will be able to predict when concrete failures will occur, which components and the combinations of these components will work best based on strength requirements of certain structures, and predict maximum allowable loads that can be achieved based on the mixtures.

Using these future trends we will we be able to reach certain conclusions on the future improvements, designs, and materials that should be used in certain structures that we will be able to present to individuals in the fields that use these structures. They then can use these recommendations in their future projects. We will be using the data set of "Concrete Compressive Strength" which was obtained using Kaggle.com [1]. We will compile all of the data into specific tables and use them to create the future trends we stated above. The Data set consists of 8 quantitative inputs and 1 quantitative output as columns and total 1030 instances that are presented as rows.    

We will be creating new tables and figures that will be of comparisons of when the concrete fails vs the concrete material, strength of concrete vs water to cement ratio, concrete composition vs concrete strength, max allowable loads vs concrete material, max allowable loads vs concrete permutations.  

We intend to use Julia to compile these new tables using machine learning tools that can be used to predict permutations and combinations, concrete to water ratios, etc that are not specifically included within the data set so we can accurately predict these unknown values that can then be used to run theoretical tests in real life construction project scenarios.

## Citations

Citation by URL [@{https://www.kaggle.com/datasets/sinamhd9/concrete-comprehensive-strength}]

## References {.page_break_before}

<!-- Explicitly insert bibliography here -->
<div id="refs"></div>
