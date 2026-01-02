# Portfolio Repository: Production-Grade Project Showcase

> **Professional Note:** Having built and deployed numerous commercial applications, I realized that much of my most impactful work remained locked in private enterprise repositories. To better demonstrate my technical depth and architectural thinking to potential partners and employers, I am publishing these curated portfolio repositories. I have worked on many projects, and I am now consolidating these representations to share my capabilities and open doors for new opportunities.

**Notice:** This repository represents a **Live Production System**. Due to commercial sensitivity and intellectual property agreements, the full source code is not public. However, I have included:
1.  **Architecture Overviews:** Deep dives into the "why" and "how" of the system logic.
2.  **Core Logic Snippets:** Selected high-impact code samples to demonstrate my standards.
3.  **Live Demos:** Fully functional environments to explore the system firsthand.

---


# GlobalShop: Cross-Border E-Commerce Solution

#### *Project Completion Date: December 2025*
![frontend_landing](https://raw.githubusercontent.com/Mohit-Hasan/globalshop-commerce-platform/refs/heads/main/screenshots/frontend_landing.png)

### Business Case & Problem Statement
In many regions, consumers face a "border barrier" where desired products are geographically restricted or lack reliable international delivery infrastructure. GlobalShop was engineered to solve this "ecommerce desert" problem. It provides a managed procurement pipeline where users can request any global product, and the platform facilitates the middle-man logistics: from international sourcing and custom quoting to secure cross-border fulfillment.

---

### Core Business Workflow
The platform utilizes a high-touch **Request-to-Order** lifecycle:
1.  **Direct Request:** Users (or Guests via session-based drafts) submit product links and specifications.
2.  **Administrative Quoting:** Admins communicate with international vendors to calculate pricing, duties, and logistics fees, sending a formal quote to the user.
3.  **Acceptance & Payment:** Users review and pay via SSLCommerz (API) or Manual methods. 
4.  **Procurement & Fulfillment:** Upon payment, the request converts to a managed Order.
5.  **Reverse Logistics:** Built-in return engine with dynamic logic for return windows and shipping cost adjustments based on specific return scenarios.

---

### Technical Architecture Highlights

* **Engineered Scalability:** While currently a monolithic PHP/Laravel application, the service layers are decoupled, allowing for a decentralized/microservices transition with minimal friction.
* **Asynchronous Processing:** To ensure high performance, emails are not sent during the web request cycle. They are pushed to a **Database Queue**, where backend workers process notifications in batches.
* **Enterprise-Grade Security:** * **Rate Limiting:** Implemented on sensitive routes including Tracking, Contact Support, and Auth attempts to mitigate brute-force and DDoS risks.
    * **Advanced Auth:** Dual-Guard system for Admin and User dashboards, Google OAuth2 integration, and secure OTP-based guest validation.
    * **Security Max-Attempt:** Account recovery and password resets feature strict expiry tokens and attempt-limiting technology.
* **Strategy Pattern Payments:** A flexible gateway management system that currently implements SSLCommerz but is architecturally ready for "N" number of future API or Manual integrations.

---

### Key System Modules

#### Administrative Control (CMS & ERP)
* **Dynamic Configuration Engine:** A centralized management layer providing granular control over site branding, color schematics, and UI visibility. Includes toggleable global settings for OTP protocols, Social Login providers, and automated Email triggers.
* **Hybrid Content Management (CMS):** A dual-mode system featuring a structured page builder for core site architecture and a low-level Plain-HTML builder for rapid deployment of custom marketing landing pages.
* **Operational Logistics Hub:** Comprehensive modules to manage global shipping jurisdictions (Countries), third-party Courier partners, and a complex 2-level (Parent-Child) product catalog designed to ingest and showcase demand-driven products from 3rd party sources.
* **Advanced Promotion Logic:** A robust promo-code engine supporting diverse business rules, including validity periods, usage limits, and tier-based discounts integrated directly into the quoting workflow.

#### User Experience & Engagement
* **Unified User Dashboard:** A data-rich command center for customers to manage the full procurement lifecycle, from initial request tracking to historical order archives and synchronized address books.
* **Secure Guest Pipeline:** A high-conversion, one-page checkout experience fortified with secure OTP (One-Time Password) validation, ensuring data integrity and preventing bot-driven submissions before reaching the system core.
* **Logistics Telemetry:** Integrated tracking system providing real-time visibility into cross-border shipment status, protected by rate-limited access to ensure API stability.

---

### Visual Walkthrough

**1. Administrative Intelligence Dashboard** *Real-time monitoring of profit, sales, and pending procurement requests.*
![admin_dash](https://raw.githubusercontent.com/Mohit-Hasan/globalshop-commerce-platform/refs/heads/main/screenshots/admin_dash.png)

---

**2. Managed Request & Quoting System** *The primary engine for converting international product links into actionable business quotes.*
![request_flow](https://raw.githubusercontent.com/Mohit-Hasan/globalshop-commerce-platform/refs/heads/main/screenshots/request_flow.png)

---

**3. Global Configuration & CMS Settings** *Centralized management of system-wide variables, from UI colors to gateway credentials.*
![settings](https://raw.githubusercontent.com/Mohit-Hasan/globalshop-commerce-platform/refs/heads/main/screenshots/settings.png)

---

**4. High-Fidelity Mobile Interface** *A fully responsive frontend designed for global accessibility across all device types.*
![mobile_ui_1](https://raw.githubusercontent.com/Mohit-Hasan/globalshop-commerce-platform/refs/heads/main/screenshots/mobile_ui_1.png)
![mobile_ui_2](https://raw.githubusercontent.com/Mohit-Hasan/globalshop-commerce-platform/refs/heads/main/screenshots/mobile_ui_2.png)

---

### Live Demonstration & Access
You can explore the live system to test the workflows, UI responsiveness, and administrative capabilities.

* **Live Demo URL:** [https://globalshop.mohithasan.com](https://globalshop.mohithasan.com)

* **Live Demo URL (Admin):** [https://globalshop.mohithasan.com/admin/login](https://globalshop.mohithasan.com/admin/login)

#### **Test Credentials**

| Account Type | Email Address | Password |
| :--- | :--- | :--- |
| **Administrator** | `superadmin@gmail.com` | `123456` |
| **User / Customer** | `user@gmail.com` | `123456` |

*Note: Data in the demo environment is reset periodically in every hour (UTC). Please do not use sensitive real-world information during testing.*

---


### Repository Structure
This repository is a **Portfolio Representation**. To protect commercial intellectual property, the full source code is not public. Instead, core logic implementation is showcased via selected snippets.

```text
├── sample_code/
├── screenshots/
└── README.md
```

---

### Explore Other Projects
I have curated a selection of my work to showcase different architectural patterns and business solutions. Feel free to explore them:

[![GlobalShop](https://img.shields.io/badge/Project-GlobalShop-blue?style=for-the-badge&logo=github)](https://github.com/mohit-hasan/globalshop-commerce-platform)
[![Classroom](https://img.shields.io/badge/Project-Classroom-lightgrey?style=for-the-badge&logo=github)](https://github.com/mohit-hasan/classroom-management)

