# Ramiro Cardelli

- <ramirocardelli89@gmail.com>
- +54 9 223 663-2207
- Mar del Plata, Argentina
- [LinkedIn](https://www.linkedin.com/in/ramirocardelli/)
- [GitHub](https://github.com/ramirocardelli/)

Informatics Engineer and backend developer with 2.5+ years of experience in production systems. Built Java and Spring services for a multitenant casino platform, where I optimized MySQL access (query latency from ~900 ms to ~400 ms), decoupled the server architecture and automated releases with Jenkins. At Nexus I tested the bridge service of a microservices platform. Also experienced in blockchain (BSV proofs of concept, 1st place at the Ethereum Argentina Hackathon), QA, and university teaching in databases.

## Experience

### <span>Backend Engineer, Nexus</span> <span>Sep 2026 - Oct 2026</span>

*Microservices architecture — GitHub, Linear, Slack, Google Workspace, Claude*

- Owned the **bridge-robustness** effort for the bridge, one of the platform's microservices: planned and wrote test cases to verify it works end to end.
- Validated the bridge across environments: local (fakes/stubs and real components), testnet and, as the final stage, mainnet.
- Took part in code reviews on GitHub, in a team that worked with Linear, Slack and AI-assisted development with Claude.

### <span>Teaching Assistant of Databases, Universidad Nacional de Mar del Plata</span> <span>Aug 2025 - Present</span>

- Provided academic support and tutoring on database fundamentals (ER modeling, relational algebra, SQL, normalization, ACID transactions, query optimization).

### <span>Teaching Assistant, Deep Dive into Blockchain 2026 (7th Ed.), University of Zurich</span> <span>Jul 6 - Jul 24, 2026</span>

- Supported an intensive 3-week course on blockchain covering technical, economic, and legal perspectives, alongside professors and industry experts.

### <span>Multicommerce</span> <span>Apr 2024 - Aug 2026</span>

#### <span>Backend Engineer</span> <span>Mar 2025 - Aug 2026</span>

*Multitenant casino management platform — Java 8 / 17, Spring, Hibernate, MySQL, Jersey, Jenkins*

- **Removed a database bottleneck:** found the server opened and closed a MySQL connection per query; replaced it with a reusable HikariCP pool (30–50 connections) with per-tenant schema switching and connection cleanup to keep tenants isolated. Cut query latency from ~900 ms to ~400 ms and MySQL load from ~100% to ~60% under stress, avoiding extra database instances.
- **Decoupled the server architecture:** extracted the Redemption Kiosk into an optional standalone library, moved business logic out of REST endpoints into Spring services, and reorganized responsibilities between the shared and core server modules. Adapted REST APIs to integrate with the frontend.
- **Modernized the stack:** migrated caching from Ehcache 2 to Ehcache 3 behind the JCache API, and integrated Jersey REST services with Spring dependency injection.
- **Hardened email delivery:** added deduplication and throttling to the SMTP service to prevent duplicate sends and control sending rate.
- **Automated releases:** built Jenkins pipelines that deploy versions directly to the test and production VMs, and developed an internal release-management tool (Spring Boot 3, SVN) that models the release flow (Draft → Testing → Ready → Released) across DEV, QA and PROD.

#### <span>QA Engineer</span> <span>Apr 2024 - Feb 2025</span>

- Executed manual and functional tests, tracked issues, and collaborated on their resolution.

### <span>Intern, BSV Association</span> <span>Oct 2025 - Dec 2025</span>

*Proof-of-concept dApps on the BSV blockchain — TypeScript, React, Node.js / Express, MongoDB, @bsv/sdk*

- **Vehicle History:** vehicle and maintenance records stored on-chain as PushDrop tokens, with VIN search and PDF reports that link each record to its transaction for public verification.
- **Micropayment Content Access:** pay-per-article content with satoshi payments sent directly to each author through BRC-29 derived keys, and a content endpoint protected by BRC-104 wallet authentication.
- **Medical Data Sharing:** prototype for patient-controlled sharing of medical images with doctors, encrypted in the browser and tied to wallet-based identities and roles.
- Developed developer tools and SDK documentation to improve usability and streamline integration flows.

### <span>Freelance Developer — Newsletter Editor</span> <span>Sep 2025 - Apr 2026</span>

- Built a desktop app (Electron, GrapesJS) that lets a non-technical, older client produce an organization's email newsletter on her own, without outside help: pick a template, edit text and banners visually, and copy email-ready HTML.
- Designed every flow around her: Spanish-only interface, minimal controls, saved projects and filterable templates, a guard against closing with unsaved changes, and a portable Windows executable with no installation.
- Built table-based HTML templates that render consistently across email clients, plus a build script that embeds banner images as Base64.

### <span>Full-Stack Developer, Apeiron</span> <span>Apr 2021 - Jul 2021</span>

- Developed a cross-selling and upselling plugin for Tiendanube using Node.js, including REST API development.
- The project increased client revenue by improving product recommendations and optimizing the shopping experience.

## Projects

### <span>KleinKauf — Management Platform for Small Shops (with a teammate)</span> <span>Nov 2026 - Present</span>

*Microservices — Java 21, Spring Boot 3, Spring Cloud Gateway, Eureka, PostgreSQL, Redis, Resilience4j, React, Docker*

- Co-developing a multitenant SaaS for small shops (catalog, stock, combos, online and in-store sales): Spring Boot microservices behind an API gateway, with schema-per-tenant PostgreSQL, two-level caching (Caffeine + Redis) and service-to-service calls protected by Resilience4j.
- Built the store and platform admin panels: sales with in-store orders, order tracking and reports; product combos with percentage or fixed discounts; a per-role permission matrix; and a superadmin panel to manage stores. Added per-store transactional email with Resend.
- Rewrote the frontend in Vite + React Router with TanStack Query and centralized session handling, made the gateway return proper 4xx errors with CORS headers, and set up the whole backend to run with one Docker Compose file plus a seed that loads a demo store through the API.

## Hackathons

### <span>1st Place — Ethereum Argentina Hackathon (Adoption, Impact & DAOs)</span> <span>2026</span>

- Built **FundMe!**, a Lemon-integrated MiniApp for transparent crowdfunding. Funds accrue DeFi yield while active and are released on goal completion. Designed DeFi yield strategies and integrated with Lemon's ecosystem for visibility.

## Education

### <span>Universidad Nacional de Mar del Plata, Informatics Engineering</span> <span>2021 - May 2026</span>

- Graduation: May 22, 2026
- **Final project — IlliApp:** Academic management web system for a secondary school. Led requirements gathering, designed system architecture, and coordinated the development team.

## Skills

- **Programming:** Java (8, 17, 21), Python, JavaScript, TypeScript, SQL
- **Backend:** Spring Boot, Spring MVC, Spring Cloud (Gateway, Eureka), Hibernate / JPA, Resilience4j, Jersey, Node.js / Express, REST APIs, microservices, multitenancy
- **Databases & Caching:** SQL (MySQL, PostgreSQL), NoSQL (MongoDB, Redis), HikariCP, Ehcache / JCache, Caffeine
- **Frontend:** React, Next.js
- **Testing & DevOps:** JUnit, Postman, Jenkins (CI/CD), Docker, Git, SVN
- **Collaboration:** GitHub (code reviews), Linear, Slack, Google Workspace, Claude (AI-assisted development)
- **Languages:** Spanish (native), English (C2), German (B2)

