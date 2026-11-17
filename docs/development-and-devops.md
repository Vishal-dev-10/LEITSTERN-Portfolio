# LEITSTERN – Development Workflow & DevOps

### Software Engineering Practices, Agile Project Management and Application Deployment

## 1. Overview

LEITSTERN is independently developed using an iterative software engineering approach covering application development, project planning, version control, deployment, debugging, and technical documentation.

The development process combines Agile project management practices with modern full-stack development technologies.

The objective is to maintain a structured development workflow while continuously improving application functionality, reliability, and maintainability.

---

## 2. Development Technology Stack

| Area | Technology |
|---|---|
| Frontend Development | React.js, JavaScript |
| Backend Development | Node.js, Express.js |
| Database | Firebase Cloud Firestore |
| Authentication | Firebase Authentication |
| Version Control | Git, GitHub |
| Project Management | Azure DevOps |
| Deployment | Render |
| CI/CD Workflow Development | Azure DevOps Pipelines |
| Development Environment | Visual Studio Code |

---

## 3. Version Control and Repository Management

Git and GitHub are used for source-code version control and development management.

The development workflow includes:

- Maintaining separate frontend and backend repositories.
- Managing development branches.
- Tracking implementation changes through commits.
- Integrating feature development through Git workflows.
- Maintaining project documentation.
- Managing configuration and deployment files.

Version control provides a history of development changes and supports more structured software maintenance.

---

## 4. Agile Project Management

Azure DevOps Boards was used to organise and structure the development of LEITSTERN.

The development backlog was organised using an Agile hierarchy.

### Work Item Structure

| Level | Purpose |
|---|---|
| Epic | Major development objectives |
| Feature | Functional areas within an objective |
| User Story | User-oriented requirements |
| Task | Individual implementation activities |

### Development Activities

- Requirements breakdown.
- Feature planning.
- User-story creation.
- Sprint organisation.
- Task estimation.
- Progress tracking.
- Development prioritisation.
- Iterative implementation.

This approach helped organise the development of the platform into manageable work packages.

---

## 5. CI/CD and Deployment Workflow

LEITSTERN includes deployment workflow development using Azure DevOps pipeline configuration.

The development involved working with pipeline YAML, deployment configuration, build environments, and troubleshooting deployment-related issues.

The deployment process was developed iteratively, with configuration and hosting challenges addressed during implementation.

### Deployment Architecture

```text
       SOURCE CODE
            |
            v
          GITHUB
            |
            v
     BUILD / DEPLOYMENT
       CONFIGURATION
            |
       +----+----+
       |         |
       v         v
   FRONTEND   BACKEND
   DEPLOYMENT DEPLOYMENT
       |         |
       v         v
     RENDER    RENDER
       |         |
       +----+----+
            |
            v
     LIVE APPLICATION
```

The frontend and backend are deployed as separate application services.

Deployment configurations and workflows have undergone iterative development and troubleshooting.

---

## 6. Application Hosting

The LEITSTERN application is deployed using Render.

### Live Application

Frontend:

https://leistern-frontend.onrender.com

The frontend communicates with the backend through application APIs.

The deployment provides an accessible environment for demonstrating the implemented application interfaces and functionality.

NAVIS is currently undergoing further development and stabilisation.

---

## 7. Debugging and Application Maintenance

Development involved identifying, investigating, and resolving issues across multiple application layers.

### Frontend

- React component behaviour.
- Application state management.
- API response handling.
- Dashboard rendering.
- Navigation and user-interface issues.

### Backend

- Express API request handling.
- Authentication and token validation.
- Request and response processing.
- Business-logic corrections.
- Backend integration issues.

### Database

- Firestore data consistency.
- Organisation-based data separation.
- Document updates.
- Data validation.
- Dependent metric recalculation.

### AI Integration

- n8n webhook communication.
- OpenAI response processing.
- Structured response parsing.
- Suggestions and action rendering.
- Action approval and execution workflows.

---

## 8. Functional Testing and Iterative Validation

The primary development validation approach involved manual functional testing.

The process followed an iterative cycle:

1. Implement a feature.
2. Run the application.
3. Exercise the relevant workflow.
4. Observe the application behaviour.
5. Identify unexpected results.
6. Investigate the underlying issue.
7. Correct the implementation.
8. Repeat the workflow to verify the correction.

### Examples of Tested Areas

- Authentication.
- Project and task management.
- Task assignments.
- Workload calculations.
- Cost and budget calculations.
- Deadline analysis.
- NAVIS request processing.
- Structured action handling.
- Manager approval.
- Firestore updates.
- Undo functionality.
- Dashboard refresh.
- Reporting and PDF export.

Formal automated testing, comprehensive performance benchmarking, and security penetration testing are not established as completed validation activities.

---

## 9. Technical Documentation

Technical documentation is maintained to support development continuity and system understanding.

Documentation areas include:

- System architecture.
- Application modules.
- Backend responsibilities.
- Database structure.
- NAVIS architecture.
- Decision-engine functionality.
- Development limitations.
- Implementation and future-development priorities.

This documentation supports maintainability and provides a reference for future development.

---

## 10. Engineering Challenges and Problem Solving

The development process involved resolving issues across frontend, backend, database, AI integration, and deployment.

Examples include:

| Area | Engineering Challenge |
|---|---|
| Authentication | Token and access-validation issues |
| Firestore | Data consistency and query-related issues |
| API Integration | Request and response handling |
| Workload | Improving effort-based workload calculations |
| Cost Intelligence | Correcting cost recalculation |
| Resource Allocation | Restricting reassignment candidates |
| NAVIS | Structured response parsing and action handling |
| Undo | Restoring previous values and dependent metrics |
| Dashboard | Correcting stale KPI and cache-refresh behaviour |
| Deployment | Pipeline configuration and hosting troubleshooting |

These experiences strengthened practical understanding of debugging, system integration, and iterative software development.

---

## 11. Current Development Status

LEITSTERN is a functioning thesis-stage software implementation that has undergone substantial feature development, debugging, and manual verification.

Its current development maturity should be distinguished from a fully operational enterprise platform.

Areas identified for further improvement include:

- Automated unit and integration testing.
- Regression testing.
- Performance and load evaluation.
- Application monitoring.
- Structured error logging.
- AI response-quality evaluation.
- Deployment and operational reliability.
- Backup and recovery planning.

These improvements form part of the platform's future development roadmap.

---

## 12. Engineering Skills Demonstrated

The development of LEITSTERN demonstrates practical experience in:

- Full-stack application development.
- Git-based version control.
- Agile project management.
- Azure DevOps Boards.
- CI/CD configuration.
- Cloud application deployment.
- REST API development.
- Firebase integration.
- Application debugging.
- Manual functional testing.
- Technical documentation.
- Iterative software engineering.

---

## 13. Conclusion

The development of LEITSTERN demonstrates an integrated software engineering workflow extending from requirements planning and application development to deployment, debugging, and maintenance.

Combining React.js, Node.js, Express.js, Firebase, AI integration, GitHub, Azure DevOps, and cloud hosting provided practical experience in developing and maintaining a full-stack application.

The project represents an ongoing engineering effort focused on building a structured, intelligent, and maintainable software platform.

---

**Project:** LEITSTERN  
**Developer:** Vishal Thaikkattil Vidyadharan  
**Programme:** Master's in Technical Management  
**University:** Hochschule Emden/Leer, Germany

**Live Application:** https://leistern-frontend.onrender.com

**GitHub Portfolio:** https://github.com/Vishal-dev-10/LEITSTERN-Portfolio
