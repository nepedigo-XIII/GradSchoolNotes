# Risk Measurement and Management  
**Instructor:** Sugata Ray  

---

## 1. Recap  

Previously, we analyzed things from a **financial perspective**, including:  
- Basic **Time Value of Money (TVM)**  
- **Financial Securities:** equities, bonds  
- **Projects:** with the ability to value optionality  

All of this used **expected cash flows**, and risk was factored into the **discount rate**, while keeping **incentives** in mind.  

---

## 2. Focus of This Class  

We are shifting from **expected** to **worst case** analysis.  

### Key Questions  
- Why do we care about the **worst case**?  
- Why isn’t accounting for risk in the discount rate enough?  
- Why isn’t the **standard deviation** or “average risk” good enough?  
- Why not focus on the **best case**?  

---

## 3. Types of Risk  

### Business Risk  
- When **Costs > Revenues**

### Financial Risk  
- **Market risk**  
- **Credit risk**  
- **Liquidity risk**

### Operational Risk  
- Failures in internal processes, systems, or people  

### Legal Risk  
- Exposure from lawsuits, regulations, or compliance failures  

---

## 4. How Much Can We Lose?  

- “Everything” is a correct but **useless** answer.  
- The real question: **How much can we lose realistically?**  
- The goal: **Measure and manage risk.**

---

## 5. Decision-Making Based on Risk  

- **Risk Measurement**  
- **Limit Monitoring**  
- **Reporting** to management and board  
- **Reporting** to regulators  
- **Diversification** and **reinsurance**

---

## 6. Basic Steps in the Risk Measurement Process  

1. Identify risks  
2. Gather and structure data  
3. Perform quantitative measurement  
4. Report results  
5. Make strategic decisions  

---

## 7. Risk Management Systems  

### A Risk Management System *Can*:  
- Predict losses given specific events  
- Identify the most dangerous scenarios  
- Recommend how to change the firm’s risk profile  

### A Risk Management System *Cannot*:  
- Predict the future perfectly  
- Eliminate uncertainty  
- Always be right  

---

## 8. Risk Measurement Approaches  

- **Quantitative metrics:**  
  - VaR (Value at Risk)  
  - CVaR (Conditional Value at Risk)  
  - Other tail risk measures  

- **Scenario Analysis**  
- **Historical Simulations**  
- **“What-if” Analyses**

---

## 9. Definition: Value at Risk (VaR)  

**Definition:**  
VaR is the **predicted worst-case loss** at a specified **confidence level** over a given time horizon.

$$
\text{VaR}_{\alpha} = \text{quantile}_{(1 - \alpha)}(\text{Loss Distribution})
$$

### Example  

If the **1% weekly VaR** of a portfolio is **5%**, it means:  
> In the worst 1% of weeks, the portfolio will lose **at least 5%** of its value.

---

## 10. Shortcomings of VaR  

- Not sensitive to the **tail** beyond the chosen percentile.  
- Encourages designs that **hide tail risk**.  
- Can be **unstable** due to data or model dependency.  

---

## 11. Remedies to VaR’s Limitations  

- Report VaR at **multiple percentiles**.  
- Use **Conditional Value at Risk (CVaR)** instead.  

---

## 12. Conditional Value at Risk (CVaR)  

**Definition:**  
CVaR is the **expected loss** given that losses exceed the VaR threshold.

$$
\text{CVaR}_{\alpha} = \mathbb{E}[ \text{Loss} \mid \text{Loss} > \text{VaR}_{\alpha} ]
$$

### Interpretation  

If the **1% weekly CVaR** of a portfolio is **5%**, it means:  
> In the worst 1% of weeks, the portfolio will lose **on average 5%** of its value.

### Advantages of CVaR  
- Captures **tail risk** more accurately.  
- More **stable** and **difficult to manipulate**.  
- Provides a clearer picture of catastrophic losses.  

---

## 13. How to Measure VaR / CVaR  

### 1. Historical Simulation  
Uses past data to simulate future losses.

### 2. Monte Carlo Simulation  
Uses **generated (synthetic)** data based on statistical assumptions.  

### 3. Analytical Methods  
Assumes a **mathematical distribution** (e.g., Normal distribution) and computes quantiles directly.  

---

## 14. Stress Testing and Scenario Analysis  

Stress tests can be based on:  
- **Historical replays:** using real events from the past.  
  - Must ensure that **parameters** apply to current positions.  
- **Hypothetical scenarios:** plausible but extreme combinations of risk factors.  

### Example: 2008 Financial Crisis  
A large nationwide drop in housing prices would have been considered **“implausible”** prior to 2008 — highlighting the need for robust scenario testing.  

---

## 15. Uses of VaR and Scenario Analysis  

- **Internal Risk Management**  
- **Reporting** to senior management  
- **Regulatory compliance** and stress testing frameworks  

---

## 16. Independence in Risk Oversight  

- If the **CRO reports to the CEO**, focus may shift toward **expected value** rather than worst-case outcomes.  
- If the **risk manager reports to the portfolio manager**, potential profits may outweigh risk control.  
- **Board of Directors** involvement is crucial — ultimately, it’s **shareholders’ money** at risk.  

---

## 17. Example: Risk Management in an International Airline  

Complex exposures include:  
- **Fuel costs:** linked to oil prices and USD exchange rate  
- **Aircraft purchases:** dollar and euro exposures  
- **Salaries:** paid in multiple currencies  
- **Ticket sales:** received in various currencies  
- **Payments to airports:** multi-currency and fee-based  

Result: **Highly complex, multi-dimensional risk profile.**

---

## 18. Concluding Thoughts  

- This only **scratches the surface** of risk management.  
- Two major quantitative methods covered:  
  1. **(C)VaR** — measures tail losses statistically.  
  2. **Scenario Analysis** — evaluates impact of specific shocks.  

**Further Learning:**  
Extensive material exists for deeper study, including **enterprise risk management (ERM)**, **credit risk modeling**, and **regulatory frameworks** like **Basel III**.

---

## Appendix: Key Formulas  

### Value at Risk (VaR)

$$
\text{VaR}_{\alpha} = \inf \{ x \mid P(L > x) \leq 1 - \alpha \}
$$

### Conditional Value at Risk (CVaR)

$$
\text{CVaR}_{\alpha} = \mathbb{E}[L \mid L > \text{VaR}_{\alpha}]
$$

Where:  
- \text{L} = Portfolio loss  
- \text{\alpha} = Confidence level (e.g., 99%)  
- \text{VaR}_{\alpha} = Threshold loss exceeded only \( 1 - \text{\alpha} \) fraction of the time  

