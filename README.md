# Top-15-NSE-Stocks-by-Market-Capitalization-in-2023
Tableau Public Link: https://public.tableau.com/app/profile/rohini.tembhurnikar/viz/Top15NSEStocksbyMarketCapitalization/NSEStocks

## Business Objective
The goal of this project is to analyze and visually present the performance of the Top 15 NSE-listed companies in 2023 based on market capitalization. The dashboard helps investors and analysts track price trends, percentage changes, and candlestick patterns over different time intervals (1 month, 6 months, 1 year, and custom date ranges), enabling better-informed investment decisions.

## Methodology
### Data Collection:

Historical stock price data for each of the top 15 NSE companies was sourced from the official NSE (National Stock Exchange of India) website.

The data for all companies was consolidated into a single dataset for ease of analysis and comparison.

### Stock Selection:

The top 15 companies were selected based on market capitalization, ensuring relevance and significance within the Indian stock market.

### Data Preparation & Calculation:

Custom calculations were created using Level of Detail (LOD) expressions in Tableau to determine starting and ending prices for each selected period.

#### Key calculations included:

tableau

// Current Close Price
Cr_Close_Date = IF [Date1]= {FIXED [Nifty Index1]: MAX([Date1])} THEN [Close1] END

// Previous Close Price
Pr_Close_Date = IF [Date1]= {FIXED [Nifty Index1]: MIN([Date1])} THEN [Close1] END

// Trend Color
Change = IF {FIXED [Nifty Index1]:MAX([Cr_Date_Close]) > MAX([Pr_Date_Close])} 
         THEN "green" 
         ELSE "red" 
         END
Line charts were dynamically color-coded:

🔵 Blue for upward trends

🔴 Red for downward trends

## Analysis Performed
Trend Analysis: Displayed the trend of each stock over selected timeframes (1M, 6M, 1Y, and custom).

Candlestick Charts: Captured price volatility, open-high-low-close patterns, and momentum across time.

Percentage Change: Showed clear indication of gain/loss over selected periods using LOD-based calculations.

Visual Differentiation: Used color-coded lines to instantly reflect bullish or bearish trends.

## Key Insights
Users can quickly compare how each top NSE stock has performed across different periods.

Instant visibility into which stocks are trending upwards or downwards using intuitive color indicators.

Candlestick charts provide deep insight into market behavior, highlighting daily price movements and volatility.

The dashboard enables custom time range filtering, helping users spot short-term versus long-term investment opportunities.

 ## Features
Date Range Toggle: 1M, 6M, 1Y, or custom period

Color-coded Line Charts based on trend direction

Candlestick View of all 15 stocks

Interactivity for better stock-by-stock exploration

Clean, responsive, and professional design in Tableau
