USWeb/CKS

Project Manager, Architect

# McDonald’s Corporation – Corporate Intranet (Archie)
## May 1999 - September 1999


McDonald’s hired USWeb to lead the effort in building their corporate Intranet, later called “Archie”. The Intranet was to be rolled out to the 3,000 or so Oak Brook employees with a view toward rolling out to all 8,000 or so US domestic employees. Access to some Intranet applications would be given to McDonald’s suppliers via extranet and to the Owner / Operator stores. The Intranet would then be rolled out internationally after that. When I left they were beginning to roll out to Sweden using Domino R5.

I was the project manager, lead architect, and LotusScript and ASP coder. The system was hosted in various point releases of R4.6.x of Lotus Domino and IIS 4 on NT 4. All of the Intranet data – articles, press releases, etc. – were stored in Notes databases for security reasons. The home page of the Intranet was hosted on NT as was the content editor. The home page was made up of modules which were periodically updated by an NT service. The NT service would connect to Notes through ODBC (not easy) and pull headlines and article summaries out of the database to populate these modules. In addition, there was a polling / survey module which had its data stored in an Access 97 database. The content management interface was used by almost 100 content managers throughout the organization to post their articles and other content. The content management interface was in Notes but the forms where the actually content editing was done was ASP because of a dependence on DHTML and IFRAMEs.

### Responsibilities

* Key architect in planning and designing corporate Intranet for global organization of 10,000+ users
* Led team design and development status meetings
* Wrote requirements, architecture, app spec, detailed design docs
* Used evolutionary prototyping to deliver incremental features implementations and revisions
* Monitored and reviewed usability studies
* Planned information architecture (navigation)
* Coded search module for Intranet
* Coded ASP for content editing tools
* Created and maintained project plan to deliver two versions of Intranet under budget and on schedule
* Evaluated 3rd party tools
* Wrote status reports and led management team status meetings
* Assisted in identifying key business applications for conversion to Intranet
* Assisted in infrastructure planning for 3-5 year implementation plan
* Performed testing on Intranet deliverables
* Assisted in migration from development to staging to production
* Assisted and reviewed server and application stress / load tests