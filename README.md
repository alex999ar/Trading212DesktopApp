# Trading212DesktopApp
### Description
The goal of this project is to get your Trading212 portfolio, calculate your returns and show everything clearly without having to log in to the Trading 212 website. 
This is achieved by getting the order information from a provided csv and searching in yahoo finance for the current prices of the stocks. This is a more interactive version
of my [Trading212Portfolio](https://github.com/alex999ar/Trading212Portfolio).

### Image example of program output
![](/example_output.png)
When you hover over a slice of the donut chart it shows you the stock ticker, the current value of this investment and the percentage of your portfolio it occupies.
Click on any any ticker in the legend under the chart to remove it or add it back in the chart.

### Information
**This project is designed for accounts with EURO currency**. It converts everything to Euro. If you want to change it to your currency follow the 
[instructions here](https://github.com/alex999ar/Trading212DesktopApp#change-currency)

### Installation
* Run the command `npx create-electron-app trading212_desktop_app` to create the skeleton of an electon app using electron forge.
* Delete the package.json file and src folder in your install location and replace them with my own files.
(Alternatively you can keep your package.json if you change `"main": "src/index.js"` to `"main": "src/main.js"`)
* Go to src\python (inside your install location) and replace my orders.csv with your own. (Don't forget to name it the same).

[Instructions on how to download your order data from Trading 212 here.](https://community.trading212.com/t/new-feature-export-your-investing-history/35612) 
**Select ONLY the orders as included data**.

### How to use
* Open `src\python\myPortfolio.py` and run it in order to make a local server
* Open a terminal and cd to your install location. Run the command `npm start`

### How to create a proper executable
* Open a terminal and cd to your install location. Run the command `npm run make`

### Change currency
Go to `src\python\myPortfolio.py` and change the variables USER_CURRENCY and USER_SYMBOL accordingly

For example for GBP you need to have `USER_CURRENCY = "GBP"` and `USER_SYMBOL = "£"`

### Dependencies
#### For Electron
- [Npm and Node.js](https://www.npmjs.com/get-npm)

#### For Python
- [Flask](https://flask.palletsprojects.com)
- [Pandas](https://pandas.pydata.org/pandas-docs/stable/getting_started/install.html)
- [BeautifulSoup 4](https://pypi.org/project/beautifulsoup4/)
- [Requests](https://pypi.org/project/requests/)
- [Yahoo finance](https://pypi.org/project/yahoo-fin/)
- [Forex python](https://pypi.org/project/forex-python/)
- [Numpy](https://numpy.org/install/)
