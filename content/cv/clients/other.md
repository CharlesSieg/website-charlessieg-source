### AON - Web-Based Field Quoting Application

_Jul 2001_

AON was in the process of writing an web-based application to allow agents in the field to capture customer information at the customer site, get online, submit the information, and retrieve a quote for the proposed coverages. The application was to be run on the agent's laptop using Personal Web Server. A local SQL Server database contained the customer and quote data and was replicated with the master SQL Server database in the office.

I was brought in to assist in meeting the proposed deadline and became responsible for the web application. The architect directed me to create an XML document definition to contain the variables captured in the customer coverage application interview. Each page would collect the data, insert it into the XML document, and pass the document to the next page to persist the data. All of this was done using ASP written in JScript and JScript classes.

*Responsibilities*

My responsibilities as _developer_ for AON were as follows:

*   Create the Active Server Pages
*   Create the DTD to capture all customer application information
*   Create the JScript classes to persist the XML document
*   Participate in numerous design and project status meetings

### Comro.com - Internet Web Site

_Sept 2000 - Oct 2000_

Comro.com's original Internet site was built using a 2-tier architecture. When I started at Comro my first responsibilities were to help them finish moving the original site over to a 3-tier architecture using ASP, VB COM, and SQL Server 7. I was responsible for the RFP functionality, the region maps, modifications to property searches, and the Comro Direct functionality. Each area required five to a dozen functions in a COM object and usually a half dozen stored procedures. Once the site had been migrated to the new architecture, it was moved to the production servers.

The Comro Direct and RFP features both used CDO and scheduled NT processes to automate sending of user email messages.

Comro did not have a replication architecture in place prior to my arrival. They also did not have separate development and staging environments or solid code promotion procedures. I contributed significantly in planning and deciding how to implement replication and how to design and promote between a multi-stage server environment.

*Responsibilities*

My responsibilities as a _web developer_ and _SQL programmer_ for Comro.com were as follows:

*   Create new tables and indexes as needed to support changes to application features
*   Create new stored procedures and modify existing stored procedures to support changes to application features
*   Implement snapshot, transactional, and merge replication between development, staging, and production environments
*   Set up DRI in application databases
*   Create triggers to manage foreign key-like relationships between tables
*   Optimize SQL stored procedures
*   Write, test, and promote COM objects using Visual Basic 6 Enterprise Edition
*   Create packages in MTS; manage existing packages and package security
*   Write new ASP pages; modify and debug existing ASP code
*   Use PC AnyWhere to remotely manage development server
*   Manage Visual Source Safe databases
*   Participated in team design and planning meetings
*   Write Functional Design documentation

### HTS Consulting, Inc. - Nalco Project Proposal

_Aug 2000 - Sept 2000_

HTS contracted me as an interim practice manager for their new e-commerce practice. They had an immediate opportunity with Nalco that required quick business requirements gathering and analysis. I attended several client meetings with the HTS account manager to interview key client personnel. During these interviews I documented the requirements of the applications needed and other details which I would use to assess the complexity of the project and estimate an accurate work effort. After the client interviews I went back and broke the project down into several stages for each application. For each application I identified technologies which I believed would yield the best cost-benefit ratio. For each stage I identified the resources needed and assigned tasks to each resource. When the project plan was complete I created a formal project proposal which documented the overall scope of the project and detailed costs and schedule estimates. Once HTS approved the project proposal, we submitted it to the client.

*Responsibilities*

My responsibilities as interim _practice manager_ for HTS were as follows:

*   Attend client interviews and gather business and applications requirements from client personnel during these interviews
*   Take requirements and assess technical complexity of applications
*   Break application and requirements down into a multi-stage, step-by-step plan
*   Itemize deliverables obtained out of successful completion of plan
*   Identify resources required to deliver successful project
*   Work with HTS to estimate costs of resources and overall project
*   Create project proposal for client to use in comparisons against other firms' proposals
*   Work with HTS sales and recruiting staff to build resource pipeline and win client business

### Arthur Andersen, LLP - EOR, BADA, QARM, Fraud, BPO, BRCA

_Apr 2000 - Jul 2000_

When I first started at Arthur Andersen, my responsibility was to learn the EOR application and to begin debugging the existing version. When a bug is reported, a System Investigation Request (SIR) is created by the tester and assigned by management to one of the developers. I completed several dozen major SIRs, the application was promoted to production, and the EOR code base was used to generate additional applications: QARM, Fraud, BPO, and BRCA. Each application was then customized to the specific requirements of the application sponsor.

There were approximately 100 ASP pages, written with VBScript, in the EOR application with a significant amount of embedded JavaScript routines. There were also about 50 SQL stored procedures and several COM objects served via MTS. The database used was SQL Server 7 running on NT 4.

One of the other responsibilities I had was to manage a daily data migration between application data stores on several SQL Servers, some V6.5 and some V7.0. The migration code was encapsulated inside of several DTS packages and scheduled with the SQL Server Agent. The packages moved approximately 600,000 records each day, some requiring BCP due to translation of code page specific characters to Unicode (nvarchar). Replication was investigated, proven, and is due to be implemented in the environment soon.

Several application components and modules were written in Visual Basic, compiled, and promoted to production to run when needed or on a scheduled basis. One of the applications used CDO and SMTP to automate emailing statistical reports to management.

Another task required me to use the Wise Installation system to create installation executables to install EOR-based applications on multiple web servers. The installation was required to set up ODBC connections, install COM objects into MTS, and install all ASP code and HTML pages.

*Responsibilities*

My responsibilities as a _web developer_ and _SQL programmer_ for the various Arthur Andersen applications were as follows:

*   Make SQL scripts to implement changes to database schema; promote the changes from development to beta to production
*   Write SQL stored procedures; debug existing stored procedures
*   Set up DRI in application databases; write triggers to ensure additional integrity
*   Optimize queries within existing SQL stored procedures
*   Create, test, and promote DTS packages to handle complex, multi-step SQL tasks on a scheduled basis
*   Create tables, indexes, and other database objects for applications
*   Write, test, and promote COM objects using Visual Basic 6
*   Manage MTS component usage
*   Write new ASP code; debug existing ASP code
*   Write JavaScript routines; debug existing JavaScript routines
*   Manage code promotions from development to testing to beta to production
*   Use Timbuktu Pro to remotely manage development, test, and beta servers
*   Manage and set up Visual Source Safe databases
*   Write HTML help files for all applications
*   Redesign screen layouts and artwork for all applications
*   Participated in team design and planning meetings


