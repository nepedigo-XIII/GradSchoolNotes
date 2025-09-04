# Equities

## Gameplan
- Understand equities as:
  - Investors
  - Sources of financing for managers  
- **Debt financing:** cost = Yield to Maturity (YTM), not coupon rate.  
  - If multiple bonds: take weighted average of YTMs (weighted by market value outstanding).  
- **Equity financing:** not as straightforward (no contractual payments). → Need models for **cost of equity**.

---

## Equity Market Performance Intuition
- Future cash is either **risk-free** or **risky**.
- People are risk averse → require compensation for holding risky assets.
- Only one source of *priced risk*: how well the economy/market is doing.
- Discounting involves:
  - Risk-free rate
  - Risk premium

---

## CAPM Expected Return
Formula:

$$
E[R_i] = R_f + \beta_i \big( E[R_m] - R_f \big)
$$

Where:
- $E[R_i]$: expected return on asset $i$  
- $R_f$: risk-free rate (T-bill)  
- $E[R_m]$: expected return on market (e.g. S&P 500)  
- $\beta_i$: sensitivity of asset $i$ to market

---

## The Risk-Free Rate
- Approximate by yield on short-term U.S. government securities.
- Annualized.
- Serves as baseline for discounting.

---

## Market Risk Premium (MRP)
- $E[R_m] - R_f$
- Historical estimates guide intuition.
- If interest rates rise, MRP estimation becomes trickier.

---

## Beta ($\beta$)
- **Meaning:** Sensitivity of an asset/business/cashflow to economy/market.
  - $\beta = 0$: no sensitivity (risk-free securities).
  - $0 < \beta < 1$: low sensitivity (e.g. utilities, food).
  - $\beta = 1$: matches market (S&P 500).
  - $\beta > 1$: high sensitivity (luxury goods, tech stocks).
  - $\beta < 0$: does well when market performs poorly.

- **Interpretation:** Characterizes market-related risk.

- **Questions:**
  - What is high beta? Low beta?
  - Beta of market = 1.
  - Beta of risk-free asset = 0.
  - Is $\beta=0$ identical to risk-free? Not necessarily.
  - What assets might have negative beta?

---

## Using Beta
- Expected return = CAPM with $\beta$.
- Example: New power company generating \$1MM profit annually forever.
  - $\beta \approx 0.5$.
  - Value it by discounting with CAPM-derived rate.

---

## Valuation Techniques
Two main approaches:
1. **Fundamental Valuation**
   - Dividend Discount Model (DDM)
   - Free Cash Flow model (not fully covered here)
2. **Relative Valuation**
   - P/E multiples
   - Other multiples (EV/EBIT, EV/EBITDA, P/B, EV/Sales, etc.)

---

## Dividend Discount Model (DDM)
- Value = PV of all future dividends.
- Good for stable, mature, dividend-paying firms.
- Growing perpetuity formula:

$$
P_0 = \frac{D_1}{k - g}
$$

Where:
- $D_1$: dividend next year  
- $k$: discount rate (from CAPM)  
- $g$: growth rate of dividends

---

## Relative Valuation
- Idea: If two companies have same risk & growth → valuation multiples should match.

Example:
- Car maker A: \$200MM profit, $\beta=1$, growth 2%.  
- Car maker B: \$300MM profit, $\beta=1$, growth 2%, Market Cap = \$3B.  
- Then A’s Market Cap = $(200/300) \times 3B = 2B$.

---

## Multiples
- Common: P/E ratio.
- Others: EV/EBIT, EV/EBITDA, P/B, EV/Sales.
- Careful: match numerator & denominator correctly.
  - Example: Market Cap / Net Income is fine.  
  - EV / EBIT is fine.  
  - Market Cap / EBIT is not consistent.  

---

## Relative Valuation Pitfalls
- Assumptions may break down if:
  - Different growth rates.
  - Different betas.
  - Cashflow proxies mismatch.
- Solutions:
  - Use bounds (firms with higher growth should have at least equal P/E).
  - Adjust for beta differences.
  - Hybrid methods (fundamental + relative).

---

## Key Themes
- Cost of debt = YTM.
- Cost of equity = CAPM expected return.
- Valuation of equity: projected future dividends/cashflows or multiples.
- Valuation of debt: simpler (cashflows known, discount with YTM).
- Valuation is more of an **art** than a science.

