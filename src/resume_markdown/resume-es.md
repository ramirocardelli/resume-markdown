# Ramiro Cardelli

- <ramirocardelli89@gmail.com>
- +54 9 223 663-2207
- Mar del Plata, Argentina
- [LinkedIn](https://www.linkedin.com/in/ramirocardelli/)
- [GitHub](https://github.com/ramirocardelli/)

Ingeniero en Informática y desarrollador backend con más de 2,5 años de experiencia en sistemas productivos. Desarrollé servicios con Java y Spring para una plataforma multitenant de gestión de casinos, donde optimicé el acceso a MySQL (latencia de las consultas de ~900 ms a ~400 ms), desacoplé la arquitectura del servidor y automaticé los releases con Jenkins. En Nexus probé el servicio de bridge de una plataforma de microservicios. También tengo experiencia en blockchain (pruebas de concepto en BSV, 1.er lugar en el Ethereum Argentina Hackathon), QA y docencia universitaria en bases de datos.

## Experiencia

### <span>Ingeniero Backend, Nexus</span> <span>sep 2026 - oct 2026</span>

*Arquitectura de microservicios — GitHub, Linear, Slack, Google Workspace, Claude*

- Estuve a cargo de la robustez del **bridge**, uno de los microservicios de la plataforma: planifiqué y escribí casos de prueba para verificar que funcione de extremo a extremo.
- Validé el bridge en distintos entornos: local (con fakes/stubs y componentes reales), testnet y, como etapa final, mainnet.
- Participé en code reviews en GitHub, en un equipo que trabajaba con Linear, Slack y desarrollo asistido por IA con Claude.

### <span>Ayudante de Cátedra de Bases de Datos, Universidad Nacional de Mar del Plata</span> <span>ago 2025 - actualidad</span>

- Brindé apoyo académico y clases de consulta sobre fundamentos de bases de datos (modelado ER, álgebra relacional, SQL, normalización, transacciones ACID y optimización de consultas).

### <span>Ayudante de Cátedra, Deep Dive into Blockchain 2026 (7.ª ed.), Universidad de Zúrich</span> <span>6 jul - 24 jul 2026</span>

- Brindé soporte en un curso intensivo de 3 semanas sobre blockchain, desde perspectivas técnicas, económicas y legales, junto a profesores y expertos de la industria.

### <span>Multicommerce</span> <span>abr 2024 - ago 2026</span>

#### <span>Ingeniero Backend</span> <span>mar 2025 - ago 2026</span>

*Plataforma multitenant de gestión de casinos — Java 8 / 17, Spring, Hibernate, MySQL, Jersey, Jenkins*

- **Eliminé un cuello de botella en la base de datos:** detecté que el servidor abría y cerraba una conexión a MySQL por cada consulta; lo reemplacé por un pool reutilizable de HikariCP (30–50 conexiones) con cambio de esquema por tenant y limpieza de conexiones para mantener el aislamiento entre clientes. Bajé la latencia de las consultas de ~900 ms a ~400 ms y la carga de MySQL de ~100% a ~60% bajo estrés, evitando sumar instancias de base de datos.
- **Desacoplé la arquitectura del servidor:** extraje el Redemption Kiosk a una biblioteca independiente y opcional, moví la lógica de negocio de los endpoints REST a servicios de Spring y reorganicé responsabilidades entre los módulos común y núcleo del servidor. Adapté APIs REST para integrarlas con el frontend.
- **Modernicé el stack:** migré la caché de Ehcache 2 a Ehcache 3 sobre la API JCache e integré los servicios REST de Jersey con la inyección de dependencias de Spring.
- **Robustecí el envío de emails:** agregué deduplicación y throttling al servicio SMTP para evitar envíos duplicados y controlar la frecuencia de envío.
- **Automaticé los releases:** armé pipelines en Jenkins que despliegan versiones directamente en las máquinas virtuales de test y producción, y desarrollé una herramienta interna de gestión de releases (Spring Boot 3, SVN) que modela el flujo (Draft → Testing → Ready → Released) entre DEV, QA y PROD.

#### <span>Ingeniero de QA</span> <span>abr 2024 - feb 2025</span>

- Ejecuté pruebas manuales y funcionales, registré incidencias y colaboré en su resolución.

### <span>Practicante, BSV Association</span> <span>oct 2025 - dic 2025</span>

*Pruebas de concepto de dApps sobre la blockchain de BSV — TypeScript, React, Node.js / Express, MongoDB, @bsv/sdk*

- **Vehicle History:** registros de vehículos y mantenimientos guardados on-chain como tokens PushDrop, con búsqueda por VIN y reportes PDF que vinculan cada registro con su transacción para verificarlo públicamente.
- **Micropayment Content Access:** contenido pago por artículo, con pagos en satoshis enviados directo a cada autor mediante claves derivadas con BRC-29 y un endpoint de contenido protegido con autenticación de wallet BRC-104.
- **Medical Data Sharing:** prototipo para que los pacientes compartan imágenes médicas con sus médicos, cifradas en el navegador y asociadas a identidades y roles basados en la wallet.
- Desarrollé herramientas y documentación de SDKs para mejorar la usabilidad y simplificar los flujos de integración.

### <span>Desarrollador Freelance — Editor de Boletines</span> <span>sep 2025 - abr 2026</span>

- Desarrollé una aplicación de escritorio (Electron, GrapesJS) para que una clienta mayor y sin conocimientos técnicos arme sola, sin ayuda de terceros, el boletín por email de una organización: elige una plantilla, edita textos y banners de forma visual y copia el HTML listo para enviar.
- Diseñé cada flujo pensando en ella: interfaz solo en español, controles mínimos, proyectos guardados y plantillas filtrables, aviso al cerrar con cambios sin guardar y un ejecutable portable para Windows que no requiere instalación.
- Armé plantillas HTML basadas en tablas que se ven igual en los distintos clientes de correo y un script de build que embebe los banners en Base64.

### <span>Desarrollador Full-Stack, Apeiron</span> <span>abr 2021 - jul 2021</span>

- Desarrollé un plugin de venta cruzada y upselling para Tiendanube con Node.js, incluyendo el desarrollo de una API REST.
- El proyecto aumentó los ingresos de los clientes al mejorar las recomendaciones de productos y optimizar la experiencia de compra.

## Proyectos

### <span>KleinKauf — Plataforma de gestión para pequeños comercios (con un compañero)</span> <span>nov 2026 - actualidad</span>

*Microservicios — Java 21, Spring Boot 3, Spring Cloud Gateway, Eureka, PostgreSQL, Redis, Resilience4j, React, Docker*

- Co-desarrollo un SaaS multitenant para pequeños comercios (catálogo, stock, combos, ventas online y en el local): microservicios en Spring Boot detrás de un API gateway, con un schema de PostgreSQL por tenant, caché en dos niveles (Caffeine + Redis) y llamadas entre servicios protegidas con Resilience4j.
- Desarrollé los paneles de administración de la tienda y de la plataforma: ventas del local, seguimiento de pedidos y reportes; combos de productos con descuento porcentual o fijo; matriz de permisos por rol; y un panel de superadmin para gestionar las tiendas. Sumé emails transaccionales por tienda con Resend.
- Reescribí el frontend en Vite + React Router con TanStack Query y manejo centralizado de la sesión, hice que el gateway devuelva errores 4xx correctos con cabeceras CORS y levanté todo el backend con un solo docker compose y un seed que carga una tienda demo a través de la API.

## Hackathons

### <span>1.er lugar — Ethereum Argentina Hackathon (Adopción, Impacto y DAOs)</span> <span>2026</span>

- Construí **FundMe!**, una MiniApp integrada con Lemon para crowdfunding transparente: los fondos generan rendimientos DeFi mientras están activos y se liberan al cumplirse la meta. Diseñé estrategias de rendimiento DeFi e integré el proyecto con el ecosistema de Lemon para darle visibilidad.

## Educación

### <span>Universidad Nacional de Mar del Plata, Ingeniería en Informática</span> <span>2021 - may 2026</span>

- Graduación: 22 de mayo de 2026
- **Trabajo final — IlliApp:** Sistema web de gestión académica para una escuela secundaria. Lideré el relevamiento de requisitos, diseñé la arquitectura del sistema y coordiné al equipo de desarrollo.

## Habilidades

- **Programación:** Java (8, 17, 21), Python, JavaScript, TypeScript, SQL
- **Backend:** Spring Boot, Spring MVC, Spring Cloud (Gateway, Eureka), Hibernate / JPA, Resilience4j, Jersey, Node.js / Express, APIs REST, microservicios, multitenancy
- **Bases de datos y caché:** SQL (MySQL, PostgreSQL), NoSQL (MongoDB, Redis), HikariCP, Ehcache / JCache, Caffeine
- **Frontend:** React, Next.js
- **Testing y DevOps:** JUnit, Postman, Jenkins (CI/CD), Docker, Git, SVN
- **Colaboración:** GitHub (code reviews), Linear, Slack, Google Workspace, Claude (desarrollo asistido por IA)
- **Idiomas:** español (nativo), inglés (C2), alemán (B2)
