# Metrics Taxonomy Cheat Sheet  
*A reference for evaluating ML systems end‑to‑end.*

---

# 1. Business Metrics (North Star Metrics)

These measure **business impact**, not model performance.

Examples:
- Revenue lift  
- Cost reduction  
- Risk reduction  
- Customer retention  
- Fraud prevented  
- Time saved / efficiency gained  
- Mission impact (for GEOINT or defense contexts)

**Characteristics:**
- Owned by product or leadership  
- Often lagging indicators  
- Hardest to attribute directly to ML  
- Most important in system design interviews  

---

# 2. Product Metrics

These measure **user behavior** and product‑level outcomes.

Examples:
- Click‑through rate (CTR)  
- Conversion rate  
- Engagement time  
- Task completion rate  
- User satisfaction (CSAT, NPS)  
- False positive/negative user impact  

**Characteristics:**
- Bridge between business and ML metrics  
- Often used for A/B testing  
- Must be monitored continuously  

---

# 3. ML Metrics — Offline (Model‑Centric)

Used during training, validation, and experimentation.

## 3.1 Classification
- Accuracy  
- Precision  
- Recall  
- F1 score  
- ROC‑AUC  
- PR‑AUC  
- Log loss  

## 3.2 Regression
- MSE / RMSE  
- MAE  
- R²  
- MAPE  

## 3.3 Ranking / Retrieval
- Recall@k  
- Precision@k  
- NDCG  
- MRR  

## 3.4 Generative Models
- BLEU  
- ROUGE  
- METEOR  
- Perplexity  

**Characteristics:**
- Fast to compute  
- Good for model iteration  
- Do NOT guarantee real‑world performance  

---

# 4. ML Metrics — Online (Production‑Centric)

Measured in real‑time or near‑real‑time.

Examples:
- Latency (P50, P90, P99)  
- Throughput  
- Error rate  
- Timeout rate  
- Token usage (LLMs)  
- Retrieval quality (RAG)  
- Tool‑call success rate (agents)  

**Characteristics:**
- Directly tied to user experience  
- Often more important than offline metrics  
- Critical for SLAs and SLOs  

---

# 5. Data Quality Metrics

Measure the health of the data pipeline.

Examples:
- Missing value rate  
- Schema drift  
- Feature distribution drift  
- Outlier rate  
- Data freshness  
- Label consistency  
- Duplicate rate  

**Characteristics:**
- Early warning signals  
- Often the root cause of model degradation  
- Essential for monitoring dashboards  

---

# 6. Operational Metrics (MLOps)

Measure system reliability and cost.

Examples:
- CPU/GPU utilization  
- Memory usage  
- Autoscaling events  
- Queue depth  
- Cost per inference  
- Cost per 1,000 predictions  
- Container restart count  

**Characteristics:**
- Owned jointly by ML + platform teams  
- Critical for production readiness  
- Often overlooked by junior practitioners  

---

# 7. Evaluation Anti‑Patterns

Avoid these common mistakes:

- **Optimizing only for offline metrics**  
- **Ignoring latency in real‑time systems**  
- **Using accuracy for imbalanced datasets**  
- **Comparing models without fixing random seeds**  
- **Ignoring cost when scaling models**  
- **Using a single metric to judge performance**  
- **Not separating business vs. ML metrics**  

---

# 8. Metric Alignment Framework

A healthy ML system has:

| Layer | Metric Type | Example |
|------|-------------|---------|
| Business | North Star | Revenue lift, risk reduction |
| Product | User behavior | CTR, conversion rate |
| ML Offline | Model quality | F1, AUC, RMSE |
| ML Online | Real‑time performance | Latency, error rate |
| Data | Pipeline health | Drift, freshness |
| Ops | Reliability & cost | Utilization, cost per inference |

**Rule of thumb:**  
If a metric doesn’t influence a business or product outcome, it’s not a primary metric.

---

# 9. Choosing the Right Metrics

Use this quick guide:

- **Classification:** F1, ROC‑AUC, PR‑AUC  
- **Imbalanced data:** Precision/Recall, PR‑AUC  
- **Ranking/RAG:** Recall@k, NDCG  
- **LLMs:** Hallucination rate, grounding score, token cost  
- **Agents:** Tool‑call success rate, task completion rate  
- **Real‑time systems:** Latency (P99), error rate  
- **Batch systems:** Throughput, cost per batch  

---

# 10. Final Notes

A senior ML practitioner:
- Aligns metrics with business goals  
- Uses multiple metrics, not one  
- Monitors metrics continuously  
- Designs systems to fail gracefully  
- Documents metric definitions clearly  

This cheat sheet should evolve as your system design skills deepen.

