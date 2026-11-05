# Information Systems: Course Notes

A structured summary of the core units covering systems concepts, information systems in organizations, decision support, knowledge management, systems development, and IT management.

---

## Table of Contents

1. [System Concepts](#1-system-concepts)
2. [Organizational Efficiency and Effectiveness](#2-organizational-efficiency-and-effectiveness)
3. [Why Do We Need Information Systems?](#3-why-do-we-need-information-systems)
4. [How IS Reshapes Organizations](#4-how-is-reshapes-organizations)
5. [Six Major Types of Systems](#5-six-major-types-of-systems)
6. [Relationship of Systems: Integration](#6-relationship-of-systems-integration)
7. [Online Analytical Processing (OLAP)](#7-online-analytical-processing-olap)
8. [Data Mining](#8-data-mining)
9. [Enhancing Management Decision-Making with DSS](#9-enhancing-management-decision-making-with-dss)
10. [Group Decision Support Systems (GDSS)](#10-group-decision-support-systems-gdss)
11. [Knowledge Management in the Organisation](#11-knowledge-management-in-the-organisation)
12. [Information and Knowledge Work Systems](#12-information-and-knowledge-work-systems)
13. [Distributing Knowledge: Office Automation Systems](#13-distributing-knowledge-office-automation-systems)
14. [Examples of Knowledge Work Systems](#14-examples-of-knowledge-work-systems)
15. [Capturing Knowledge: Expert Systems](#15-capturing-knowledge-expert-systems)
16. [Other Intelligent Techniques](#16-other-intelligent-techniques)
17. [The Traditional Systems Development Life Cycle (SDLC)](#17-the-traditional-systems-development-life-cycle-sdlc)
18. [Alternative System-Building Approaches](#18-alternative-system-building-approaches)
19. [Managing Information Technology](#19-managing-information-technology)
20. [Business/IT Planning](#20-businessit-planning)
21. [Managing the IS Function](#21-managing-the-is-function)
22. [Failures in IT Management](#22-failures-in-it-management)

---

## 1. System Concepts

The unit introduces you to what a system is and how to think in systems — a way of viewing the world as interconnected parts working together, rather than as isolated pieces.

---

## 2. Organizational Efficiency and Effectiveness

Two key performance measures:

- **Efficiency:** Doing things right — getting the most output from the least input (resource use).
- **Effectiveness:** Doing the right things — actually achieving the organization's goals.

---

## 3. Why Do We Need Information Systems?

The motivations/drivers. Typically:

- To survive and compete in a changing business environment
- To process and manage information at scale (too much data for humans alone)
- To support decision-making at all levels (operational, tactical, strategic)
- To improve efficiency, coordination, and communication
- Legal/regulatory compliance and customer expectations
- Competitive advantage — doing things faster, cheaper, better than rivals

---

## 4. How IS Reshapes Organizations

How IS reshapes how organizations are structured and operate. Examples:

- **Flattening hierarchies** — fewer middle managers, because information flows directly
- **Decentralization** — decisions pushed to where the information is
- **Flexible/networked structures** — teams, virtual organizations, remote work
- **Faster communication & coordination** across departments and geographies
- **New business models** — e-commerce, platforms, outsourcing, global operations
- **Data-driven management** — decisions based on analytics rather than intuition

---

## 5. Six Major Types of Systems

| System | Serves | Main Purpose |
|---|---|---|
| Transaction Processing System (TPS) | Operational staff / supervisors | Records daily routine transactions (sales, payroll, orders) |
| Office Automation System (OAS) / Office Information System | Clerical / data workers | Manages documents, scheduling, communication (word processing, email, calendars) |
| Knowledge Work System (KWS) | Professionals / technical staff | Creates new knowledge (engineering design, scientific modeling) |
| Management Information System (MIS) | Middle managers | Produces summary and exception reports from TPS data to monitor operations |
| Decision Support System (DSS) | Managers / professionals | Supports non-routine decisions with models, analysis, "what-if" scenarios |
| Executive Support System (ESS) | Top / strategic managers | Provides high-level summaries and external data for strategic decisions |

> **Key point:** TPS sits at the base and is a major producer of data for all the other systems above it.

---

## 6. Relationship of Systems: Integration

- **TPS → MIS:** TPS captures raw transaction data; MIS summarizes and reports on it.
- **TPS/MIS → DSS:** DSS pulls detailed data and adds analytical models for complex decisions.
- **All lower systems → ESS:** ESS aggregates internal data from TPS/MIS/DSS plus external data for executives.
- **Data flows upward:** from detailed, routine transactions to summarized, strategic insight.
- **Integration** also means systems share databases and feed each other, rather than duplicating data entry.

---

## 7. Online Analytical Processing (OLAP)

OLAP is an architecture that allows users to perform **dynamic, multidimensional analysis** of data from data warehouses. It places the analyst in direct contact with the data, enabling them to view information from different perspectives (dimensions) and perform actions like:

- **Drill-down:** Moving from summarized data to detailed data.
- **Roll-up:** Aggregating detailed data into summaries.
- **Slice and Dice:** Viewing the data cube from different angles to find patterns.

---

## 8. Data Mining

Data mining (or Knowledge Discovery) is the process of automatically searching large databases for **hidden patterns, correlations, and rules** that are not obvious through traditional querying. Common techniques include:

- **Predictive Modeling:** Using historical data to predict future behavior (e.g., credit risk, response to marketing).
- **Clustering/Segmentation:** Grouping customers with similar characteristics to target them effectively.
- **Association Rules:** Discovering what items are frequently purchased together (e.g., market basket analysis).

---

## 9. Enhancing Management Decision-Making with DSS

DSS enhances decision-making by providing specific analytical capabilities that support the manager's judgment:

- **What-If Analysis:** Assessing the impact of changing a variable (e.g., "What if we increase the advertising budget by 30%?").
- **Sensitivity Analysis:** Analyzing how changes in multiple variables affect the outcome.
- **Goal Seeking:** Determining the input required to achieve a desired goal (e.g., "What price do we need to achieve a 20% ROI?").
- **Risk Analysis:** Evaluating the probability of different outcomes to assess risk.

These tools help managers at all levels — operational, tactical, and strategic — by turning raw data into actionable information.

---

## 10. Group Decision Support Systems (GDSS)

A **GDSS** is an interactive, computer-based system that facilitates the solution of unstructured problems by a **group of decision-makers**. It combines communication, computing, and decision support technologies to improve the process and outcomes of group meetings.

Key features and components include:

- **Anonymity:** Allowing participants to contribute ideas or votes without fear of criticism, reducing groupthink.
- **Parallel Communication:** Enabling all participants to input ideas simultaneously via their terminals, speeding up brainstorming.
- **Process Structuring:** Tools for organizing ideas, voting, and building consensus (e.g., electronic brainstorming, weighted voting).
- **Facilitation:** Often includes a facilitator to manage the technology and guide the group process.
- **Settings:** Can be used in a **Decision Room** (face-to-face with networked computers) or for dispersed groups via networks.

The goal of a GDSS is to improve the **efficiency** (faster meetings) and **effectiveness** (better quality decisions) of group work by removing common barriers like dominant personalities or lack of focus.

---

## 11. Knowledge Management in the Organisation

**Knowledge Management (KM)** is the discipline of creating a work environment that fosters the continuous creation, sharing, and reuse of organizational and personal knowledge to create business value. In the modern economy, knowledge has become a critical factor of production alongside labor, land, and capital. Effective KM helps organizations reduce repetitive efforts, improve decision-making, increase efficiency, and gain competitive advantage. The goal is to leverage the collective **"intellectual capital"** of employees — their insights, know-how, and practical understanding — rather than relying solely on physical assets.

---

## 12. Information and Knowledge Work Systems

These systems serve different groups of workers. **Information work systems** (often Office Automation) support clerical and data workers who handle and disseminate information. **Knowledge work systems (KWS)** support professionals and technical staff whose primary job is to create *new* knowledge and information. KWS require powerful graphics, analytical tools, and document management capabilities to aid in tasks like engineering design or scientific modeling.

---

## 13. Distributing Knowledge: Office Automation Systems

**Office Automation Systems (OAS)** are designed to distribute and coordinate information across the organization. They handle the "information work" that keeps a business running — tasks like word processing, email, scheduling, document management, and internal communication. Their role in Knowledge Management is to ensure that **explicit knowledge** (documented information) flows efficiently to the people who need it.

---

## 14. Examples of Knowledge Work Systems

These are specialized tools for professionals who create new knowledge:

- **Computer-aided design (CAD):** Used by engineers and architects to create, modify, and analyze designs digitally, replacing traditional drafting tables.
- **Virtual reality systems:** Used for simulation and visualization, such as flight simulators for training or virtual prototypes for design review.
- **Artificial Intelligence:** A broad field of technologies (discussed further below) that can be integrated into KWS to automate analysis, generate insights, or assist with complex problem-solving.

---

## 15. Capturing Knowledge: Expert Systems

An **Expert System** is a type of AI designed to capture and replicate the decision-making ability of a human expert in a narrow, specific domain. It typically consists of a **knowledge base** (containing rules and facts extracted from human experts) and an **inference engine** (which applies those rules to new problems). These systems are valuable when expertise is scarce, the task is hazardous, or decisions require consistent application of complex rules. However, they are expensive to build and maintain, and are limited to narrow problem areas.

---

## 16. Other Intelligent Techniques

This section covers broader AI techniques that support knowledge work and decision-making:

- **Neural Networks:** Computing systems inspired by biological brains that "learn" by analyzing patterns in large datasets. They are used for tasks like predictive modeling, pattern recognition, and classification.
- **Robotics & Vision Systems:** Physical robots combined with computer vision allow machines to perceive and interact with the physical world, used in manufacturing, warehousing, and inspection.
- **Natural Language Processing (NLP):** Technology that enables computers to understand, interpret, and generate human language. This powers applications like chatbots, sentiment analysis, and document summarization.
- **Learning Systems:** Systems that improve their performance over time by learning from data or experience, a core capability of modern AI that allows knowledge systems to adapt and become more useful without manual reprogramming.

---

## 17. The Traditional Systems Development Life Cycle (SDLC)

The SDLC is a formal, sequential, activity-driven process for building systems. It is often called the **"waterfall"** model because each phase must be completed and heavily documented before the next begins, and different teams typically handle each phase.

A common breakdown of phases is:

1. **Definition:** Identifying the problem or need.
2. **Analysis:** Studying the existing system and defining requirements.
3. **Design:** Creating the technical blueprint (logical and physical).
4. **Construction:** Writing the code and building the system.
5. **Test:** Verifying that the system works as intended.
6. **Transition/Migration:** Moving from the old system to the new one.
7. **Production:** The system is live and maintained.

A major criticism of the traditional SDLC is that requirements are often **"frozen"** after the design is approved. This is inefficient for users because if the business environment changes, the system can become outdated before it is even finished.

---

## 18. Alternative System-Building Approaches

Because the traditional SDLC can be slow and rigid, several alternatives exist to reduce risk and better match user needs.

### Prototyping

Prototyping is based on the idea that users find it easier to point out what they dislike about a working model than to describe what they want in an abstract specification. The developer builds a rough, working version of the system (a prototype), shows it to the user, and refines it based on feedback in an iterative loop. This approach generally leads to **higher user satisfaction** and can **lower design costs** by reducing the time spent on abstract analysis and design.

### Application Software Packages

Instead of building everything from scratch, organizations can buy pre-written software for common functions. Examples include financial accounting packages (accounts receivable, general ledger) or payroll systems. The main attraction is **speed and cost**: the software already exists and is tested. However, the organization may have to adapt its business processes to fit the package, and it may pay ongoing licensing fees.

### End-User Development (EUD)

EUD is when the people who will actually use the system build or customize it themselves, often using tools like spreadsheets, report generators, or simple scripting, **without needing professional programmers**. It empowers users and can be fast. The downside is that it creates **management challenges**: ensuring quality, preventing errors, and maintaining the software when the original user leaves or the spreadsheet becomes too complex.

### Outsourcing

Outsourcing is contracting an external vendor to develop, run, or manage the information system. The promised benefits include access to **skilled expertise** the organization lacks internally, **reduced risk of technological obsolescence**, and potentially lower costs. The risks are significant, though: **loss of control** over quality and timelines, **security and confidentiality concerns**, and the difficulty of retaining critical internal knowledge.

---

## 19. Managing Information Technology

This is about treating IT as a **strategic organizational resource** rather than a technical back-office function. It involves:

- **Resource stewardship:** Managing hardware, software, networks, data, and people as shared enterprise assets.
- **Alignment:** Ensuring IT strategy is integrated with and driven by business strategy, not the reverse.
- **Governance:** Establishing authority patterns and decision rights for key IT activities — infrastructure, IT use, and project management.

---

## 20. Business/IT Planning

This is the formal process of deciding **where IT should go and how it gets there**. A sound IT strategic plan typically rests on three building blocks:

1. **IT assessment:** Identifying current issues, problems, and requirements.
2. **Business/IT alignment:** Understanding business drivers, management expectations, and customer requirements so technology solutions serve real business needs.
3. **Initiatives planning:** Formulating and prioritizing projects, since requirements will exceed available resources.

The plan must be a **living document** — updated as business conditions change — not a binder that sits on a shelf.

---

## 21. Managing the IS Function

The IS function (often an IS department or IT unit) has a role that has become increasingly **managerial** rather than purely technical. Key responsibilities include:

- **Service delivery and support:** Running help desks, managing infrastructure, ensuring uptime.
- **Vendor and contract management:** Overseeing outsourcing relationships, licenses, and procurement.
- **Security and risk:** Protecting data privacy, integrity, and business continuity.
- **Steering committees:** Facilitating cooperation between the IS department and end users, resolving conflicts, and setting priorities.
- **Budget and human resources:** Managing the IT budget, staffing, and skills development.

---

## 22. Failures in IT Management

IT projects fail at notoriously high rates, and the causes are rarely purely technical. Research on project failures consistently points to **management and organizational factors** as the top reasons:

| Rank | Cause of IT Problems |
|---|---|
| 1 | Lack of top management commitment |
| 2 | Failure to gain user commitment |
| 3 | Misunderstanding requirements |
| 4 | Lack of user involvement |
| 5 | Failure to manage end-user expectations |
| 6 | Changing scope and objectives |
| 7 | Lack of required knowledge and skills in the team |

Beyond these, poor **project management** (unrealistic estimates, weak change control, poor communication) and **technological immaturity** also contribute. The Australian case studies of Sydney Water, RMIT, and One.Tel illustrate how **governance failures** — senior management disengagement and lack of oversight — turned costly projects into organizational crises.