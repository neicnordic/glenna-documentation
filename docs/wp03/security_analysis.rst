Security Analysis, Test and Evaluation
======================================

In this section we discuss about the tasks we have done with respect to the analysis and evaluation of the security mechanisms used in the cloud infrastructure of the service providers within Glenna. When we refer to Glenna, it roughly has two components. First is the cloud infrastructure in use by the participating countries. Due to resource limitations and the different status the participating institutes were on with respect to cloud deployment and service adoption, it was not possible to make a uniform and detailed security analysis. As an alternative however we made a survey to check the state of the art in the security mechaisms of the cloud service providers by preparing a questionnaire and collect information that we found necessary for Glenna project. The questionnaire was distributed to four cloud service providers and we have received three responses. The questionnaire is annexed in the NEIC glenna wiki page and can be referred from there. 

The second component in Glenna is the mechanism used to enable federated authentication to make the available cloud services accessible to users. Within the participating cloud service providers there were two federated autentication solutions used : 

* kalmar2: by DeIC for Data.dk service and by USIT for Lifeportal and 

* Dataporten: by UH-IaaS as a way to connect to openstack keystone module

In this way service providers make thier service available by authenticating users through federated auhtentication solution and without users' authentication credential within the cloud service provider's premise. In Data DeIC for instance, users can access the data storage service after authentication through kalmar2. In UH-IaaS, users can login to the openstack based cloud service through Dataporten. In both cases the federated authentication solutions are based on industry standards and users' credentials are handled in a secure manner. For more information on security in kalmar2 and Dataporten please refer to (https://www.kalmar2.org/kalmar2web/members_attchmt/appendix_A_2010_10_25.pdf)  and (https://www.uninett.no/tjenester/dataporten/personvern-og-informasjonssikkerhet).   

Based on the responses we got from the quesionnare, 


In addition to the questionnaire we put our focus on major security threats to cloud infrastuructre that can possibly materialize in the cloud infrastructure within glenna. The CSA has done some concrete tasks with respect to identifying measures required to deal with various treats to cloud infrastructure and we mapped the possible threats to Glenna with measures required to mitigate with them and we advise the cloud service providers to consider those identified measures inorder to secure thier cloud and related IT infrastructure. In the next section we briefly discuss about the required measuers which CSA refer them as Cloud Control Matrix (CCM)


Whati is CCM?
*************

The Cloud Security Alliance (CSA), which is one of the leading organizations that are working towards secure and resilient cloud services for organizations and for individual users that use cloud services in their day-to-day activities. The activities of CSA also include guiding cloud service providers to offer their services and solutions in a way that is compliant to different international and local standards and at the same time satisfy additional needs of cloud service customers and users. 

One of the working groups at CSA produced “Cloud Control Matrix (CCM)” which is specifically designed to provide fundamental security principles to guide cloud vendors and to assist prospective cloud customers in assessing the overall security risk of a cloud provider []. This makes it an interesting work and a potential input for Glenna that includes stakeholders that will be both cloud vendors as well as customers. One of the most useful aspects of the CCM is that it is mapped to many other major industry standards, controls and frameworks [] - 

* HIPAA and HITECH Act
* ISO/IEC 27001-2005
* NIST SP800-53 R3
* PCI DSS 2.0
* Generally Accepted Privacy Principles, or GAPP
* Jericho Forum
* FedRAMP

Based on the work of CSA and their documentation, one can easily map a given control from CCM to the controls of all of the above standards and frameworks. The CCM gives a detailed explanation of security concepts and principles by categorizing them in groups. The first version of CCM (V1.1) was published in 2010 and it comprises 98 controls within 10 groups. The last version of CCM (V.3.0.1), which is published in 2014, comprises 133 controls grouped under 16 domains. The domains cover a large variety of security principles and concepts that can address security related issues in cloud computing. 

1. Application and Interface Security (AIS)
2. Audit Assurance and Compliance (AAC)
3. Business Continuity and Management and Operational Resilience (BCR)
4. Change Control and Configuration Management (CCM)
5. Data Security and Information Lifecycle Management (DSI)
6. Datacenter Security (DSC)
7. Encryption and Key Management (EKM)
8. Governance and Risk Management (GRM)
9. Human Resource Security (HRS)
10. Identity and Access Management (IAM)
11. Infrastructure and Virtualization (IVS)
12. Interoperability and Portability (IPY)
13. Mobile Security (MOS)
14. Security Incident Management, E-Disc and Cloud Forensics (SEF)
15. Supply Chain Management, Transparency and Accountability (STA)
16. Threat and Vulnerability Management (TVM) 

Identifying Required Controls
**************************************

The higher number of controls included in CCM makes it applicable in various cloud service provisions and application domains. For cloud service providers, it´s not a requirement to comply with all the controls and it might not also be feasible. But one can find applicable controls based on the security needs and risks associated with the target cloud service. One approach to identify the required controls is by using Consensus Assessments Initiative Questionnaire (CAIQ). The CAIQ is a set of questions a cloud consumer and cloud auditor may wish to ask of a cloud provider. It provides a series of “yes” or “no” controls assertion questions, which can then be tailored to suit each unique cloud customer´s evidentiary requirements []. However, in Glenna the cloud service provider and the consumer are working as partners and with interchangeable roles (not in a formal client and vendor service provision model). Some of the services are also already live in production and inducing additional security requirements from clients to the vendors may not be feasible. 
We suggest the use of another requirement identification that can make the cloud service provision secure and by at the same time satisfying common security requirements from the main users. The method we found feasible is the use of common threats on cloud computing as a base to identify the most important controls from the CCM. Even if users within Glenna don't make the selection conrols directly, there is an acceptable level of certainity that the users need shall be addressed by addressing the common security threats. 

The CSA has identified “The Notorious Nine: Cloud Computing Top Threats” in 2013 and gave suggestions on which cloud controls can help to mitigate with these common and critical threats. Basing the control selection on these can help us address the common security issues that shall arise on the infrastructures of the cloud service providers within Glenna.

The Notorious Nine Cloud Computing Top Threats are [https://downloads.cloudsecurityalliance.org/initiatives/top_threats/The_Notorious_Nine_Cloud_Computing_Top_Threats_in_2013.pdf] –

1. Data Breaches
2. Data Loss
3. Account Hijacking
4. Insecure APIs 
5. Denial of Service
6. Malicious Insiders
7. Abuse of Cloud Services
8. Insufficient Due Diligence
9. Shared Technology Issues

These are the top threats that materialized on cloud infrastructures and implementing controls against these threats can help to secure a cloud infrastructure from future similar and potential incidents or attacks. 

The controls for each threat are identified from the CCM V 1.0 and V 3.0.1. At the time of the publication of the top threats, the available CCM version was V 1.0 and CSA has suggested controls from the list of controls in version 1.0. At the time of this writting, the latest CCM version is (V 3.0.1) and in order to entertain these latest measures in our project, we made mapping of those controls from V 1.0 (suggested to the Top Cloud Computing Threats) to the controls in CCM version 3.0.1. 

Each control in the CCM is identified by a unique ID that comprises the category of the control (three alphabets for controls in version 3.01.1 and two alphabets in V 1.0) and a number. For instance Identity & Access Management controls are identified by IAM followed by a number (e.g. IAM-01) in CCM V 3.0.1. On the other hand, V 1.0 refers "Security Architecture - User ID Credentials" as SA followed by a number (e.g. SA-01).

In the following section we listed the top nine cloud computing threats and the controls that are suggested for each threat. For ease of reference we put the ID of the control from v 3.0.1 followed by the id of a similar control in the previous version (which is put in bracket). As shown below for each threat there is a list of controls that one can use to mitigate with. For Threat 1 for instance there are 11 suggested controls. All required controls for the nine notorious cloud security threats are listed in the section below. Please note that, controls that are described in one threat will not be described again in another threat to avoid repeatition. 

Threat 1: Data Breaches
*********************

**BCR-11 (DG-04): Business Continuity Management & Operational Resilience Retention Policy**

**Description:** Policies and procedures shall be established, and supporting business processes and technical measures implemented, for defining and adhering to the retention period of any critical asset as per established policies and procedures, as well as applicable legal, statutory, or regulatory compliance obligations. Backup and recovery measures shall be incorporated as part of business continuity planning and tested accordingly for effectiveness.

**DSI-07 (DG-05): Data Security & Information Lifecycle Management Secure Disposal**

**Description:** Any use of customer data in non-production environments requires explicit, documented approval from all customers whose data is affected, and must comply with all legal and regulatory requirements for scrubbing of sensitive data elements.

**DSI-05 (DG-06): Data Security & Information Lifecycle Management Non-Production Data**

**Description:** Production data shall not be replicated or used in non-production environments.

**AIS-04 (DG-07): Application & Interface Security Data Security / Integrity**

**Description:** Policies and procedures shall be established and maintained in support of data security to include (confidentiality, integrity and availability) across multiple system interfaces, jurisdictions and business functions to prevent improper disclosure, alteration, or destruction.

**GRM-02 (DG-08): Governance and Risk Management Data Focus Risk Assessments**

**Description:** Risk assessments associated with data governance requirements shall be conducted at planned intervals and shall consider the following:

* Awareness of where sensitive data is stored and transmitted across applications, databases, servers, and network infrastructure
* Compliance with defined retention periods and end-of-life disposal requirements
* Data classification and protection from unauthorized use, access, loss, destruction, and falsification

**EKM-03 (IS-18): Encryption & Key Management Sensitive Data Protection**

**Description:** Policies and procedures shall be established, and supporting business processes and technical measures implemented, for the use of encryption protocols for protection of sensitive data in storage (e.g., file servers, databases, and end-user workstations), data in use (memory), and data in transmission (e.g., system interfaces, over public networks, and electronic messaging) as per applicable legal, statutory, and regulatory compliance obligations.

**EKM-02 (IS-19): Encryption & Key Management Key Generation**

**Description:** Policies and procedures shall be established for the management of cryptographic keys in the service's cryptosystem (e.g., lifecycle management from key generation to revocation and replacement, public key infrastructure, cryptographic protocol design and algorithms used, access controls in place for secure key generation, and exchange and storage including segregation of keys used for encrypted data or sessions). Upon request, provider shall inform the customer (tenant) of changes within the cryptosystem, especially if the customer (tenant) data is used as part of the service, and/or the customer (tenant) has some shared responsibility over implementation of the control.

**IAM-12 (SA-02): Identity & Access Management User ID Credentials**

**Description:** Internal corporate or customer (tenant) user account credentials shall be restricted as per the following, ensuring appropriate identity, entitlement, and access management and in accordance with established policies and procedures:

* Identity trust verification and service-to-service application (API) and information processing interoperability (e.g., SSO and Federation)
* Account credential lifecycle management from instantiation through revocation
* Account credential and/or identity store minimization or re-use when feasible
* Adherence to industry acceptable and/or regulatory compliant authentication, authorization, and accounting (AAA) rules (e.g., strong/multi-factor, expireable, non-shared authentication secrets)

**AIS-04 (SA-03): Application & Interface Security Data Security / Integrity**

**Description:** Policies and procedures shall be established and maintained in support of data security to include (confidentiality, integrity and availability) across multiple system interfaces, jurisdictions and business functions to prevent improper disclosure, alteration, or destruction.

**IVS-08 (SA-06): Infrastructure & Virtualization Security Production / Non-Production Environments**

**Description:** Production and non-production environments shall be separated to prevent unauthorized access or changes to information assets. Separation of the environments may include: stateful inspection firewalls, domain/realm authentication sources, and clear segregation of duties for personnel accessing these environments as part of their job duties.

**IAM-12 (SA-07): Identity & Access Management User ID Credentials**

**Description:** Internal corporate or customer (tenant) user account credentials shall be restricted as per the following, ensuring appropriate identity, entitlement, and access management and in accordance with established policies and procedures:

* Identity trust verification and service-to-service application (API) and information processing interoperability (e.g., SSO and Federation)
* Account credential lifecycle management from instantiation through revocation
* Account credential and/or identity store minimization or re-use when feasible
* Adherence to industry acceptable and/or regulatory compliant authentication, authorization, and accounting (AAA) rules (e.g., strong/multi-factor, expireable, non-shared authentication secrets)

Threat 2: Data Loss
*******************

**BCR-11 (DG-04)**

**GRM-02 (DG-08)**

**BCR-05 (RS-05): Business Continuity Management & Operational Resilience Environmental Risks**

**Description:** Physical protection against damage from natural causes and disasters, as well as deliberate attacks, including fire, flood, atmospheric electrical discharge, solar induced geomagnetic storm, wind, earthquake, tsunami, explosion, nuclear accident, volcanic activity, biological hazard, civil unrest, mudslide, tectonic activity, and other forms of natural or man-made disaster shall be anticipated, designed, and have countermeasures applied.

**BCR-06 (RS-06): Business Continuity Management & Operational Resilience Equipment Location**

**Description:** To reduce the risks from environmental threats, hazards, and opportunities for unauthorized access, equipment shall be kept away from locations subject to high probability environmental risks and supplemented by redundant equipment located at a reasonable distance.

Threat 3: Account or Service Traffic Hijacking	
**********************************************

**IAM-02 (IS-07): Identity & Access Management Credential Lifecycle / Provision Management**

**Description:** User access policies and procedures shall be established, and supporting business processes and technical measures implemented, for ensuring appropriate identity, entitlement, and access management for all internal corporate and customer (tenant) users with access to data and organizationally-owned or managed (physical and virtual) application interfaces and infrastructure network and systems components. These policies, procedures, processes, and measures must incorporate the following:

* Procedures and supporting roles and responsibilities for provisioning and de-provisioning user account entitlements following the rule of least privilege based on job function (e.g., internal employee and contingent staff personnel changes, customer-controlled access, suppliers' business relationships, or other third-party business relationships)
* Business case considerations for higher levels of assurance and multi-factor authentication secrets (e.g., management interfaces, key generation, remote access, segregation of duties, emergency access, large-scale provisioning or geographically-distributed deployments, and personnel redundancy for critical systems)
* Access segmentation to sessions and data in multi-tenant architectures by any third party (e.g., provider and/or other customer (tenant))
* Identity trust verification and service-to-service application (API) and information processing interoperability (e.g., SSO and federation)
* Account credential lifecycle management from instantiation through revocation
* Account credential and/or identity store minimization or re-use when feasible
* Authentication, authorization, and accounting (AAA) rules for access to data and sessions (e.g., encryption and strong/multi-factor, expireable, non-shared authentication secrets)
* Permissions and supporting capabilities for customer (tenant) controls over authentication, authorization, and accounting (AAA) rules for access to data and sessions
* Adherence to applicable legal, statutory, or regulatory compliance requirements

**IAM-08 and IAM-09 (IS-08): Identity & Access Management Trusted Sources (IAM-08) and Identity & Access Management User Access Authorization (IAM-09)**

**IAM-08**

**Description:** Policies and procedures are established for permissible storage and access of identities used for authentication to ensure identities are only accessible based on rules of least privilege and replication limitation only to users explicitly defined as business necessary.

**IAM-009**

**Description:** Provisioning user access (e.g., employees, contractors, customers (tenants), business partners and/or supplier relationships) to data and organizationally-owned or managed (physical and virtual) applications, infrastructure systems, and network components shall be authorized by the organization's management prior to access being granted and appropriately restricted as per established policies and procedures. Upon request, provider shall inform customer (tenant) of this user access, especially if customer (tenant) data is used as part the service and/or customer (tenant) has some shared responsibility over implementation of control.

**IAM-11 (IS-09): Identity & Access Management User Access Revocation**

**Description:** Timely de-provisioning (revocation or modification) of user access to data and organizationally-owned or managed (physical and virtual) applications, infrastructure systems, and network components, shall be implemented as per established policies and procedures and based on user's change in status (e.g., termination of employment or other business relationship, job change or transfer). Upon request, provider shall inform customer (tenant) of these changes, especially if customer (tenant) data is used as part the service and/or customer (tenant) has some shared responsibility over implementation of control.

**IAM-10 (IS-10): Identity & Access Management User Access Reviews**

**Description:** User access shall be authorized and revalidated for entitlement appropriateness, at planned intervals, by the organization's business leadership or other accountable business role or function supported by evidence to demonstrate the organization is adhering to the rule of least privilege based on job function. For identified access violations, remediation must follow established user access policies and procedures.

**SEF-02 (IS-22): Security Incident Management, E-Discovery & Cloud Forensics Incident Management**

**Description:** Policies and procedures shall be established, and supporting business processes and technical measures implemented, to triage security-related events and ensure timely and thorough incident management, as per established IT service management policies and procedures.

**IAM-12 (SA-02)**

**IAM-12 (SA-07)**

**IVS-01 (SA-14): Infrastructure & Virtualization Security Audit Logging / Intrusion Detection**

**Description:** Higher levels of assurance are required for protection, retention, and lifecycle management of audit logs, adhering to applicable legal, statutory or regulatory compliance obligations and providing unique user access accountability to detect potentially suspicious network behaviors and/or file integrity anomalies, and to support forensic investigative capabilities in the event of a security breach.

Threat 4: Insecure Interfaces and APIs
**************************

**IAM-08 and IAM-09 (IS-08)**

**AIS-04 (SA-03)**

**AIS-01 (SA-04): Application & Interface Security Application Security**

**Description:** Applications and programming interfaces (APIs) shall be designed, developed, deployed, and tested in accordance with leading industry standards (e.g., OWASP for web applications) and adhere to applicable legal, statutory, or regulatory compliance obligations.

Threat 5: Denial of Service
******************
**GRM-01 (IS-04): Governance and Risk Management Baseline Requirement**

**Description:** Baseline security requirements shall be established for developed or acquired, organizationally-owned or managed, physical or virtual, applications and infrastructure system and network components that comply with applicable legal, statutory and regulatory compliance obligations. Deviations from standard baseline configurations must be authorized following change management policies and procedures prior to deployment, provisioning, or use. Compliance with security baseline requirements must be reassessed at least annually unless an alternate frequency has been established and authorized based on business need.

**IVS-04 (OP-03): Infrastructure & Virtualization Security Information System Documentation**

**Description:** The availability, quality, and adequate capacity and resources shall be planned, prepared, and measured to deliver the required system performance in accordance with legal, statutory, and regulatory compliance obligations. Projections of future capacity requirements shall be made to mitigate the risk of system overload.

**BCR-08 (RS-07): Business Continuity Management & Operational Resilience Equipment Power Failures**

**Description:** Protection measures shall be put into place to react to natural and man-made threats based upon a geographically-specific Business Impact Assessment

**AIS-01 (SA-04)**

Threat 6: Malicious Insiders
************************

**STA-09 (CO-03): Supply Chain Management, Transparency and Accountability Third Party Audits**

**Description:** Third-party service providers shall demonstrate compliance with information security and confidentiality, access control, service definitions, and delivery level agreements included in third-party contracts. Third-party reports, records, and services shall undergo audit and review at least annually to govern and maintain compliance with the service delivery agreements.

**DSI-06 (DG-01): Data Security & Information Lifecycle Management Ownership / Stewardship**

**Description:** All data shall be designated with stewardship, with assigned responsibilities defined, documented, and communicated.

**DSI-01 (DG-03): Data Security & Information Lifecycle Management  Classification**

**Description:** Data and objects containing data shall be assigned a classification by the data owner based on data type, value, sensitivity, and criticality to the organization.

**DSI-04 (DG-07): Data Security & Information Lifecycle Management Handling / Labeling / Security Policy**

**Description:** Policies and procedures shall be established for the labeling, handling, and security of data and objects which contain data. Mechanisms for label inheritance shall be implemented for objects that act as aggregate containers for data.
**DCS-09 (FS-02): Datacenter Security User Access**

**Description:** Physical access to information assets and functions by users and support personnel shall be restricted.

**DCS-08 (FS-05): Datacenter Security Unauthorized Persons Entry**

**Description:** Ingress and egress points such as service areas and other points where unauthorized personnel may enter the premises shall be monitored, controlled and, if possible, isolated from data storage and processing facilities to prevent unauthorized data corruption, compromise, and loss.


**DCS-04 (FS-06): Datacenter Security Off-Site Authorization**

**Description:** Authorization must be obtained prior to relocation or transfer of hardware, software, or data to an offsite premises.

**HRS-02 (HR-01): Human Resources Background Screening**

**Description:** Pursuant to local laws, regulations, ethics, and contractual constraints, all employment candidates, contractors, and third parties shall be subject to background verification proportional to the data classification to be accessed, the business requirements, and acceptable risk.

**GRM-07 (IS-06): Governance and Risk Management Policy Enforcement**

**Description:** A formal disciplinary or sanction policy shall be established for employees who have violated security policies and procedures. Employees shall be made aware of what action might be taken in the event of a violation, and disciplinary measures must be stated in the policies and procedures.

**IAM-08 and IAM-09 (IS-08)**

**IAM-10 (IS-10)**

**HRS-07 (IS-13): Human Resources Roles / Responsibilities**

**Description:** Roles and responsibilities of contractors, employees, and third-party users shall be documented as they relate to information assets and security.

**IAM-05 (IS-15): Identity & Access Management Segregation of Duties**

**Description:** User access policies and procedures shall be established, and supporting business processes and technical measures implemented, for restricting user access as per defined segregation of duties to address business risks associated with a user-role conflict of interest.

**EKM-03 (IS-18)**

**EKM-02 (IS-19)**

**IAM-01 (IS-29): Identity & Access Management Audit Tools Access**

**Description:** Access to, and use of, audit tools that interact with the organization's information systems shall be appropriately segmented and restricted to prevent compromise and misuse of log data.

**GRM-10 (RI-02): Governance and Risk Management Risk Assessments**

**Description:** Aligned with the enterprise-wide framework, formal risk assessments shall be performed at least annually or at planned intervals, (and in conjunction with any changes to information systems) to determine the likelihood and impact of all identified risks using qualitative and quantitative methods. The likelihood and impact associated with inherent and residual risk shall be determined independently, considering all risk categories (e.g., audit results, threat and vulnerability analysis, and regulatory compliance).

**IVS-09 (SA-09): Infrastructure & Virtualization Security Segmentation**

**Description:** Multi-tenant organizationally-owned or managed (physical and virtual) applications, and infrastructure system and network components, shall be designed, developed, deployed and configured such that provider and customer (tenant) user access is appropriately segmented from other tenant users, based on the following considerations:

* Established policies and procedures
* Isolation of business critical assets and/or sensitive user data, and sessions that mandate stronger internal controls and high levels of assurance
* Compliance with legal, statutory and regulatory compliance obligations

Threat 7: Abuse of Cloud Services
*******************

**SEF-04 (IS-24): Security Incident Management, E-Discovery & Cloud Forensics Incident Response Legal Preparation**

**Description:** Proper forensic procedures, including chain of custody, are required for the presentation of evidence to support potential legal action subject to the relevant jurisdiction after an information security incident. Upon notification, customers and/or other external business partners impacted by a security breach shall be given the opportunity to participate as is legally permissible in the forensic investigation.

**HRS-08 (IS-26): Human Resources Technology Acceptable Use**

**Description:** Policies and procedures shall be established, and supporting business processes and technical measures implemented, for defining allowances and conditions for permitting usage of organizationally-owned or managed user end-point devices (e.g., issued workstations, laptops, and mobile devices) and IT infrastructure network and systems components. Additionally, defining allowances and conditions to permit usage of personal mobile devices and associated applications with access to corporate resources (i.e., BYOD) shall be considered and incorporated as appropriate.

Threat 8: Insufficient Due Diligence
************
**GRM-02 (DG-08)**

**GRM-01 (IS-04)**

**IAM-08 (IS-12): Identity & Access Management Trusted Sources**

**Description:** Policies and procedures are established for permissible storage and access of identities used for authentication to ensure identities are only accessible based on rules of least privilege and replication limitation only to users explicitly defined as business necessary.

**IVS-04 (OP-03)**

**GRM-11 (RI-01): Governance and Risk Management Risk Management Framework**

**Description:** Risks shall be mitigated to an acceptable level. Acceptance levels based on risk criteria shall be established and documented in accordance with reasonable resolution time frames and stakeholder approval.

**GRM-10 (RI-02): Governance and Risk Management Risk Assessments**

**Description:** Aligned with the enterprise-wide framework, formal risk assessments shall be performed at least annually or at planned intervals, (and in conjunction with any changes to information systems) to determine the likelihood and impact of all identified risks using qualitative and quantitative methods. The likelihood and impact associated with inherent and residual risk shall be determined independently, considering all risk categories (e.g., audit results, threat and vulnerability analysis, and regulatory compliance).

**BCR-01(RS-01) : Business Continuity Management & Operational Resilience, Business Continuity Planning**

**Description:** A consistent unified framework for business continuity planning and plan development shall be established, documented and adopted to ensure all business continuity plans are consistent in addressing priorities for testing, maintenance, and information security requirements. Requirements for business continuity plans include the following:

* Defined purpose and scope, aligned with relevant dependencies
* Accessible to and understood by those who will use them
* Owned by a named person(s) who is responsible for their review, update, and approval
* Defined lines of communication, roles, and responsibilities
* Detailed recovery procedures, manual work-around, and reference information
* Method for plan invocation

**BCR-09 (RS-02): Business Continuity Management & Operational Resilience Impact Analysis**

**Description:** There shall be a defined and documented method for determining the impact of any disruption to the organization (cloud provider, cloud consumer) that must incorporate the following:

* Identify critical products and services
* Identify all dependencies, including processes, applications, business partners, and third party service providers
* Understand threats to critical products and services
* Determine impacts resulting from planned or unplanned disruptions and how these vary over time
* Establish the maximum tolerable period for disruption
* Establish priorities for recovery
* Establish recovery time objectives for resumption of critical products and services within their maximum tolerable period of disruption
* Estimate the resources required for resumption

**BCR-01 (RS-03): Business Continuity Management & Operational Resilience Business Continuity Planning**

**Description:** A consistent unified framework for business continuity planning and plan development shall be established, documented and adopted to ensure all business continuity plans are consistent in addressing priorities for testing, maintenance, and information security requirements. Requirements for business continuity plans include the following:

* Defined purpose and scope, aligned with relevant dependencies
* Accessible to and understood by those who will use them
* Owned by a named person(s) who is responsible for their review, update, and approval
* Defined lines of communication, roles, and responsibilities
* Detailed recovery procedures, manual work-around, and reference information
* Method for plan invocation

**AIS-04 (SA-03)**

**AIS-01 (SA-04)**

**IVS-06 (SA-08): Infrastructure & Virtualization Security Network Security**

**Description:** Network environments and virtual instances shall be designed and configured to restrict and monitor traffic between trusted and untrusted connections. These configurations shall be reviewed at least annually, and supported by a documented justification for use for all allowed services, protocols, and ports, and by compensating controls.

**IVS-09 (SA-09)**

Threat 9: Shared Technology Vulnerabilities
**********************
**DSI-01 (DG-03)**

**GRM-01 (IS-04)**

**IAM-02 (IS-07)**

**IAM-05 (IS-15)**

**EKM-03 (IS-18)**

**TVM-02 (IS-20): Threat and Vulnerability Management Vulnerability / Patch Management**

**Description:** Policies and procedures shall be established, and supporting processes and technical measures implemented, for timely detection of vulnerabilities within organizationally-owned or managed applications, infrastructure network and system components (e.g. network vulnerability assessment, penetration testing) to ensure the efficiency of implemented security controls. A risk-based model for prioritizing remediation of identified vulnerabilities shall be used. Changes shall be managed through a change management process for all vendor-supplied patches, configuration changes, or changes to the organization's internally developed software. Upon request, the provider informs customer (tenant) of policies and procedures and identfied weaknesses especially if customer (tenant) data is used as part the service and/or customer (tenant) has some shared responsibility over implementation of control.

**IAM-12 (SA-02)**

**IVS-09 (SA-09)**

**IVS-09 (SA-11): Infrastructure & Virtualization Security Segmentation **

**Description:** Multi-tenant organizationally-owned or managed (physical and virtual) applications, and infrastructure system and network components, shall be designed, developed, deployed and configured such that provider and customer (tenant) user access is appropriately segmented from other tenant users, based on the following considerations:

* Established policies and procedures
* Isolation of business critical assets and/or sensitive user data, and sessions that mandate stronger internal controls and high levels of assurance
* Compliance with legal, statutory and regulatory compliance obligations

**IVS-01 (SA-14)**

