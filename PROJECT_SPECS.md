# Open Live Mixing System (OLMS) - Full and Integrated Project Document (Version 0.0.2)

This document redefines the **Open Live Mixing System (OLMS)**, a modular digital mixing solution based on free software. It integrates gain management, which is both manual and optionally remotely controllable, maintaining "Plug-and-Play" reliability as an absolute priority through strict hardware certification. The central idea is to transform a common, affordable, and easily available computer into a dedicated rack digital mixer, reliable and entirely controllable via Wi-Fi network, replicating the "power on and mix" simplicity and reliability of dedicated commercial systems.

***

## 1. Project Vision and Objectives

The Open Live Mixing System (OLMS) aims to transform a standard PC/Mini-PC into a dedicated and flexible rack digital mixer. The objective is to provide a self-installing operating system (the OLMS distro) that guarantees the reliability and ease of use required in a live environment, with total network control.

| Key Feature | Functional Detail |
| :--- | :--- |
| **Base Platform** | Custom Linux Distribution with a real-time (RT) kernel. |
| **Mixer Core** | Ardour (DAW/Mixer) in headless mode (without GUI). |
| **Control** | Web Browser User Interface (HTML5/JS) via OSC. |
| **Modularity** | Support for a wide range of certified USB audio interfaces, adaptable to the budget. |

***

## 2. Technology Stack (Tech Stack) and Components

### Software

### 2.1. Operating System and Audio Server (PipeWire)

**Base Distribution:** Linux (derived from Debian/Ubuntu) with an emphasis on lightness and stability.
* **Kernel:** Use of a **Real-Time (RT) Kernel** to guarantee the minimum possible latency (target: less than $10 \text{ ms}$ round-trip).
* **Main Audio Server:** **PipeWire (PW)** replaces JACK. PipeWire is configured to operate with maximum Real-Time (RT) priorities to minimize latency.
* **Ardour Integration:** Ardour communicates directly with PipeWire (through its native backend).

***

## 3. Business Model and License (Hybrid Open Core)

OLMS adopts a **Hybrid Open Core** model, balancing community contribution (GPLv3) with a clear path towards commercial sustainability (Proprietary).

### 3.1. The Open Source Core (GPLv3)

The entire critical mixing system (the **Core**) is released under the **GPLv3 License**. This includes:
* The **OLMS Distro** and the **RT Kernel**.
* **PipeWire** and the **Headless Ardour configuration**.
* The **Control Web Interface (GUI)** and the **OSC Bridge Server**.

### 3.2. The Monetization Strategy (Proprietary)

Monetization is managed by the Project Manager (Project Owner) and focuses on two channels:
1.  **Proprietary Additional Plugins:** Development and sale of advanced functionalities, such as 'Anti-Feedback System (AFS), released under a proprietary license.
2.  **Value-Added Services:** Sale of Service Level Agreements (SLA), support, and Official Certified Hardware (e.g., configured Mini-PCs).

### 3.3. Proprietary Showcase and Technical Barrier

The User Interface (GPLv3) will integrate a dedicated area (link or iFrame) that redirects to the Official Proprietary Website for the purchase and download of plugins. **Maximum functionality** and the activation of proprietary plugins will only be guaranteed through the **Official OLMS Server**, creating a **technical barrier** that protects the exclusivity of the proprietary business while keeping the Core completely open.

***

## 4. Initial Team (Core Team) and Recognitions

The Core Team is composed of 5 key members who will be cited as Founders of the OLMS Project. The primary incentive for the 4 Leads/Supervisors is the prestige and priority in a future commercial phase.

| Role | Official Title (Recognition) | Primary Incentive | Main Responsibility |
| :--- | :--- | :--- | :--- |
| Project Manager/Sound Engineer (You) | Project Owner, Technical Vision | Control of Proprietary Business (Plugin Site/SLA) | Definition of the Vision, Final Technical Validation. |
| Recruiter Volunteer | Developer Relations (DevRel) Specialist | Community Leadership, High Prestige | Recruitment, Brand Narrative, Non-Code Documentation Management. |
| Embedded Linux System Administrator | Lead Architect / Core Maintainer | Full Technical Authority over the Linux RT/Audio Core | RT Kernel, PipeWire, Multi-card Stability (Issue #1). |
| UX/UI Designer | Lead UX/UI | Full Design Authority (Live/Touch-Friendly Ergonomics) | Web Interface Design, Live User Experience. |
| Full-Stack Developer | Lead Developer (Control) | Full Authority over the Bridge Server and Web Coding | Bridge Server (Web/OSC), OSC Fader Integration (Issue #1). |

### Recognition and Credits (The 5 Founders):

The five members of the Core Team will receive full and prominent credits in the `README.md` and, if technically feasible, on a system boot screen.

### Rule for the Commercial Phase (Transparency):

If the project reaches the commercial phase (sale of plugins or services), the 4 Leads/Supervisors will be given **absolute priority** for the offer of a paid role, a supply contract, or a shareholding in the commercial company, recognizing their fundamental role in launching the GPL Core.

***

## 5. Detail on the Role of the Developer Relations (DevRel) Specialist

The DevRel Specialist is the leading figure in community building and the only "Recruiter" for the project, transforming the Manifesto into a compelling narrative for recruiting technical talent.

| Main Function | Specific Tasks |
| :--- | :--- |
| **Brand Evangelist** | Writes and publishes the Manifesto (Script 1 & 2) on the right forums, presenting OLMS as the ultimate technical and professional challenge. |
| **Recruiter and Vetting** | Actively searches (Talent Hunt B1-B3) for the 3 Lead/Supervisor roles, sifting through GitHub and specific forums. |
| **Community Facilitator** | Maintains enthusiasm, answers non-technical project questions, manages non-code documentation (e.g., CONTRIBUTING.md). |

### 5.1. Starting Strategy: Finding the DevRel and the 3 Supervisors

This sequence of actions outlines the steps to start recruitment:

#### PHASE 1: Setup and DevRel Recruitment (PM's Task)

| Step | Action Detail | Output |
| :--- | :--- | :--- |
| **1.1. Public Setup** | Create the Repository, publish the GPLv3, the Manifesto, the Technical Specifications, and Issue #1 (PoC). | Public OLMS Repository |
| **1.2. DevRel Recruitment** | Actively search for candidates (Communication students, Open Source experts, DevRel enthusiasts) on non-technical forums, offering Communication Leadership as the main incentive. | Volunteer DevRel Specialist On Board |
| **1.3. Briefing Delivery** | Provide the DevRel with the Manifesto and the complete briefing for the 3 technical roles (Architect, UX/UI, Full-Stack Dev). | "Talent Hunt" Document for the 3 Supervisors |

#### PHASE 2: Talent Hunt and Final Selection (DevRel + PM)

| Step | Action Detail | Responsible |
| :--- | :--- | :--- |
| **2.1. Public Call and Search** | The DevRel launches the targeted call (Script 2) on all platforms (Ardour, PipeWire, Linux Audio, etc.) to find candidates for the 3 Lead/Supervisor roles. | DevRel Specialist |
| **2.2. Pre-Selection and Interview** | The DevRel filters responses, looking for motivation and cultural fit. Organizes the initial interviews. | DevRel Specialist |
| **2.3. Joint Technical Selection** | The PM (You) joins the process. The final interview focuses on the candidate's technical strategy for solving Issue #1 (PoC). | PM (You) + DevRel Specialist |
| **2.4. Onboarding of the 3 Supervisors** | Once the 3 Leads/Supervisors are chosen, they are nominated, and the DevRel manages the public communication and the assignment of Issue #1 as their first coordinated task. | PM (You) |

This plan allows you to delegate the burdensome task of recruitment to the DevRel, while maintaining final control and technical validation over the selection of the 3 Supervisors.

***

## Section: PROJECT_MILESTONES.md (PoC Extract)

The goal is to create the new standard for open source digital rack mixers.

### PHASE 0: Critical Infrastructure and Proof of Concept (PoC)

**Primary Goal:** Establish the core of the real-time audio system and demonstrate that it is remotely controllable with acceptable latency.

| Deliverable | Key Role | Status | Detailed Description |
| :--- | :--- | :--- | :--- |
| **0.3. Latency and Multi-card Stability Certification** | Lead Architect/Core Maintainer | In Progress | Practical tests and documentation (Round-Trip Latency Tolerance: $< 5\text{ ms}$). Crucial validation of multi-card stability on PipeWire without X-runs for a prolonged period. |

### Fundamental PoC Issue: Stable Linux RT Core, Ardour Headless & Minimal OSC Bridge

The critical technical validation (Issue #1) is divided into three main tasks, assigned to the three Leads/Supervisors, whose success is necessary for Onboarding.

| PoC Task | Responsible | Expected Output |
| :--- | :--- | :--- |
| **PoC-1: Ergonomic Fader Mockup** | Lead UX/UI | HTML/CSS page (static) of a Master fader, completely responsive and touch-friendly. |
| **PoC-2: OSC Fader Validation (End-to-End)** | Lead Developer (Control) | Functioning Bridge Server + JS/OSC Integration to connect PoC-1 to the Master Fader of Ardour. Immediate fader movement. |
| **PoC-3: 1-Channel Live Functioning** | Lead Architect / Core Maintainer | Complete configuration (RT Kernel + PipeWire + Ardour Headless) capable of routing 1 Input $\rightarrow$ Ardour $\rightarrow$ 1 Output, remotely controlled via PoC-2, with ZERO X-runs in 1 hour. |

**RTL Goal:** Round-Trip Latency (RTL) must be $< 10\text{ ms}$; the target is $< 5\text{ ms}$.

**X-runs Goal:** ZERO (0) X-runs in one hour of stress test under load.
