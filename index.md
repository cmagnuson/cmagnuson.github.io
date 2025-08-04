## Portfolio

---

### [![Solution Design Group](images/logo-sdg.png)](https://www.solutiondesign.com)
**HealthPartners Virtuwell Client Project**
- Description: Telehealth platform for fast and convenient treatment of acute conditions
- Technologies: Java 21, Spring Boot 3, Spock, Angular, GitOps
- Infrastructure: Argo, OpenShift, Helm, GitHub, MS SQL Server, Kafka
- Background: [HealthPartners](https://www.healthpartners.com), [Virtuwell](https://www.virtuwell.com)
- Contributions:
  - Migration of data and code from 3rd party data center VM based deployments to in house OpenShift/Kubernetes deployments via Helm, Argo and GitHub Actions.  Data migration from shared NFS mount to S3 compatible storage layer
  - Enhanced blue/green deployment with application version cookie, allowing for graceful upgrades, draining of existing user sessions and testing newly deployed code prior to making it live
  - Hybrid preventative care initiative - greatly enhancing our codebase to allow for preventative care workflows, integration with Epic and custom internal APIs, Lab ordering and resulting via HL7 protocol over MLLP. Close communication with HealthPartners integration points for seamlessly integrating data with existing workflows
  - Observability enhancements to logging, metrics, trace propagation, remote call instrumentation, health checks, kubernetes probes, monitoring dashboards, custom alerting
  
**McKesson SupplyManager Client Project**
- Description: B2B ecommerce system for medical purchasing
- Technologies: Java 17, Spring Boot 2.x, React, Microservices
- Infrastructure: AKS, Oracle, MS SQL, Redis, Kafka, Elastic, JDE, Concourse CI, Distributed Tracing
- Background: [SupplyManager](https://mms.mckesson.com), [McKesson](https://www.mckesson.com)
- Contributions: 
  - Migration from legacy monolith to modern microservices, refactoring and rebuilding of existing functionality, new feature work, customer migrations to updated system
  - CSOS (controlled substances ordering system) integration with 3rd party vendor to allow ordering and digital signing for schedule 2 controlled substances
  - Concourse CI resources and pipeline templating to support development and operational needs
  - Extend internal microservices support library to improve distributed tracing, introduce micrometer metrics reporting. Spring extensions to handle cross-cutting concerns for apps and services - standard logging, security, authentication, caching, async functionality and config.
  - Lead architecture and development for customer loyalty program, interfacing with marketing, legal, compliance, ERP, and data teams along 3rd party vendor.  Negotiate with all parties to find a solution that satisfies unique regulatory constraints
  - Migration from legacy self-hosted Endeca search to SaaS solution. Refactoring of search internal microservice in backwards compatible fashion to replace implementation while maintaining existing public API 
  - Troubleshoot and diagnose performance issues.  Solve resource pooling bugs, cache timeliness and stability, N+1 communication patterns, production support

---

### [![MyLaps](images/logo-mylaps.png)](https://www.mylaps.com)

**Timing & Scoring**
- Description: Middleware to interface with timing hardware, collect manage and export data, monitoring of hardware.  Multiple hardware protocols, versions and capabilities supported and displayed in unified interface.  Communications via local network, WAN via relay server, RS232, RS485, USB HID, text file import.  Interfaces for import/export with MySQL, MS SQL, MS Access, ODBC, TCP stream, custom file format.  Multi-user client/server handling with event streaming via Protocol Buffers.  Embedded web app for optionally producing race results.
- Technologies: Java, Guava, Joda Time, Swing, JavaFX, Protocol Buffers, Protostuff, Serialio
- Infrastructure: H2, MySQL, MS SQL, MS Access, Excelsior JET (now launch4j), Jetty
- Background: [Timing & Scoring](https://www.mylaps.com/timing-scoring-software/), [MyLaps](https://www.mylaps.com)
- Contributions: Introduction of client/server functionality, integration/interfacing race scoring module built by contracted firm, support for USB HID reader device, implement software controls to allow for pay per use business model for RFID tags, maintenance work removing unused code, refactoring for better maintainability and understanding, diagnoses and fixes for tricky thread safety issues, performance profiling and improvement

---

### [![Mtec Results](images/logo-mtec.png)](https://www.mtectiming.com)

**www.mtecresults.com**
- Description: Race results and rankings, personalized race video, custom generated PDF certificates, live results.  2010-present
- Technologies: Grails, Groovy, GORM, Guava, JQuery
- Infrastructure: CloudFront, S3, MySQL, ActiveMQ, EHCache, Elastic Beanstalk, STOMP, Quartz, Compass, Tomcat, SES
- Background: [www.mtecresults.com](https://www.mtecresults.com), [Virtual Run Brochure](https://www.mtectiming.com/archive/MtecResults-Virtual.pdf) August 2020: 3,502,137 individual participant results (1,730,507 unique participants), 13,884,586 individual times.
	8.5M yearly page views (2019) 5.5M unique, peak daily page views: 500,000, peak hourly page views: 50,000

**Shoutout Video**
- Description: Video submission and playback platform, online submission of encouragement videos for athletes on race course, triggered by RFID system as participant approaches video board, optional video switcher control via RS232
- Technologies: Java, JavaFX, picocli, NanoHttpd, JMH, JQuery, videojs
- Infrastructure: Lambda, S3, CloudFront, Elastic Transcoder
- Background: [Promo Video](https://www.mtectiming.com/shoutout.html), [Brochure](https://www.mtectiming.com/archive/Spring_Brochure_2020.pdf), [Video Submission Demo](https://www.mtectiming.com/ShoutoutVideo/Demo/VideoUpload.html)  Released Fall 2019 at Columbus Marathon

**Dynamic Assignment**
- Description: On site dynamic assignment of participant number.  Allows for less waste of supplies vs. pre-assigning, faster/more flexible pickup experience for participant.  Offline first system, must be reliable for good participant experience and with limited pickup window
- Technologies: Java(Server), Android(Client), gRPC, Protocol Buffers, Dropwizard, JDBI, Lombok
- Infrastructure: H2, Android POS terminals
- Background: Developed winter 2019-2020 [Screenshot](images/app-screenshots/dynamic.png)

**Selfie Clock**
- Hardware and software build of portable LED display for use as selfie background, running time clock.  Android and desktop mangement apps.  Custom built PCB to simulate reverse engineered keypad for existing clock to make it interoperable with same software.
- Technologies: Java, Android, Protocol Buffers, Lombok
- Infrastructure: Raspberry Pi, LED Matrix Hat, KiCad, ZeroTier, Table Saw, PVC, Spray Paint
- Background: PCB Images [1.0](images/clockcontrol-pcb/pcb0.jpg), [1.1](images/clockcontrol-pcb/pcb1.jpg), [1.2](images/clockcontrol-pcb/pcb2.jpg)

**Internal Android Apps**
- Description: Internal Android apps for various functions - AnnouncerDisplay (tablet/desktop info display for race announcer, live results feed, gRPC integration for live updates/messaging from timing software) / ResultsReceipts (receipt printout of results from POS device, using internal API of www.mtecresults.com ) / BackupTiming (manual time capture for backup/verification uses, integration with external services with TCP and HTTP APIs) / ClockControl (control/monitoring of in house LED display and commercial LED clock with reverse engineered input) / S3PhotoSync (live sync of captured photos to S3 and metadata HTTP API)
- Technologies: OkHttp, gRPC, Protocol Buffers, TrueTime Android
- Infrastructure: S3, Lambda, ZeroTier

**Media Reporting Site**
- Description: S3 directory listing with email/SMS notification to interested parties of updated files matching given regexp
- Technologies: Node, Pug
- Infrastructure: Serverless, S3, Lambda, SNS

**Data Transformation**
- Description: Data transformation for common use cases, diff of CSV file based on unique id column. JSON DSL for data transformations. Splitting CSV on unique column values.
- Technologies: Haskell, aeson, parsec, lucid, Groovy
- Background: GitHub repos - [DataLoader](https://github.com/cmagnuson/DataLoader), [CsvDiff](https://github.com/cmagnuson/CsvDiff), [TeamSplitter](https://github.com/cmagnuson/TeamSplitter)

**API clients - RaceEntry/RaceRoster/RunSignUp**
- Description: API clients to access registrations services via CLI or to embed as library
- Technologies: OkHttp, picocli, Lombok, Gson
- Background: GitHub repos - [RaceEntry API Client](https://github.com/cmagnuson/raceentry-api-client), [RunSignUp API Client](https://github.com/cmagnuson/runsignup-api-client)

**RS-Pretty**
- Description: Parse text report from 3rd party tool and build Latex template to generate more polished PDF report.  Customizable config of reports and file watch for automatic regeneration
- Technologies: Java, JSoup, Protocol Buffers, picocli
- Infrastructure: Latex, launch4j

**TCP protocol handling/conversion - Various tools (5+)**
- Description: Tooling for converting 3rd party TCP/UDP streams from custom protocol to Java API, DB or JMS handling, conversion to other 3rd party protocol
- Technologies: Java, Mina, JMS
- Infrastructure: Jitpack, ActiveMQ
- Background: GitHub repos - [MyLaps TCP Server](https://github.com/cmagnuson/mylaps-tcp-server), [RM Timing UDP Server](https://github.com/cmagnuson/rm-timing-udp-server), [rs-happy](https://github.com/cmagnuson/rs-happy), [RunScoreTCPToFile](https://github.com/cmagnuson/RunScoreTCPToFile)

**Live Ranking**
- Description:	Extending Order Statistic Tree implementation to allow for duplicate entries and keep proper count
- Technologies: Java
- Infrastructure: Jitpack, MySQL
- Background - GitHub Repos - [LiveRanking](https://github.com/cmagnuson/LiveRanking), [OrderStatisticTree](https://github.com/cmagnuson/OrderStatisticTree)

---
<p style="font-size:11px">Page template forked from <a href="https://github.com/evanca/quick-portfolio">evanca</a></p>
<!-- Remove above link if you don't want to attibute -->
