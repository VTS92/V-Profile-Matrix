# V-Profile Matrix — Volume Profile Indicator

**Pine Script v5 | TradingView | Institutional Volume Analysis**

Built and used daily in live trading. Part of the V-Suite — works best combined with the [V-WAPE Engine](https://github.com/VTS92/V-WAPE-Engine).

---

## What it does

V-Profile Matrix maps where volume concentrates across price levels over a selected time window. It answers one question: **where were institutions active?**

The indicator identifies:

- **POC (Point of Control)** — the price level with the highest traded volume. Price tends to return here repeatedly.
- **Value Area** — the price range containing 70% of all volume. Defines the market's accepted fair value zone.
- **HVN (High Volume Nodes)** — areas of heavy institutional activity. Act as strong support and resistance.
- **LVN (Low Volume Nodes)** — price gaps with little trading activity. Price moves through these rapidly.
- **Fair Value Gaps (FVG)** — price imbalances classified by volume density to distinguish exhaustion gaps from momentum gaps.

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

---

## Configuration

| Parameter | Default | Description |
|---|---|---|
| Anchor Timeframe | 1 Day | Historical window for volume calculation |
| Row Resolution | 100 bins | Vertical price granularity |
| FVG Filter (ATR) | 0.8 | Minimum gap size relative to volatility |
| Clean Chart (1D+) | On | Shows POC and FVG only on higher timeframes |

---

## Part of the V-Suite

This indicator works best combined with the **[V-WAPE Engine](https://github.com/VTS92/V-WAPE-Engine)** — an anchored VWAP system with volume shock detection and live volatility dashboard.

Used together: V-Profile Matrix identifies **where** institutions were active. V-WAPE identifies **when** they are moving aggressively relative to fair value.

---

## Author

**Vito Santarsiero** — Trading Platform Operations Specialist | CISI IOC Candidate | London, UK

[LinkedIn](https://linkedin.com/in/vito-santarsiero) · [V-WAPE Engine](https://github.com/VTS92/V-WAPE-Engine)
