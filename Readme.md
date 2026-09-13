# Dataset for regional input-output tables estimation of Japan

## About this project

In this project, we provide the input-output tables and macroeconomic data of the select regions in Japan, which were used to construct the regional input-output table estimation model in the following papers:

* Shogo Fukui (2024), "Estimating Input Coefficients for Regional Input–Output Tables Using Deep Learning with Mixup", _Computational Economics._ (https://doi.org/10.1007/s10614-024-10641-1)
* Shogo Fukui (2026), "Enhancing the Accuracy of Regional Input-Output Table Estimation: A Deep Learning Approach", _arXiv_ (https://arxiv.org/abs/2603.13823)

## Getting started

CSV files are stored in the `Data` folder.
The contents of each file are as follows:

* **[2015Data_Japan.csv](Data/2015Data_Japan.csv):** Each item (in units of 1 million Japanese yen) of the input-output tables and Macroeconomic data for Japan as a whole, its prefectures, and its cities that were the subject of the above studies
* **[AreaID.csv](Data/AreaID.csv):** Correspondence table between region IDs (`AreaID`) and region names

## Usage

### ID of areas

The data file "[2015Data_Japan.csv](Data/2015Data_Japan.csv)"records regional data in each row, and the region is expressed by `AreaID`. Please check "[AreaID.csv](Data/AreaID.csv)" for the correspondence between the actual regional names and the `AreaID`s.

### Input-output tables

The file "[2015Data_Japan.csv](Data/2015Data_Japan.csv)" contains input-output tables for some regions of Japan.

The column `A_[i]_[j]` records intermediate inputs from industry `i` to industry `j`.
The column `D_[i]_[d]` represents sales from industry `i` to final demand sector `d`, and `M_[i]` represents imports and inflow in industry `i`.
The column `V_[i]_[g]` represents inputs from industry `i` to gross value added sector `g`.
Moreover, the column `Y_[i]` records gross products of industry `i`.

The tables below show the correspondence between `i`, `j`, `d`, and `g` and each industry and sector.

| `i, j` | Industry |
| --- | --- |
| 1 | Agriculture, forestry, and fisheries |
| 2 | Mining |
| 3 | Manufacturing |
| 4 | Construction |
| 5 | Electricity, gas, heat supply, water supply, and waste disposal business |
| 6 | Commerce |
| 7 | Finance, insurance, and real estate |
| 8 | Transport and postal services |
| 9 | Information and communication |
| 10 | Public administration |
| 11 | Service industries |
| 12 | Unclassified |

| `d` | Sector of final demand |
| --- | --- |
| 1 | Consumption expenditure outside households |
| 2 | Consumption expenditure (private) |
| 3 | Consumption expenditure of general government |
| 4 | Gross regional fixed capital formation |
| 5 | Increase in stocks |
| 6 | Exports (or total of exports and outflow) |

| `g` | Sector of gross value added |
| --- | --- |
| 1 | Consumption expenditure outside households |
| 2 | Compensation of employees |
| 3 | Operating surplus |
| 4 | Depreciation of fixed capital |
| 5 | Indirect taxes |
| 6 | (less) Current subsidies |

### Macroeconomic data

The regional macroeconomic data used as the basis for the explanatory variables in our research are also recorded in each column of the "[2015Data_Japan.csv](Data/2015Data_Japan.csv)" file. The details of each column are as follows:

| Column | Data | Source |
| --- | --- | --- |
|`Firm_[id_l]` | Number of establishments 2014 Economic Census (major classification) | 2014 Economic Census for Business Frame |
|`SFirm_[id_s]` | Number of establishments (minor classification) | Ibid. |
|`SEmp_[id_s]` | Number of employees (minor classification) | Ibid. |
|`MUnitAg` | Number of agriculture management entities | 2015 Census of Agriculture and Forestry |
|`MUnitFo` | Number of forestal management entities | Ibid. |
|`ProductsCr` | Production value (crop subtotal, 100 million yen) | 2015 Statistics of Agricultural Income Produced and 2015 Agricultural Output by Municipality (Estimates) |
|`ProductsAn` | Production value (livestock subtotal, 100 million yen) | Ibid. |
|`CFArea_[id_lb]` | Total floor area of buildings started (non-residential, major classification, m^2) | 2015 Building Starts |
|`VA_[id_l]` | Value added (major classification, million yen) | 2015 Statistical Observations of Prefectures and 2015 Statistical Observations of Municipalities |
|`Sales_[id_l]` | Sales (major classification, million yen) | Ibid. |
|`Income` | Taxable income (thousand yen) | Ibid. |
|`TP` | Number of taxpayer | Ibid. |
|`PopLF` | Population in labor force | Ibid. |
|`Unemp` | Number of unemployed | Ibid. |
|`Pop15` | Population aged 15 and over | Ibid. |


_Note:_
* The Ministry of Agriculture, Forestry and Fisheries has estimated `ProductsCr` and `ProductsAn` of each city.
* `Pop15` were calculated by the author based on the source data.
* As shown in the table above, the citations for the data, `VA_[id_l]`, `Sales_[id_l]`, and `Firm_[id_l]`, in Table 1 of [the original paper](https://link.springer.com/article/10.1007/s10614-024-10641-1) have been corrected. These corrections do not affect the original paper's analysis results.

### Large industry classification

The `id_l` contained in some column names indicates the industry of the large industry classification in the Economic Census of Japan. The correspondence between the numbers of `id_l` and the industries is as follows:

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

### Small industry classification

The `id_s` contained in some column names indicates the industry of the small industry classification in the Economic Census of Japan.

For information on the `id_s`, please refer to the Ministry of Internal Affairs and Communications website. (https://www.soumu.go.jp/english/dgpp_ss/seido/sangyo/index13.htm)

### Industry categorization of Building Starts

For `CFArea_[id_lb]`, `id_lb` means industry in the categorization of the Building Starts. In "[2015Data_Japan.csv](Data/2015Data_Japan.csv)", `id_lb` covers the categories from "d. Agricultural, forestry and fishery buildings" (`CFArea_D`) to "r. Buildings that can not be included in other categories" (`CFArea_R`).

For details, please refer to "3) Types of Dwellings and Industries," Section 3, Chapter 2 of the Ministry of Land, Infrastructure, Transport and Tourism's "[Construction Statistics Guidebook](https://www.mlit.go.jp/toukeijouhou/chojou/csg/csg_f.htm)."

## Contact
Shogo Fukui (sfukui07@gmail.com)

## Acknowledgement
Information about the sources of each data, as well as information about modifications and distribution is presented in [Notice.txt](./Notice.txt).
