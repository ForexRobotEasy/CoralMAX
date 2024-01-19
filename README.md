# CoralMAX Expert Advisor

This is the ReadMe file for the CoralMAX Expert Advisor code. The CoralMAX Expert Advisor is a customizable trading robot developed by Forex Robot Easy Team. For detailed reviews and trading results of this product, please visit [Forex Robot Easy - CoralMAX Review](https://forexroboteasy.com/forex-robot-review/coralmax-review-automating-forex-trades-with-precision/).

## Input Parameters
- `EntryCondition1`: Example customizable entry condition (default: 1.5)
- `EntryCondition2`: Example customizable entry condition (default: -0.5)
- `MaxDrawdown`: Maximum drawdown percentage (default: 10)

## Global Variables
- `previousPrice`: Stores the previous price
- `tradeOpen`: Indicates whether a trade is open or not

## Initialization Function
The `OnInit()` function is called during the initialization of the Expert Advisor. It sets the initial values of the global variables `previousPrice` and `tradeOpen`.

## Tick Function
The `OnTick()` function is called on every tick of the market. It retrieves the current price and checks if the entry conditions are met. If the conditions are met and a trade is not already open, it opens a buy trade using the `OrderSend()` function.

If a trade is open and the drawdown exceeds the specified `MaxDrawdown` percentage, it scales in by adding an additional position with a higher volume.

If the trade is open and the profit reaches 5%, it closes the trade using the `OrderClose()` function.

## Deinitialization Function
The `OnDeinit()` function is called when the Expert Advisor is being deinitialized. It closes any remaining open trades if `tradeOpen` is true.

Please note that ForexRobotEasy is not the official developer of this product. We are only providing a sample code that can work as described in the product. To find the official developer of this product, please use MQL5.

For more information and support, please visit [Forex Robot Easy](https://forexroboteasy.com).
