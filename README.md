# Decentralized Inflation Dashboard

The goal of this project is to build a censorship resistant inflation dashboard. Detailed information about the inspiration behind this project can be found [!here](https://1729.com/inflation). 

## What Do We Need to Build an Inflation Dashboard?

Building the inflation dashboard has so many mooving parts, but here are the things we need to do to build the dashboard. 

1. **Identify a large basket of goods**: A basket of goods refers to a fixed set of consumer products and services whose price is evaluated on a regular basis, often monthly or annually. This basket is used to track inflation in a specific market or country, so that if the price of the basket of goods increases by 2% in a year, inflation can thus be said to be 2%.

For this project, we'll be considering 10 of the products listed [!here](https://data.bls.gov/cgi-bin/surveymost?ap) by the US Bureau of Statistics. 

2. **Obtain price data**: We will obtain real-time price data of the basket of goods identified in `1.` from [!Instacart](https://www.instacart.com/). To achieve this, we'll train an ML model that can automatically identify products and their associated prices on a website.

3. **Put price data on-chain**: Once, we have our data, we'll publish it on-chain. The refined data could be on-chain, the raw price data could be on IPFS or equivalent, and any original URLs with prices of goods could potentially also be redundantly backed up using services like archive.is or web.archive.org.

4. **A smart contract to calculate inflation**

5. **Frontend**: We'll also create a simple frontend application where people can go to view inflation dashboard.

## Step 1: Training Our ML Model

To train our ML model, we need to collect some data. We'll take some screenshots on instacart and label them using labelimg. The labels that will be considered are the Product, Name, and Price. Here is a sample screenshot.

[!image](labelimg.png)

The screenshots from Instacart should be saved in the data/images folder and the annotations should be saved in data/annotations folder.