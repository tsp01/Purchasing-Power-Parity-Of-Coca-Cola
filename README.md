# Purchasing Power Parity Of Coca Cola
This Program takes information about the pricing of Coca Cola cans(0.33 liters) from several countries and produces tables, and graphs using that information, as displayed below.

## What is purchasing power parity?
Purchasing power parity is when you measure and compare the price of a certain good in different countries to determine the ability of different currencies to purchase said good.

## Coca Cola?
Otherwise known simply as Coke, this is a soft drink sold around the world and easily recognized by its distinctive red can with its unique font.

## Program Step by Step
following this will be a step by step explanation of the code going through each individual cell. The first cell will begin at the number "1" and all future cells will count up. Cells that are entirely commented out will be ignored.

## 1:
The first cell is here to import most of the needed packages for the rest of the program.

## 2:
This cell is here for the creation of the "scrape_table" function. This function will help with every table that is taken from the internet by turning said tables into formats readable by the rest of our code.

## 3:
This Cell scrapes a table of the price of a 0.33 litre coke in 104 countries. These prices are in Canadian Dollars.

## 4:
Cell 4 creates the "Convert" function which uses an api to convert a number in one currency to another currency. It should be noted that this particular API requires an API key which can become non functional. If you need to use this function and get a 403 error code you will need a new API key which can be gotten for free at currencyscroop.com.

## 5:
This cell scrapes a table containing country names and currency codes. We will use this to get the currency codes in our table of coke prices.

## 6:
This cell defines the "get_currency_code" and "clean_currency_code" and uses them to take the currency codes from the table scraped in the previous cell, and attach them to the table with coke prices. An astute observer might notice that we used the ".apply" function instead of ".join". This is becuase in the table with the currency codes all country names were in all capital letters and to use ".join" we would have had to use ".apply" regardeless to alter capitalization. 

## 7:
This relatively large cell is here to add tax rates to our price table. Specifically, we scraped a table of Value Added Tax(VAT) rates by country. These rates were in percentages and also placed into strings in the original table. Having to isolate the actual number from the string, remove any countries where we could not get an actual VAT rate, and converting the rates into floats is why this particular cell is longer then most others.

## 8:
Here we join the VAT rate table and out prices table so that our prices table has a VAT rate for each country. This significantly reduces the size of our table down to 60 on account of us not being able to get every countries VAT rate in a reasonable manner in the VAT rate table.

## 9:

