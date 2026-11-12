# InteractiveBrokersVR

An unofficial WebXR design mock of a brokerage mobile app in VR.
It runs in a desktop browser with mouse look and in a headset browser with the controller ray and trigger.

This project is not affiliated with Interactive Brokers.
It uses none of their logos, icons or assets, shows example data only, sends nothing anywhere and never asks for a login.
The layout is inspired by the tab structure of the IBKR Mobile app: Watchlist, Portfolio, Trade, Orders, Markets, News and Menu.

## Live page

The page is served by GitHub Pages at <https://larytet.github.io/InteractiveBrokersVR/>.

## What is in the mock

- The watchlist, the order ticket, and the portfolio, orders, markets, news and menu screens.
- Six 3D chart modes on the table for the selected symbol: candles with volume as depth, deviation from VWAP, five layered days, an order book terrain, an implied volatility surface and a yield curve.
- A portfolio constellation on the table: every symbol is an orb orbiting the account core, held positions are larger, and a paper order sends a pulse through its orb.
- A sky above the user with the major indices and a news feed, both example data on a timer.
- Hold-to-confirm on the submit button, large buttons and plus and minus steppers instead of sliders, and panels that can be dragged and are saved in the browser.

## Running locally

Serve the folder and open it in a browser, since the page loads three.js and the fonts from a CDN.

```bash
python3 -m http.server 8000
```

## Prior art and links

This list comes from a search of GitHub, GitLab and the web on 12 November 2026.
Star counts and licenses were not checked except where stated, and several projects are small or abandoned experiments.

### Has anyone put Interactive Brokers in VR?

No VR client for Interactive Brokers turned up, and no one appears to have reverse engineered the IBKR Mobile app or the TWS desktop client for VR.
The practical route is the official API, which needs a running TWS or IB Gateway and does not replace the login screen.

- [TWS API on GitHub](https://github.com/InteractiveBrokers/tws-api-public), the official client sources.
- [IBKR API solutions](https://www.interactivebrokers.com/en/trading/ib-api.php) and the [TWS API introduction](https://interactivebrokers.github.io/tws-api/introduction.html).
  Their pages disagree about the license, so read the current terms before building on it.
- [virtualritz/twsapi](https://github.com/virtualritz/twsapi), a Rust port of the TWS API.

### Brokers and banks in VR or spatial computing

- eToro said in February 2024 that it was exploring its trading app on Apple Vision Pro and Meta Quest: [CNBC](https://www.cnbc.com/2024/02/27/etoro-wants-trading-app-on-apple-vision-pro-meta-quest-vr-headsets.html), [Finance Magnates](https://www.financemagnates.com/forex/etoro-ventures-into-virtual-reality-trading-app-on-apple-and-meta-headsets/).
  I found no confirmation of a launch.
- Plynk, a stock trading app with 3D research and trading on Apple Vision Pro: [press page](https://www.plynkinvest.com/press/plynkspatial), [press release](https://www.silicon.co.uk/press-release/plynk-is-now-available-as-a-visionary-stock-trading-app-on-apple-vision-pro).
- NatWest launched its banking app on Apple Vision Pro in July 2024: [FinTech Global](https://fintech.global/2024/07/19/natwest-pioneers-banking-app-on-apple-vision-pro/), [XR Today](https://www.xrtoday.com/?p=53707).
- Swissquote showed a VR trading prototype with eye tracking in 2017: [FinTech Futures](https://www.fintechfutures.com/fintech/glance-and-trade-swissquote-introduces-vr-trading).
- Bloomberg showed a virtual trading desk on the Oculus Rift in 2014, a mockup with an unlimited number of screens: [Engadget](https://www.engadget.com/2014/06/09/bloomberg-vr-terminal-oculus-rift/).
  Their later work on analyzing financial data in extended reality: [Bloomberg](https://www.bloomberg.com/professional/insights/data/analyzing-financial-data-in-extended-reality), [Harvard D3 case](https://d3.harvard.edu/platform-digit/submission/arvr-bloomberg-and-financial-services/).
- Fidelity Labs built StockCity in 2014, a portfolio rendered as a city for Oculus Rift and the web: [Hypergrid Business](https://hypergridbusiness.com/2014/11/fidelity-tracks-stocks-in-3d).
- ApeMaps, 3D stock heatmaps and charts in early access: [Meta Quest listing](https://queststoredb.com/app/ape-maps-26217820814473969), [Vision Pro listing](https://chrome-stats.com/d/id6756840780).
- No VR or headset app from Robinhood, Schwab or Fidelity turned up.

### Open source projects

- [bodyionita/Project-BlackHole](https://github.com/bodyionita/Project-BlackHole), a Unity app for Cardboard that shows historical stock data as a galaxy around a black hole, one star per company (GPL-3.0).
  Its README has screenshots such as [app_tooltip.JPG](https://github.com/bodyionita/Project-BlackHole/raw/master/app_tooltip.JPG).
- [michaelm142/RAI-Stock-Market-Visualizer-VR](https://github.com/michaelm142/RAI-Stock-Market-Visualizer-VR), a VR stock market visualizer.
- [smurmus/MoneyTrees](https://github.com/smurmus/MoneyTrees), a VR stock market game for Oculus Rift with Leap Motion, built on the Aladdin API: [project page](https://smurmus.github.io/moneytrees.html).
- [prucha/stock-cube](https://github.com/prucha/stock-cube), a small Unity sketch with stock quotes in VR for Oculus Rift and Gear VR.
- [antofy/vr-trading](https://github.com/antofy/vr-trading), a trading prototype in VR.
- [nventimiglia/stockgame](https://github.com/nventimiglia/stockgame), a Unity stock terminal demo with buy and sell buttons, a candlestick chart and a volume chart, not VR.
- [BitcoinXR/M-Trader](https://github.com/BitcoinXR/M-Trader), metaverse and AR trading tools.
- GitLab has little: [colorbird/panotrader](https://gitlab.com/colorbird/panotrader), described as AR and VR trading, which I did not inspect.
- 3D order books: [Is0tope/3D_order_book](https://github.com/Is0tope/3D_order_book) (MIT, TypeScript) and [3303mavihS/Crypto-Orderbook-3d](https://github.com/3303mavihS/Crypto-Orderbook-3d), a WebGL view of the BTC/USDT book with history.
- Immersive analytics toolkits: [IATK](https://github.com/MaximeCordeil/IATK) for Unity, [VinkedViewsMR](https://github.com/limbusdev/VinkedViewsMR) for HoloLens, [vria](https://github.com/vriajs/vria) for the web, [data-sphere](https://github.com/lawerencem/data-sphere), and the [DXR toolkit](https://www.pure.ed.ac.uk/ws/files/75503756/dxr_toolkit_building9.pdf), a declarative grammar for Unity.
- WebXR projects in general: [GitHub topic webxr](https://github.com/topics/webxr).

### Articles and tutorials

- [Live display of cryptocurrency data in a VR environment on the web](https://towardsdatascience.com/live-display-of-cryptocurrency-data-in-a-vr-environment-on-the-web-af476376d018/), Towards Data Science.
- [Build a 3D augmented reality stock data visualization on the web](https://medium.com/@tessrUX/build-a-3d-augmented-reality-stock-data-visualization-on-the-web-with-javascript-part-1-40f59c3784f9), Medium.
- [A virtual reality guided tour of 21 years of the Nasdaq](https://blogs.scu.edu/dataviz/?p=1485), a three.js and D3 piece.
- [Virtual reality for data visualization](https://www.gravityjack.com/?p=1614), Gravity Jack, based on an old three.js release.
- [Putting an interactive HTML5 canvas into VR](https://forum.babylonjs.com/t/how-can-we-best-bring-an-interactive-html5-canvas-into-3d-vr-check-out-my-first-steps/9641), the technique this mock uses for its panels.
- [Cathode](https://discourse.threejs.org/t/cathode-a-crt-phosphor-trading-workspace-with-a-three-js-barrel-lens-candlestick-renderer/92767), a three.js candlestick trading workspace, not VR.

### Research

- [3D stock heatmaps in VR](https://doi.org/10.5334/dsj-2025-014), Data Science Journal 2025, an early study.
- [Financial data visualization in 3D on immersive displays](https://espace.curtin.edu.au/handle/20.500.11937/76324), a 2019 prototype for energy sector data.
- [There is no spoon](https://research.monash.edu/en/publications/there-is-no-spoon-evaluating-performance-space-use-and-presence-w/), how economists used space in a VR analysis system.
- [FinVRViz](https://finvr-viz.s3.amazonaws.com/FinVRViz.pdf) and [Uncharted Software's finance research](https://uncharted.software/research/finance/).
- Cambridge student projects: [Virtual Reality Trading Desk](https://group-projects.cst.cam.ac.uk/Virtual_Reality_Trading_Desk) and [Fly-past Finance](https://wiki.cam.ac.uk/cl-design-projects/Fly-past_Finance).
- [Immersive Analytics Toolkit paper](https://www.pure.ed.ac.uk/ws/files/138540593/IATK_An_Immersive_CORDEIL_DOA15112018_AFV.pdf) and the Brown University notes on [table-top data visualization](https://www.vrwiki.cs.brown.edu/vr-visualization-software/table-top-data-visualization).
- The evidence is small prototypes and short user studies, with no large trial showing better trading decisions.

### Visualization references

- [Bookmap](https://bookmap.com/features), the liquidity heatmap of resting orders over time and price, and a [TradingView order flow heatmap script](https://in.tradingview.com/script/DpSz2HVL-Order-Flow-Heatmap).
- [A guide to stock heat maps](https://www.redchip.com/education/what-are-stock-heat-maps).
- Galaxy, city and orbit metaphors: Project-BlackHole, StockCity and this mock's portfolio constellation.

## 3D price chart modes

The Trade tab implements candle depth as volume, deviation from VWAP in depth, five layered days with today on top, an order book terrain, an implied volatility surface and a yield curve.
The order book, the surface and the curve use synthetic data, and the others are generated from example prices.
Volume at price in depth and indicator sheets are not built yet.

The ideas behind them are design suggestions, not findings.
Keep time on X and price on Y, and spend the depth axis only on data that adds information.

- **Volume at price in depth:** candles on the front plane, a slab behind each time slice showing how much traded at each price, with the most-traded price glowing.
- **Candle depth as volume:** each candle is a box whose height is the range and whose depth is the volume.
- **Deviation from VWAP in depth:** price floats in front of or behind a VWAP plane, measured in standard deviations, with anchored VWAPs as lanes.
  The average price itself is redundant with price, so avoid plotting it on the depth axis.
- **Order book terrain:** time, price and resting liquidity as height, colored by traded volume.
- **Layers in depth:** one sheet per timeframe, per symbol (rebased to 100) or per indicator such as RSI and MACD, all sharing the time axis.
- **Natural 3D data:** an implied volatility surface over strike and expiry, or a yield curve over maturity and time.
- Keep price on a flat plane facing the user, project values onto a back wall, use at most two or three layers, and fade the layers you are not focused on.
