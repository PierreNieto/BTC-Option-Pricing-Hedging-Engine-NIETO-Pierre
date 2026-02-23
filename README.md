# BTC-Option-Pricing-Hedging-Engine-NIETO-Pierre

API Integration: Engineered a real-time options pricing dashboard by connecting Excel to the Deribit REST API (JSON parsing via VBA) to extract live Spot prices, Forward curves, and Implied Volatility.

Quantitative Modeling: Developed a custom VBA mathematical library implementing the Black-Scholes model and computing first/second-order Greeks (Delta, Gamma, Vega).

Yield Extraction: Extracted the implied crypto risk-free rate (cost of carry) dynamically using Put-Call parity and synthetic forwards.

Portfolio Hedging: Designed an automated Delta-Vega neutral hedging simulator using a multi-leg strategy (Short Call, Long Call, Spot BTC).

Risk Analysis: Built a Mark-to-Model Full Revaluation stress-testing tool to visualize PnL asymmetry and analyze residual Short Gamma tail risk under extreme market shocks (+/- 50%).
