![](MUTANT-MONEYBALL-logo.png)

# Mutant Moneyball Data v 1.1

This data is related to the article entitled MUTANT MONEYBALL on Rally Rd.

---

As we’ve moved and developed into a society that leans into the utility of information and data in so many modalities, more and more of us find that we need to understand data in new and deeper ways. Take this quote from The Forbes Magazine Technology Council: “When most people think about “currency,” they think of dollars or euros. Data is currency. It’s material, and both consumers and enterprises carry it.” The best way data can be analyzed is by making data more open and available, and this article hopes to do this in a fun engaging way.

Data analysis and visualization comes in many different forms and flavors. Some computer scientists prefer to use their object oriented programming skills and use Python Programming to produce visualizations and run data analysis. Others with an aversion to the complexities of programming lean heavily into spreadsheet software like Excel that can create more and more intricate data visualization deliverables all the time. For this article, the R Language was utilized.

The R Language, often referred to simply as R, is software, along with the R-centric IDE RStudio, was used to build initial data visualizations along with libraries like ggplot2 which uses Hadley Wickham’s “Grammar of Graphics” approaches to create charts and graphics. These were then moved into photoshop where they were used as base layers to create more attractive visualizations complete with relevant avatars connected to X-Men team members being analyzed.

Data visualization is certainly more accessible than it ever has been, but that certainly doesn’t mean it isn’t without difficulties. The point of this article is not to magically make all readers into data scientists, but here are a couple of well written tutorials for anyone that might be interested in using this data to work with R Language data viz. There are so many solid tutorials out there, why not stick with the Moneyball theme and check some of these approaches to analyzing Baseball:

A Short Introduction to Using R for Baseball Research - https://tht.fangraphs.com/a-short-ish-introduction-to-using-r-for-baseball-research/

A Gentle Introduction to GGPLOT2: https://bayesball.github.io/VB/gentle_introduction.html

Now that that’s out of the way, here are some formulas if you’d like to test your results against the ones we’ve provided with you here:

### Mutant Moneyball Cookbook:

**Recipe 1**: Import provided Mutant Moneyball Data into R/RStudio:

```
library(readr)
xteam1 <- read_csv("xteam1.csv")
head(xteam1)
```

**Recipe 2**: Plot X-Men team members on a graph in which the X axis represents the total number of 1980s issues each member appears in and the Y axis represents the total value of 1980s issues each member appears in. Do this with value data pulled from Heritage auctions.

```
> library(dplyr)
> library(tidyr)
> library(ggplot2)
> library(ggthemes)
> ggplot(xteam1, aes(TotalIssues80s, TotalValue80s_heritage))+ geom_point(aes(color=Member))

```

**Recipe 3**: Plot X-Men team members on a graph in which the X axis represents total number 1980s issues each member appears in and the Y axis represents total value of 1980s issues each member appears in. Do this with value data pulled from ebay.

```
> library(dplyr)
> library(tidyr)
> library(ggplot2)
> library(ggthemes)
> ggplot(xteam1, aes(TotalIssues80s, TotalValue80s_ebay))+ geom_point(aes(color=Member))
```

---

**MutantMoneyballOpenData.csv**: This file holds all the cleaned up data used in the Rally article Mutant Moneyball: The Search for the Most Valuable X-Men Team. The following items represent the headers in this csv file.
| COLUMN TITLE | SUMMARY |
| ------------ | ------- |
| **Member** | The name of the X-Men team member the data is connected to. In many cases these names are their civilian names and not their "Superhero" names (i.e. `warrenWorthington` is *Angel*, `hankMcCoy` is Beast, etc. |
| **TotalIssues** | This shows the total number of issues each X-Men member appeared in between 1963 and 1992. |
| **TotalIssues60s** | Total number of issues each X-Men member appeared between 1963 and 1969. |
| **TotalIssues70s** | Total number of issues each X-Men member appeared between 1970 and 1979. |
| **TotalIssues80s** | Total number of issues each X-Men member appeared between 1980 and 1989. |
| **TotalIssues90s** | Total number of issues each X-Men member appeared between 1990 and 1992. |
| **TotalValue_heritage** | Total value of each X-Men team member's total number of issues as reflected by Heritage highest sale. |
| **TotalValue60s_heritage** | Total value of each X-Men team member's total number of issues as reflected by Heritage highest sale of comics released between 1963 and 1969. |
| **TotalValue70s_heritage** | Total value of each X-Men team member's total number of issues as reflected by Heritage highest sale of comics released between 1970 and 1979. |
| **TotalValue80s_heritage** | Total value of each X-Men team member's total number of issues as reflected by Heritage highest sale of comics released between 1980 and 1989. |
| **TotalValue90s_heritage** | Total value of each X-Men team member's total number of issues as reflected by Heritage highest sale of comics released between 1990 and 1992. |
| **TotalValue_ebay** | Total value of each X-Men team member's total number of issues as reflected by ebay sales in 2022 in which sellers tagged the issue as VG (Very Good) Condition. |
| **TotalValue60s_ebay** | Total value of each X-Men team member's total number of issues released between 1963 and 1969 as reflected by ebay sales in 2022 in which sellers tagged the issue as VG (Very Good) Condition. |
| **TotalValue70s_ebay** | Total value of each X-Men team member's total number of issues released between 1970 and 1979 as reflected by ebay sales in 2022 in which sellers tagged the issue as VG (Very Good) Condition. |
| **TotalValue80s_ebay** | Total value of each X-Men team member's total number of issues released between 1980 and 1989 as reflected by ebay sales in 2022 in which sellers tagged the issue as VG (Very Good) Condition. |
| **TotalValue90s_ebay** | Total value of each X-Men team member's total number of issues released between 1990 and 1992 as reflected by ebay sales in 2022 in which sellers tagged the issue as VG (Very Good) Condition. |
| **60s_Appearance_Percent** | The percentage each X-Men member appeared in an issue published between 1963 and 1969 |
| **70s_Appearance_Percent** | The percentage each X-Men member appeared in an issue published between 1970 and 1979 |
| **80s_Appearance_Percent** | The percentage each X-Men member appeared in an issue published between 1980 and 1989 |
| **90s_Appearance_Percent** | The percentage each X-Men member appeared in an issue published between 1990 and 1992 |
| **PPI60s_heritage** | Average price per issue for each X-Men member based on highest sales on Heritage for issues published between 1963 and 1969. | 
| **PPI70s_heritage** | Average price per issue for each X-Men member based on highest sales on Heritage for issues published between 1970 and 1979. |
| **PPI80s_heritage** | Average price per issue for each X-Men member based on highest sales on Heritage for issues published between 1980 and 1989. |
| **PPI90s_heritage** | Average price per issue for each X-Men member based on highest sales on Heritage for issues published between 1990 and 1992. |
| **PPI60s_ebay** | Average price per issue for each X-Men member based on VG sales on eBay for issues published between 1963 and 1969. |
| **PPI70s_ebay** | Average price per issue for each X-Men member based on VG sales on eBay for issues published between 1970 and 1979. |
| **PPI80s_ebay** | Average price per issue for each X-Men member based on VG sales on eBay for issues published between 1980 and 1989. |
| **PPI90s_ebay** |  Average price per issue for each X-Men member based on VG sales on eBay for issues published between 1990 and 1992. |
| **TotalValue60s_wiz** | Total value of each X-Men team member's total number of issues released between 1963 and 1969 as they were valued in April 1993's Wizard Price Guide. |
| **TotalValue70s_wiz** | Total value of each X-Men team member's total number of issues released between 1970 and 1979 as they were valued in April 1993's Wizard Price Guide. |
| **TotalValue80s_wiz** | Total value of each X-Men team member's total number of issues released between 1980 and 1989 as they were valued in April 1993's Wizard Price Guide. |
| **TotalValue90s_wiz** | Total value of each X-Men team member's total number of issues released between 1990 and 1992 as they were valued in April 1993's Wizard Price Guide. |
| **TotalValue60s_oStreet** | Total value of each X-Men team member's total number of issues released between 1963 and 1969 as they were valued in 2015's Overstreet Price Guide. |
| **TotalValue70s_oStreet** | Total value of each X-Men team member's total number of issues released between 1970 and 1979 as they were valued in 2015's Overstreet Price Guide. |
| **TotalValue80s_oStreet** | Total value of each X-Men team member's total number of issues released between 1980 and 1989 as they were valued in 2015's Overstreet Price Guide. |
| **TotalValue90s_oStreet** |  Total value of each X-Men team member's total number of issues released between 1990 and 1992 as they were valued in 2015's Overstreet Price Guide. |
| **PPI60s_wiz** | Average price per issue for each X-Men member based on April 1993 Wizard Price Guide for issues published between 1963 and 1969. |
| **PPI70s_wiz** | Average price per issue for each X-Men member based on April 1993 Wizard Price Guide for issues published between 1970 and 1979. |
| **PPI80s_wiz** | Average price per issue for each X-Men member based on April 1993 Wizard Price Guide for issues published between 1980 and 1989. |
| **PPI90s_wiz** | Average price per issue for each X-Men member based on April 1993 Wizard Price Guide for issues published between 1990 and 1992. |
| **PPI60s_oStreet** | Average price per issue for each X-Men member based on 2015 Overstreet Price Guide for issues published between 1963 and 1969. |
| **PPI70s_oStreet** | Average price per issue for each X-Men member based on 2015 Overstreet Price Guide for issues published between 1970 and 1979. |
| **PPI80s_oStreet** | Average price per issue for each X-Men member based on 2015 Overstreet Price Guide for issues published between 1980 and 1989. |
| **PPI90s_oStreet** | Average price per issue for each X-Men member based on 2015 Overstreet Price Guide for issues published between 1990 and 1992. |

* **MostImproved_60s(DELETE?)**:
* **MostImproved_70s(DELETE?)**:
* **MostImproved_80s(DELETE?)**:
* **MostImproved_90s(DELETE?)**: