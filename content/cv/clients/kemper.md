### Kemper Insurance - APLUS Application

The assessment I wrote for Kemper in November 2000 was reviewed and a migration plan was approved to improve the architecture of the APLUS application. I was contracted to assist in this effort. The majority of my time on this project has been spent between development and production support. As part of the APLUS team I am assigned various production support issues that arise. Sometimes those issues are simple data changes, sometimes they are complicated bug fixes in the application code. The development time is spent adding new features to the application required by the business customer and cleaning up the existing code by separating logic into presentation and business tiers. A data tier was also proposed but has not been approved to date. The eventual goal being to have a thin client with the majority of the presentation logic and a server-based business tier. In July 2001, APLUS was one large client application.

The effort has been largely successful. New features have been added on time and on budget while significant improvements have been made to the structure and stability of the code base. The overall
footprint has decreased despite additional features because of increased code reuse between areas of the application.

*Responsibilities*

My responsibilities as _architect_ and _developer_ for Kemper were as follows:

*   Maintain the DB2 ERD files using ERwin
*   Support the production version of APLUS
*   Design and development of new features of APLUS
*   Write functional and technical documentation for APLUS and participate in knowledge transfer to other developers
*   Participate in numerous design and project status meetings
*   Help create test data and test cases

### Kemper Insurance - FIS Clearance Web Site

_Jan 2002 - Mar 2002_

The FIS Clearance web site was created to allow United Kingdom producers to clear business for FIS in the United States. After ruling out modifications to the APLUS client application, a web application was decided to be the best solution. Over a 12 week period, the site was created from scratch, including about 3 dozen ASP files and associated includes and 3 middle tier business objects. The ASP pages were written with Visual InterDev with integrated SourceSafe. The business objects were written with Visual Basic 6. The business objects returned data to the ASPs in a custom XML format. The MSXML component was used to create and parse these XML data streams. Photoshop 6 was used to create the images for the site.

As with other Kemper web applications, the site is served on IIS 4 and goes through the Webthority proxy server which handles SSL and LDAP-based authentication. Traditionally, a significant amount of work has gone into working with the Webthority team to test the security of the site and to ensure maximum availability.

*Responsibilities*

My responsibilities as _architect_ and _developer_ on this project were as follows:

*   Design, construct, and test the Active Server Pages
*   Design, construct, and test the business objects
*   Write the SQL to get data into and out of the DB2 database
*   Participate in numerous design and project status meetings
*   Interview client for interface design requirements and general business process analysis
*   Work with security architects to ensure safe, secure availability of system

### Kemper Insurance - APLUS Document Generation Server

_Oct 2001 - Feb 2002_

One of the most time-consuming tasks involved in using APLUS in the generation and printing of various forms and letters. Before this project it took between 40 seconds and 2 minutes to generate a given document in the field. The same document only took 10 seconds or so when generated local to the database. The overhead was due to the slow connections between field offices and the home office and the massive number of database queries required to generate a given document.

I proposed offloading the document generation task to a powerful server in the home office. A request would be initiated by APLUS in the field, the server would receive the request, generate the required document, and return a completion result. The documents were and continue to be stored on a file server at the home office so the document itself did not need to be sent back across the network.

The solution was implemented as a web service using SOAP and the accompanying components. The document request was sent via SOAP, collected by the SOAP Listener on the server, and then the documents were generated. A significant amount of componentization of the APLUS logic was required to make this work. The document generation logic was eventually hosted in MTS and was separated between several objects.

This was one of the bigger successes for APLUS as the average time for document generation went down to 3-4 seconds in the field. The generation time was better than expected due to the server actually generating the document much faster than in the field. The server was a dual processor, 1 GB machine where the average field machine was an older Pentium model with 32 MB RAM and most users having Lotus Notes loaded simultaneously, i.e. very slow machine.

*Responsibilities*

My responsibilities as _architect_ and _developer_ for Kemper were as follows:

*   Separate out the document generation logic and create COM components for the server
*   Install SOAP on the server and plan the rollout of SOAP to all APLUS client machines in the field
*   Modify APLUS client application to interface with the server through SOAP
*   Created and executed load tests to ensure document server could handle many document requests simultaneously

### Kemper Insurance - TelePlus

_May 2001 - Jun 2001_

TelePlus is the online system that claims operators use to take claim information over the phone. TelePlus is mostly a COBOL application with a semi-GUI front end. Kemper is in the process of replacing the front end with a web-based front end served in the Internet Explorer browser. My responsibility was to review all front end screens and document the conversion of those screens to web page equivalents. I was also required to review the COBOL code and identify key business logic which could be moved to an NT middle tier.

*Responsibilities*

My responsibilities as _business analyst_ for TelePlus were as follows:

*   Review GUI front end and map migration of each screen to HTML equivalent
*   Identify issues related to sessionless web environment
*   Review COBOL code and document logic to be moved to NT middle tier

### Kemper Insurance - JPI Legal Bill Review System

_Nov 2000 - Apr 2001_

Kemper receives over $200 million in legal bills from over 700 law firms which it does business with. Ideally, each legal bill is audited for compliance with the services agreement between Kemper and the law firm. The average legal bill is generally 10-20% overstated. In other words, the majority of law firms charge Kemper more than they are allowed to in their agreement with Kemper. Unfortunately, only a handful of internal auditors are on staff to perform these audits and, hence, the vast majority - over 80% - of the legal bills go unaudited. If these legal bills could be audited, Kemper would save millions per year in legal fees.

The JPI system allows law firms to submit legal bills to Kemper electronically for payment. The system performs an automatic audit on the invoices in the electronic document based on a set of threshold rules and math checks. Some reductions are made automatically. Other invoice line items are flagged for manual review by internal auditors. The system then provides tools for the auditor to do the audit more quickly. After an invoice is complete, an Explanation of Payment (EOP) is sent to the claim adjuster and made available to the law firm via an online "inbox" provided by the external site. Emails are sent to the adjuster using AspQMail and Lotus Notes.

As architect and developer on this project, I was responsible for designing and building the manual review interface and for designing and building an interface which allows admin personnel to set up law firms, agreements, roles, timekeepers, and other key items in the database. I was also responsible for overseeing the design and construction of the law firm interface as well as implementation of certain business rules in the overall system. I was responsible for maintaining the DB2 and SQL Server 7 versions of the ERD. DB2 was the production database but both Access and SQL Server 7 were used in prototyping.

I was responsible for the architecture of the system overall and its integration with existing Kemper facilities. I was responsible for selecting and configuring the web server and application server hardware. External user logon is performed by Webthority against the enterprise LDAP server. The proxy server maintains the 128-bit SLL certificates. The web sites are hosted on two web servers with business components residing on an application server. The web servers have hardware-based load balancing using Network Dispatcher. The web servers are running NT 4 with IIS 4. The application server is running NT 4 and ADO 2.5. Data access is restricted to the application server for security reasons. All business and data access components are located on the application server and referenced on the web servers via DCOM.

The internal web site is comprised of almost 9,000 lines of ASP code across over 30 web documents. A single COM object is used and is comprised of over 3,000 lines of Visual Basic 6 code. The invoice loader application is an additional 2,000 lines of VB code. I was responsible for the code reviews of the external site and the EOP object.

*Responsibilities*

My responsibilities as _architect_ and _developer_ for Kemper were as follows:

*   Maintain the DB2 and SQL Server 7 ERD files using ERwin
*   Design, construct, and test the invoice loader application
*   Design, construct, and test the manual review application
*   Design, construct, and test the system maintenance application
*   Write functional and technical documentation for all applications and participate in knowledge transfer to other developers
*   Participate in numerous design and project status meetings
*   Interview client for interface design requirements and general business process analysis
*   Help create test data and test cases
*   Specify the architecture used for the system
*   Specify the hardware requirements and validate against delivered hardware
*   Work with security architects to ensure safe, secure availability of system
*   Project management duties during the testing and implementation phase of the project

### Kemper Insurance - APLUS Architecture Migration Assessment

_Nov 2000_

This was a short, two week engagement. I was contracted by Kemper to analyze a small, 2-tier application written in VB with an IBM DB2 Universal Database backend. The application was originally intended only for departmental use. The application was very successful and popular, though, and had been rewritten and / or extended for three additional lines of business. I examined two versions of the application and documented a migration path to convert them from the 2-tier architecture to a scaleable 3-tier architecture using VB and COM, ASP, MTS, and the existing DB2 database. I analyzed each form and code module in the VB application and documented the complexities of the forms and the functions in the code. I itemized the tasks for separating the application into 3 tiers. I assessed the current IIS infrastructure and made recommendations for maximizing performance, scalability, and availability. I also assessed the possibility of deploying the application using CITRIX nFuse as a quick method of getting the application out to users on the web. Finally, I assessed the challenges in interfacing the application with existing or pending CORBA Java components using a COM / CORBA bridge or SOAP.

*Responsibilities*

My responsibilities as _enterprise architect_ for Kemper were as follows:

*   Analyze existing VB 6 forms and code modules
*   Analyze existing DB2 schema and SQL statements
*   Meet with various business owners and managers to determine scalability requirements
*   Redesign application using ASP and VB6 COM
*   Write comprehensive migration plan, including project plan with resource and work estimates
*   Write Executive Summary describing migration strategy
