# Medical Knowledge Graph and Conversational AI for Fifty Plus Health

---

##  1. Business Objective

**Fifty Plus Health** is a health-focused startup aiming to provide accurate, accessible, and age-relevant medical information to individuals aged 50 and older. Their core goal is to build a trustworthy platform where users can explore curated medical content and receive real-time answers to health-related queries through an AI-powered assistant.

The business objective here was to develop a **Knowledge Graph** for Fifty Plus Health that they can leverage in multiple ways:
- Power an AI-powered assistant
- Enable article generation
- Enhance user experience

The knowledge graph is intended to act as a **pseudo-medical professional** for Fifty Plus Health.

---

## 2. Key Actionable Business Initiative

### Business Initiatives Considered:
- Building a searchable medical knowledge base
- Generating medically accurate articles tailored for a non-technical audience
- Integrating a conversational chatbot that directs users to relevant articles or insights

### Most Impactful Initiative:
> Creating an intelligent chatbot powered by a medical knowledge graph to guide users toward relevant articles and answers

### Actionability & Execution:
- Integrate **PrimeKG-based** knowledge graph into a **Retrieval-Augmented Generation (RAG)** pipeline
- Fine-tune the conversational flow for clarity, empathy, and accuracy
- Continuously expand the graph and article bank based on user queries

---

##  3. Metrics of Success

**Key Metrics:**
- Accuracy of chatbot responses (based on medical relevance)
- Coverage of disease-topic mapping (graph completeness)

**Hypothesis:**
> A knowledge graph-based chatbot will improve the accuracy and depth of medical answers by at least **30%** compared to standard retrieval approaches and reduce bounce rates by **15%** on article pages.

---

##  4. Role of Analytics

**Enable the Initiative:** Graph structure enables better article linkage and chatbot understanding  
**Refine the Initiative:** Exploratory insights help identify underrepresented diseases or articles  
**Evaluate the Initiative:** Analysis can measure improvements in chatbot accuracy and coverage

---

## 5. Thinking Through the Analytics

### **Data**
- **Data Source:** PrimeKG open dataset
- **Outcome Variable:** Quality of chatbot recommendation or relevance score
- **Features:** Node types (disease, drug, symptom), edge types (drug-drug, disease-phenotype), connectivity, path lengths, etc.

### **Variation**
Graph topology reveals highly connected nodes (e.g., Quinidine), sparse subgraphs, and underrepresented conditions, useful for both article generation and chatbot development.

### **Exploratory Insights**
- Disease and drug entities are well-represented
- Some target conditions had limited graph representation due to alternate naming or abbreviation issues
- Manual review and matching resolved some gaps

#### List of diseases not found in PrimeKG:

| Node ID | Condition Name       |
|---------|----------------------|
| 28      | Mind Diet            |
| 29      | DASH Diet            |
| 36      | Inflammation Diet    |
| 51      | Ingrown Hair Cyst    |
| 213     | Corns                |
| 277     | Stockholm Syndrome   |
| 387     | Nervous Breakdown    |

> **Most connected node:** Quinidine (2600+ links), indicating centrality in the network.

---

##  6. Executing the Analytics

### Data Preparation & Integration
We loaded the Knowledge Graph CSV from the **Harvard Dataverse** and carefully processed it to generate two separate files:
- `nodes.csv`
- `edges.csv`

This required close attention to detail to ensure that each unique entity and relationship was accurately captured.

### Analytical Design & Development
- Explored graph structure
- Identified highly connected nodes
- Compared disease coverage
- Designed potential use cases (chatbot integration, article generation)

### Collaboration and Roles
- Use cases and priorities were clarified with the startup partner
- Technical execution was handled as a course project
- Internship phase may involve deeper collaboration with the partner's team

### Defining Metrics and Evaluation Plans
Key success metrics were defined based on business objectives and refined through instructor feedback.

---

##  7. Implementation

### Influenced Decisions
- Identified and flagged missing diseases for new content
- Used graph substructures to generate prompts for article writing
- Prototyped RAG architecture for backend chatbot deployment

### Workflow Integration Plan
- Embed graph-query APIs and chatbot into the Fifty Plus Health website
- Develop article generation pipeline using graph facts

---

##  8. Scale

### Challenges & Solutions

| Challenge                              | Solution                                                  |
|----------------------------------------|-----------------------------------------------------------|
| Incomplete coverage of age-specific conditions | Expand with UMLS, SNOMED, and other datasets             |
| Small engineering team                 | Ensure robust documentation and handover                 |
| Graph hosting/querying at scale        | Use Neo4j Aura or AWS Neptune                            |
| Non-technical stakeholder access       | Add explainability layers to chatbot outputs             |



---

##  Appendix

### Deliverables Completed
- Graph ingestion and construction from PrimeKG
- Exploratory analysis on node/edge distributions
- Disease coverage matching with Fifty Plus Health content
- Subgraph visualization and entity-level statistics


