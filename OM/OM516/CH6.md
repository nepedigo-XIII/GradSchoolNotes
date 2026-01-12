# **Chapter 6 – Statistical Quality Control (SQC) Study Guide**

---

## **1. What is SQC?**
Statistical Quality Control (SQC) is the set of statistical tools used to measure, monitor, and improve the quality of processes and outputs.

### **Three Categories of SQC**
1. **Statistical Process Control (SPC)**  
   - Uses sample data to monitor processes during production.  
   - Detects whether a process is operating within acceptable limits.

2. **Descriptive Statistics**  
   - Mean, range, standard deviation.  
   - Used to describe and analyze quality characteristics.

3. **Acceptance Sampling**  
   - Inspects samples from a lot to decide if the whole batch should be accepted or rejected.  
   - Used before or after the process, not during.

---

## **2. Causes of Variation**
### **Common (Random) Causes**
- Natural variations inherent in any process.
- Cannot be easily identified or eliminated.

### **Assignable Causes**
- Specific, identifiable sources of variation.
- Can be corrected (e.g., training issues, worn tools, equipment maintenance).

---

## **3. Descriptive Statistics for Quality**
- **Mean (x̄):** Average value.  
- **Range (R):** Max – Min of a set.  
- **Standard Deviation (σ):** Spread of data around the mean.  
- **Distributions:** Normal (bell-curve) or skewed.

---

## **4. SPC & Control Charts**
Control charts graphically monitor a process over time using:
- **Center Line (CL)**  
- **Upper Control Limit (UCL)**  
- **Lower Control Limit (LCL)**  

### **Types of Control Charts**
#### **Charts for Variables**
- **X-bar Chart:** Tracks changes in process mean.  
- **R Chart:** Tracks process variability (spread).  
- Used together for full analysis.

#### **Charts for Attributes**
- **p-Chart:** Monitors proportion defective (yes/no outcomes).  
- **c-Chart:** Monitors number of defects per unit (multiple defects possible).

---

## **5. Building X-bar & R Charts**
### **X-bar Chart Steps**
1. Compute sample means.  
2. Calculate overall mean (x̄̄).  
3. Use σ (or R-bar and A₂ factor) to compute UCL and LCL.  
4. Plot results and evaluate.

### **R Chart Steps**
1. Compute sample ranges.  
2. Calculate R-bar.  
3. Compute UCL and LCL using D₃ and D₄ factors.  
4. Plot and analyze variability.

---

## **6. Attribute Chart Usage**
### **P-Chart**
- Use when you know # defective and sample size.  
- Control limits depend on p̄ (average proportion defective).

### **C-Chart**
- Use when counting number of defects per item (not proportion).  
- Control limits based on the average count of defects.

---

## **7. Process Capability**
Assesses how well a process meets design specifications.

### **Cp (Process Capability Ratio)**
- Assumes process is centered.  
- Higher Cp = more capable process.

### **Cpk (Process Capability Index)**
- Accounts for process centering.  
- If **Cpk < 1**, the process is not capable.

---

## **8. Six Sigma**
- Quality level where process variation fits within ±6 standard deviations.  
- Represents **3.4 defects per million opportunities (DPMO)**.  
- Benchmark for world-class quality.

---

## **9. Acceptance Sampling**
Used to accept/reject lots based on:
- Lot size (N)  
- Sample size (n)  
- Acceptable defects (c)  

### **Operating Characteristic (OC) Curves**
- Show probability of accepting a lot vs. defect percentage.  
- Used to visualize sampling risks.

### **Key Terms**
- **AQL:** Acceptable defect level.  
- **LTPD:** Maximum tolerable defect level.  
- **Producer's Risk (α):** Rejecting a good lot.  
- **Consumer's Risk (β):** Accepting a bad lot.

---

## **10. Managerial Decisions in SQC**
Managers must choose:
- How often to inspect  
- How much to inspect  
- Where to inspect (incoming, in-process, final)  
- Which tools (SPC charts vs. acceptance sampling)  

---

## **11. SQC in Service Organizations**
Challenges:
- Services are intangible.  
- Quality is often subjective.  

Solutions:
- Develop measurable metrics (wait time, number of complaints, response times).  
- Use control charts to monitor performance.

---

## **12. Advanced Out-of-Control Signals**
A process is likely out of control when:
- A single point falls outside limits.  
- 2 of 3 successive points are beyond ±2σ on the same side.  
- 4 of 5 points are beyond ±1σ on the same side.  
- A run of 8 points appears on one side of the mean.  
- Data shows unnatural patterns or trends.

---

# **Chapter 6 Summary**
- SQC includes descriptive statistics, SPC, and acceptance sampling.  
- Variation can be common or assignable.  
- X-bar and R charts monitor mean and variability.  
- P-charts and C-charts handle attribute data.  
- Process capability (Cp and Cpk) measures if a process meets specs.  
- Six Sigma aims for near-perfect quality.  
- Acceptance sampling uses probability to judge whole lots.  
- Services require quantifiable metrics to apply SQC effectively.

---
