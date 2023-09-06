### How the "Institutional Insight Indicator [Enhanced]" Works

> **Note**: This enhanced version of the indicator includes new features like RSI, dynamic multipliers, and improved visual elements. It is no longer directly available on TradingView. To use it, you'll need to upload the source code available from this repository into your TradingView editor and save it as a custom indicator into the "My scripts" section.

#### Parameters
- **Multiplier**: A factor used to amplify the average trading volume for identifying buying and selling pressures.
- **Dynamic Multiplier**: The original multiplier is dynamically adjusted based on the market's volatility.
- **Length of Moving Average**: Specifies the period for calculating the Simple Moving Average (SMA) of the trading volume.
- **SMA Length for Trend**: Specifies the period for calculating the SMA of the closing prices to determine the overall market trend.
- **Length for Supply/Demand Zones**: The period used for identifying swing highs and lows.
- **Buffer for Swing Highs/Lows**: A percentage buffer applied to swing highs and lows to filter out market noise.
- **RSI Period**: Specifies the period for calculating the Relative Strength Index (RSI).

#### Calculations
1. **Average Volume**: The SMA of the trading volume over a specified period.
2. **Trend SMA**: The SMA of the closing prices over a specified period, used to identify the market trend.
3. **Swing Highs/Lows**: Identified when the closing price exceeds or falls below the highest or lowest closing prices within a specified zone, adjusted by a buffer.
4. **Most Recent Swing High/Low**: The most recent price levels at which a swing high or low occurred.
5. **Buying/Selling Pressure**: Conditions identified based on the relationship between the closing price, Trend SMA, average volume, and RSI.

#### Adaptive Fibonacci Levels
- **Fibonacci 38.2%**: Calculated as `mostRecentSwingLow + 0.382 * (mostRecentSwingHigh - mostRecentSwingLow)`
- **Fibonacci 50%**: Calculated as `mostRecentSwingLow + 0.500 * (mostRecentSwingHigh - mostRecentSwingLow)`
- **Fibonacci 61.8%**: Calculated as `mostRecentSwingLow + 0.618 * (mostRecentSwingHigh - mostRecentSwingLow)`

#### Visual Elements
- **Bar Colors**: Bars are colored green (with 90% transparency) for buying pressure and red (with 90% transparency) for selling pressure.
- **Trend SMA**: Plotted with a purple line of width 2 for better visibility.
- **Swing High/Low Markers**: Labels "High" and "Low" are plotted above or below bars where swing highs or lows occur.
- **Fibonacci Levels**: Plotted as lines on the chart with varying line widths to distinguish between different levels.
- **High Volume Areas**: Highlighted with a very transparent blue background (95% transparency).

#### Alerts
- **Buying Pressure Alert**: Triggered when the conditions for buying pressure are met.
- **Selling Pressure Alert**: Triggered when the conditions for selling pressure are met.

By combining these elements, the Institutional Insight Indicator [Enhanced] aims to offer a multi-faceted view of the market, assisting traders in making more informed decisions.
