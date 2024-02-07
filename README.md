# Total Lock MT4

Total Lock MT4 is a custom Expert Advisor (EA) developed by the Forex Robot Easy Team. This EA is designed to freeze losses by activating a lock when the market moves against the trader's position. It can be a useful tool for risk management and protecting profits in volatile markets.

## How it Works

The EA utilizes two global variables: `stopLoss` and `lockLevel`. 

During initialization, the `OnInit()` function sets the initial stop loss level based on the current bid and ask prices. It calculates the stop loss level by subtracting 1.5 times the spread from the ask price. The `Digits` variable is used to ensure the stop loss level is rounded to the appropriate number of decimal places.

The `OnTick()` function is called on every tick of the market. It first checks if the lock is already activated (`isLockActivated`). If the lock is not activated, it checks if the market moves against the trader's position by comparing the current bid price (`Bid`) with the stop loss level. If the bid price is lower than the stop loss level, indicating a loss, the lock is activated. The lock level is set to the stop loss level, and a message is printed to the log.

If the lock is already activated, the function checks if the market moves further against the trader's position by comparing the current bid price with the lock level. If the bid price is lower than the lock level, the lock level is updated to the current bid price, and a message is printed to the log.

The `OnDeinit()` function is called when the EA is being removed from the chart or during program shutdown. It prints the final lock level to the log.

## Product Description

Total Lock MT4 is a powerful tool developed by the Forex Robot Easy Team to help traders manage their risk and protect profits in the forex market. This custom Expert Advisor freezes losses by activating a lock when the market moves against the trader's position.

With Total Lock MT4, traders can set an initial stop loss level based on the current bid and ask prices. If the market moves against the trader's position and the bid price falls below the stop loss level, the lock is activated. The lock level is then set to the stop loss level, effectively freezing the losses.

If the market continues to move against the trader's position, the lock level is updated to the current bid price, ensuring that the losses remain frozen and minimizing further potential losses.

Total Lock MT4 is a valuable addition to any trader's toolkit, providing an automated solution for risk management and loss mitigation. It allows traders to stay in control of their trades even in volatile market conditions.

Please note that Forex Robot Easy is not the official developer of Total Lock MT4. We provide this sample code as an example of how the product works. For detailed reviews and trading results of this product, please visit the official website: [Total Lock MT4 Review - Freeze Losses with Forex Robot](https://forexroboteasy.com/forex-robot-review/total-lock-mt4-review-freeze-losses-with-forex-robot/).

To find the official developer of this product and access the full version, please visit the MQL5 marketplace.
