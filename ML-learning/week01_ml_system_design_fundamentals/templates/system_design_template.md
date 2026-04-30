# ML System Design Template  
*A reusable template for designing machine learning systems.*

---

# 1. Problem Statement

## 1.1 Business Problem  
Describe the real-world problem, who it affects, and why it matters.

## 1.2 ML Problem Framing  
Define the ML task (classification, ranking, retrieval, forecasting, etc.).  
Clarify whether ML is even necessary.

## 1.3 Success Criteria  
Define what “good” looks like in measurable terms.

---

# 2. Requirements

## 2.1 Functional Requirements  
What the system must do:
- Inputs  
- Outputs  
- User interactions  
- System behaviors  

## 2.2 Non‑Functional Requirements  
Constraints and expectations:
- Latency  
- Throughput  
- Availability  
- Reliability  
- Interpretability  
- Privacy/security  
- Cost constraints  

---

# 3. Data

## 3.1 Data Sources  
List all data sources:
- Internal databases  
- Logs  
- APIs  
- Third‑party datasets  
- Streaming sources  

## 3.2 Data Characteristics  
- Volume  
- Velocity  
- Variety  
- Quality issues  
- Label availability  

## 3.3 Data Pipeline  
Describe:
- Ingestion  
- Validation  
- Transformation  
- Feature engineering  
- Storage  

Include diagrams if helpful.

---

# 4. Modeling

## 4.1 Model Selection  
Describe candidate model families and justify your choice.

## 4.2 Training Pipeline  
- Preprocessing  
- Feature extraction  
- Training loop  
- Hyperparameter tuning  
- Validation strategy  

## 4.3 Evaluation

### Offline Metrics  
(e.g., accuracy, F1, AUC, MSE, BLEU, recall@k)

### Online Metrics  
(e.g., CTR, conversion rate, latency, error rate)

### Business Metrics  
(e.g., revenue lift, cost savings, risk reduction)

---

# 5. Serving & Deployment

## 5.1 Inference Architecture  
Choose and justify:
- Batch vs. real‑time  
- CPU vs. GPU  
- Containerization  
- Serverless vs. managed endpoints  

## 5.2 Scaling Strategy  
- Autoscaling  
- Caching  
- Sharding  
- Load balancing  

## 5.3 Deployment Strategy  
- Blue/green  
- Canary  
- Shadow testing  
- A/B testing  

---

# 6. Monitoring & Observability

## 6.1 Model Monitoring  
Track:
- Data drift  
- Concept drift  
- Feature distribution changes  
- Prediction distribution changes  

## 6.2 System Monitoring  
Track:
- Latency  
- Throughput  
- Error rates  
- Resource usage  

## 6.3 Alerting  
Define thresholds and escalation paths.

---

# 7. Retraining & Lifecycle Management

## 7.1 Retraining Triggers  
- Time‑based  
- Data‑based  
- Performance‑based  

## 7.2 Model Versioning  
- Model registry  
- Rollback strategy  

## 7.3 Continuous Training (CT)  
If applicable.

---

# 8. Risks & Tradeoffs  
Identify and discuss:
- Technical risks  
- Data risks  
- Ethical risks  
- Operational risks  
- Tradeoffs between accuracy, latency, cost, complexity  

---

# 9. Architecture Diagram  
Include a diagram showing:
- Data flow  
- Model flow  
- Serving flow  
- Monitoring components  

Save the diagram in `/diagrams/` and embed it here.

---

# 10. Final Summary  
A concise explanation of:
- What you designed  
- Why it works  
- What tradeoffs you made  
- How it meets the business goals  
