# Assignment_1_CS_290
In this assignment, you'll write a simple web application that will introduce you to HTML and JavaScript.

# Instructions
Write a web application using Node.js that serves the 3 pages listed below.

1. Home Page.
2. Stock Listing Page.
3. Stock Search Page.
The data for this application is provided in the file stocks.js and we have also provided a package.json file for you. Do not change anything in the files stocks.js and package.json. You can use the server.js file provided to you to start your coding. Do not change the value of the variable PORT in server.js. You can also use any code presented in the course modules.

__Update July 2, 2021: You are allowed to make changes to package.json__

You can choose the names of the static HTML pages and the URLs for the routes however you want with one exception - the static HTML file for the Home Page must be named index.html.
# 1. Home Page
* A GET request for the root URL should return a static HTML page named index.html.
* This page must include links to the following 2 pages:
  * Stock Listing Page
  * Stock Search Page
* In addition to the links, you can optionally add welcome text on this page describing the web application.
# 2. Stock Listing Page
For this page, create a static HTML file that the displays the following information
An HTML table with the data provided in the file stocks.js, and
A form to order stocks
HTML Table:
Each row in the HTML table must have the following 3 columns
Company name
Stock symbol
Current price
The table must have a header row.
Form to order stocks:
Underneath the HTML table, you must provide inputs for the user to submit a stock order. The following inputs must be provided:
A input element to specify the symbol of the stock to order.
You can choose to use a text element or radio-buttons or a drop-down list for this.
A number element to enter the quantity to buy.
A button to submit the form.
You are free to choose the URL for the action.
You can choose either GET or POST as the method for the form.
After the form is submitted, the Stock Order Response must be displayed.
Stock Order Response
This response must be dynamically generated by the server.
The response must be in HTML and should include a message with the following information:
You placed an order to buy N stocks of CompanyName. The price of one stock is $Y and the total price for this order is $Z.
For example:
You placed an order to buy 10 stocks of Splunk. The price of one stock is $137.55 and the total price for this order is $1375.5.
Note: If a string value is passed to res.send() as an argument, then by default the response body contains it as HTML, which is what is required for Stock Order response.
# 3. Stock Search Page
This must be a static page with a form that provides two criteria to the user for searching the stock information:
Highest price
Lowest price
The user should be able to choose one of these choices and submit the form.
You are free to choose the URL for the action.
You can choose either GET or POST as the method for the form.
After the form is submitted, the Stock Details Response must be displayed.
Stock Search Response
This response must be a JSON object with all the information corresponding to that stock from the variable stocks.
Note: If a JSON object is passed to res.send() as an argument, then by default the response body contains it as JSON, which is what is required for the Stock Details Response.
When processing the request, your JavaScript code must call a function findStockByPrice(...) which should find the stock with the highest or lowest price (as needed) from among the stocks in the variable stocks.
This function must find the relevant stock "on the fly," i.e., you must not hard-code or permanently store the information about which stock has the highest price and which stock has the lowest price.
