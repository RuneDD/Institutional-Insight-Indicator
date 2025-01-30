# Institutional Insight Indicator [Enhanced]

This Pine Script indicator combines volume, price action swings, RSI, and supply/demand zones to help traders identify potential market turning points and volume-driven signals.

> **Note**: This indicator is not publicly published on TradingView. To use it, **copy the script** from this repository into the TradingView Pine Editor and **save** it under your “My scripts”.

---

## How It Works

1. **Volume & Volatility**  
   - Calculates average volume using a Simple Moving Average (SMA).  
   - Uses market volatility (standard deviation) to create a dynamic multiplier, scaling the average volume threshold.

2. **Trend Detection**  
   - Employs a second SMA (Trend SMA) on closing prices to determine the overall market trend.

3. **Swing High/Low Detection**  
   - Identifies swing highs and lows based on whether the closing price rises above or falls below recent extremes (adjusted by a user-defined buffer).

4. **Supply & Demand Zones**  
   - Each new swing high spawns a **supply zone** (red box) from that pivot high down to the pivot’s close.  
   - Each new swing low spawns a **demand zone** (green box) from that pivot’s close down to the pivot low.  
   - Old zones are replaced when a new swing occurs.

5. **Fibonacci Levels**  
   - Calculates standard Fibonacci retracement levels (38.2%, 50%, 61.8%) based on the **most recent** swing high and swing low.

6. **Buying & Selling Pressure**  
   - **Buying Pressure**: Triggered if price is above the Trend SMA, forms a bullish bar with volume above the dynamic threshold, and RSI signals potential oversold conditions.  
   - **Selling Pressure**: Triggered if price is below the Trend SMA, forms a bearish bar with volume above the dynamic threshold, and RSI signals potential overbought conditions.

---

## Parameters

- **Volume Multiplier**  
  Scales the calculated average volume threshold.
- **Volume MA Length**  
  Sets the SMA period for average volume.
- **Swing Buffer**  
  A percentage buffer used to confirm a swing high/low beyond typical noise.
- **Trend SMA Length**  
  The SMA period of the closing price used to identify the overall market trend.
- **Supply/Demand Zone Length**  
  Lookback period for detecting significant swing highs/lows.
- **RSI Period**  
  The number of bars used in the RSI calculation.

---

## Visual Elements

- **Bar Colors**  
  - Green (90% opacity) if buying pressure is detected.  
  - Red (90% opacity) if selling pressure is detected.  
- **Trend SMA**  
  Plotted in purple with a line width of 2, clearly indicating the trend direction.
- **Fibonacci Levels**  
  Lines marking the 38.2%, 50%, and 61.8% retracement levels based on the most recent swing points.
- **Supply & Demand Boxes**  
  Boxes (red for supply, green for demand) that update when new swing highs or lows are detected.
- **High Volume Background**  
  A pale blue background indicates bars that exceed the dynamic volume threshold.

---

## Alerts

- **Buying Pressure Alert**  
  Notifies you when the script detects a potential buying opportunity.
- **Selling Pressure Alert**  
  Notifies you when the script detects a potential selling opportunity.

---

## Usage

1. **Open TradingView Pine Editor**  
   Navigate to [TradingView](https://www.tradingview.com/), open a chart, and click “Pine Editor” at the bottom.
2. **Paste the Source Code**  
   Copy the script from this repository into the editor.
3. **Save & Add to Chart**  
   Click “Save,” then “Add to Chart.” Your custom indicator will now appear in “My Scripts.”

By combining volume analysis, RSI, supply/demand zones, and adaptive Fibonacci levels, the **Institutional Insight Indicator [Enhanced]** can help traders spot potential inflection points and overall market sentiment in real time.
