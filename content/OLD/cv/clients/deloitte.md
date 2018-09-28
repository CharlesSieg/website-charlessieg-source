
### Deloitte - DESC

_2005 - 2010_

I moved to the DESC - Deloitte Entity Search and Compliance - project in 2005. DESC is a critical risk management system for DTT as it is where new opportunities are vetted for compliance across a variety of strict standards.

Primarily an ASP.NET application with a clustered SQL Server persistent store, DESC is the perfect example of a modern web application with heavy demands across many architectural measurements:

**Performance.** Used thousands of times daily by partners and other practitioners, the performance of DESC application had to be fast enough that these valuable employees were not wasting time waiting for slow page loads or inefficient queries.

**Availability.** DESC is a mission critical application. Unexpected downtime was not acceptable. High availability was provided through robust handling of error scenarios at the code level as well as through provisioning redundant hardware to eliminate single points of failure.

**Scalability.** DESC was designed to be installed on as many web servers as needed in order to scale out and meet the performance requirements of the application.

**Securability.** DESC contains an incredible amount of sensitive data and, thus, security was a paramount concern. Beyond normal authentication requirements, the data and the actions within the application required proper authorization. For example, for a given entity, only authorized parties were allowed to view certain details about the entity or to perform various actions for this entity. This authorization was provided through a complex data-driven rules engine that analyzed both the entity as well as its relationships to other entities and inbound changes that were dynamically applied to the entity structure.

**Maintainability.** DESC is a very complex application but was designed in a structured way such that each significant component is maintainable on its own without having to understand the rest of the system. Appropriate unit test coverage was provided so that components could be refactored by new developers without jeopardizing the correctness of existing code. New developers would only have to become familiar with a single component before delivering useful code.

**Deployability.** The DESC application was packaged as a set of assemblies which could be deployed automatically by IT staff to servers throughout the data center with minimal external dependencies and configuration.

**Extensibility.** Entity compliance is an ever-changing domain and, as such, any application in the space must be easily extended so that new rules can be injected into the various approval workflows. The DESC application was written such that these rules, as well as other significant components, were distinct, testable pieces of the system. Rules and components could be created and added on demand while others could be modified in place or removed, all with the system dynamically updating accordingly.

### Deloitte - Deloitte Platform

_Jul 2002 - 2005_

I was brought onto the Deloitte Platform project at the end of July 2002. The Deloitte Platform is a global initiative within the DTT Global Office of Information Management to create a Web Services-based reusable architecture for deploying future globally-accessible web applications.

Initially my role was as software engineer in a Proof of Concept project where it was demonstrated that a number of existing applications and data stores could be exposed via a Web Services interface and hosted inside of two separate enterprise portals, SAP Enterprise Portal and Microsoft SharePoint Portal Server. I built a Web Service using C# in Microsoft Visual Studio.NET which encapsulated two Lotus Notes databases and made them searchable in the two portals. The Web Service was published in the UDDI directory hosted on our Microsoft Windows.NET Server. The Proof of Concept was a success and resulted in a change of strategy.

Instead of building a number of custom Web Services to provide portal functionality such as single sign on, search, and collaborative workspaces, the decision was made to partner with a number of 3rd party vendors and expose their existing functionality through Web Services interfaces.

My role changed to technical architect and I began a long process of evaluating 3rd party products for use in the portal. DTT uses both SAP Enterprise Portal and Microsoft's SharePoint so all proposed solutions must work seamlessly with both portals. The products evaluated include the following: Verity K2 Enterprise, Vignette Content Management Suite, eRoom v5 and v6, Groove, Epicentric Modular Web Services, Netegrity SiteMinder, and Documentum. For each of these products I wrote an in-depth technical evaluation.

Upon final selection of the key products, which include all of the above except for Epicentric and Documentum, I was tasked with creating a global infrastructure to upport a full lifecycle deployment of the Deloitte Platform. Working with in-house and external administrators, I devised an infrastructure supporting development, QA, staging, and production for deployment in the United States, United Kingdom, and a to-be-decided Asia / Pacific installation. The development environment consisted of 9 servers and scaled up to an initial 20 server installation in production, supporting 15,000 users. The architecture is scaleable and will eventually support 150,000 internal and external users and will host the three major web sites for DTT including Deloitte.com, Deloitte Resources (intranet), and Deloitte Online (extranet).

*Responsibilities*

My responsibilities as technical _architect_ for DTT were as follows:

*   Build a prototype portal in SAP EP and SharePoint demonstrating Web Service integration with Lotus Notes database
*   Create global infrastructure plan supporting development, QA, staging, and production
*   Evaluate and document use of 3rd party tools, including Verity, Vignette, eRoom, and Netegrity
*   Participate in numerous design and project status meetings
