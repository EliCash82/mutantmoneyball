![](MUTANT-MONEYBALL-logo.png)

# Mutant Moneyball Data v 1.2

This data is related to the article entitled [*Mutant Moneyball*](https://rallyrd.com/mutant-moneyball-a-data-driven-ultimate-x-men/) on [Rally](https://www.rallyrd.com).

---

This GitHub repo holds the data used in Rally's [*Mutant Moneyball*](https://rallyrd.com/mutant-moneyball-a-data-driven-ultimate-x-men/) article which visualizes X-Men value data, era by era, from the X-Men's creation in 1963 up to 1993. The data collected has been made open access, and the following README.MD file attempts to suggest some ways in which this data can be used to create some R Language data visualizations. This README.md file also contextualizess all of the collected CSV data in an easy to understand table at the foot of the document.

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

---

**v. 1.2 UPDATE**: A CSV entitled `MutantMoneyballAppearanceData.csv` has been added to the collection. This shows exact issue numbers, year of release, and which X-Men team members appeared in each issue. This data was confirmed via a variety of sources, including but not limited to:
* [UncannyXMen.net](https://uncannyxmen.net/)
* [Marvel Fandom Database](https://marvel.fandom.com)