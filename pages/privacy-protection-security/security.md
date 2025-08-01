---
title: Security Practices
slug: /security
sidebar_position: 3
tags:
  - free
  - team
  - business
  - enterprise
---

:::note

Applicable to customers on any plan.

:::

We take the security of your data very seriously at Retool. If you have additional questions regarding security, we are happy to answer them. Please write to [security@retool.com](mailto:security@retool.com) and we will respond as quickly as we can or check our self serve [Trust Center](https://trust.retool.com/) for more security information. This Security Practices page describes the administrative, technical and physical controls applicable to Retool.

## Hosting, Architecture, and configurations

### Cloud-Based Services

The cloud-based Retool services are operated on a multitenant architecture at both the platform and infrastructure layers that is designed to segregate and restrict access to any applications, workflows or processes you and your users build using the Retool services (each, a "Custom App"). This infrastructure is provided and hosted by Amazon Web Services, Inc. ("AWS"). Information about security provided by AWS is available from the [AWS Security website](https://aws.amazon.com/security/). Information about security and privacy-related audits and certifications received by AWS, including information on SOC reports, is available from the [AWS Compliance website](https://aws.amazon.com/compliance/).

### Self-Hosted Services

For self-hosted Retool services, Custom Apps are hosted using your own infrastructure - such as on-premises — so that you and your users can build Custom Apps in your virtual private cloud (VPC) or behind your virtual private network (VPN). In provisioning a self-hosted account of the Retool services, our self-hosted image is built with the latest upstream version of Debian (Retool's base operating system image) with the latest security patches, and updates on a daily-basis.

### Database, Query and Workflow Configurations

Whether using Retool's cloud-based or self-hosted services, you and your users may submit data and content to your Custom Apps ("Customer Data"), for example by querying a database or automating a workflow. You have the option to build and use Custom Apps without workflows and/or without connecting them to any database, or alternatively, you have the ability to connect Custom Apps to your own databases, databases hosted by third parties, or databases hosted by Retool.

### Storage of Customer Data

### Retool Cloud Services

When you use the Retool Cloud Services, Retool’s storage of Customer Data primarily depends on whether you connect a Custom App to a database provided by Retool, in which case Retool will store Customer Data using third-party infrastructure.When you instead connect a Custom App to your own database or data resource or that of a third party, Retool does not store Customer Data but rather proxies requests to that database and applies the credentials server-side. The Retool services are architected this way because having the end-user's browser connect directly to the database would require you to provision every user individually, rather than just the Retool server, which would potentially expose credentials.

 Other features, functionality, and products of the Services may also require Retool to store Customer Data. For example, if you enable [query or workflow caching](https://docs.retool.com/docs/caching-in-retool), Customer Data is temporarily cached by Retool for the specified cache duration. You can invalidate a query's cache—or disable query and workflow caching entirely—at any time.

### Self-Hosted Services

When you use the Self-Hosted Services, no Retool systems store Customer Data and no Retool personnel have technical or logical access to Customer Data. Only Usage Information (as defined in the Agreement) is shared with Retool, and when you elect to deploy self-hosted Workflows with a Retool-managed Temporal cluster, only orchestration data, such as internal Workflow IDs, and encrypted Workflow block names, user IDs, Workflow name, host name, and base domain, are stored in Temporal Technologies’ Cloud offering (see our [Documentation](https://docs.retool.com/self-hosted/concepts/temporal) for more information).

## Confidentiality and security controls

### Confidentiality

Retool places strict controls over its employees' access to Custom Apps and any associated Customer Data. The operation of the Retool services requires that some employees have access to the systems which store or process this information and data. For example, in order to diagnose a problem you are having with the Retool services, we may need to access your account. These employees are prohibited from using these permissions to view Customer Data unless it is necessary to do so. We have technical controls and audit policies in place to ensure that any access to your account is logged.

All of our employees and contract personnel are bound to our policies regarding confidentiality and we treat these issues as matters of the highest importance within our company.

### Protection of Customer Data

While the protection of Customer Data is a joint responsibility between you and Retool, Retool will implement and maintain appropriate technical and organizational measures designed to protect your Customer Data against accidental or unlawful destruction, loss, alteration, and unauthorized disclosure when stored or processed using the Retool services. The Retool services have a number of security controls, including but not limited to:

+ Audit logging. Detailed audit logs are available to administrators of your account if you are on the [Business or Enterprise plan](https://retool.com/pricing/). We log every time an account signs in, noting the type of device used and the IP address of the connection. Administrators can review consolidated access logs for their whole team. More information about access logging is available in our [Documentation](https://docs.retool.com/docs/audit-logs).
+ Access Management. Administrators can remotely disable users authenticated to the Retool services, on demand. More information about access management is available in our [Documentation](https://docs.retool.com/docs/disabling-users).
+ Host Management. We perform automated vulnerability and malware scans on our production hosts and company endpoints, and promptly triage or remediate any findings that present a risk to our environment. We enforce screen lock-outs and the use of full disk encryption for company laptops.
+ Network Protection. In addition to sophisticated system monitoring and logging, we have implemented two-factor authentication for all server access across our production environment. Firewalls are configured according to industry best practices, using AWS security groups, network segmentation, and real-time intrusion monitoring.
+ Product security practices. New features, significant functionality, and design changes go through a security review process facilitated by the security team. In addition, our code is audited with automated static analysis software, tested, and manually peer-reviewed prior to being deployed to production. The security team works closely with development teams to resolve any additional security concerns that may arise during development. Retool also operates a vulnerability disclosure program. Security researchers around the world continuously test the security of the Retool services, and report issues via the program. For more program details please see [retool.com/vulnerability-reporting](https://retool.com/vulnerability-reporting).
+ Team-wide two-factor authentication. Administrators can require all users to set up two-factor authentication on their accounts. Instructions for doing this are available in our [Documentation](https://docs.retool.com/docs/two-factor-authentication).

### Data Encryption

The Retool services use industry-accepted encryption products to protect Customer Data during transmissions between your network and the Retool services, and when at rest. The Retool services support the latest recommended secure cipher suites and protocols to encrypt all traffic in transit. Retool monitors the changing cryptographic landscape closely and works promptly to upgrade the service to respond to new cryptographic weaknesses as they are discovered and implement best practices as they evolve. For encryption in transit, Retool does this while also balancing the need for compatibility with older data sources.

### Reliability, Backup, and Business Continuity

Retool is committed to making the Retool services a highly available service that you can rely on. The infrastructure Retool uses for delivering the services run on systems that are fault-tolerant, for failures of individual servers or even entire data centers. Retool's operations team tests disaster recovery measures regularly and has a 24-hour on-call team to quickly resolve unexpected incidents. Retool performs regular backups, facilitates rollbacks of software and system changes when necessary and replication of data as needed.

Customer Data, when stored by Retool, is done so redundantly in multiple locations in our hosting provider's data centers to ensure availability. Retool has well-tested backup and restoration procedures which allow recovery from a major disaster. Customer Data, Custom Apps and our source code are automatically backed up every night and stored for seven days. The operations team is alerted in the event of a failure in this system. Backups are stored for seven days in the event of a catastrophic failure and fully tested at least every 90 days to confirm that Retool's processes and tools work as expected.

### Portability of Custom Apps

During the term of a subscription, your administrator may import and export Custom Apps in JSON, as further described in our [Documentation](https://docs.retool.com/docs/import-export-apps), but please be advised that there may be technical constraints to such portability and any subsequent compatibility and utility.

### Return of Customer Data

Within 30 days post contract termination, you may request return of Customer Data stored by Retool (to the extent such data has not already been deleted by you). Information about the export capabilities of the Retool services can be found by reaching out to our data protection team at [dpo@retool.com](mailto:dpo@retool.com).

### Deletion of Custom Apps and Customer Data

The Retool services provide the option for administrators to delete Custom Apps and all associated Customer Data stored by Retool at any time during a subscription term. Within 24 hours of administrator-initiated deletion, Retool hard deletes all Custom Apps and Customer Data from currently running production systems. Retool-maintained backups of services and data are destroyed within 30 days (backups are destroyed within 30 days, except that during an on-going investigation of an incident such period may be temporarily extended).

## Monitoring, validation, and practices

### Certifications

Certifications are performed on the Retool services, and Customers may download a copy of available applicable certifications by heading to our self serve [Trust Center](https://trust.retool.com/). At a minimum, Retool will align with prevailing industry standards such as SOC 2 Type 2, or any successor or superseding standard.

### Audits

To verify that our security practices are sound and to monitor the Retool services for new vulnerabilities discovered by the security research community, the Retool services undergo security assessments by internal personnel, and for the Retool services by respected external security firms who perform regular audits of the Retool services. In addition to periodic and targeted audits of the Retool services, we also employ the use of continuous hybrid automated scanning of our web platform. Customers may download a copy of available applicable external audit reports by heading to our self serve [Trust Center](https://trust.retool.com/).

### Intrusion Detection

Retool, or an authorized external entity, will monitor all Retool services and endpoints. Endpoints are monitored through continuous malware and anomaly detection. Retool-hosted cloud environments are logged and alerted 24/7 for suspicious or known malicious activity. Logs are also reviewed manually at least every 90 days.

### Security Logs

Systems used in the provision of the Retool services log information to their respective system log facilities or a centralized logging service (for network systems) in order to enable security reviews and analysis. Retool maintains an extensive centralized logging environment in the production environment which contains information pertaining to security, monitoring, availability, access and other metrics about the Retool services. These logs are analyzed for security events via automated monitoring software, overseen by the security team.

Incident Management

Retool maintains security incident management policies and procedures. Retool notifies impacted customers without undue delay of any unauthorized disclosure of their respective Customer Data by Retool or its agents of which Retool becomes aware to the extent permitted by law. Retool typically notifies customers of significant system incidents by email.

### Personnel Practices

Retool conducts background checks on all employees before employment, and employees receive privacy and security training during onboarding as well as on an ongoing basis. All employees are required to read and sign our comprehensive information security policy covering the security, availability, and confidentiality of the Retool services.
