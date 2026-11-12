# InteractiveBrokersVR

An unofficial WebXR design mock of a brokerage mobile app in VR.
It runs in a desktop browser with mouse look and in a headset browser with the controller ray and trigger.

This project is not affiliated with Interactive Brokers.
It uses none of their logos, icons or assets, shows example data only, sends nothing anywhere and never asks for a login.
The layout is inspired by the tab structure of the IBKR Mobile app: Watchlist, Portfolio, Trade, Orders, Markets, News and Menu.

## Live page

The page is served by GitHub Pages at <https://larytet.github.io/InteractiveBrokersVR/>.

## What is in the mock

- The watchlist, a candlestick chart with periods, the order ticket, the portfolio, orders, markets, news and menu screens.
- A portfolio constellation on the table: every symbol is an orb orbiting the account core, held positions are larger, and a paper order sends a pulse through its orb.
- A sky above the user with the major indices and a news feed, both example data on a timer.
- Hold-to-confirm on the submit button, large buttons and plus and minus steppers instead of sliders, and panels that can be dragged and are saved in the browser.

## Running locally

Serve the folder and open it in a browser, since the page loads three.js and the fonts from a CDN.

```bash
python3 -m http.server 8000
```
