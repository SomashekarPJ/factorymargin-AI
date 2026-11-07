# Research References — FactoryMargin AI

This file lists the research and standards that inform the design of **FactoryMargin AI**, an Agentic AI platform for supplier-quote comparison, landed-cost calculation, manufacturing cost estimation, and human-approved commercial decisions.

> **Scope note:** These sources support the problem context and design choices. They do not prove that FactoryMargin AI has already reduced costs, improved margins, or achieved a particular accuracy. Those outcomes must be validated through factory pilots using measured baseline and post-deployment data.

## 1. Indian MSME procurement context

### [1] Strategic Vendor Selection and Purchasing Challenges in India's Manufacturing MSMEs: An Empirical Perspective

R. Mohite, R. Patil, R. Pisal, S. Akre, R. Bhadani, and A. Yadav, *South Asian Journal of Management*, vol. 33, no. 2, pp. 100–127, 2026.

- DOI: https://doi.org/10.62206/sajm.33.2.2026.100-127
- Publisher page: https://sajm-amdisa.org/component/content/article/251
- Relevance: Indian MSME procurement practices, supplier selection, manual or semi-formal purchasing, vendor dependency, and digital procurement adoption.
- Product connection: Supports the need to make procurement information easier to structure and compare. The paper reports vendor-selection considerations including quality, delivery reliability, and pricing flexibility; this supports a multi-criteria comparison rather than a price-only ranking.

### [2] Industrial Outlook Survey of the Manufacturing Sector for Q2:2026-27

Reserve Bank of India, 7 October 2026.

- Official publication: https://www.rbi.org.in/Scripts/PublicationsView.aspx?id=24090
- Relevance: Current macro-level manufacturing context. The RBI reports results from 1,224 responding manufacturing companies and notes that raw-material cost pressures remained elevated in Q2:2026-27.
- Product connection: Provides current context for the importance of tracking raw-material cost conditions.
- Interpretation limit: This survey is not specific to small factories and does not quantify the savings FactoryMargin AI could produce.

## 2. Supplier selection and procurement decision methods

### [3] Supplier Selection Using Fuzzy TOPSIS Multi Criteria Model for a Small Scale Steel Manufacturing Unit

S. Kumar, S. Kumar, and A. G. Barman, *Procedia Computer Science*, vol. 133, pp. 905–912, 2018.

- DOI: https://doi.org/10.1016/j.procs.2018.07.097
- Publisher page: https://www.sciencedirect.com/science/article/pii/S1877050918310500
- Relevance: Applies a multi-criteria supplier-selection method to a small-scale steel manufacturing unit in India.
- Product connection: Informs the supplier-ranking approach. FactoryMargin AI should compare price together with quality, delivery, and other configured criteria, and should expose the weights used in a recommendation.

### [4] An Integrated Fuzzy Multiple Criteria Supplier Selection Approach and Its Application in a Welding Company

S. Sarkar, D. K. Pratihar, and B. Sarkar, *Journal of Manufacturing Systems*, vol. 46, pp. 163–178, 2018.

- DOI: https://doi.org/10.1016/j.jmsy.2017.12.004
- Publisher page: https://www.sciencedirect.com/science/article/abs/pii/S0278612517301607
- Relevance: A manufacturing case study combining quantitative and qualitative supplier-evaluation criteria.
- Product connection: Supports transparent, multi-factor supplier evaluation rather than selecting the lowest quoted unit price without considering delivery and other operational factors.

### [5] A Multi-Agent Architecture for Multi-Product Supplier Selection in Consideration of the Synergy Between Products

C. Yu and T. N. Wong, *International Journal of Production Research*, vol. 53, no. 20, pp. 6059–6082, 2015.

- DOI: https://doi.org/10.1080/00207543.2015.1010745
- Publisher page: https://www.tandfonline.com/doi/full/10.1080/00207543.2015.1010745
- Relevance: Proposes a multi-agent architecture for supplier selection when purchasing multiple products.
- Product connection: Provides background for dividing procurement work into coordinated agents or services. It is a research precedent for multi-agent decision support, not evidence that the proposed LLM agent implementation is already validated.

## 3. Manufacturing cost estimation

### [6] Implementation of TDABC in SME: A Case Study

A. B. Ganorkar, R. R. Lakhe, and K. N. Agrawal, *Journal of Corporate Accounting & Finance*, vol. 29, no. 2, pp. 87–113, 2018.

- DOI: https://doi.org/10.1002/jcaf.22327
- Publisher page: https://onlinelibrary.wiley.com/doi/10.1002/jcaf.22327
- Relevance: Applies time-driven activity-based costing in a small manufacturing business and discusses tracing overheads such as power and machine maintenance to activities and products.
- Product connection: Informs the costing model for labour, machine time, utilities, maintenance, and production overheads.

### [7] Build-Up an Economical Tool for Machining Operations Cost Estimation

F. J. G. Silva, V. F. C. Sousa, A. G. Pinto, L. P. Ferreira, and T. Pereira, *Metals*, vol. 12, no. 7, article 1205, 2022.

- DOI: https://doi.org/10.3390/met12071205
- Open-access article: https://www.mdpi.com/2075-4701/12/7/1205
- Relevance: Presents a cost-estimation tool for machining operations, using machining time and required material quantities; the article specifically discusses the need for accessible cost-estimation tools for manufacturing SMEs.
- Product connection: Supports the idea of a transparent, structured cost model rather than relying on informal rule-of-thumb estimates.

### [8] Cost Estimation System for Machined Parts

D. Ben-Arieh, *International Journal of Production Research*, vol. 38, no. 17, pp. 4481–4494, 2000.

- DOI: https://doi.org/10.1080/00207540050205244
- Publisher page: https://www.tandfonline.com/doi/abs/10.1080/00207540050205244
- Relevance: Describes a hybrid cost-estimation approach combining historical process data with explicit calculations of machining time and cost.
- Product connection: Supports combining historical factory data with explainable calculation rules when estimating the cost of a new order.

## 4. Responsible AI and human oversight

### [9] Artificial Intelligence Risk Management Framework (AI RMF 1.0)

E. Tabassi, National Institute of Standards and Technology, NIST AI 100-1, 2023.

- DOI: https://doi.org/10.6028/NIST.AI.100-1
- Official publication: https://www.nist.gov/publications/artificial-intelligence-risk-management-framework-ai-rmf-10
- Relevance: A voluntary framework for identifying, assessing, and managing risks associated with AI systems.
- Product connection: Informs confidence checks, transparent recommendations, audit trails, human review, and governance around consequential actions.

## 5. How these references map to the product

| FactoryMargin AI capability | Research basis |
|---|---|
| Supplier quote comparison | [1], [3], [4] |
| Multi-criteria supplier ranking | [3], [4] |
| Coordinated procurement agents | [5] |
| Material, labour, machine, and overhead costing | [6], [7], [8] |
| Historical-cost-informed estimation | [8] |
| Current raw-material cost context | [2] |
| Confidence checks, human review, and AI governance | [9] |

## 6. Suggested validation plan

The research is a starting point, not a substitute for field evidence. Before claiming measurable savings, test the prototype with manufacturing units and record:

1. Time taken to compare a typical supplier set before and after using the system.
2. Difference between quoted unit price and total landed cost after freight, taxes, and applicable charges.
3. Difference between estimated and actual production cost for completed orders.
4. Number of missing or incorrect quote fields caught during extraction and review.
5. Number of recommendations accepted, rejected, or edited by the factory owner.

Report sample size, time period, industry segment, assumptions, and limitations with every result. Do not describe synthetic demo data as real factory results.
