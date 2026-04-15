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


---

### Tailored Training
- Training should be **aligned with job roles and responsibilities**:
  - Developers → secure coding practices
  - HR → data privacy handling
  - Executives → risk and governance


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

---

## **`Management Standards`**

### Universal (Checkbox) vs. Firm-Tailored Cybersecurity Policy

- **Universal (Checkbox) Approach**
  - Standardized, generic policies applied uniformly across the organization
  - Often designed to meet baseline compliance requirements
  - Advantages:
    - Easy to implement
    - Ensures minimum compliance coverage
  - Disadvantages:
    - May not align with actual business operations
    - Can create a “check-the-box” mentality
    - Less effective at addressing specific risks

- **Firm-Tailored Approach**
  - Policies customized to the organization’s:
    - Industry
    - Size
    - Risk profile
    - Operational structure
  - Advantages:
    - More relevant and effective
    - Better alignment with real-world risks
  - Disadvantages:
    - Requires more time, expertise, and resources

> **Key Insight:** Tailored policies are generally more effective, while universal policies are often used for baseline compliance.

---

### ISO 27001
- **ISO/IEC 27001** is an international standard for **Information Security Management Systems (ISMS)**.
- It provides a structured framework for:
  - Managing sensitive information
  - Identifying and treating risks
  - Implementing security controls

> **Purpose:** Establish a systematic approach to managing information security risks.

---

### Control Objective Structure
- A **control objective** defines what a security control is intended to achieve.
- Typically structured as:
  - **Objective**: Desired security outcome (e.g., protect data confidentiality)
  - **Control(s)**: Specific measures implemented to achieve the objective
  - **Metrics/Indicators**: Used to evaluate effectiveness

> **Example:**  
> Objective: Prevent unauthorized access  
> Control: Multi-factor authentication (MFA)  
> Metric: % of systems with MFA enabled

---

### Why Use Standards?
- Most **CISOs (Chief Information Security Officers)** are interested in:
  - Measurable outcomes
  - Clear reporting structures
  - Answering questions from executives and regulators
  - Meeting compliance requirements

---

### Reasons for Adopting Standards
1. **Legal Protection**
   - Demonstrates due diligence in the event of legal or regulatory action

2. **Protection Against Criticism**
   - Provides defensibility if a breach occurs (“industry-standard practices were followed”)

3. **Address Knowledge Gaps**
   - Helps CISOs and teams leverage established best practices

4. **Build Trust**
   - Increases confidence among customers and business partners

5. **Compliance Requirements**
   - Many partners or customers require adherence to recognized standards

---

### Certification vs. Auditing

- **Certification**
  - Indicates that a firm **meets the requirements** of a specific standard (e.g., ISO 27001)
  - Typically granted by an accredited external body

- **Auditing**
  - Process where an **auditor verifies** that the organization adheres to the standard
  - Can be:
    - Internal
    - External

> **Key Distinction:** Certification is the outcome; auditing is the verification process.

---

### ISO Certification Considerations
- Benefits:
  - Enhances **public image and credibility**
  - Signals strong security posture to stakeholders

- Costs:
  - Typically ranges from **$50,000 to $200,000**
  - Includes:
    - Preparation
    - Implementation
    - Audit and certification fees

---

### Limitations of Audits
- Audits may focus heavily on:
  - **Documentation**
  - **Policies and procedures**

- Potential issue:
  - Documented controls may not reflect **actual day-to-day practices**

> **Implication:** Organizations may appear compliant on paper but remain vulnerable in practice.

---

### Importance of Organizational Differences

- Security controls must account for variations across organizations:

#### 1. Operational Differences
- Different business processes require different security measures

#### 2. Organizational Size
- Larger firms:
  - More resources
  - Greater complexity
- Smaller firms:
  - Limited budgets and personnel

#### 3. Industry-Specific Risks
- Different industries face unique threats:
  - Healthcare → patient data privacy
  - Finance → fraud and transaction security
  - Retail → payment card data protection

#### 4. Regulatory Requirements
- Compliance obligations vary by:
  - Industry
  - Geography
  - Data sensitivity

> **Key Takeaway:** A one-size-fits-all approach to cybersecurity is ineffective; controls must be adapted to the organization’s context.

---

## Investment (Cybersecurity Study Guide)

### Underinvestment in Cybersecurity
- Organizations frequently **underinvest in cybersecurity** despite increasing threats.
- Common reasons:
  - Benefits are not immediately visible
  - Costs are upfront, while benefits are preventative
  - Competing budget priorities

> **Key Insight:** Cybersecurity is often undervalued because its success is measured by the absence of incidents.

---

### Cyber vs. IT Budget
- Cybersecurity budgets are often a **subset of overall IT budgets**.
- Tension exists between:
  - **Operational IT needs** (systems, infrastructure, innovation)
  - **Security investments** (risk reduction, compliance)

> **Implication:** Security spending is frequently deprioritized in favor of revenue-generating or operational initiatives.

---

### Perception Problem: “Nothing Goes Wrong”
- When no breaches occur:
  - Leadership may assume current spending is excessive
  - Pressure increases to **cut cybersecurity budgets**

> **Paradox:** Effective security reduces visible incidents, which can lead to reduced future investment.

---

### Cybersecurity as a Cost Center
- Security:
  - **Does not directly generate revenue**
  - Is viewed as an **expense rather than an investment**

- Challenge:
  - Difficult to justify spending on something that prevents hypothetical future losses

> **Result:** CISOs must frame cybersecurity in terms of **risk reduction and business impact**, not just technical necessity.

---

### Challenges for CISOs (Buy-In)
- CISOs often struggle to gain support from:
  - Executives
  - Finance teams
  - Business unit leaders

- Reasons:
  - Misalignment between technical language and business priorities
  - Lack of clear ROI (Return on Investment)

---

### Gordon and Loeb Model
- The **Gordon-Loeb Model** suggests:
  - Optimal cybersecurity investment depends on:
    - **Expected loss from a breach**
    - **Probability of a breach**

> **Core Idea:** Firms should not overspend; there is an **optimal level of investment**, not maximum investment.

---

### Applicability Concerns
1. **Unreliable Data and Measures**
   - Lack of accurate historical breach data

2. **Unproven Assumptions**
   - Model relies on assumptions that may not hold in real-world scenarios

3. **False Assumptions**
   - Simplifications may not reflect complex threat environments

---

### Difficulty in Quantification
- **Cost of a breach** is difficult to estimate due to:
  - Indirect costs (reputation damage, customer churn)
  - Long-term impacts

- **Probability of a breach** is also uncertain:
  - Threat landscape is constantly evolving
  - Limited predictive accuracy

> **Conclusion:** Cyber investment decisions are often made under uncertainty.

---

### Non-Intervening vs. Intervening Investments

- **Non-Intervening Investments**
  - Do not significantly alter how employees perform their work
  - Example: backend monitoring tools

- **Intervening Investments**
  - Directly impact employee workflows or behavior
  - Example: multi-factor authentication (MFA), stricter access controls

> **Trade-off:** Intervening controls may improve security but reduce convenience or productivity.

---

### Steps to Gain Investment Acceptance
1. **Identify Critical Stakeholders**
   - Determine who influences or controls budget decisions

2. **Understand Stakeholder Perspectives**
   - Operational, and strategic priorities differ across groups

3. **Build Support**
   - Persuade key individuals within each stakeholder group

4. **Pilot or Test the Investment**
   - Demonstrate value through:
     - Small-scale implementation
     - Measurable results

> **Key Strategy:** Evidence-based persuasion is more effective than theoretical arguments.

---

### Key CISO Failures
1. **Failure to Understand the Business**
   - Security initiatives misaligned with organizational goals

2. **Poor Communication**
   - Overly technical explanations that fail to resonate with executives

3. **Overreliance on Technical Quality**
   - Assuming the best technical solution is automatically the best business solution

4. **Presenting Multiple Options Without Clear Direction**
   - Weakens perceived leadership and decision-making

5. **Overdependence on Standards**
   - While standards are useful, strictly following them may not yield the best fit for the organization

> **Key Takeaway:** Effective cybersecurity leadership requires **business alignment, communication, and strategic thinking**, not just technical expertise.


---

## **`BCPM (Business Continuity and Disaster Recovery Planning) and IR (Incident Response)`**

### Why Have a Plan?

- **Service disruptions impact customer loyalty negatively**
  - Even short outages can erode user trust and brand perception.
  - In highly competitive markets (e.g., SaaS, finance, healthcare), reliability is a key differentiator.

- **Persistent failures drive customer churn**
  - If issues are not resolved quickly, customers will switch to competitors.
  - Low switching costs in many digital services accelerate this behavior.

- **Accountability often falls on security leadership (e.g., CISO)**
  - Poor incident response or recovery is frequently attributed to the Chief Information Security Officer (CISO).
  - Highlights the importance of preparedness, communication, and governance.

- **Regulatory and reputational risk**
  - Failure to respond effectively may result in compliance violations, legal penalties, and public scrutiny.

---

### Incident Response (IR) Definition

- **Incident Response (IR)** primarily focuses on:
  - **Identification** of security incidents (e.g., breaches, malware, insider threats)
  - **Containment** to limit damage and prevent spread
  - **Eradication** of the root cause (e.g., removing malware, closing vulnerabilities)
  - **Recovery** of affected systems and services
  - **Availability concerns**, ensuring systems remain operational or are restored quickly

- **Key Characteristics**
  - Largely **proactive planning** combined with **reactive execution**
  - Requires defined roles, tools, and communication channels
  - Often supported by Security Operations Centers (SOCs)

---

### Business Continuity Plan (BCP) Definition

- **Business Continuity Plan (BCP)**:
  - A structured plan to **maintain business operations** during and after an incident
  - Ensures an **acceptable level of service** is sustained despite disruptions

- **Core Objectives**
  - Minimize downtime and operational impact
  - Maintain critical business functions
  - Protect revenue streams and customer relationships

- **Examples of BCP Measures**
  - Redundant systems and failover infrastructure
  - Backup and disaster recovery solutions
  - Alternate work locations or remote capabilities

---

### Business Continuity Program Management (BPCM)

- **BPCM Definition**
  - The **management and integration** of Incident Response (IR) and Business Continuity Planning (BCP)
  - Includes **policies, processes, and technologies** to ensure organizational resilience

- **Key Components**
  - Governance frameworks
  - Risk management processes
  - Continuous testing and improvement
  - Cross-functional coordination (IT, security, legal, operations)

---

### Risk-Based Foundation of BPCM

- BPCM is heavily based on:
  - **Risk identification**
    - Identifying potential threats (cyberattacks, natural disasters, system failures)
  - **Understanding critical assets**
    - Systems, data, personnel, and infrastructure essential to operations
  - **Business impact analysis (BIA)**
    - Determines which operations are most critical and acceptable downtime thresholds
  - **Threat landscape awareness**
    - Evaluating likelihood and impact of different threat scenarios

---

### Executive Communication and Public Response

- Following a major incident:
  - The **CEO or executive leadership** may be required to issue public statements
    - Address customers, stakeholders, regulators, and media
  - Communication must be:
    - Timely
    - Transparent (without overexposing sensitive details)
    - Aligned with legal and PR strategies

- Poor communication can:
  - Amplify reputational damage
  - Reduce stakeholder confidence

---

### Recovery Beyond Technology

- Recovery is **not just technical**:
  - Must also restore:
    - **Customer trust**
    - **Partner relationships**
    - **Employee confidence**

- Key Considerations:
  - Clear internal communication to employees
  - External messaging to customers and partners
  - Demonstrating corrective actions and improvements

---

### Third-Party and Outsourcing Considerations

- **Outsourced contracts should include BCP requirements**
  - Vendors must define:
    - Their **business continuity policies**
    - **Testing frequency** (e.g., annual, semi-annual)
    - **Audit practices**

- **Third-party risk management is critical**
  - A vendor failure can directly impact your operations
  - Requires due diligence and ongoing monitoring

---

### Audits and Testing

- **Audits are typically conducted by trusted third parties**
  - Ensures objectivity and compliance with standards (e.g., ISO 22301, NIST)

- **Testing Types**
  - Tabletop exercises (discussion-based scenarios)
  - Simulation exercises (realistic incident drills)
  - Full-scale disaster recovery tests

- **Purpose of Testing**
  - Validate effectiveness of IR and BCP plans
  - Identify gaps and areas for improvement
  - Ensure personnel are familiar with procedures

---

### Typical Incident Response (IR) Process

1. **Detection**
   - Identify potential security incidents via monitoring tools, alerts, or reports

2. **Containment**
   - Limit the spread and impact of the incident
   - Examples: isolating systems, blocking malicious traffic

3. **Eradication**
   - Remove the root cause of the incident
   - Examples: deleting malware, patching vulnerabilities

4. **Recovery**
   - Restore systems and operations to normal
   - Validate system integrity before returning to production

5. **Post-Incident Analysis (Lessons Learned)**
   - Review what happened and why
   - Improve processes, controls, and defenses

---

### Generic vs. Specific Attacks

- **Generic Attacks**
  - Broad, automated, and non-targeted
  - Examples:
    - Mass phishing campaigns
    - Automated vulnerability scans
  - Typically rely on scale rather than precision

- **Specific (Targeted) Attacks**
  - Tailored to a specific organization or individual
  - Often more sophisticated and harder to detect
  - Examples:
    - Advanced Persistent Threats (APTs)
    - Spear phishing campaigns

---

### Specific Threat Intelligence

- **Threat Intelligence**
  - Data and insights about current and emerging threats

- **Specific Threat Intelligence Focuses On**
  - Indicators of Compromise (IOCs)
  - Tactics, Techniques, and Procedures (TTPs) used by attackers
  - Threat actor profiles and motivations

- **Benefits**
  - Enables proactive defense strategies
  - Improves detection and response speed
  - Helps prioritize security investments

- **Sources**
  - Internal logs and monitoring systems
  - External intelligence feeds
  - Information sharing organizations (e.g., ISACs)