# iFVGPro+

A Pine Script v6 research indicator for visualizing fair value gaps, inverse fair value gaps, liquidity sweeps, market structure, trading sessions, and fractal pivots in a single charting workflow.

## Overview

iFVGPro+ combines several price-action tools that I use when reviewing rule-based trading setups. The project was developed iteratively from chart examples and test cases, with a focus on turning discretionary concepts into explicit and testable conditions.

The indicator is designed for analysis and visualization. It does not execute trades or provide financial advice.

## Features

### Fair Value Gaps and Inversions

- Bullish and bearish FVG detection on a configurable timeframe
- Optional candle-close confirmation
- Configurable FVG extension and colors
- iFVG detection when price closes through an active FVG
- Optional filters for minimum size, momentum, age, spacing, and overlap
- Visual highlighting of confirmed inversions

### Liquidity Sweeps

- Bullish and bearish pivot-based sweep detection
- Configurable sweep-line appearance
- Optional restriction to sweeps occurring inside matching FVGs
- Optional wick-only FVG interaction filter
- First-touch tracking for active FVGs

### Market Structure

- Close-based Break of Structure (BOS) and Market Structure Shift (MSS) detection
- Configurable swing length, colors, line style, line width, and label size
- One-time signaling when a structure level is broken

### Trading Sessions

- Configurable New York, London, Tokyo, and Sydney sessions
- Session ranges, trendlines, means, VWAP, and maximum/minimum levels
- Optional session dashboard
- Session and daily dividers
- Exchange-timezone or custom UTC-offset support

### Fractals and Pivots

- Selectable three-bar or five-bar fractal detection
- Optional pivot classification as HH, LH, LL, and HL
- Configurable pivot lookback and display colors

## Alert Conditions

The script exposes five TradingView alert conditions:

1. iFVG inversion detected
2. Liquidity sweep inside a matching FVG
3. Wick-only sweep inside an FVG
4. Standard liquidity sweep without FVG filters
5. First bullish or bearish FVG touch

## Installation

1. Open the Pine Editor in TradingView.
2. Create a new indicator.
3. Copy the contents of [`indicator.pine`](indicator.pine) into the editor.
4. Save the script and select **Add to chart**.
5. Configure the desired modules and alert conditions in the indicator settings.

## Development Approach

This is an AI-assisted development project. My contribution centers on defining the trading rules and expected behavior, translating chart observations into functional requirements, validating signals against historical charts, identifying false positives and edge cases, and guiding the iterative refinement of the implementation.

## Attribution

This project integrates and adapts open-source work from the following TradingView authors:

- [Sessions [LuxAlgo]](https://www.tradingview.com/script/bkb6vZDz-Sessions-LuxAlgo/) by LuxAlgo
- [Liquidity Sweeps [LuxAlgo]](https://www.tradingview.com/script/JRqryeJ5-Liquidity-Sweeps-LuxAlgo/) by LuxAlgo
- Fractals and pivots logic attributed to [nephew_sam_](https://www.tradingview.com/u/nephew_sam_/)

The LuxAlgo-derived components are used and adapted under the [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). Changes include integration with the FVG system, additional filters and alert behavior, naming, and formatting.

## License

See [`LICENSE.md`](LICENSE.md) for licensing and third-party attribution details.

## Disclaimer

This software is provided for educational and research purposes only. It is not financial advice, and no result or signal produced by the indicator guarantees future performance.
