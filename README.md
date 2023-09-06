### How the "Institutional Insight Indicator" Works

> **Note**: This updated version of the indicator includes new features like RSI and dynamic multipliers. It is no longer directly available on TradingView. To use it, you'll need to upload the source code available in the repository into your TradingView editor.

#### Parameters
- **Multiplier**: A factor used to amplify the average volume for identifying buying and selling pressures.
- **Dynamic Multiplier**: The original multiplier is adjusted based on the market's volatility.
- **Length of Moving Average**: The period for calculating the Simple Moving Average (SMA) of the volume.
- **SMA Length for Trend**: The period for calculating the SMA of the closing prices to determine the overall trend.
- **Length for Supply/Demand Zones**: The period used for identifying swing highs and lows.
- **Buffer for Swing Highs/Lows**: A percentage buffer applied to swing highs and lows to filter out noise.
- **RSI Period**: The period for calculating the Relative Strength Index (RSI).

#### Calculations
1. **Average Volume**: The SMA of the trading volume over a specified length.
2. **Trend SMA**: The SMA of the closing prices over a specified length, used to identify the market trend.
3. **Swing Highs/Lows**: Identified based on the closing price exceeding or falling below the highest or lowest closing prices within a zone, adjusted by a buffer.
4. **Most Recent Swing High/Low**: The most recent price levels where a swing high or low occurred.
5. **Buying/Selling Pressure**: Conditions based on the relationship between the closing price, Trend SMA, average volume, and RSI.

#### Adaptive Fibonacci Levels
- **Fibonacci 38.2%**: Calculated as `mostRecentSwingLow + 0.382 * (mostRecentSwingHigh - mostRecentSwingLow)`
- **Fibonacci 50%**: Calculated as `mostRecentSwingLow + 0.500 * (mostRecentSwingHigh - mostRecentSwingLow)`
- **Fibonacci 61.8%**: Calculated as `mostRecentSwingLow + 0.618 * (mostRecentSwingHigh - mostRecentSwingLow)`

#### Visual Elements
- **Bar Colors**: Bars are colored green for buying pressure and red for selling pressure.
- **Swing High/Low Markers**: Triangles are plotted above or below bars where swing highs or lows occur.
- **Fibonacci Levels**: Plotted as lines on the chart.
- **High Volume Areas**: Highlighted with a transparent blue background.

#### Alerts
- **Buying Pressure Alert**: Triggered when buying pressure conditions are met.
- **Selling Pressure Alert**: Triggered when selling pressure conditions are met.

By combining these elements, the Institutional Insight Indicator aims to offer a multi-faceted view of the market, helping traders make more informed decisions.
