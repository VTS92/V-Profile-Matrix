# V-Profile Matrix — Volume Profile with Power Score Engine

**Pine Script v5 | TradingView | Institutional Volume Analysis**

Built and used daily in live trading. Part of the V-Suite — works best combined with the [V-Sessions Engine](https://github.com/VTS92/V-Sessions-Engine) and the [V-WAPE Engine](https://github.com/VTS92/V-WAPE-Engine).

---

## What it does

V-Profile Matrix maps where volume concentrates across price levels, then quantifies the strength of every detected price imbalance with a numeric Power Score. It answers two questions: **where were institutions active — and which imbalances are most likely to drive the next move?**

The indicator combines four layers:

**Volume Distribution Analysis**
- **POC (Point of Control)** — the price level with the highest traded volume. Price tends to return here repeatedly.
- **Value Area** — the price range containing 70% of all volume. Defines the market's accepted fair value zone.
- **HVN (High Volume Nodes)** — areas of heavy institutional activity. Act as strong support and resistance.
- **LVN (Low Volume Nodes)** — price gaps with little trading activity. Price moves through these rapidly.

**Fair Value Gap (FVG) with Power Score** *(new)*
- Detects bullish and bearish FVGs filtered by an ATR-based volatility threshold (eliminates noise)
- Each FVG is classified as **LVN (low-volume imbalance)** or **HVN (high-volume imbalance)** based on the volume density at the gap level
- **Power Score (1–5)** — quantifies the strength of each LVN imbalance combining three factors:
  - **Vacuum factor** (primary weight) — how empty the volume profile is at the gap's price
  - **Gradient factor** — how steep the volume drop is versus adjacent price levels
  - **Kinetic factor** — gap size relative to ATR (volatility-normalized energy)
- The score appears as a numeric label next to each LVN, making it instantly clear which imbalances deserve attention

**PowerBox — Core Vacuum Zone** *(new)*
- Inside each LVN, a smaller inner box marks the **single bin with the lowest volume** — the zone where price is most likely to accelerate through
- Provides a precise execution target inside the wider FVG range

**Adaptive Profile Rendering** *(new)*
- Profile elements (polyline, Value Area, secondary POC) auto-hide when the chart timeframe meets or exceeds the anchor timeframe — keeping higher-timeframe charts clean while preserving POC and FVG visibility
- No more manual toggle: the indicator reacts to the chart you're on

---

## Screenshots

![V-Profile Overview](v-profile-overview.png)
![V-Profile Detail](v-profile-detail.png)

---

## How to use

1. Open TradingView and go to **Pine Editor**
2. Paste the contents of `V-Profile-Matrix.pine`
3. Click **Add to chart**
4. Select your **Anchor Timeframe** (recommended: 1 Day for intraday, 1 Week for swing)
5. Adjust **Row Resolution** based on your trading style:
   - Scalping: 50–80 bins
   - Intraday: 100–200 bins
   - Swing / Macro: 200–400 bins
6. Watch for **Power Score 4–5** labels on LVN imbalances — those are the highest-conviction setups

---

## Configuration

| Parameter | Default | Description |
|---|---|---|
| Enable Profile Visualization | On | Show the volume profile polyline & Value Area |
| Enable LVN/HVN Visualization | On | Show secondary POC and inner PowerBox |
| Enable Fair Value Gap (FVG) | On | Detect and display FVGs with Power Score |
| Anchor Timeframe | 1 Day | Historical window for volume calculation |
| Row Resolution | 100 bins | Vertical price granularity |
| FVG (ATR Filter) | 0.8 | Minimum gap size relative to volatility |

---

## Part of the V-Suite

V-Profile Matrix works best when combined with the rest of the suite:
- **[V-Sessions Engine](https://github.com/VTS92/V-Sessions-Engine)** — multi-timezone session mapping with per-session POC, LVN and VWAP
- **[V-WAPE Engine](https://github.com/VTS92/V-WAPE-Engine)** — anchored VWAP with volume shock detection and live volatility dashboard

**How they fit together:** V-Profile Matrix tells you *where* volume concentrated and rates the strength of each imbalance. V-Sessions tells you *when* each market was active and how it distributed volume. V-WAPE tells you *whether price is overextended* from fair value right now.

---

## Author

**Vito Santarsiero** — Trading Platform Operations Specialist | CISI IOC Candidate | London, UK

[LinkedIn](https://linkedin.com/in/vito-santarsiero) · [V-Sessions Engine](https://github.com/VTS92/V-Sessions-Engine) · [V-WAPE Engine](https://github.com/VTS92/V-WAPE-Engine)
