# Mona Lisa Expert Advisor

This Expert Advisor (EA) is developed by the Forex Robot Easy Team. For detailed reviews and trading results of this product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/mona-lisa-forex-software-review-real-results-and-download-options/). Please note that ForexRobotEasy is not the official developer of this product. This code is provided as a sample and may not be the exact implementation of the official product. To find the official developer of this product, please use MQL5.

## Description
The Mona Lisa Expert Advisor is designed to trade during the rollover period when market volatility is low. It uses Bollinger Bands and Average True Range (ATR) to determine the market volatility and identify optimal entry and exit points. The EA calculates the risk amount based on the account balance and a user-defined risk percentage. It then places pending limit orders with a specified lot size, stop loss, and take profit levels. The EA also handles trade execution, trade events, and errors.

## Input Parameters
- **LotSize**: The lot size for each trade.
- **StopLoss**: The stop loss value in pips.
- **TakeProfit**: The take profit value in pips.
- **RiskPercentage**: The risk percentage per trade.

## Global Variables
- **AccountBalance**: Stores the account balance.
- **RiskAmount**: Stores the calculated risk amount.
- **EntryPrice**: Stores the calculated entry price.
- **StopLossPrice**: Stores the calculated stop loss price.
- **TakeProfitPrice**: Stores the calculated take profit price.

## Initialization function
The `OnInit()` function initializes the global variables. It retrieves the account balance using the `AccountInfoDouble()` function and calculates the risk amount based on the account balance and the user-defined risk percentage.

## Start function
The `OnStart()` function is executed when the EA is started. It checks if it is the rollover period and if the market volatility is low. If both conditions are met, it calls the `CalculateEntryAndExitPoints()` function and places pending limit orders using the `PlacePendingOrders()` function.

## Check if it is Rollover period
The `IsRolloverPeriod()` function is responsible for checking if it is the rollover period. The logic to determine the rollover period is not provided in the code and should be implemented separately.

## Check if market volatility is low
The `IsChannelLow()` function checks if the market volatility is low by using Bollinger Bands and Average True Range (ATR). The logic to determine the market volatility is not provided in the code and should be implemented separately.

## Calculate entry and exit points
The `CalculateEntryAndExitPoints()` function calculates the entry and exit points based on the market conditions. The exact logic for calculating these points is not provided in the code and should be implemented separately.

## Place pending orders
The `PlacePendingOrders()` function places pending limit orders using the `OrderSend()` function. It first sends a buy limit order with the calculated entry, stop loss, and take profit levels. If the buy limit order is placed successfully, it selects the order using the `OrderSelect()` function and sends a sell limit order with the same parameters. Error handling is included for each step of placing the orders.

## Handle trade execution and errors
The `OnTrade()` function handles trade execution and errors. The exact logic for handling these events is not provided in the code and should be implemented separately.

## Handle trade events
The `OnTradeEvent()` function handles trade events. The exact logic for handling these events is not provided in the code and should be implemented separately.

## Handle errors
The `OnError()` function handles errors. The exact logic for handling errors is not provided in the code and should be implemented separately.
