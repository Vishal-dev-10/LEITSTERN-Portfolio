# LEITSTERN – Engineering Case Studies

### Practical Software Engineering, AI Integration and Problem Solving

This document presents selected engineering challenges encountered during the independent development of LEITSTERN and the implementation approaches used to address them.

The case studies demonstrate practical experience across full-stack engineering, AI integration, deterministic decision logic, database management, and application reliability.

---

# Case Study 01 – Integrating AI into a Full-Stack Application

## Challenge

Integrating conversational AI into a project-management application introduced several engineering challenges.

A conventional chatbot could generate natural-language responses, but LEITSTERN required something more structured: AI-generated recommendations needed to interact with existing application functionality without allowing unrestricted modifications to project data.

The system needed to connect conversational interaction with backend validation and controlled application operations.

## Engineering Approach

I developed NAVIS as an AI-assisted interaction layer using:

- React.js for the conversational interface.
- Node.js and Express.js for backend request handling.
- n8n for workflow orchestration.
- OpenAI API for AI-generated responses.
- Firebase Firestore for application data management.

The backend communicates with the n8n workflow, which processes the request and returns structured information.

The response architecture includes:

- `reply` – Main conversational response.
- `suggestions` – Suggested follow-up interactions.
- `actions` – Structured action-oriented outputs.

## Solution

Rather than allowing AI-generated text to directly modify project records, I implemented structured action handling.

The application separates recommendation generation from action execution.

The manager reviews the proposed action, examines the available impact information, and confirms or cancels the operation.

The backend then validates the request and executes supported operations.

## Engineering Outcome

This implementation connected AI-generated recommendations with existing application functionality while preserving backend control and managerial decision authority.

It demonstrates practical experience in:

- OpenAI API integration.
- n8n workflow orchestration.
- Backend API development.
- Structured response processing.
- AI-assisted application workflows.
- Human-in-the-loop interaction design.

---

# Case Study 02 – Building Deterministic Project Intelligence

## Challenge

Traditional project dashboards often display information without helping managers understand what operational action might be appropriate.

LEITSTERN needed to analyse project information and identify workload imbalances, financial risks, deadline conditions, and tasks requiring attention.

The challenge was to develop measurable decision-support logic rather than relying entirely on AI-generated interpretations.

## Engineering Approach

I developed interconnected intelligence components using application-defined calculations and business rules.

### Workload Intelligence

The workload engine uses estimated working hours and available capacity to analyse team-member utilisation.

This provides more meaningful workload information than simply counting assigned tasks.

### Cost Intelligence

Task-level financial calculations use:

- Cost per hour.
- Estimated hours.
- Actual hours.
- Estimated cost.
- Actual cost.
- Remaining cost.

### Task Decision Engine

The Task Decision Engine evaluates task conditions and supports managerial actions such as:

- Escalate.
- Fast Track.
- De-scope.
- Pause.

### Resource Reallocation

The resource-reallocation functionality evaluates valid project members using relevant workload and cost information.

Candidate selection is restricted by organisation and project membership.

## Solution

The intelligence components calculate operational information independently of conversational AI.

NAVIS complements these calculations by helping managers interact with the resulting insights through natural-language questions, explanations, and structured recommendations.

## Engineering Outcome

The result is a hybrid AI-assisted decision-support architecture combining deterministic calculations with conversational AI.

This demonstrates practical experience in:

- Algorithmic business logic.
- Data processing.
- Financial calculations.
- Workload analysis.
- Dynamic prioritisation.
- Resource allocation.
- Decision-support software design.

---

# Case Study 03 – Improving Application Reliability Across Multiple Layers

## Challenge

During development, several issues emerged across the frontend, backend, authentication, Firestore database, AI workflows, and dashboard calculations.

Because application features depend on shared data, a change in one area could affect several other modules.

For example, modifying a task assignment could affect workload calculations, cost information, project KPIs, activity logs, and undo functionality.

## Engineering Approach

I used an iterative debugging and manual validation process.

The workflow involved:

1. Reproducing the issue.
2. Identifying the affected application layer.
3. Investigating the relevant implementation.
4. Correcting the underlying logic.
5. Repeating the affected workflow.
6. Checking dependent application information.

## Examples of Engineering Issues Addressed

| Area | Issue addressed |
|---|---|
| Authentication | Token and access-validation issues |
| Firestore | Data consistency and validation issues |
| Workload | Replaced task-count-based logic with estimated-hours-based calculations |
| Cost | Corrected task and project cost recalculation |
| Resource allocation | Restricted candidates to valid organisation and project members |
| Assignment | Corrected member ID and member-name synchronisation |
| Deadline analysis | Corrected Firestore date handling and overdue-task visibility |
| NAVIS | Corrected structured response parsing, suggestions and approval flow |
| Undo | Improved restoration of previous values and dependent calculations |
| Dashboard | Corrected stale KPI and cache-refresh behaviour |
| Reports | Corrected filters, rendering and PDF export behaviour |

## Solution

The fixes involved improving validation, correcting data handling, recalculating dependent metrics, and ensuring that backend operations used current database records.

The undo mechanism was particularly important because restoring a previous task state also required recalculating related workload, cost, progress, and project metrics.

## Engineering Outcome

These improvements strengthened the consistency of the implemented application workflows.

They demonstrate practical experience in:

- Full-stack debugging.
- API troubleshooting.
- Firestore data management.
- Authentication and access validation.
- Cross-module dependency management.
- State restoration.
- Manual functional testing.
- Iterative software maintenance.

---

# Engineering Principles Demonstrated

The three case studies illustrate several engineering principles applied during LEITSTERN development.

| Principle | Application |
|---|---|
| Separation of concerns | Frontend, backend, database and AI responsibilities |
| Structured communication | Defined AI response fields and backend APIs |
| Deterministic logic | Measurable project and financial calculations |
| Human oversight | Manager review before supported operations |
| Data validation | Backend validation and organisation boundaries |
| Reversibility | Undo for supported actions |
| Iterative development | Manual testing, debugging and retesting |
| Technical documentation | Architecture and implementation records |

---

# Validation Boundaries

The documented engineering outcomes are based on implementation experience and manual functional testing.

They should not be interpreted as evidence of complete automated test coverage, formal performance benchmarking, statistically validated AI accuracy, or production-scale reliability.

These remain areas for further development.

---

# Conclusion

LEITSTERN provided an opportunity to work across multiple layers of a modern software application.

From integrating OpenAI through n8n to developing deterministic decision engines and resolving cross-layer application issues, the project demonstrates practical full-stack engineering and problem-solving experience.

It also explores how AI-assisted interaction can be integrated into operational software while retaining deterministic calculations, backend validation, and human decision authority.

---

**Project:** LEITSTERN  
**Developer:** Vishal Thaikkattil Vidyadharan  
**Programme:** Master's in Technical Management  
**University:** Hochschule Emden/Leer, Germany

**Technologies:** React.js · Node.js · Express.js · Firebase · OpenAI API · n8n · JavaScript
