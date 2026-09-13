# Secure AWS Architecture for a Medical SaaS Platform

## Overview
This individual academic project presents a secure and highly available AWS reference architecture for a medical SaaS organization migrating from leased physical Windows servers. The design maps business, security, availability, audit, and continuity requirements to AWS services and controls.

> **Scope note:** This is an architecture design supported by selected hands-on validation in an AWS Academy environment. It is not represented as a fully deployed production system. Components restricted by the Academy lab role are identified as design-specified.

## Project Objectives
- Apply least-privilege identity and access management.
- Isolate web, application, and database tiers.
- Protect sensitive medical and payment information.
- Support high availability, scaling, monitoring, auditing, and recovery.
- Document technical decisions, risks, limitations, and recommendations.

## AWS Services and Security Concepts
- AWS Identity and Access Management (IAM)
- Amazon VPC with public and private subnets
- Amazon EC2
- Elastic Load Balancing and Auto Scaling design
- Amazon RDS for SQL Server with Multi-AZ design
- Amazon S3
- AWS CloudTrail
- Amazon CloudWatch
- AWS Key Management Service (KMS)
- AWS Certificate Manager
- Security groups and security-group referencing
- Multifactor authentication and least privilege
- Encryption at rest and in transit
- Separation of duties
- Business continuity and audit logging

## Architecture Summary
The proposed solution uses a multi-tier, multi-Availability Zone architecture. Internet-facing traffic is routed through a load balancer. Application resources are isolated from direct public access, and the database tier is restricted to approved application-tier traffic. IAM groups, roles, MFA, and least-privilege policies support separation of duties. CloudTrail and CloudWatch provide audit and monitoring capabilities, while encryption services protect data at rest and in transit.

## Hands-on Validation
Selected controls were configured or reviewed in AWS Academy, including:
- Creating and modifying security groups.
- Configuring security-group rules and tier-to-tier references.
- Reviewing CloudTrail event history for account and API activity.
- Evaluating IAM password-policy and permission-boundary behavior.
- Documenting controls that could not be committed because of lab-role restrictions.

## Key Deliverables
- Final architecture report
- Executive presentation
- AWS architecture diagram
- Sanitized screenshots of selected configurations
- Security and business-continuity recommendations

## Repository Structure
```text
aws-secure-medical-saas-architecture/
├── README.md
├── architecture/
│   └── aws-architecture-diagram.png
├── documentation/
│   ├── final-project-report.pdf
│   └── presentation.pdf
├── screenshots/
│   ├── security-group-chaining.png
│   ├── cloudtrail-events.png
│   ├── iam-password-policy.png
│   └── cloudwatch-alarm.png
└── SECURITY.md
```

## Security and Privacy
Before publication, all artifacts should be reviewed to remove or obscure:
- AWS account identifiers
- Access keys, secret keys, and session tokens
- Email addresses or usernames that should remain private
- Resource identifiers and IP addresses where disclosure is unnecessary
- Browser profile information and unrelated personal information

No credentials or secrets should be stored in this repository.

## Lessons Learned
- How business requirements translate into AWS architecture and controls.
- How IAM roles, groups, MFA, and least privilege support separation of duties.
- How security-group references can restrict communication between tiers.
- How CloudTrail and CloudWatch support auditing and operational monitoring.
- How laboratory permission boundaries affect implementation and validation.
- Why production claims must distinguish deployed controls from proposed architecture.

## Author
Wisdom Kwame Djam
