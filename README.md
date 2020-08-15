The Global Dashboard
===

## Overview

The Global Dashboard is an application intended to show, within specific stated constraints, 
the state of the world at a glance.  

It does so by collecting political, economic, trade, and other types of data, so that they can be 
compared across time (year-on-year) and space (country-to-country) in one place. 

## Data
The goal would be to have access to as many public domain data sources as possible, in order 
to create a single integrated dashboard. The data would fall along the following types.

### 1. Geography
Data relating to country and regional geography. Not actionable, but useful for geospatial 
analysis and event mapping. 

### 2. People, Government, and Society
Data relating to population and population trends, government type and stability, and other 
societal trendlines. 

### 3. Economy
Basic national economic and financial data.

#### 3.1 Trade Flows

#### 3.2 Reserves
##### 3.2.1 Food Reserves
Data on available reserves is taken from commodities which are actively traded on global markets, and 
for which data is available on brokerage platforms such as TradingView or Interactive Brokers.

Examples from TradingView include:

market name | ticker
--- | ---
COCOA FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|CC1!
MILK, CLASS III FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|DC1!
Feeder Cattle Futures	|GF1!
Lean Hogs Futures	|HE1!
COFFEE C FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|KC1!
KC HRW WHEAT FUTURES - ELECTRONIC (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|KE1!
LUMBER FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|LBS1!
Live Cattle Futures	|LE1!
SUGAR NO. 11 FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|SB1!
CORN MINI FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|XC1!
Wheat Mini Futures	|XW1!
Corn Futures	|ZC1!
SOYBEAN OIL FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|ZL1!
Soybean Meal Futures	|ZM1!
Oat Futures	|ZO1!
Rice Futures	|ZR1!
Soybean Futures	|ZS1!
Wheat Futures	|ZW1!

###### Maps
* Crop and ranch land
* Arable land
##### 3.2.2 Water Reserves
###### Maps
* Water Sources (including capacity/fill levels)
    * Surface water
        * Streams
        * Lakes
        * Rivers 
        * Wetlands
    * Glaciers
    * Aquifers
* Rainfall patterns
##### 3.2.3 Energy Reserves
Data on available reserves is taken from commodities which are actively traded on global markets, and 
for which data is available on brokerage platforms such as TradingView or Interactive Brokers.

Examples from TradingView include:

market name | ticker
--- | ---
Light Crude Oil Futures	|CL1!
DENATURED FUEL ETHANOL FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|EH1!
NY Harbor ULSD Futures	|HO1!
MINI BRENT FINANCIAL FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|MBC1!
Natural Gas Futures	|NG1!
E-mini Natural Gas Futures	|QG1!
E-mini Light Crude Oil Futures	|QM1!
RBOB Gasoline Futures	|RB1!

###### Maps
* Mining locations 
* Geologic formations

##### 3.2.4 Commodity Reserves
Data on available reserves is taken from commodities which are actively traded on global markets, and 
for which data is available on brokerage platforms such as TradingView or Interactive Brokers.

Examples from TradingView include:

market name | ticker
--- | ---
gold futures|GC1!|
Copper Futures	|HG1!
GOLD (E-MICRO) FUTURES (CONTINUOUS: CURRENT CONTRACT IN FRONT)	|MGC1!
Palladium Futures	|PA1!
Platinum Futures	|PL1!
E-mini Copper Futures	|QC1!
Silver (Mini) Futures	|QI1!
Gold (Mini) Futures	|QO1!
Silver Futures	|SI1!

###### Maps
* Mining locations 
* Geologic formations
##### 3.2.5 Miscellaneous Reserves

#### 3.3 Consumer Prices
##### 3.3.1 Food Prices
##### 3.3.2 Water Prices
##### 3.3.3 Energy Prices
##### 3.3.4 Miscellaneous Subsistence Consumer Prices

#### 3.4 Consumption
##### 3.4.1 Domestic Agricultural Consumption
##### 3.4.2 Water Intensity Rate
##### 3.4.3 Energy Usage

## The Model
Once data is collected, the dashboard can take selected data and synthesize it in order to 
create risk scores, which can be updated using either new dashboard data or from other 
real-time sources (such as an Event Detector).

## How It Works
The Global Dashboard contains the following jobs, each correlating with a specific 
part of dashboard creation process.


### 1. The Data Collector
This job connects to a data source for each type of data required by the dashboard, downloads it, parses it, 
then saves it to persistent storage for analysis and visualization.
### 2. The Dashboard UI
Shows detected data in a UI that allows the user to select, filter, and parse data by time and/or space.