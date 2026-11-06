# Ramiro Cardelli

- <ramirocardelli89@gmail.com>
- +54 9 223 663-2207
- Mar del Plata, Argentina
- [LinkedIn](https://www.linkedin.com/in/ramirocardelli/)
- [GitHub](https://github.com/ramirocardelli/)

**Desarrollador Backend Java** con más de 2,5 años de experiencia en sistemas productivos (Java 8, 17 y 21, Spring, Hibernate). Optimicé el rendimiento de una plataforma multitenant (latencia de las consultas de ~900 ms a ~400 ms y carga de MySQL de ~100% a ~60%), desacoplé su arquitectura y automaticé los releases con Jenkins. Trabajé en una arquitectura de microservicios con code reviews en GitHub, y hoy co-desarrollo una plataforma de microservicios con Spring Boot, Spring Cloud, PostgreSQL y Redis. Experiencia en APIs REST, bases de datos SQL y NoSQL, QA y docencia universitaria en bases de datos.

## Experiencia

### <span>Ingeniero Backend, Nexus</span> <span>sep 2026 - oct 2026</span>

*Arquitectura de microservicios — GitHub, Linear, Slack, Google Workspace, Claude*

- Estuve a cargo de la robustez del **bridge**, uno de los microservicios de la plataforma: planifiqué y escribí casos de prueba para verificar que funcione de extremo a extremo.
- Validé el servicio en distintos entornos: local (con fakes/stubs y componentes reales), testnet y, como etapa final, mainnet.
- Participé en code reviews en GitHub, en un equipo que trabajaba con Linear, Slack y desarrollo asistido por IA con Claude.

### <span>Multicommerce</span> <span>abr 2024 - ago 2026</span>

#### <span>Ingeniero Backend</span> <span>mar 2025 - ago 2026</span>

*Plataforma multitenant de gestión de casinos — Java 8 / 17, Spring, Hibernate, MySQL, Jersey, Jenkins*

- **Optimicé el rendimiento de la base de datos:** detecté que el servidor abría y cerraba una conexión a MySQL por cada consulta; lo reemplacé por un pool reutilizable de HikariCP (30–50 conexiones) con cambio de esquema por tenant y limpieza de conexiones para mantener el aislamiento entre clientes. Bajé la latencia de las consultas de ~900 ms a ~400 ms y la carga de MySQL de ~100% a ~60% bajo estrés, sin sumar instancias de base de datos.
- **Desacoplé la arquitectura del servidor:** extraje el Redemption Kiosk a una biblioteca independiente y opcional, moví la lógica de negocio de los endpoints REST a servicios de Spring y reorganicé responsabilidades entre los módulos común y núcleo.
- **Integré el backend con el frontend:** adapté APIs REST a lo que necesitaba el frontend e integré los servicios REST de Jersey con la inyección de dependencias de Spring.
- **Modernicé el stack:** migré la caché de Ehcache 2 a Ehcache 3 sobre la API JCache y agregué deduplicación y throttling al servicio de envío de emails (SMTP).
- **Automaticé los releases:** armé pipelines en Jenkins que despliegan versiones en las máquinas virtuales de test y producción, y desarrollé una herramienta interna de gestión de releases (Spring Boot 3, SVN) con el flujo Draft → Testing → Ready → Released entre DEV, QA y PROD.

#### <span>Ingeniero de QA</span> <span>abr 2024 - feb 2025</span>

- Ejecuté pruebas manuales y funcionales, registré incidencias y colaboré con el equipo de desarrollo en su resolución.

### <span>Practicante, BSV Association</span> <span>oct 2025 - dic 2025</span>

- Desarrollé tres pruebas de concepto full-stack sobre blockchain (TypeScript, Node.js / Express, MongoDB, React): APIs REST con persistencia en MongoDB, autenticación por firma de wallet y registros verificables on-chain. También desarrollé herramientas y documentación de SDKs.

### <span>Desarrollador Freelance — Editor de Boletines</span> <span>sep 2025 - abr 2026</span>

- Desarrollé una aplicación de escritorio (Electron, GrapesJS) para que una clienta mayor y sin conocimientos técnicos arme sola el boletín por email de una organización. Diseñé la experiencia de uso a partir de sus necesidades: interfaz simple en español, plantillas listas y un ejecutable portable sin instalación.

### <span>Desarrollador Full-Stack, Apeiron</span> <span>abr 2021 - jul 2021</span>

- Desarrollé un plugin de venta cruzada y upselling para Tiendanube con Node.js, incluyendo su API REST.

## Proyectos

### <span>KleinKauf — Plataforma de gestión para pequeños comercios (con un compañero)</span> <span>nov 2026 - actualidad</span>

*Microservicios — Java 21, Spring Boot 3, Spring Cloud Gateway, Eureka, PostgreSQL, Redis, Resilience4j, Docker*

- Co-desarrollo un SaaS multitenant (catálogo, stock, combos, ventas online y en el local): microservicios en Spring Boot detrás de un API gateway, con un schema de PostgreSQL por tenant, caché en dos niveles (Caffeine + Redis) y llamadas entre servicios protegidas con Resilience4j.
- Desarrollé los paneles de administración: ventas del local, seguimiento de pedidos y reportes; combos con descuento porcentual o fijo; matriz de permisos por rol; panel de superadmin para gestionar las tiendas; y emails transaccionales por tienda con Resend.
- Hice que el gateway devuelva errores 4xx correctos con cabeceras CORS, reescribí el frontend en React con TanStack Query y levanté todo el backend con un solo docker compose y un seed de datos de prueba.

### <span>1.er lugar — Ethereum Argentina Hackathon: FundMe!</span> <span>2026</span>

- En un equipo de tres, construí una MiniApp de crowdfunding para Lemon con Next.js, una API REST en capas (dominio, repositorios) y PostgreSQL con Sequelize.

## Docencia

- **Ayudante de Cátedra de Bases de Datos**, Universidad Nacional de Mar del Plata (ago 2025 - actualidad): modelado ER, SQL, normalización, transacciones ACID y optimización de consultas.
- **Ayudante de Cátedra, Deep Dive into Blockchain**, Universidad de Zúrich (jul 2026): curso intensivo de 3 semanas junto a profesores y expertos de la industria.

## Educación

### <span>Universidad Nacional de Mar del Plata, Ingeniería en Informática</span> <span>2021 - may 2026</span>

- **Trabajo final — IlliApp:** sistema web de gestión académica para una escuela secundaria. Lideré el relevamiento de requisitos, diseñé la arquitectura del sistema y coordiné al equipo de desarrollo.

## Habilidades

- **Java y backend:** Java (8, 17, 21), Spring Boot, Spring MVC, Spring Cloud (Gateway, Eureka), Hibernate / JPA, Resilience4j, Jersey, APIs REST, microservicios, multitenancy
- **Bases de datos y caché:** SQL (MySQL, PostgreSQL), NoSQL (MongoDB, Redis), HikariCP, Ehcache / JCache, Caffeine
- **Testing y DevOps:** JUnit, Postman, Jenkins (CI/CD), Docker, Git, SVN
- **Otros lenguajes y frontend:** Python, TypeScript, JavaScript, Node.js / Express, React, Next.js
- **Colaboración:** GitHub (code reviews), Linear, Slack, Google Workspace, Claude (desarrollo asistido por IA)
- **Idiomas:** español (nativo), inglés (C2), alemán (B2)
