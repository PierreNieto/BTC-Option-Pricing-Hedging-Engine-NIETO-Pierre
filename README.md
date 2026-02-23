# BTC-Option-Pricing-Hedging-Engine-NIETO-Pierre

Content :

- Engineered a real-time options pricing dashboard by connecting Excel to the Deribit REST API (JSON parsing via VBA) to extract live Spot prices, Forward curves, and Implied Volatility.

- Developed a custom VBA mathematical library implementing the Black-Scholes model and computing first/second-order Greeks (Delta, Gamma, Vega).

- Extracted the implied crypto risk-free rate (cost of carry) dynamically using Put-Call parity and synthetic forwards.

- Designed an automated Delta-Vega neutral hedging simulator using a multi-leg strategy (Short Call, Long Call, Spot BTC).

- Built a Mark-to-Model Full Revaluation stress-testing tool to visualize PnL asymmetry and analyze residual Short Gamma tail risk under extreme market shocks (+/- 50%).

limits :

The Theta impact (Time Decay)
My portfolio is currently Short Gamma. While my relative PnL looks green or with small losses, this table is just a snapshot in time. In reality, if Bitcoin’s price remains stagnant (0% change), I will lose money every single day due to Theta. I am essentially paying a daily rent to maintain this structure; if the market stays flat for too long, this cost will erode any potential gains shown in my simulation.

Dynamic Delta Drift
My hedge is Delta-Neutral only at the current spot price. Because I have a non-zero Gamma, my Delta will drift as soon as the BTC price moves. To stay protected, I would have to constantly re-balance my Spot BTC position. This dynamic hedging involves transaction costs and slippage that are not yet factored into my Excel model. To hedge my gamma, i have to introduce a new short term (maturity) option but in real life, often compensate with another gamma option.

Volatility Surface & Curve Risks (Vega)
I am Vega Neutral, which protects me against a parallel shift in implied volatility. However: my model assumes volatility moves uniformly across strikes. In a real market crash, the smile deforms, and my Greeks will not behave linearly.
