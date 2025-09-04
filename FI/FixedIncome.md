# Fixed Income — Study Guide

## Main Categories
- Government  
- Municipal  
- Corporate  
- Securitized / Mortgage  
- Others  
- Cash & Equivalents

---

## Key Drivers of Fixed-Income Prices
- **Interest rates** (dominant driver)  
- **Credit risk** (default likelihood)  
- **Maturity** (term/tenor)  
- **Tax rates** (esp. munis)  
- **Inflation** (real vs nominal)  
- **Optionality** (call/prepay features)

---

## Bond Building Blocks
"Bond is the simplest fixed income instrument"

- **Par (Face) Value:** typically \$1,000.  
- **Maturity:** years until principal is due.  
- **Coupon Rate ($c$):** stated annual rate applied to par.  
- **Coupon Payment ($INT$):**  
  ```text
  Coupon Payment = ((Coupon Rate) × (Par or Face Value)) / (Number of Payments per Year)
  ```

- **Market Rate / Required Return ($k_d$):** depends on risk, term, etc.

---

## Price–Yield (YTM) Intuition

The relationship between a bond's **yield to maturity (YTM, $k_d$)** and its **coupon rate ($c$)** determines whether the bond sells at par, at a discount, or at a premium.

- **If $k_d = c$ → price = par**  
  When the required return (YTM) equals the coupon rate, the bond’s cash flows are exactly what investors expect at the market rate.  
  Example:  
  - Coupon rate: 5%  
  - YTM: 5%  
  - Par value: $1,000  
  - **Price ≈ $1,000**  

- **If $k_d > c$ → price < par (discount)**  
  When the required return exceeds the coupon rate, investors demand a higher return than the bond’s coupons provide. The bond must sell **below par** to compensate.  
  Example:  
  - Coupon rate: 5%  
  - YTM: 6%  
  - Par value: $1,000  
  - **Price < $1,000**  

- **If $k_d < c$ → price > par (premium)**  
  When the required return is lower than the coupon rate, the bond’s coupons are attractive relative to the market. Investors are willing to pay **more than par**.  
  Example:  
  - Coupon rate: 5%  
  - YTM: 4%  
  - Par value: $1,000  
  - **Price > $1,000**  

**Intuition:**  
- Bond price moves **inversely** to YTM.  
- Higher required returns → lower bond prices (discount).  
- Lower required returns → higher bond prices (premium).  

**Visual Summary:**

| YTM ($k_d$) | Coupon Rate ($c$) | Price         |
|-------------|-----------------|--------------|
| = $c$       | = $c$           | Par ($1000$) |
| > $c$       | < $k_d$          | Discount     |
| < $c$       | > $k_d$          | Premium     |


---

## Bond Valuation (Level Annual Coupon)
Price is PV of coupons + principal:

$$
V_B = \sum_{t=1}^{N} \frac{INT}{(1+k_d)^t} + \frac{M}{(1+k_d)^N}
$$

where $INT=cM$, $M=$ par, $N=$ years to maturity.

**Example (10y, 10% coupon, par \$1,000):**
- If $k_d=7\%$: $V_B \approx 1210.71$  
- If $k_d=10\%$: $V_B = 1000$ (par)  
- If $k_d=13\%$: $V_B \approx 837.21$  

**1-year comparison (same par/coupon):**
- $k_d=7\%$: $\approx 1028.04$  
- $k_d=10\%$: $=1000$  
- $k_d=13\%$: $\approx 973.45$  

**Takeaway:** bond values move **inversely** with yields; longer maturities move **more** (interest rate risk).

---

## Yield to Maturity (solve-for-rate)
YTM is the discount rate $k_d$ that sets price = PV of cash flows.

**Example (10y, 9% coupon, par \$1,000, price \$887):**

$$
887 = \sum_{t=1}^{10}\frac{90}{(1+k_d)^t} + \frac{1000}{(1+k_d)^{10}}
$$

This requires iteration → $k_d \approx 10.9\%$.

---

## Zero-Coupon Bond Illustration
Bond pays \$100 in 30 years; no interim coupons.

**Price at 3%:** 
$$
P = \frac{100}{(1.03)^{30}} \approx 41.19
$$

**If rate ↑ to 4%:** $P \approx 30.83$ (–25.1%).  
**If rate ↓ to 2%:** $P \approx 55.21$ (+34.0%).  

---

## Duration (Rate Sensitivity)
- **Concept:** the (approximate) % price change for a small change in yield.  
- **Zero-coupon:** duration $\approx$ time to maturity.  
- **Coupon bonds:** duration $<$ maturity.  

**Macaulay Duration (weighted-average time of cash flows):**

$$
D_{\text{Mac}} = \sum_{t=1}^{N} \frac{t \cdot \dfrac{CF_t}{(1+y)^t}}{P}
$$

*Example:* For a sample bond at $y=6\%$, $D_{\text{Mac}} \approx 14.6$ years.

**Modified Duration (price sensitivity):**

$$
D_{\text{mod}} = \frac{D_{\text{Mac}}}{1+y}, 
\qquad
\frac{\Delta P}{P} \approx -D_{\text{mod}} \cdot \Delta y
$$

---

## Credit, Optionality, Liquidity, Taxes
- **Credit quality:** ratings (AAA, AA, A, BBB, …); lower rating → higher required yield, lower price.  
- **Optionality (callable bonds, mortgage prepay):** when rates fall, issuers refinance → caps price upside.  
- **Liquidity:** more-liquid bonds trade at a premium.  
- **Taxation:** tax-exempt muni coupons gain value as tax rates rise.

---

## Compact Reference

**Price (annual coupons):**
$$
V_B = \sum_{t=1}^{N}\frac{cM}{(1+k_d)^t} + \frac{M}{(1+k_d)^N}
$$

**Premium/Par/Discount rule:**  
- $k_d < c \Rightarrow$ premium  
- $k_d = c \Rightarrow$ par  
- $k_d > c \Rightarrow$ discount  

**YTM (solve $k_d$ from price):**
$$
P = \sum_{t=1}^{N}\frac{CF_t}{(1+k_d)^t}
$$

**Zero price:** 
$$
P = \frac{M}{(1+y)^N}
$$

**Macaulay duration:** 
$$
D_{\text{Mac}} = \sum_{t=1}^{N} \frac{t \cdot \dfrac{CF_t}{(1+y)^t}}{P}
$$

**Modified duration & price-change approximation:** 
$$
D_{\text{mod}} = \frac{D_{\text{Mac}}}{1+y}, \qquad
\frac{\Delta P}{P} \approx -D_{\text{mod}}\Delta y
$$

---

## Quick Tables

**10-year vs 1-year (par \$1,000, 10% coupon):**

| $k_d$ | 10-year Price | 1-year Price |
|---:|---:|---:|
| 7%  | \$1,210.71 | \$1,028.04 |
| 10% | \$1,000.00 | \$1,000.00 |
| 13% | \$   837.21 | \$   973.45 |

---

## Bottom Line
- Rates drive bond prices; **price ↓ when yield ↑**.  
- Longer maturity → **greater** interest-rate risk (higher duration).  
- Other important levers: **credit**, **optionality**, **liquidity**, **taxes**.
