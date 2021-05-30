[
<img width="845" alt="Screen Shot 2021-05-18 at 9 50 41 AM" src="https://user-images.githubusercontent.com/80833988/118692111-96680200-b7be-11eb-8a31-a39556f521b6.png">
](url)

> "Diversification is a protection against ignorance. It can be achieved by combining assets that move in the opposite direction, which means those assets react to the same economic event differently.
"



# Diversified portfolio analyzer


:star: Cryptocurrencies and index funds.


In this Project, we assumed the role of a quantitative analyst for a FinTech investing platform. This platform aims to offer clients a one-stop online investment solution for their portfolio.

[
<img width="595" alt="Screen Shot 2021-05-18 at 10 22 37 AM" src="https://user-images.githubusercontent.com/80833988/118696288-ff517900-b7c2-11eb-944d-50b5ca93cc94.png">
](url)



## Table of content
- [An executive summary](https://github.com/nataliaburrey/project_1#an-executive-summary)
    - [Overview of the project and project goals](https://github.com/nataliaburrey/project_1#overview-of-the-project-and-project-goals)
    - [What is special about out project?](https://github.com/nataliaburrey/project_1#what-special-about-out-project)
- [Software version control](https://github.com/nataliaburrey/project_1#software-version-control)
    - [Libraries / interfaces](https://github.com/nataliaburrey/project_1#libraries--interfaces)
    - [Work with GitHub](https://github.com/nataliaburrey/project_1#work-with-github)
    - [How to install](https://github.com/nataliaburrey/project_1#how-to-install)
    - [How to use Voila](https://github.com/nataliaburrey/project_1#how-to-use-voila)
    - [Run Alpaca](https://github.com/nataliaburrey/project_1/blob/main/README.md#run-alpaca)
- [Work with data](https://github.com/nataliaburrey/project_1#work-with-data)
    - [Data Collection](https://github.com/nataliaburrey/project_1#data-collection)
    - [Cleanup & Analyse](https://github.com/nataliaburrey/project_1#cleanup--analyse)
    - [Data visualization](https://github.com/nataliaburrey/project_1#data-visualization)
- [Results and summary of the analysis](https://github.com/nataliaburrey/project_1/blob/main/README.md#results-and-summary-of-the-analysis)
- [License](https://github.com/nataliaburrey/project_1#license)
- [Team](https://github.com/nataliaburrey/project_1/blob/main/README.md#team)
- [Links](https://github.com/nataliaburrey/project_1#links)



## An executive summary

*  A portfolio analyzer: Create a framework can be used in the future to create a  Diversified Portfolio can be tune in for any goal and risk-tolerance
* Put into practice our new skills we learned: collect, clean and analyze complex financial data and how to use APIs to access a wide range of high-quality, up-to-date data in real time. 
* Using Python and Pandas libraries compares the performance of different assets. Include calculations, tables, financial models and interactive visualizations. Also include information about past  performance of the portfolios, as well as suggestions for portfolio composition to insure moderate risk/return profile.

[
<img width="601" alt="Screen Shot 2021-05-18 at 10 28 47 AM" src="https://user-images.githubusercontent.com/80833988/118697206-e72e2980-b7c3-11eb-86c7-bb9ba63a7125.png">
](url)



###  Overview of the project and project goals.

* We’re been tasked with evaluating various  investment options  for inclusion in the client portfolios. Need to determine the options with most investment potential based on key risk-management metrics: the daily returns, standard deviations, Sharpe ratios.
* To keep the costs low, the firm uses algorithms to build each client's portfolio. The algorithms choose from various investment styles and options.
* Our solution is for unexperienced investor-somebody with low risk tolerance, Interested in cryptocurrency but would like to chose the ones with higher returns to create a riskier part of portfolio with higher returns to take advantage of emerging market
* On one hand, our customer does not have a time to individually pick the stock-so we chose 3 most popular indexes, which will introduce diversify to a  customers portfolio in allow user to have moderate returns with lower risk as user plans for retirement 

[
<img width="446" alt="Screen Shot 2021-05-18 at 10 38 59 AM" src="https://user-images.githubusercontent.com/80833988/118698527-5f491f00-b7c5-11eb-8970-157d7b6fe5eb.png">
](url)

* On the other hand, following the hype of emerging crypto market, our investor would like to take  an advantage of fabulous returns. For this reason we decided to introduce moderate risk into the portfolio, by picking one of the most known and established cryptocurrencies on the market: Bitcoin (BTC), Ethereum (ETH), Litecoin (LTC) and Ripple (XRP) to balance out low-risk low-return index portion


### What is special about out project?

* Very well  commented code with deeply analyses and explained results for technical user lacking an understanding
* Reading financial data and making the connection between code results and meaning of it for the user unexperienced in financial tools and lanscrape

[
<img width="1193" alt="Screen Shot 2021-05-18 at 10 54 47 AM" src="https://user-images.githubusercontent.com/80833988/118700386-78eb6600-b7c7-11eb-88e1-62905fda34b6.png">
](url)



## Software version control

### Libraries / interfaces
*  Pandas - is a software library designed for data analytics that makes it easier to work with data from practically any type of file. Pandas supplies powerful tools for working with time data in particular, and time is a key aspect of financial analysis. Analysts typically compare and measure financial assets—from single stocks to large portfolios—across time.
* With the combination of Pandas and Jupyter Notebook, you can efficiently import, prepare, and analyze data of any type or quantity.
* Following libraries were used to analyze the data

```
# Import the required libraries and dependencies
import os
import requests
import json
import pandas as pd
from dotenv import load_dotenv
import alpaca_trade_api as tradeapi
from pathlib import Path
import numpy as np
import matplotlib.pyplot as plt
import hvplot.pandas
import seaborn as sns
%matplotlib inline

```

* New libriry we used helped us to clean the warnings in the code

[
<img width="1165" alt="Screen Shot 2021-05-20 at 8 57 23 PM" src="https://user-images.githubusercontent.com/80833988/119079932-012b6000-b9ae-11eb-8d96-1bbffc8b5c31.png">
](url)



 ## Run Alpaca

In order to succesfully run the file you have to generate your own Alpaca key and save it to .env file. Those files are hidden so Hold down the Command, Shift and Period keys (for Mac) to be sure you have it in the same folder as Jupyter Lab notebook

```
 cmd + shift + [.]
```
To generate Alpaca key you have to create your own account and request a new key. Save it in .env file, make sure to name the variables ALPACA_API_KEY and ALPACA_SECRET_KEY 
```

ALPACA_API_KEY = '<your key>'
ALPACA_SECRET_KEY = '<your key>'

```

Those steps are nessesary to maintain a security of private information. 

### Work with GitHub
* Repository created on GitHub
* Our group made sure that files  were frequently committed to repository
* Our repository is organized, and includes Resources folder with CSV  project files, 
* Jupyter Notebook with code well commented with concise, relevant notes.
* Detailed explanation of each step with explanation of financial data and conclusions of analyses (example)

### How to install

* Save remote repo from GitHub to your computer (Desktop): in Terninal type:

```
cd desktop

git clone https://github.com/nataliaburrey/SQL_Financial_Application.git
```

now you can find repo on your desktop


* Open a Jupyter Lab: In Terminal type command

```
jupyter lab
```

* In Jupyter Lab access saved repo folder 
* Choose [ project_1.ipynb ] file to see the analysis report.



## How to use Voila

Following screenshots and videos of the web application, created by deploying your Jupyter notebook via the Voilà library

To deploy Voilà library via terminal type in code:


```
conda activate <name-of-your-enviroment>
cd <relative-path-to-notebook>
voila <notebook_name>

```
The file will be opened into default WEB browser, like on the following video.



https://user-images.githubusercontent.com/80833988/118702763-34ad9500-b7ca-11eb-8465-a1caf78b2873.mov




User will be able to explore and interact with Analyses report.
Following video shows the interactive visualization withing the Jupyter Notebook in action




https://user-images.githubusercontent.com/80833988/118703354-db923100-b7ca-11eb-9a61-19ca800ff21a.mov



## Work with data

### Data Collection

* We used various skills learned in a bootcamp and various sources of date to collect information: data collected from CSV files, APIs, or databases by using Python or a Python library
* Source of data: Cryptocurrensies - [Coindesk](https://www.coindesk.com/), ETF index funds - [Fred](https://fred.stlouisfed.org/)
* Imported data from a CSV file into a Pandas DataFrame.
* API calls: Cryptocurrensies - JSON 

[
<img width="1198" alt="Screen Shot 2021-05-18 at 8 01 09 PM" src="https://user-images.githubusercontent.com/80833988/118750208-d7d6cc80-b813-11eb-832d-64a149eea0df.png">
](url)


* ETF index funds - [Alpaca](https://alpaca.markets/) - instructions on installation [Run Alpaca](https://github.com/nataliaburrey/project_1/blob/main/README.md#run-alpaca)


[
<img width="1178" alt="Screen Shot 2021-05-18 at 8 03 37 PM" src="https://user-images.githubusercontent.com/80833988/118750423-4156db00-b814-11eb-9a7e-6044ac0ba6ca.png">
](url)



### Cleanup & Analyse

* We identified and cleaned up missing, incomplete, erroneous, and duplicated text values in the dataset
* Generate summary statistics and visualizations to help you better understand the DataFrame
* Reorganized  subsets of information within the DataFrame to do a targeted analysis
* Write Python code to capture the price differences across the cryptocurrency market.


### Data visualization 
* The next step was to dive a bit more deeply into that data through visualizations.
* Some sets of data to analyses use a simple plot function, but for others included longer time period and overlaying data we included interactive visualizations to explore and uncover relationships and patterns in your data
* We will be able to present information to our client using [Voila](https://github.com/nataliaburrey/project_1/blob/main/README.md#how-to-use-voila)


### Results and summary of the analysis

Data cleanup resulting DataFrame

[
<img width="657" alt="Screen Shot 2021-05-19 at 10 11 51 PM" src="https://user-images.githubusercontent.com/80833988/119078600-5e71e200-b9ab-11eb-9e4a-24587362802d.png">
](url)


Financial analyses we used include following steps:

[
<img width="834" alt="Screen Shot 2021-05-20 at 8 34 40 PM" src="https://user-images.githubusercontent.com/80833988/119078491-28346280-b9ab-11eb-815f-598a9b919960.png">
](url)

We presented results into interactive hvplots like:
* LinePlot for Cumulative return



[
<img width="1143" alt="Screen Shot 2021-05-20 at 8 51 59 PM" src="https://user-images.githubusercontent.com/80833988/119079605-44390380-b9ad-11eb-9d25-bf9d3a27bac7.png">
](url)



* Box Plot for daily returnes

[
<img width="1110" alt="Screen Shot 2021-05-20 at 8 53 45 PM" src="https://user-images.githubusercontent.com/80833988/119079701-7a768300-b9ad-11eb-857f-924a15957290.png">
](url)

* Heatmap for correlation of the assets

[
<img width="1210" alt="Screen Shot 2021-05-20 at 8 46 43 PM" src="https://user-images.githubusercontent.com/80833988/119079210-84e44d00-b9ac-11eb-9f75-bd0a9f8a62ae.png">
](url)

* The resulting portfolio is presented in a pie chart to better understand procentage

[
<img width="1711" alt="Screen Shot 2021-05-20 at 8 33 54 PM" src="https://user-images.githubusercontent.com/80833988/119079072-3fc01b00-b9ac-11eb-87c7-2515a5d59609.png">
](url)

* Next steps for our project would be following


[
<img width="796" alt="Screen Shot 2021-05-20 at 8 54 55 PM" src="https://user-images.githubusercontent.com/80833988/119079768-a4c84080-b9ad-11eb-9a0c-e26617995274.png">
](url)


## Team
* [Natalia Burrey](https://github.com/nataliaburrey)
* [Van Maquilan](https://github.com/VanMSM)
* [Nestor Ramirez](https://github.com/nestor39)

## License

MIT

## Links

* [Resourses](https://github.com/nataliaburrey/project_1/tree/main/Resources)
* [Jupyter Lab](https://github.com/nataliaburrey/project_1/blob/main/project_1.ipynb)
* [Repository copy link](https://github.com/nataliaburrey/project_1.git)

