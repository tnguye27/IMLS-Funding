# IMLS Funding

<img src="https://github.com/tnguye27/IMLS-Funding/blob/main/imlslogo.png?raw=True" alt="IMLS Logo">

## Introduction

The Institute of Museum and Library Services (IMLS) is a federal agency dedicated to funding library, archive, and museum services. According to the [IMLS website](https://www.imls.gov/about/learn-about-imls/our-mission-vision), the agency's mission is to provide access for individuals and communities to museums and libraries to champion lifelong learning, strengthen community engagement, and advance the agency's mission to empower America's museums, libraries, and related organizations. 

According to the[ American Library Association (ALA)](https://www.ala.org/faq-executive-order-targeting-imls), The White House annouced orders that seven agencies, including the IMLS, "be eliminated to the maximum extent of the law". Noted, the order does not directly eliminate the agency entirely since it would exceed executive authority. 

Although, library funding only draws less than 0.003% of the annual federal budget, yet it has huge impact to the millions of Americans who rely on library and museum services in their every day life. 

For this project, I will analyze funding for these IMLS programs in all 50 states from the time period of 1997-2022, in addition to party government breakdown (Congress and Presidency) from the same time period. I will attempt to answer the question: "Are there relationships between IMLS funding and party government?"

Note: I did not analyze the 118th Congressional term (2023-2025) since funding might not be in effect yet for year 2024 or January 2025. The 117th (2021-2023) Congressional term ended in January 2023 but I did not include year 2023 for simplicity sake. In addition, since Congressional terms end on January of odd-numbered years, I did not analyze those ending month and treated those ending months as the new term for simplicity sake. Also, I did not analyze the effect of inflation on funding.   

## Sources
- IMLS funding data is from [IMLS website](https://www.imls.gov/grants/awarded-grants). Also in repository titled: "awarded-grants-2025-04-11 (1).csv".
- [Party government](https://history.house.gov/Institution/Presidents-Coinciding/Party-Government/) data is scraped via BeautifulSoup. Code is below:
```
# scrape data
# get request
url = "https://history.house.gov/Institution/Presidents-Coinciding/Party-Government/"
webpage = get(url)

# check status code
webpage.status_code

# use BeatifulSoup to parse webpage
content = BeautifulSoup(webpage.content, "html.parser")
```

## Setup

You will need the folllowing libraries downloaded: 

```
pip install requests
pip install numpy
pip install pandas
pip install matplotlib
pip install beautifulsoup4
pip install re
pip install seaborn
pip install plotly
``` 

## Launch
Here's a snippet of the code output. 

<img src="https://github.com/tnguye27/IMLS-Funding/blob/main/imlsscrsht.png?raw=True" alt="Here's a snippet of the code output.">
