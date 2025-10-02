### 1. Bond Price

$$
P = \sum_{t=1}^{T} \frac{C}{(1+y)^t} + \frac{F}{(1+y)^T}
$$

- $ P $ = Price of the bond  
- $ C $ = Annual coupon payment $ (F \cdot c) $  
- $ F $ = Face value of bond  
- $ c $ = Coupon rate  
- $ y $ = Yield to maturity (YTM) per period  
- $ T $ = Number of periods to maturity  


### 2. Yield to Maturity (Approximation)

$$
y \approx \frac{C + \frac{F - P}{T}}{\frac{F + P}{2}}
$$

- $ y $ = Approximate yield to maturity  
- $ C $ = Coupon payment  
- $ F $ = Face value of bond  
- $ P $ = Price of the bond  
- $ T $ = Number of periods to maturity  


### 3. Net Present Value (NPV)

$$
NPV = \sum_{t=1}^{n} \frac{CF_t}{(1+r)^t} - C_0
$$

- $ CF_t $ = Cash flow at time $ t $  
- $ r $ = Discount rate  
- $ C_0 $ = Initial investment (outflow)  
- $ n $ = Number of periods  


### 4. Internal Rate of Return (IRR)

Defined as the discount rate that makes NPV = 0:

$$
0 = \sum_{t=1}^{n} \frac{CF_t}{(1+IRR)^t} - C_0
$$

- $ CF_t $ = Cash flow at time $ t $  
- $ IRR $ = Internal Rate of Return  
- $ C_0 $ = Initial investment  
- $ n $ = Number of periods  


### 5. Profitability Index (PI)

$$
PI = \frac{\sum_{t=1}^{n} \frac{CF_t}{(1+r)^t}}{C_0}
$$

- $ PI $ = Profitability index  
- $ CF_t $ = Cash flow at time $ t $  
- $ r $ = Discount rate  
- $ C_0 $ = Initial investment  
- $ n $ = Number of periods  


### 6. Weighted Average Cost of Capital (WACC)

$$
WACC = \frac{E}{V} \cdot R_e + \frac{D}{V} \cdot R_d \cdot (1-T_c)
$$

- $ E $ = Market value of equity  
- $ D $ = Market value of debt  
- $ V = E + D $ = Total firm value  
- $ R_e $ = Cost of equity  
- $ R_d $ = Cost of debt  
- $ T_c $ = Corporate tax rate  


### 7. Macaulay Duration

$$
D = \frac{\sum_{t=1}^{T} \left( \frac{t \cdot CF_t}{(1+y)^t} \right)}{P}
$$

- $ D $ = Macaulay duration  
- $ CF_t $ = Cash flow at time $ t $  
- $ y $ = Yield per period  
- $ P $ = Price of the bond  
- $ T $ = Number of periods to maturity  


### 8. Risk-Free Rate (Rearranged CAPM)

From CAPM:

$$
E(R_i) = R_f + \beta_i (E(R_m) - R_f)
$$

Rearranged (using Market Risk Premium, $ MRP $):

$$
R_f = E(R_i) - \beta_i \cdot MRP
$$

- $ R_f $ = Risk-free rate  
- $ E(R_i) $ = Expected return of asset $ i $  
- $ \beta_i $ = Beta of asset $ i $  
- $ E(R_m) $ = Expected market return  
- $ MRP = E(R_m) - R_f $ = Market risk premium  


### 9. Bond Coupon Cashflows (Discounted)

For year $ t $:

$$
DCF_t = \frac{C}{(1+y)^t}
$$

At maturity year $ T $:

$$
DCF_T = \frac{C + F}{(1+y)^T}
$$

- $ DCF_t $ = Discounted cash flow at time $ t $  
- $ C $ = Coupon payment  
- $ y $ = Yield per period  
- $ F $ = Face value of bond (principal)  
- $ T $ = Number of periods to maturity  


### 10. Cost of Equity (CAPM)

$$
R_e = R_f + \beta \cdot (E(R_m) - R_f)
$$

Or equivalently, using Market Risk Premium:

$$
R_e = R_f + \beta \cdot MRP
$$

- $ R_e $ = Cost of equity  
- $ R_f $ = Risk-free rate  
- $ \beta $ = Beta of the company  
- $ E(R_m) $ = Expected return on the market  
- $ MRP = E(R_m) - R_f $ = Market risk premium  
