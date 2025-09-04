# Time Value of Money (TVM)

---

## 1. What is Finance?
- **Definition**: A subfield of economics concerned with the supply and demand of a special good — **consumption at different points in time**.
- Example:
  - A **$1 bill today** → consumes $1 now or later.
  - A **$1 Certificate of Deposit (CD)** locked for 1 year at 2.5% → consumes $1.025 in one year.
- **Key Idea**: All financial goods reflect consumption possibilities **at different times**, either certain or uncertain.

---

## 2. Discounting
- **Core principle**:  
  > A dollar tomorrow is worth less than a dollar today.
- Reasons:
  - With $1 today → you can invest and earn interest → worth more tomorrow.
  - With $1 tomorrow → you could borrow today, but due to interest/frictions you’d consume **less than $1 today**.
- **Financial Friction**: Lending rate << Borrowing rate  
  (e.g., CD vs. credit card interest).  
  - In theory, we often assume borrowing = lending rates.

-**Friction Elaborated**:  
  - **Inflation**: $1 today buys more than $1 tomorrow.
  - **Uncertainty**: Future payments may not materialize.
  - **Opportunity Cost**: Money today can be invested.

-**Simple Illustration**:

Imagine two people:

- Alice has $1,000 today but no need for it.

- Bob wants $1,000 today, promises to repay in a year.

In a frictionless world:

- They’d agree on a fair rate, say 5%.

- Alice earns 5% → Bob pays 5%.

- In the real world (with friction):

- If Bob borrows via credit card → pays 20%.

- If Alice deposits in a CD → earns only 2%.

The 18% spread = financial friction.


---

## 3. Discount Rate
- **Definition**: The rate used to discount future cash flows to their present value (PV).  

$$
PV = \frac{FV}{(1 + r)^t}
$$

- **Example**:  
  - Signing bonus = $5,000 in 6 months.  
  - Credit card 6-month interest rate = 15%.  
  - Max amount you can consume today:

$$
PV = \frac{5000}{1.15} = 4347
$$

⚠️ Not a good idea to borrow today against a future bonus at high interest.

---

## 4. Annuities
- **Definition**: A steady stream of payments (inflows/outflows) at fixed intervals.  
  - Example: Rent = $500/month for 12 months.  

**Formula (ordinary annuity):**

$$
PV = R \cdot \frac{1 - (1 + i)^{-n}}{i}
$$

where:
- \(R\) = cash flow per period ($500),
- \(i\) = periodic interest rate = 10%/12,
- \(n\) = number of periods = 12.

**Expanded form:**

$$
PV = \frac{500}{(1+10\%/12)^1} + \frac{500}{(1+10\%/12)^2} + \cdots + \frac{500}{(1+10\%/12)^{12}}
$$

---

## 5. Perpetuities
- **Definition**: A constant stream of cash flows that continues forever.  

**Formula:**

$$
PV = \frac{A}{r}
$$

where:
- \(A\) = payment per period,
- \(r\) = periodic discount rate.

**Example**:  
Rent = $500/month forever, rate = 10%/12.  

$$
PV = \frac{500}{(10\%/12)} = 60,000
$$

---

## 6. Growing Perpetuities
- **Definition**: A perpetuity where payments grow at a constant rate \(g\). When the term `Step Function` is mentioned, it usually refers to a mathematical function that is constant within certain intervals and jumps to different values at specific points. In the context of growing perpetuities, the payments increase by a fixed percentage each period, or `g`.

**Formula:**

$$
PV = \frac{A}{r - g}
$$

Conditions:
- \(r > g\) (otherwise PV is infinite).  
- \(A\) = payment at \(t=1\).

---

## 7. Applications
- **Decision-making**:
  - If PV of rents = $60,000 → landlord should not sell property for less than this value.
  - Offers > PV should be carefully considered.
- **Real-life trade-offs**:  
  - Monthly vs. lifetime subscriptions (e.g., Tivo).  
  - Implied discount rates reveal how consumers value **now vs. later**.

---

## 8. Key Formulas (Summary)
- **Discounting**:

$$
PV = \frac{FV}{(1 + r)^t}
$$

- **Annuity**:

$$
PV = R \cdot \frac{1 - (1 + i)^{-n}}{i}
$$

- **Perpetuity**:

$$
PV = \frac{A}{r}
$$

- **Growing Perpetuity**:

$$
PV = \frac{A}{r - g}
$$

---

## 9. Extra Notes (Supplementary Knowledge)
- **Compounding vs. Discounting**:
  - Compounding moves values forward in time.
  - Discounting moves values backward in time.
- **Effective Annual Rate (EAR)** vs. **Nominal Annual Rate (APR)**:
  - APR often quoted, but actual effective return depends on compounding frequency.
- **Risk Considerations**:
  - These examples assume guaranteed cash flows.  
  - In reality, uncertainty requires **risk-adjusted discount rates**.

---
