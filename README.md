1. Business Objective
Fifty Plus Health is a health-focused startup aiming to provide accurate, accessible, and age-relevant medical information to individuals aged 50 and older. Their core goal is to build a trustworthy platform where users can explore curated medical content and receive real-time answers to health-related queries through an AI-powered assistant. 

The business objective here was to develop a Knowledge Graph for Fifty Plus Health that they can leverage in multiple ways - to power an AI-powered assistant, to write articles and enhance user experience. We hope that the knowledge graph would be able to act like a pseudo medical professional for Fifty Plus Health.

2. Key Actionable Business Initiative
Business Initiatives Considered:
Building a searchable medical knowledge base.
Generating medically accurate articles tailored for a non-technical audience.
Integrating a conversational chatbot that directs users to relevant articles or insights.
Most Impactful Initiative:
Creating an intelligent chatbot powered by a medical knowledge graph to guide users toward relevant articles and answers.
Actionability & Execution:
Integrate PrimeKG-based knowledge graph into a Retrieval-Augmented Generation (RAG) pipeline.
Fine-tune the conversational flow for clarity, empathy, and accuracy.
Continuously expand the graph and article bank based on user queries.

4. Metrics of Success
Key Metrics:
Accuracy of chatbot responses (based on medical relevance)
Coverage of disease-topic mapping (graph completeness)
Hypothesis:
A knowledge graph-based chatbot will improve the accuracy and depth of medical answers by at least 30% compared to standard retrieval approaches and reduce bounce rates by 15% on article pages.

6. Role of Analytics
Enable the Initiative: The graph structure enables better article linkage and chatbot understanding.
Refine the Initiative: Exploratory insights help identify underrepresented diseases or articles.
Evaluate the Initiative: Analysis can measure improvements in chatbot accuracy and coverage.

7. Thinking Through the Analytics
Data
Data Source: PrimeKG open dataset.
Outcome Variable (for future classification tasks): Quality of chatbot recommendation or relevance score.
Features: Graph node types (disease, drug, symptom), edge types (drug-drug, disease-phenotype), connectivity, path lengths, etc.
Variation: Graph topology reveals highly connected nodes (e.g., Quinidine), sparse subgraphs, and underrepresented conditions, useful for both article generation and chatbot development.
Type of Analytics
Exploratory Analytics:
Understand node distribution, common relations, and subgraph connectivity.
Identify high-centrality nodes and coverage gaps.
Predictive Analytics (Future Work):
Predict relevance of responses or missing links in article coverage.
Exploratory Insights
Disease and drug entities are well-represented; however, some target conditions from Fifty Plus Health had limited graph representation. Several conditions initially appeared unmatched due to abbreviations or alternate naming in the JSON file. We manually reviewed and matched many of these to existing nodes in PrimeKG.
List of diseases identified which are not in the PrimeKG dataset:
Node ID
Condition Name
28
Mind Diet
29
DASH Diet
36
Inflammation Diet
51
Ingrown Hair Cyst
213
Corns
277
Stockholm Syndrome
387
Nervous Breakdown

Colab Link (for cross checking diseases not present in PrimeKG dataset)
The most connected node was Quinidine (2600+ links), indicating its central role in the medical network.

6. Executing the Analytics
All components of the project, including data preparation, graph construction, exploratory analysis, and initial application design, were independently executed by the team, under the guidance of the course instructor.
Data Preparation and Integration:
We loaded the Knowledge Graph CSV from the Harvard Dataverse and carefully processed it to generate two separate files, one for nodes (nodes.csv) and one for edges (edges.csv). This required close attention to detail to ensure that each unique entity and relationship was accurately captured.
Analytical Design and Development:
Key analytics tasks such as exploring graph structure, identifying highly connected nodes, comparing disease coverage, and designing potential use cases (e.g., chatbot integration, article generation) were completed internally. These efforts informed the structure of the proposed Retrieval-Augmented Generation (RAG) pipeline.
Collaboration and Roles:
While the project was informed by early discussions with the startup partner to clarify use cases and priorities, technical execution has been limited to the course project context. Potential collaboration with the partner’s technical team may take place in the upcoming internship phase.
Defining Metrics and Evaluation Plans:
Key success metrics were defined based on the stated business objectives and refined through feedback from the course instructor.

7. Implementation
Influenced Decisions:
Identified missing disease nodes and flagged them for content creation.
Used graph substructure to prototype article generation prompts for LLMs.
Designed a prototype RAG architecture to be deployed in the chatbot backend.
Workflow Integration:
Plan to embed graph-query APIs and chatbot into the Fifty Plus Health website.
Article generation pipeline using graph facts is being designed for editorial use.

8. Scale
Challenges:
Data: Incomplete coverage of age-specific conditions.
People: Small engineering team requires robust documentation and handover.
Systems: Hosting and querying a large graph database at scale.
Culture: Non-technical stakeholders need interpretable analytics.
Solutions:
Expand graphs understanding of medical terms with external datasets (e.g., UMLS, SNOMED).
Use cloud-based graph platforms (e.g., Neo4j Aura, AWS Neptune).
Add explainability layers to chatbot outputs (e.g., “This answer is based on…”).
Sustainability Plan:
Ongoing internship will:
Finalize the chatbot MVP.
Build a feedback loop from user queries to content creation.
Iterate on graph enrichment and model refinement.



