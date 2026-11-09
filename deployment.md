# Deployment & Local Setup Guide

**Project:** Company A Customs Clearance Automation Platform  
**Repository:** `https://github.com/your-username/isocode-company-a-customs`  

---

## 1. Quick Start (Local Execution)

Since the application is designed as a self-contained Single Page Application (SPA), no complex build chain or `npm install` step is required.

### Steps to Run:
1. Clone the repository:
   ```bash
   git clone https://github.com/Kamal-123-gupta/isocode-company-a-customs.git
   cd isocode-company-a-customs
   ```
2. Launch directly in your web browser:
   * **Option A:** Double-click `index.html` to open in Google Chrome, Microsoft Edge, or Mozilla Firefox.
   * **Option B (Recommended):** Serve using a local web server:
     ```bash
     npx serve .
     ```
3. Open `http://localhost:3000` in your web browser.

---

## 2. Environment Variables Specification

When deploying the application backend to production (e.g., Vercel, Render, or AWS EC2), configure the following environment variable names (values kept secure):

| Variable Name | Purpose / Description | Region / Scope |
| :--- | :--- | :--- |
| `GEMINI_API_KEY` | Multimodal Vision AI Key for extraction | Private API Key |
| `DATABASE_URL` | PostgreSQL connection string | Local/Cloud DB |
| `AWS_REGION` | Compliant host region under DPDP Act 2023 | `ap-south-1` (Mumbai) |
| `JWT_SECRET` | Secret key for Role-Based Access Control | Production Auth |

---

## 3. Demo Credentials & Test Workflow

Use the **Role Selector** dropdown at the top right of the application header to switch user roles:

1. **Documentation Executive Role:**
   * Review pending shipment **SHP-24811**.
   * Observe the flagged Gross Weight discrepancy (Invoice 3,120 kg vs Packing List 3,165 kg).
   * Click **Confirm & Accept Weight Variance** to resolve the mismatch and unlock the **Export Filing CSV** button.

2. **Documentation Manager Role:**
   * Switch role to **Documentation Manager (Approver)**.
   * Inspect accuracy analytics across **Company B (China)** and **Company C (Sweden)**.
