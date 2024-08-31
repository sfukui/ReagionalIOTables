# Explanation of Explanatory Variables Base Data

## Explanation of Data
The base data for the explanatory variables ([ExplanatoryVariablesBase.csv](Data/ExplanatoryVariablesBase.csv)) records regional data for each row, and the region names are represented by `AreaID`.

For the correspondence between the actual regional names and the `AreaID`s, see [AreaID.csv](Data/AreaID.csv).

### Data Names
The data of the economic variables used as the basis for the explanatory variables are recorded in each column of the [ExplanatoryVariablesBase.csv](Data/ExplanatoryVariablesBase.csv) file. The details of each column are as follows:

| Name | Data | Unit | Source |
| --- | --- | --- | --- |
| `SFirm_[id_s]` | Number of establishments (minor classification) |  | 2014 Economic Census for Business Frame |
| `SEmp_[id_s]` | Number of employees (minor classification) |  | 2014 Economic Census for Business Frame |
| `VA_[id_l]` | Added value (large classification) |  | 2012 Economic Census for Business Activity |
| `Sales_[id_l]` | Sales (large classification) |  | 2012 Economic Census for Business Activity |
| `Firm_[id_l]` | Number of establishments (large classification) |  | 2012 Economic Census for Business Activity |
| `Income` | Taxable income |  | Statistical Observations of Prefectures 2015 and Statistical Observations of Municipalities 2015 |
| `TP` | Taxpayer |  | Statistical Observations of Prefectures 2015 and Statistical Observations of Municipalities 2015 |
| `PopLF` | Population in labor force |  | Statistical Observations of Prefectures 2015 and Statistical Observations of Municipalities 2015 |
| `Unemp` | Number of unemployed persons |  | Statistical Observations of Prefectures 2015 and Statistical Observations of Municipalities 2015 |
| `Pop15` | Total population (15 and over) |  | Calculated by the author from Statistical Observations of Prefectures 2015 and Statistical Observations of Municipalities 2015 |

### Large Industry Classification

The `id_l` contained in some column names indicates the industry of the large industry classification in the Japanese Economic Census. The correspondence between the numbers of `id_l` and the industries is as follows:

| `id_l` | industry |
| --- | --- |
| 1 | “AGRICULTURE AND FORESTRY” and “FISHERIES” |
| 2 | “MINING AND QUARRYING OF STONE AND GRAVEL” |
| 3 | “CONSTRUCTION” |
| 4 | “MANUFACTURING” |
| 5 | “ELECTRICITY, GAS, HEAT SUPPLY AND WATER”
| 6 | “INFORMATION AND COMMUNICATIONS” |
| 7 | “TRANSPORT AND POSTAL SERVICES” |
| 8 | “WHOLESALE AND RETAIL TRADE” |
| 9 | “FINANCE AND INSURANCE” |
| 10 | “REAL ESTATE AND GOODS RENTAL AND LEASING” |
| 11 | “SCIENTIFIC RESEARCH, PROFESSIONAL AND TECHNICAL SERVICES” |
| 12 | “ACCOMMODATIONS, EATING AND DRINKING SERVICES” |
| 13 | “LIVING-RELATED AND PERSONAL SERVICES AND AMUSEMENT SERVICES” |
| 14 | “EDUCATION, LEARNING SUPPORT” |
| 15 | “MEDICAL, HEALTH CARE AND WELFARE” |
| 16 | “COMPOUND SERVICES” |
| 17 | “SERVICES, N.E.C.” |

### Small Industry Classification

The `id_s` contained in some column names indicates the industry of the small industry classification in the Japanese Economic Census.
For information on the `id_s`, please refer to the Ministry of Internal Affairs and Communications website. (https://www.soumu.go.jp/english/dgpp_ss/seido/sangyo/index13.htm)
