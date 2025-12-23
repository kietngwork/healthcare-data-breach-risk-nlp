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

