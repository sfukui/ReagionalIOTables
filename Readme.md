# Data used to estimate input coefficients of regional input-output tables in Japan

## About The Project

In this project, we provide the intermediate inputs and gross products of the input-output tables and macroeconomic data of the regions in Japan, which were used to construct the regional input coefficient estimation model in the following paper:

* Shogo Fukui(2024), "Estimating Input Coefficients for Regional Input–Output Tables Using Deep Learning with Mixup", _Computational Economics._ (https://doi.org/10.1007/s10614-024-10641-1)

## Getting Started

The CSV data files are stored in the `Data` folder. The contents of each file are as follows:

* **[IOTable.csv](Data/IOTable.csv):** Intermediate inputs and gross outputs (in units of 1 million Japanese yen) of the input-output tables for prefectures and cities in Japan that were the subject of the model learning
* **[ExplanatoryVairablesBase.csv](Data/ExplanatoryVariablesBase.csv):** Macroeconomic data that serve as the basis for the explanatory variables of our model
* **[AreaID.csv](Data/AreaID.csv):** Table of actual area names and the 'AreaID's

## Usage

The data files record regional data in each row, and the region is expressed by `AreaID`. Please check [AreaID.csv](Data/AreaID.csv) for the correspondence between the actual regional names and the `AreaID`s.

In the input-output table data ([IOTable.csv](Data/IOTable.csv)), the column `R[i]C[j]` records intermediate inputs from industry i to industry j, and the column `Y[i]` records gross products of industry i. The relationship between the actual industry and `i,j` is as follows.

| `i, j` | Industry |
| --- | --- |
| 1 | Agriculture (agriculture, forestry, and fisheries) |
| 2 | Mining |
| 3 | Manufacturing |
| 4 | Construction |
| 5 | Energy (electricity, gas, and water) |
| 6 | Trade |
| 7 | Finance (finance, insurance, and real estate) |
| 8 | Transportation (transportation and postal) |
| 9 | Communication (information and communication) |
| 10 | Public business |
| 11 | Services |
| 12 | Other industry |

The explanatory variables base data ([ExplanatoryVariablesBase.csv](Data/ExplanatoryVariablesBase.csv)) is explained in detail in [Explanation of Explanatory Variables Base Data](ExpDataExplanation.md).

## Contact
Shogo Fukui (sfukui07@gmail.com)

## Acknowledgement
Information about the sources of each data, as well as information about modifications and distribution is presented in [Notice.txt](./Notice.txt).
