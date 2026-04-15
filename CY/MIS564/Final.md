# Final Study Guide for MIS564 Organizational Cyber Security

## **`Risk Management`**


### Definition of Risk
- **Risk** refers to the potential for loss, damage, or harm to an organization’s assets due to a threat exploiting a vulnerability.
- In cybersecurity, risk is typically considered as a combination of:
  - **Threats** (e.g., attackers, malware, insider actions)
  - **Vulnerabilities** (e.g., unpatched systems, weak access controls)
  - **Impact** (e.g., financial loss, reputational damage, operational disruption)

> **Key Concept:** Risk is not just the presence of a threat—it is the likelihood that the threat will successfully exploit a weakness and cause harm.

---

### Probability vs. Possibility
- Risk is based on the **probability of a breach**, not just the possibility.
- Using *possibility* implies that an event could occur (which is always true in cybersecurity).
- Using *probability* helps prioritize risks based on how likely they are to happen.

> **Example:**  
> - Possible: A nation-state attack on a small business  
> - Probable: Phishing attack targeting employees  

---

### Risk Cannot Be Eliminated
- **Elimination of risk is not possible** in any system.
- The goal of cybersecurity is to **reduce risk to an acceptable level**, not to achieve zero risk.

> **Important Principle:** Absolute security is unattainable; organizations must balance protection with practicality.

---

### Operational Trade-offs
- Blocking all threats (even if it were possible) would:
  - Severely restrict system functionality
  - Reduce productivity
  - Increase operational friction

> **Example:** Completely isolating systems from the internet would reduce risk but make most modern business operations impossible.

---

### Risk Comparison vs. Quantification
- It is often more practical to describe risk in **relative terms**:
  - “This approach is more risky than that one”
- Exact numerical quantification of risk can be difficult due to:
  - Uncertain threat behavior
  - Changing environments
  - Lack of complete data

---

### Risk Management Definition
- **Risk Management** is the practice of **identifying, analyzing, and controlling risk to an acceptable level**.
- It is an ongoing, continuous process rather than a one-time activity.

#### Core Steps in Risk Management
1. Identify risks
2. Assess risks
3. Treat risks
4. Monitor and review risks

---

### Ways to Treat Risk
Organizations have several strategies to manage risk:

#### 1. Mitigation
- Reduce the likelihood or impact of a risk.
- Achieved through controls such as:
  - Firewalls
  - Encryption
  - Access controls
  - Security training

> Example: Installing antivirus software to reduce malware risk.

---

#### 2. Transference
- Shift the risk to another party.
- Typically done through:
  - Outsourcing
  - Contracts
  - Service providers

> Example: Using a cloud provider to handle infrastructure security.

---

#### 3. Tolerance (Acceptance)
- Accept the risk without taking additional action.
- Used when:
  - Risk is low
  - Cost of mitigation exceeds potential loss

> Example: Accepting minor website downtime risk.

---

#### 4. Avoidance
- Eliminate the activity that introduces the risk.
- Most effective but often impractical.

> Example: Not storing sensitive data to avoid data breach risk.

---

#### 5. Insurance
- Transfer financial impact through insurance policies.
- Does not prevent risk, but reduces financial consequences.

> Example: Cyber liability insurance covering breach costs.

---

### Quantitative vs. Qualitative Risk Assessment

#### Quantitative Risk Assessment
- Uses **numerical values** to measure risk.
- Often involves formulas such as:
  - Annual Loss Expectancy (ALE)
  - Single Loss Expectancy (SLE)

**Advantages:**
- Objective and data-driven
- Useful for cost-benefit analysis

**Disadvantages:**
- Requires accurate data (often unavailable)
- Can give a false sense of precision

---

#### Qualitative Risk Assessment
- Uses **descriptive categories** instead of numbers:
  - High / Medium / Low
  - Likely / Unlikely

**Advantages:**
- Easier to perform
- Does not require precise data
- More flexible

**Disadvantages:**
- Subjective
- Less precise for financial decision-making

---

## **`SETA (Security Education, Training, and Awareness)`**

### Sanctions (Definition)
- **Sanctions** are disciplinary actions taken against individuals who violate organizational security policies or procedures.
- They are used to:
  - Enforce compliance
  - Deter undesirable behavior
  - Reinforce the importance of security policies

#### Types of Sanctions
- Verbal or written warnings
- Mandatory retraining
- Suspension of access privileges
- Financial penalties
- Termination of employment (in severe cases)

> **Key Point:** Sanctions are most effective when they are clearly communicated, consistently enforced, and perceived as fair.

---

### Cyber SETA (Security Education, Training, and Awareness)
- **Cyber SETA** refers to programs designed to educate employees about cybersecurity risks and train them to follow secure practices.
- It includes:
  - **Education**: Broad understanding of security concepts
  - **Training**: Job-specific skills and procedures
  - **Awareness**: Ongoing reinforcement of security mindset

> **Goal:** Influence user behavior to reduce human-related security risks.

---

### Issues with SETA
1. **Employees may not take it seriously**
   - Seen as a checkbox activity rather than a critical responsibility

2. **One-size-fits-all education**
   - Training is often identical across roles despite differing responsibilities and risk exposure

3. **Training may be ineffective**
   - If root causes of non-compliance (e.g., time pressure, poor usability) are not addressed, training alone fails

---

### Limitations of Training Assessments
- Multiple-choice assessments after training:
  - Help **document completion and basic understanding**
  - Do **not reliably indicate behavior change**

> **Key Insight:** Knowing the correct answer does not mean an employee will act correctly in real scenarios.

---

### Human Behavior Challenges
- Employees may:
  - **Know the rules** but lack the ability to follow them (e.g., complex systems)
  - **Choose not to follow them** due to convenience, incentives, or conflicting priorities

> **Implication:** Effective security programs must address both knowledge and motivation.

---

### Tailored Training
- Training should be **aligned with job roles and responsibilities**:
  - Developers → secure coding practices
  - HR → data privacy handling
  - Executives → risk and governance

> **Benefit:** Increases relevance, engagement, and effectiveness.

---

### Effective SETA Principles
1. **Train leaders first**: Leadership buy-in drives organizational culture and compliance

2. **Use formal and informal communication**: Policies, emails, workshops, and casual reinforcement all contribute

3. **Interactive communication**: Simulations, phishing tests, discussions, and hands-on activities improve retention

4. **Promote employee agency**: Employees should feel they have input and ownership in policies

5. **Leaders teach security**: Security becomes part of daily operations, not just IT’s responsibility

6. **Use real incidents**: Demonstrates real-world consequences and increases perceived relevance

---

### Challenges with Rewards
- Reward systems for good security behavior:
  - Can be **difficult to design and measure**
  - May face resistance from management due to cost or complexity

> **Trade-off:** While rewards can motivate, they must be carefully structured to avoid misuse or superficial compliance.

---

### Protection Motivation Theory (PMT)
A psychological framework explaining how individuals respond to threats.

#### Components:
1. **Perceived Vulnerability**: Belief about the likelihood of being affected by a threat

2. **Perceived Severity**: Belief about the seriousness of the consequences

3. **Response Efficacy**: Belief that the recommended action will mitigate the threat

4. **Self-Efficacy**: Confidence in one’s ability to perform the action

5. **Response Cost**: Perceived barriers (time, effort, inconvenience) to taking action

> **Application:** Effective training increases vulnerability, severity, efficacy, and confidence while minimizing perceived cost.

---

### Forms of Neutralization (and Training Implications)
- **Neutralization** refers to psychological justifications individuals use to rationalize non-compliant behavior.

#### Common Forms:
1. **Denial of Responsibility**
   - “It’s not my fault”
   - *Training implication:* Clarify accountability

2. **Denial of Injury**
   - “No one will be harmed”
   - *Training implication:* Emphasize real consequences

3. **Denial of the Victim**
   - “They deserved it” or “no real victim”
   - *Training implication:* Highlight impact on individuals and organization

4. **Condemnation of the Condemners**
   - “Management doesn’t follow the rules either”
   - *Training implication:* Ensure leadership models correct behavior

5. **Appeal to Higher Loyalties**
   - “I was just trying to get my work done”
   - *Training implication:* Align security with business goals

> **Key Takeaway:** Training must address not just knowledge gaps, but also the rationalization
