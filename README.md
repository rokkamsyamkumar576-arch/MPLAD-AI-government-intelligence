# MPLAD-AI-government-intelligence
AI-powered system for anomaly detection, risk analysis and monitoring of MPLADS projects.
# MPLAD-AI

### AI-Powered Monitoring & Early-Warning System for MPLADS

**Smart India Hackathon 2026 | Problem Statement ID: SIH26102**

> **Detect. Explain. Predict. Act.**

---

## Project Overview

MPLAD-AI is an AI-powered monitoring and decision-support system designed to improve transparency, efficiency, and accountability in the implementation of the Members of Parliament Local Area Development Scheme (MPLADS).

The platform analyzes project, financial, progress, payment, geographic, and implementation-related data to identify unusual patterns, potential inefficiencies, delays, cost anomalies, duplicate/similar works, and mismatches between financial and physical progress.

MPLAD-AI generates a **project-level risk score and explainable alerts** so that authorized authorities can identify projects that may require closer verification.

> **Important:** MPLAD-AI does not declare fraud or wrongdoing. It provides risk indicators and decision-support information for human verification.

---

##  Problem Statement

MPLADS involves a large number of development works such as roads, public facilities, community infrastructure, schools, and other durable community assets.

Monitoring these projects manually can be difficult because authorities may need to analyze:

- Sanctioned amounts
- Released funds
- Expenditure
- Physical progress
- Project timelines
- Payment patterns
- Implementing agencies
- Contractors
- Project locations
- Work descriptions
- Completion status

This makes it challenging to identify unusual patterns at an early stage.

Potential issues may include:

- Cost overruns
- Delayed projects
- Unusual expenditure patterns
- Financial vs physical progress mismatches
- Potentially duplicate or highly similar works
- Payment anomalies
- Concentration of risk across contractors or implementing agencies

---

##  Proposed Solution

MPLAD-AI converts project and financial data into actionable monitoring insights.

### Core workflow

```text
MPLADS Data
     ↓
Data Ingestion
     ↓
Data Cleaning & Validation
     ↓
Feature Engineering
     ↓
AI/ML Analysis
     ↓
Risk Scoring
     ↓
Explainable AI
     ↓
Alerts & Reports
     ↓
Human Verification
Key Features
1. Executive Dashboard
Provides an overall view of MPLADS implementation.
It can display:
- Recommended allocation
- Sanctioned amount
- Released amount
- Expenditure
- Project status
- State-wise project distribution
- Sector/category distribution
- Risk distribution
- Year-wise project trends
- AI-generated insights
2. State-wise Analytics
Provides monitoring at the state level.
Users can analyze:
- Projects by state
- State-wise allocation
- State-wise expenditure
- Project status
- Risk distribution
- Sector/category distribution
- Year-wise trends
3. Year-wise Analytics
Tracks project and financial activity across financial years.
It helps analyze:
- Annual allocations
- Annual sanctions
- Annual expenditure
- Number of projects
- Completion trends
- Delayed projects
- Risk trends
4. Lok Sabha & Rajya Sabha MP Analytics
Provides project-level analytical views based on MP type.
The system can show:
- MP name
- MP type
- State
- Constituency/area
- Year-wise projects
- Sanctioned amount
- Expenditure
- Project status
- Sector/category
- Physical progress
- Financial progress
- Risk indicators
The purpose is objective project monitoring and analytics, not political ranking or evaluation.
5. MP Project Activity Profile
For each MP, the system can provide a structured project profile.
Example:
MP
 ↓
Year
 ↓
Projects
 ↓
Sector / Category
 ↓
Sanctioned Amount
 ↓
Expenditure
 ↓
Progress
 ↓
Risk Indicators
This enables year-wise analysis of project activity and fund utilization.
6. Risk & Alerts
Each project can receive a composite AI risk score.
Example:
Risk Score: 78 / 100
Risk Level: HIGH
The system also explains the factors contributing to the score.
Example indicators:
- Cost anomaly
- Delay
- Payment anomaly
- Financial-progress mismatch
- Duplicate similarity
- Other unusual patterns
Risk scores are decision-support indicators and require human verification.

7. Anomaly Detection
The system identifies unusual patterns using statistical and machine-learning techniques.
Potential anomaly categories include:
Cost Anomaly
A project may be flagged when its sanctioned amount is significantly higher than comparable projects within relevant peer groups.
Financial vs Physical Progress Mismatch
Example:
Financial Progress: 80%
Physical Progress: 40%

Difference: 40 percentage points
This can generate a risk indicator for further verification.
Payment Anomaly
The system can identify unusual payment or expenditure patterns compared with expected project behavior.
8. Duplicate / Similar Work Detection
MPLAD-AI uses Natural Language Processing to identify potentially similar project descriptions.
The system can compare:
- Work descriptions
- Project categories
- Locations
- Contractors
- Costs
- Geographic proximity
Technology
- Sentence Transformers
- Text embeddings
- Cosine similarity
- Geographic distance analysis
Example:
Work A ───────┐
              ├── Similarity Analysis ──> Potential Similar Work
Work B ───────┘
Similarity does not confirm duplicate work or misconduct. Verification is required.

9. Contractor / Implementing Agency Analysis
The system analyzes relationships between:
- Contractors
- Implementing agencies
- Projects
- Districts
- Risk indicators
It can help identify concentrations of high-risk projects that may require closer review.
10. Delay Prediction
The system estimates project delay risk using factors such as:
- Project age
- Physical completion
- Financial utilization
- Historical project performance
- Category
- District
- Expected timeline
The output can include:
- Expected progress
- Actual progress
- Days delayed
- Delay probability
- Contributing factors
11. Explainable AI
MPLAD-AI is designed to explain why a project received a particular risk indicator.
Possible techniques:
- SHAP
- LIME
- Feature contribution analysis
Example:
Risk Score: 78

Contributing Factors:
• Financial-progress mismatch
• Project delay
• Cost deviation
• Unusual payment pattern
• Similar nearby work
This makes the system more transparent than a black-box alert.
12. Interactive Map
Projects can be visualized geographically.
The map can show:
- Project locations
- Risk levels
- State
- District
- Project category
- Project status
Users can drill down from:
State → District → Project → Risk Details
13. AI / Voice Assistant
Users can ask questions about the available project dataset using natural language.
Example queries:
Show high-risk projects in Andhra Pradesh.

How many delayed projects are there?

Show potential duplicate projects.

Which district has the highest expenditure?

Show projects with financial-progress mismatch.
14. Citizen Feedback
Citizens can report issues related to public works.
Example:
- Incomplete work
- Quality concerns
- Location mismatch
- Project not visible at the reported location
Workflow:
Submitted
   ↓
Under Review
   ↓
Field Verification
   ↓
Resolved
Citizen feedback can act as an additional information source for authorized verification.
15. Automated Reports
MPLAD-AI can generate project and monitoring reports based on selected filters.
Reports can include:
- Project information
- Financial status
- Physical progress
- Risk score
- Anomaly indicators
- Delay information
- Explanation
- Recommended verification actions
16. Real-Time Alert Framework
The system is designed to support automated early-warning alerts when new risk indicators are detected.
Example:
 HIGH-RISK PROJECT

Project ID: MPLAD-XXXX

Reason:
Financial progress significantly exceeds
physical progress.

Action:
Verification recommended.
 AI / ML Methodology
MPLAD-AI uses multiple analytical techniques.
Component	Technique
Anomaly Detection	Isolation Forest
Delay Prediction	Random Forest / XGBoost
Duplicate Detection	Sentence Transformers
Text Similarity	Cosine Similarity
Geographic Analysis	Distance / DBSCAN
Explainability	SHAP / LIME
Compliance Checks	Rule Engine
Risk Calculation	Composite Risk Engine


 Risk Scoring
The platform combines multiple indicators into a composite project-level risk score.
A prototype risk model can consider:
Indicator	Example Weight
Financial Anomaly	25%
Cost Deviation	20%
Delay Risk	15%
Payment Anomaly	15%
Financial-Physical Mismatch	15%
Duplicate Similarity	10%


The final score is converted into risk categories.
Low
Medium
High
Critical
The exact thresholds and weights can be calibrated using validated historical data and domain expertise.
Risk scores are indicators for prioritizing verification. They are not findings of fraud.

 System Architecture
              MPLADS / eSAKSHI / Authorized Data
                         │
                         ▼
                  Data Ingestion
                         │
                         ▼
                Data Cleaning
                         │
                         ▼
               Feature Engineering
                         │
          ┌──────────────┼──────────────┐
          ▼              ▼              ▼
     State/Year      MP Analytics   Geo Analytics
      Analytics
          │              │              │
          └──────────────┼──────────────┘
                         ▼
                  AI Analytics Engine
                         │
       ┌─────────────────┼─────────────────┐
       ▼                 ▼                 ▼
 Anomaly Detection  Duplicate Detection  Delay Prediction
       │                 │                 │
       └─────────────────┼─────────────────┘
                         ▼
                    Risk Engine
                         │
                         ▼
                  Explainable AI
                         │
                         ▼
                  Alerts & Reports
                         │
                         ▼
                Monitoring Dashboard
                         │
                         ▼
                 Human Verification
 Technology Stack
Frontend
- React.js
- Tailwind CSS
- HTML
- CSS
- JavaScript
Backend
- Python
- FastAPI
AI / Machine Learning
- Python
- Pandas
- NumPy
- Scikit-learn
- Isolation Forest
- Random Forest / XGBoost
- Sentence Transformers
- SHAP
- LIME
Database
- PostgreSQL
Visualization
- Recharts / Plotly
- Leaflet
- OpenStreetMap
Deployment / Prototype
- Netlify
- Cloud-based backend and database services
 Dataset
The system is designed to work with authorized MPLADS project and financial data.
Potential fields include:
Project ID
Work Name
MP Name
MP Type
State
District
Constituency / Area
Sector
Category
Estimated Cost
Sanctioned Amount
Released Amount
Expenditure
Sanction Date
Completion Date
Physical Progress
Financial Progress
Project Status
Implementing Agency
Payment Information
Latitude
Longitude
Financial Year
Prototype Dataset
The current prototype uses synthetic/demo data for testing and demonstration purposes.
It does not represent actual government records.
For real-world deployment, the system should be validated using authorized and appropriately governed MPLADS data.
 End-to-End Workflow
1. Collect authorized project data
             ↓
2. Clean and validate data
             ↓
3. Generate analytical features
             ↓
4. Run AI/ML models
             ↓
5. Detect anomalies and patterns
             ↓
6. Calculate project risk score
             ↓
7. Explain contributing factors
             ↓
8. Generate alerts
             ↓
9. Authority reviews the case
             ↓
10. Field / documentary verification
             ↓
11. Appropriate action, if required
 Security & Responsible AI
MPLAD-AI follows a human-in-the-loop approach.
The system:
- Does not automatically declare fraud.
- Does not replace authorized government decision-makers.
- Provides explainable risk indicators.
- Requires verification before action.
- Should use authorized data sources.
- Should protect sensitive information.
- Should maintain appropriate access controls.
- Should maintain audit logs for important system actions.
 Prototype Limitations
The current prototype has several limitations:
- Demo data is synthetic.
- It is not connected to live government databases.
- Satellite verification is simulated.
- Real-time alert generation is simulated.
- AI models require validation with authorized historical data.
- Risk thresholds require domain-specific calibration.
- Production deployment would require government security, privacy, infrastructure, and integration requirements.
 Future Scope
Future versions can include:
- Integration with authorized MPLADS/eSAKSHI data sources
- Live data pipelines
- Advanced geospatial analytics
- Real satellite imagery analysis
- Computer vision-based project verification
- Mobile application
- Multilingual AI assistant
- Advanced contractor network analytics
- Automated compliance monitoring
- Government system integration
- Field verification applications
- Improved predictive models
- Continuous model monitoring and recalibration
 Innovation & USP
Our USP
MPLAD-AI transforms MPLADS monitoring from reactive reporting into proactive, explainable AI-based risk management.

Unlike a simple dashboard, MPLAD-AI combines:
Analytics + AI Detection + Risk Scoring + Explainability + Alerts + Geographic Intelligence + Human Verification
The system helps authorities focus their attention on projects that may require closer examination.
Key principle
“We don't replace the authority's decision. We help the authority know where to look first.”

 Live Prototype
 Live Prototype:
https://mplad-ai-one.vercel.app?_vercel_share=UqCdNP8X2uSYlQDRKb8Cv2u2uV5C80LC
The prototype demonstrates:
- Dashboard
- Risk & Alerts
- Anomaly Detection
- Duplicate Work Detection
- Contractor Network Analysis
- Delay Prediction
- Explainable AI
- Satellite Verification workflow
- Voice Assistant
- Interactive Map
- Citizen Feedback
- Automated Reports
- Real-Time Alert simulation
 Project Repository
This repository contains the project code and supporting files.
GitHub:
https://github.com/rokkamsyamkumar576-arch/MPLAD-AI
Demo
YouTube Demo:
https://youtu.be/2Ir-DstB_h8?si=wXmoqoOB4cKgerGh
Technical Documentation
Technical Documentation:
https://docs.google.com/document/d/1YGBxUFL84g_IX7aQtPmp0Vfh-utSlzqcR0ZFNS2USFw/edit?tab=t.0
Smart India Hackathon 2026
Problem Statement: SIH26102
Title: Development of an AI-powered system to detect anomalies, fraud, and inefficiencies in MPLAD Scheme implementation
Project: MPLAD-AI
Tagline: Detect. Explain. Predict. Act.
Team : civisietnial
Project: MPLAD-AI
Hackathon: Smart India Hackathon 2026
Problem Statement ID: SIH26102 Disclaimer
MPLAD-AI is a prototype decision-support and early-warning system developed for demonstration and innovation purposes.
Risk scores, anomaly indicators, similarity results, and alerts do not establish fraud, misconduct, or wrongdoing.
All flagged cases require appropriate human review and verification by authorized authorities before any action is taken.
The current prototype uses synthetic/demo data and should not be interpreted as an analysis of actual government records.
 Summary
MPLAD-AI provides an integrated AI-powered approach to MPLADS monitoring:
DATA
 ↓
ANALYZE
 ↓
DETECT
 ↓
SCORE
 ↓
EXPLAIN
 ↓
ALERT
 ↓
VERIFY
 ↓
ACT
MPLAD-AI — Detect. Explain. Predict. Act.

