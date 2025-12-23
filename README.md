# 🏥 Proactive Data Breach Risk Management in Healthcare

## 1. Background & Overview
Healthcare data breaches threaten patient privacy, organizational trust, and regulatory compliance. With the growth of digital health records, sensitive information such as Protected Health Information (PHI), insurance details, and Social Security data is increasingly exposed.

According to the *Ponemon Institute Cost of a Data Breach Report (2023)*, healthcare has the **highest average breach cost ($10.93M)** and the **longest identification and containment time (329 days)**.  

This project applies **text mining and NLP techniques** to healthcare breach reports to uncover patterns, classify breach severity, and support **proactive risk management** strategies. :contentReference[oaicite:0]{index=0}

## 2. Data Structure Overview
**Source:** U.S. Department of Health and Human Services (HHS) – Office for Civil Rights (OCR) Healthcare Breach Report Portal  

**Description:**  
Publicly reported healthcare data breaches affecting **500 or more individuals** across the United States. Each record represents a reported breach incident with structured attributes and an unstructured textual description.

**File:** `breach_report.csv`  
**Size:** 5,370 rows × 9 columns  

<img width="1352" height="608" alt="Screenshot 2025-12-23 at 1 22 07 PM" src="https://github.com/user-attachments/assets/ff156f44-a34f-498e-a26b-3bdf5feb2a8b" />

**Key Columns:**
- `name_of_covered_entity` – Organization reporting the breach  
- `state` – U.S. state where the breach occurred  
- `type_of_breach` – Breach category (e.g., hacking, theft, loss)  
- `individuals_affected` – Number of individuals impacted  
- `breach_submission_date` – Date the breach was reported  
- `web_description` – Free-text description of the breach incident  

**Notes:**
- Data includes only breaches reported to HHS OCR and may not represent all incidents
- Textual descriptions are used for NLP and topic modeling analyses

## 3. Executive Summary
Key findings from the analysis:
- **Hacking and IT incidents** are the most severe breach types by number of individuals affected
- **Business Associates (BAs)** play a major role in breach propagation
- **Regulatory compliance** (HIPAA, HHS, OCR) is a dominant theme across incidents
- States such as **California** report higher breach volumes, likely due to stricter disclosure laws

<img width="613" height="661" alt="Screenshot 2025-12-23 at 1 28 33 PM" src="https://github.com/user-attachments/assets/cd8aa496-112e-4e8e-9021-4ca5e3843e77" />

Advanced NLP methods reveal breach patterns that traditional security monitoring may overlook, enabling earlier detection and targeted response.

 ## 4. Executive Summary

### Text Patterns
- Breach descriptions frequently reference **PHI exposure**, affected individuals, and security failures
- Common phrase patterns emphasize **regulatory notification and compliance actions**

<img width="743" height="262" alt="Screenshot 2025-12-23 at 1 31 52 PM" src="https://github.com/user-attachments/assets/02b4be7f-9a9f-4feb-93f1-28c8b8e4f2b3" />

### Breach Severity Classification
- Logistic regression separates **high-impact vs low-impact breaches** using the top 25% of individuals affected
- Model performs well in prioritizing severe incidents, supporting faster response and risk triage

<img width="687" height="324" alt="Screenshot 2025-12-23 at 1 33 58 PM" src="https://github.com/user-attachments/assets/f736cbc3-3232-431f-9eb0-705b67a11749" />

### Topic Modeling Insights
- **NER:** PHI, HIPAA, HHS, and OCR dominate entity mentions, highlighting regulatory and data-sensitivity risks
<img width="986" height="492" alt="Screenshot 2025-12-23 at 1 35 11 PM" src="https://github.com/user-attachments/assets/02a4a02f-8477-408d-9569-3d076e1cd22c" />

- **LDA:** Core themes center on compliance, breach reporting, and oversight investigations
<img width="852" height="315" alt="Screenshot 2025-12-23 at 1 36 09 PM" src="https://github.com/user-attachments/assets/ed9e4829-5a45-4d77-872e-9c3be3d87407" />

- **BERTopic:** Reveals nuanced risks such as **Business Associate involvement**, **ransomware**, and **email-based attacks**
<img width="672" height="490" alt="Screenshot 2025-12-23 at 1 36 38 PM" src="https://github.com/user-attachments/assets/aa8c10f9-ae9d-4c94-bc4a-3a386955676d" />

### Key Takeaway
Healthcare data breaches are primarily driven by **third-party risk, cyberattacks, and regulatory exposure**, indicating that proactive monitoring and vendor oversight are critical to reducing breach impact.

