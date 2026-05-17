### Project Jorgan: Final Report

#### 1\. Project Definition and Mission Overview

Project Jorgan represents a strategic architectural transition from cloud dependencies to a sovereign, open-source personal server infrastructure. The mission is to establish a viable alternative to the Google Cloud ecosystem—specifically Google Photos, Google Docs, and hosting services—by deploying a localized, high-availability hardware stack.The primary objective is to facilitate remote data access and manipulation while ensuring the user retains absolute data sovereignty. By abstracting the latency and complexities of remote infrastructure, Project Jorgan provides a seamless user experience that rivals commercial providers without the associated privacy compromises or recurring subscription fees for storage exceeding 10GB. This project asserts that data ownership is a technical right, achieved through the rigorous implementation of open-source protocols on dedicated hardware.

#### 2\. Project Management Strategy: Agile and Methodology

The deployment was governed by an Agile/Scrum framework, optimized for a two-person development team. Development cycles were structured into iterative sprints of two to four weeks, allowing for rapid prototyping and the continuous integration of sub-functionalities.

##### Positive Patterns and Strategic Catalysis

To maximize the productivity of a lean team, two core patterns were adopted:

* **Subgoals Setting:**  High-level milestones from the Project Charter were decomposed into concrete technical tasks (e.g., DNS record configuration and SSL certificate acquisition via Cloudflare) to eliminate architectural drift.  
* **Problem Solving:**  A "zero-blocker" policy was enforced. If a team member remained stalled on a technical impediment (such as MariaDB permission conflicts) for over two hours, a collaborative debugging session was initiated. This prevented the 50% productivity loss inherent in single-point-of-failure stalls within two-person teams.

##### Mitigation of Management Antipatterns

The project strictly avoided several high-risk management behaviors:

* **Neglecting Human Factors:**  Given the small size of team, daily check-ins were used to monitor burnout and academic stress.  
* **Avoidance of Infantilization:**  Equal technical ownership was maintained to prevent the "hovering manager" syndrome. Technical domains (e.g., networking vs. UI) were respected to maintain high morale and individual accountability.

#### 3\. Stakeholder Analysis

The following table analyzes a few internal and external stakeholders, identifying potential conflicts and the team's responses to them.

| Stakeholder | Status | Interest | Potential Conflicts | Mitigation Strategy/Team Response |
| --- | --- | --- | --- | --- |
|**Dev Team** | **Positive** |  Successful delivery of a private cloud for personal utility and potential commercialization. | Internal conflicts among team members | Implementation of Scrum methodology. |
| **Google LLC** | **Negative** |   Both Google and our company offer similar services, competing for the same customers. | Users prefering Google's *'free'* services, not caring about their data being proccessed by AI | Fulfillment of user requirements through architecture, focusing on data control. |
| **Government** | **Neutral** |  Ensuring strict compliance with data privacy regulations and regional laws. | Non-compliance with legal frameworks regarding sovereign data handling. | Deployment of a compliance framework including periodic audits by an external organization. |
| **Students** | **Positive** |  Access to high-performance, private cloud storage and application hosting. | Price sensitivity - desire/need for free services. | Implementation of a tiers: a free Basic tier and a €5/month Premium tier. |
| **University** | **Neutral** |  Fulfillment of student needs with minimal resource expenditure. | Budgetary constraints regarding resource allocation for student services. | Proposing a contractual partnership where the University subsidizes student access tiers. |

#### 4\. User Stories and Personas

Three persona profiles were synthesized to validate the projects versatility across varying technical competencies, as well as user needs.

##### Persona Summaries

* **Andrew (The Photographer):**  A 24-year-old student/professional (Tech Level: 7/10). He seeks to mitigate the escalating costs of proprietary storage for his expanding high-resolution media library. Project Jorgan provides a cost-effective hosting solution for his portfolio and media assets.  
* **Brad (The Clerk):**  A 52-year-old retired clerk (Tech Level: 4/10). He manages critical family documentation and maintains a high distrust of third-party data processors. Project Jorgan serves as a secure digital archive, replacing his reliance on physical archival storage (paper boxes).  
* **Christy (The Programmer):**  A 22-year-old CS student (Tech Level: 9/10). She requires a flexible, isolated virtual environment for deploying Unity backends and React frontends. Project Jorgan offers a customizable hosting platform without the constraints of commercial providers.

##### User Stories and Acceptance Criteria

* **Andrew (Photographer)**  
* **User Story I:**  As a photographer, I want to upload and share my high-resolution assets to preserve storage on my local devices.  
* **Acceptance Criteria:**  Successful multi-file upload; gallery view confirmation; time-limited sharing link generation.  
* **User Story II:**  As a photographer, I want to host a public portfolio to market my professional services.  
* **Acceptance Criteria:**  24/7 public availability; integrated sales interface; low-latency image rendering.  
* **Brad (Clerk)**  
* **User Story I:**  As a family archivist, I want to digitize and organize documentation for secure, location-independent access.  
* **Acceptance Criteria:**  Successful PDF/scan upload; intuitive folder hierarchy; storage confirmation notifications.  
* **User Story II:**  As a family archivist, I want to share specific documents with family members for collaborative management.  
* **Acceptance Criteria:**  Granular permission control (Viewer vs. Editor); link-based sharing; access revocation capability.  
* **Christy (Programmer)**  
* **User Story I:**  As a developer, I require a remote Linux environment to practice network configuration and server management.  
* **Acceptance Criteria:**  High-security SSH access; full UNIX terminal capability; environment isolation (virtualization).  
* **User Story II:**  As a developer, I need to host full-stack applications (React/Node.js) and Unity multiplayer backends.  
* **Acceptance Criteria:**  Persistent background process hosting; support for various runtime environments; public DNS routing.

#### 5\. Market Hypothesis and User Validation

The viability of Project Jorgan was tested through qualitative interviews with five Computer Science students.

* **Interrogative Findings:**  100% of participants currently utilize cloud solutions, yet 80% expressed significant concern regarding data ownership.  
* **The Car Metaphor (Ownership vs. Convenience):**  When contrasted between Option A (Renting/Convenience) and Option B (Owning/Sovereignty), 80% of participants selected Option B. This validates a market shift toward ownership, provided the maintenance barrier is sufficiently lowered.  
* **Financial Feasibility:**  Validation testing indicated a user willingness to pay between €3 and €10 for hosting. With the project's internal ROI model reflecting a monthly saving of €8.40 compared to commercial rates, the financial hypothesis is confirmed as viable.

#### 6\. Technical Specifications: Hardware and Software considrations

The system architecture was designed to last, prioritizing longevity through while keeping the scale and cost at low.

##### Hardware Architectural Decisions

While the  **Zima Board**  was considered for its raw power, the  **Raspberry Pi 5**  was eventually selected as the primary compute module due to its superior ecosystem support, documentation, and somewhate better thermal efficiency.

* **Compute:**  Raspberry Pi 5 (8GB LPDDR4X, 2.4GHz Quad-core ARM Cortex-A76).  
* **Storage Logic:**  Samsung T7 2TB Portable SSD. A USB-C interface was prioritized over PCIe for better "salvageability". In the event of project decommissioning, the SSD remains a high-value portable asset, mitigating the risk of the €270 capital expenditure.

##### Financial Investment Breakdown

* Raspberry Pi 5 (8GB): €130  
* Samsung T7 2TB SSD: €270  
* Supporting Components (32GB OS Boot SSD, EU Power Supply, Active Cooler): €50  
* **Total Hardware Cost/Initial Investment**: €450**

##### Software Stack

The infrastructure utilizes a 100% open-source stack:

* **CasaOS:**  Primary orchestration layer and file management.  
* **Cloudflare:**  DNS management and secure tunnel networking.  
* **Immich:**  High-performance media management (Google Photos alternative).  
* **VS Code Server:**  Remote browser-based Integrated Development Environment (IDE).  
* **MariaDB & PhpMyAdmin:**  Relational database management and GUI.

##### Maintenance and ROI Analysis - Quick and Dirty Maths

Operating at a 5W average load, the annual electrical cost is estimated at €10, supplemented by a €10/year domain registration fee.

* **Annual Maintenance:**  €20  
* **Monthly Operating Expense (OPEX):**  €1.60  
* **Commercial Benchmark (Google 2TB):**  €10.00/month  
* **Monthly Delta (Savings):**  €8.40  
* **Break-even Point (ROI):**  53.57 months (\~4.5 years).

#### 7\. Design Evolution and Physical Prototyping

The physical enclosure underwent three iterative phases.
![All_prototypes](/Implemenatation/Prototypes/images/All_prototypes.jpg)

* **Prototype I (Conceptual):**  Initial component orientation in a plastic container. This phase identified a spatial conflict; from this prototype onwards a USB-C extender was required to align all interfaces onto a single geometric plane for easier external access.
![Prototype1_1](/Implemenatation/Prototypes/images/Prototype1_1.jpg)

* **Prototype II (Structural):**  A Fusion360 model printed on a  **Stratasys PolyJet Objet 260 CONNEX 3**  industrial printer. This iteration introduced floor offsets to facilitate passive airflow. However, dimension inaccuracies (shown on third picture) forced the development to transition from "googled" specs to actual manual caliper measurements.
![Prototype2_1](/Implemenatation/Prototypes/images/Prototype2_1.jpg)
![Prototype2_2](/Implemenatation/Prototypes/images/Prototype2_2.jpg)
![Prototype2_3](/Implemenatation/Prototypes/images/Prototype2_3.jpg)

* **Prototype III (Final):**  A so called "precision-engineered" print resulting in spot-on components residency. This final version incorporates a  **mesh fan cover** (not shown in the pictures) in order to increase airflow while reducing dust collection, allowing for 24/7 uptime. The unit is now in permanent residency under the primary workstation, integrated with cable management for power and networking.

![Prototype3_1](/Implemenatation/Prototypes/images/Prototype3_1.jpg)
![Prototype3_2](/Implemenatation/Prototypes/images/Prototype3_2.jpg)
![Prototype3_3](/Implemenatation/Prototypes/images/Prototype3_3.jpg)
![Prototype3_4](/Implemenatation/Prototypes/images/Prototype3_4.jpg)

#### 8\. SOFTWARE PROTOTYPES IMPLEMENTATION
The software implementation involved deploying a suite of containerized applications through the CasaOS orchestration layer to provide a comprehensive personal cloud experience.
Centralized Administration (CasaOS): The "home" interface was implemented to allow unified access to files, system metrics, and the SSH terminal. 
![CasaOs_Home](/Implemenatation/Prototypes/images/CasaOS.png)
![CasaOs_Files](/Implemenatation/Prototypes/images/Files.png)
![CasaOs_SSH](/Implemenatation/Prototypes/images/SSH.png)
Media Hosting (Immich): A high-performance media server was deployed to handle image storage and browsing, offering features comparable to proprietary photo clouds. [image]
![Immich](/Implemenatation/Prototypes/images/Immich.png)
Development and Hosting Services: The prototype includes a remote VS Code instance for on-server development and MariaDB for database management, enabling the hosting of up to three low-traffic websites. [image]
![VsCode](/Implemenatation/Prototypes/images/Vscode.png)
![PhpMyAdmin](/Implemenatation/Prototypes/images/PhpMyAdmin.png)
Networking Architecture: Global access was achieved using Cloudflare to manage DNS and tunnels, abstracting complex networking hurdles for the user.



#### 9\. Implementation Roadmap and Milestones
The software implementation involved deploying a suite of containerized applications through the CasaOS orchestration layer to provide a comprehensive personal cloud experience.
Centralized Administration (CasaOS): The "home" interface was implemented to allow unified access to files, system metrics, and the SSH terminal.

Media Hosting (Immich): A high-performance media server was deployed to handle image storage and browsing, offering features comparable to proprietary photo clouds.

Development and Hosting Services: The prototype includes a remote VS Code instance for on-server development and MariaDB with phpMyAdmin for database management, enabling the hosting of up to 5 low-traffic websites.

Networking Architecture: Global access was achieved using Cloudflare to manage DNS and tunnels, abstracting complex networking hurdles for the user. 

#### 10\. Implementation Roadmap and Milestones

The project followed a rigorous timeline, mapping objectives to specific Charter deadlines.

1. **Hardware Selection, Sourcing & Benchmarking:**  Completed February 2026\.  
2. **Software Stack Selection:**  Completed March 2, 2026\.  
3. **LAN Operationality:**  Completed March 9, 2026\.  
4. **Global Browser Accessibility:**  Completed March 23, 2026\.  
5. **Secure SSH Remote Manipulation:**  Completed March 23, 2026\.   
6. **Cloud Image Services (Immich) Deployment:**  Completed April 30, 2026\.  
7. **Multi-Site Web Hosting (up to 3 sites):**  Completed May 20, 2026\.  
8. **Uptime Optimization:**  Ongoing.  
9. **Budget (Caped at €700):**  Achieved (Total €450).  
10. **Maintenance Minimization:**  Achieved (€1.60/month) after paid of initial investment. 

#### 11\. Usability Testing and Quality Assurance

Quantitative performance metrics and qualitative feedback were gathered from three test subjects focusing on the Immich and VS Code interfaces.

##### Quantitative Metrics

Task completion (uploading, navigating, and basic CLI commands) ranged from  **13 to 32 seconds** , confirming a low barrier to entry for non-technical personas like "Brad."

##### Technical Findings and UX Refinements

* **Immich Interface:**  Identified a lack of application-level context menus (right-click defaulting to the browser). Subjects also noted a delay in discovering the download button.  
* **VS Code Server:** A technical bug was identified where terminal auto-completion remained case-sensitive (e.g., 'Fro' failing to complete 'frontEnd').

#### 11\. Conclusion and Project Outlook

Project Jorgan successfully demonstrates that a sovereign open-source cloud can effectively rival the functionality of Google Cloud while maintaining superior budgetary discipline. By utilizing only  **€450 of the €700 allocated budget** , the project achieved its technical objectives with a 35% capital surplus.The project validates the "car ownership" metaphor; users are willing to accept the responsibilities of maintenance in exchange for the monthly €8.40 saving and the security of absolute data sovereignty. With a maintenance cost of just €1.60 per month and a robust thermal design for long-term residency, Project Jorgan stands as a blueprint for the future of decentralized personal infrastructure.  
