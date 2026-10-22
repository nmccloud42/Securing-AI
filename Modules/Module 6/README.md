# Module 6 — Secure Deployment & Infrastructure

## Module Overview

Welcome to **Module 6: Secure Deployment & Infrastructure** of the Securing AI certification course.

In Module 5, you examined security risks associated with Large Language Models (LLMs), prompt injection, retrieval systems, and connected tools.

This module builds on those concepts by examining how artificial intelligence and machine learning systems can be securely deployed and operated in production environments.

Protecting an AI model during development and training is only one part of securing an AI system. Once a model is deployed, it depends on additional infrastructure, including APIs, model servers, databases, containers, cloud services, networks, credentials, and deployment pipelines.

Each of these components introduces potential security risks.

An attacker may not need to compromise the machine learning model directly. Instead, the attacker may exploit an exposed API, stolen credentials, an insecure container, a misconfigured cloud service, or a compromised deployment pipeline.

This module focuses on **securing the infrastructure and services surrounding deployed AI systems**.

You will explore:

- AI deployment architectures and attack surfaces.
- Securing AI APIs and inference endpoints.
- Identity, access control, and least privilege.
- Secrets, credentials, and configuration security.
- Container and runtime security.
- Network and cloud infrastructure security.
- Model artifact integrity and deployment pipeline security.
- Logging, monitoring, incident response, and secure operations.

Throughout the module, you will complete guided Python simulations, security configuration exercises, knowledge checks, and hands-on activities.

The module concludes with a comprehensive security assessment of a fictional cloud-hosted AI service called **SentinelAI**.

You will evaluate the service's deployment configuration, implement security controls, detect suspicious activity, respond to a simulated incident, and restore the system to a trusted state.

---

## Learning Objectives

By the end of this module, you should be able to:

1. Identify the major components of a deployed AI/ML system and explain how they contribute to its attack surface.
2. Analyze AI deployment architectures to identify exposed services, trust boundaries, communication paths, and potential entry points.
3. Explain how AI APIs and inference endpoints can be secured through authentication, authorization, request validation, rate limiting, and secure communication.
4. Apply identity and access management principles, including role-based access control, service identities, separation of duties, and least privilege.
5. Identify insecure handling of API keys, passwords, access tokens, cloud credentials, and configuration information.
6. Explain secure approaches to secret management, credential rotation, short-lived credentials, and configuration validation.
7. Identify container security risks involving vulnerable images, unnecessary privileges, insecure configurations, and untrusted dependencies.
8. Explain how container hardening and runtime restrictions reduce the impact of workload compromise.
9. Apply network segmentation and zero-trust principles to reduce unnecessary communication between infrastructure components.
10. Identify cloud security risks involving public endpoints, storage access, service permissions, and workload isolation.
11. Explain how cryptographic hashes, digital signatures, and provenance verification help protect model artifacts.
12. Identify security risks associated with automated model deployment pipelines.
13. Explain how deployment security gates can prevent unverified or insecure artifacts from reaching production.
14. Describe how logging and monitoring help identify suspicious activity in deployed AI systems.
15. Explain the importance of incident response, containment, recovery, and continuous security operations.
16. Evaluate the security of a deployed AI system and recommend defensive improvements.

---

## Module Contents

| Section | Topic | What You Will Learn |
|---|---|---|
| 1 | AI/ML Deployment Architecture and Attack Surface | Identify the components of deployed AI systems, understand communication paths, and examine infrastructure attack surfaces. |
| 2 | Securing AI APIs and Inference Endpoints | Protect prediction interfaces through authentication, authorization, request validation, rate limiting, and secure responses. |
| 3 | Identity, Access Control, and Least Privilege | Examine user identities, service accounts, permissions, and role-based access controls. |
| 4 | Secrets, Credentials, and Configuration Security | Identify exposed credentials and apply secure secret management and configuration practices. |
| 5 | Container and Runtime Security | Examine container images, runtime permissions, workload restrictions, and security hardening. |
| 6 | Network and Cloud Infrastructure Security | Investigate network exposure, segmentation, cloud permissions, and workload isolation. |
| 7 | Model Artifact and Deployment Pipeline Security | Verify model integrity, protect deployment pipelines, and enforce security checks before production deployment. |
| 8 | Logging, Monitoring, Incident Response, and Secure Operations | Detect suspicious activity, correlate security events, respond to incidents, and restore trusted operation. |
| Final Lab | SentinelAI Secure Deployment Assessment | Secure a fictional production AI service, detect a simulated incident, contain the affected workload, and evaluate the final security posture. |

---

## Getting Started

**Notebook:** [Module6_SecureDeployment&Infrastructure.ipynb](./Module6_SecureDeployment%26Infrastructure.ipynb)

To begin Module 6:

1. Open the Module 6 folder in the course's GitHub repository using your cyber range browser.
2. Select `Module6_SecureDeployment&Infrastructure.ipynb`.
3. Open the notebook in Google Colab. If an **Open in Colab** option is unavailable, visit [Google Colab](https://colab.research.google.com/), select the **GitHub** tab, and locate the notebook in the course repository.
4. Select **File → Save a copy in Drive** to create your own editable version.
5. Begin with the Module Overview and Learning Objectives.
6. Complete each section in order, including the reading material, code demonstrations, hands-on activities, and knowledge checks.

> **Important:** This module is designed for Google Colab. Some code cells use Colab-specific collapsible titles and interactive settings that may display differently in other notebook environments.

---

## How to Work Through the Notebook

### Reading Sections

Each instructional section contains collapsible reading material labeled **Click to Expand**.

Expand the main section and its subsections to review the security concepts, infrastructure components, attack scenarios, and defensive techniques.

Read the instructional material before completing the associated activities.

### Hands-On Labs

Each of the eight instructional sections includes a hands-on lab.

These activities demonstrate how security weaknesses can arise in deployed AI systems and how defensive controls can reduce the associated risks.

The labs use Python-based simulations to represent infrastructure components and security configurations.

You will examine both insecure and hardened environments, review security findings, and observe how configuration changes affect system security.

### Interactive Code Cells

The notebook contains interactive code cells that allow you to experiment with different security configurations.

These activities may involve:

- Reviewing AI deployment architectures.
- Identifying exposed services.
- Testing API authentication and authorization.
- Applying rate limits.
- Evaluating service permissions.
- Identifying insecure credential storage.
- Hardening container configurations.
- Restricting network communication.
- Verifying model artifact integrity.
- Evaluating deployment security gates.
- Analyzing logs and monitoring results.
- Responding to simulated security incidents.

Run each code cell using the **play button** beside the cell.

Review the output and accompanying explanations before continuing.

### Knowledge Checks

Complete the knowledge checks and interactive questions throughout the notebook.

These exercises reinforce the concepts introduced in each section and help prepare you for the final lab.

Review the feedback and explanations provided when an answer is incorrect.

### Working in Google Colab

- Run code cells in the intended order.
- Allow each cell to finish executing before continuing.
- Follow the instructions provided for each activity.
- Modify only the variables or configurations identified for experimentation.
- Review generated tables, diagrams, security results, and explanations.
- Save your notebook periodically.
- If your runtime disconnects or restarts, rerun the necessary setup cells.

The labs use simulated infrastructure rather than requiring students to deploy real cloud services.

This allows you to explore infrastructure security concepts in a controlled environment without requiring paid cloud resources or production systems.

---

## Hands-On Activities

### Section 1 — AI/ML Deployment Architecture and Attack Surface

In this lab, you will examine the architecture of a fictional deployed AI service.

You will identify important infrastructure components, review their communication paths, and determine which services should be accessible from the Internet.

You will:

- Examine an AI deployment architecture.
- Identify important services and resources.
- Review public and private communication paths.
- Identify potential attack surfaces.
- Examine trust boundaries.
- Compare deployment designs.
- Evaluate security improvements.

The activity demonstrates why securing an AI system requires understanding the infrastructure surrounding the model.

### Section 2 — Securing AI APIs and Inference Endpoints

This lab focuses on protecting the interfaces through which users and applications interact with deployed AI models.

You will examine a simulated prediction API and identify weaknesses that could allow unauthorized access or excessive resource consumption.

You will investigate security controls such as:

- Authentication.
- Authorization.
- Request validation.
- Rate limiting.
- Secure communication.
- Response handling.
- API monitoring.

The activity demonstrates how an AI model can be exposed to security risks through its prediction interface even when the model itself has not been compromised.

### Section 3 — Identity, Access Control, and Least Privilege

This lab examines how identities and permissions affect the security of AI infrastructure.

You will evaluate a fictional environment containing users, services, and protected resources.

You will examine which identities require access to specific components and whether unnecessary permissions create additional risk.

The activity demonstrates the importance of:

- Authentication.
- Authorization.
- Role-based access control.
- Service identities.
- Separation of duties.
- Least privilege.

You will explore how reducing unnecessary permissions can limit the impact of a compromised account or service.

### Section 4 — Secrets, Credentials, and Configuration Security

This lab focuses on protecting sensitive information used by deployed AI systems.

You will examine insecure handling of credentials and configuration settings.

Examples include:

- Hardcoded API keys.
- Exposed passwords.
- Embedded access tokens.
- Insecure configuration values.
- Excessive credential permissions.

You will investigate secure alternatives such as centralized secret management, credential rotation, and configuration validation.

The activity demonstrates why credentials should be protected independently of application source code and why secure configuration is an essential part of deployment security.

### Section 5 — Container and Runtime Security

This lab examines the security of containerized AI workloads.

Containers are commonly used to package machine learning applications and their dependencies for deployment.

However, insecure container configurations can introduce additional attack surfaces.

You will investigate:

- Container image security.
- Vulnerable or unnecessary packages.
- Excessive runtime privileges.
- Unrestricted resource access.
- Insecure container settings.
- Workload hardening.

You will compare insecure and hardened configurations to understand how runtime restrictions can reduce the impact of a compromised service.

### Section 6 — Network and Cloud Infrastructure Security

This lab explores the network and cloud infrastructure supporting deployed AI systems.

You will examine how services communicate and determine whether those communication paths are necessary.

The activity introduces security concepts such as:

- Public and private endpoints.
- Network segmentation.
- Service-to-service communication.
- Zero-trust principles.
- Cloud access permissions.
- Workload isolation.
- Reducing the blast radius of compromise.

You will evaluate how restricting unnecessary communication can prevent a compromised workload from accessing unrelated infrastructure components.

### Section 7 — Model Artifact and Deployment Pipeline Security

This lab focuses on protecting trained models as they move from development into production.

A model may be trained securely but still become compromised if an attacker modifies the stored artifact or deployment process.

You will examine:

- Model artifacts.
- Model registries.
- Cryptographic hashes.
- Integrity verification.
- Artifact provenance.
- Deployment pipelines.
- Automated security checks.
- Deployment approval gates.

The activity demonstrates why organizations must verify that the model entering production is the same trusted artifact that was approved during development.

### Section 8 — Logging, Monitoring, Incident Response, and Secure Operations

This lab examines how organizations detect and respond to security problems after an AI system has been deployed.

You will investigate simulated operational events and identify patterns that may indicate suspicious activity.

These may include:

- Unusual API request volumes.
- Authentication failures.
- Resource exhaustion.
- Service errors.
- Unexpected changes in model behavior.
- Abnormal communication patterns.

You will examine how monitoring systems establish normal operating conditions and identify deviations.

The activity also introduces incident response concepts, including investigation, containment, recovery, and validation.

It demonstrates why secure deployment requires continuous monitoring rather than assuming that preventive controls will always succeed.

---

## End-of-Module Lab — SentinelAI Secure Deployment Assessment

At the end of Module 6, you will complete a comprehensive security assessment of a fictional production AI service called **SentinelAI**.

SentinelAI provides fraud predictions through a cloud-hosted API.

The system includes several components:

- API Gateway.
- Inference Service.
- Model Registry.
- Production Database.
- Secret Manager.
- Logging Service.
- Training Storage.
- CI/CD Pipeline.

The development team believes the system is ready for production.

However, your security team must determine whether the environment has been configured securely and whether the organization can detect, contain, and recover from a security incident.

You will evaluate the deployment, implement defensive improvements, and respond to a simulated compromise.

### Part 1 — Review the Production Environment

Examine the initial SentinelAI architecture.

Identify which services require direct Internet access and which should remain private.

Consider whether the inference service, training storage, and supporting infrastructure are unnecessarily exposed.

### Part 2 — Reduce Unnecessary Exposure

Review the deployment configuration and restrict unnecessary public access.

Ensure external requests enter through the controlled API gateway rather than directly accessing internal services.

### Part 3 — Harden the API

Apply security controls to the prediction API.

Examine authentication, request restrictions, and rate limiting.

Determine how these controls reduce unauthorized access and abusive request activity.

### Part 4 — Apply Least-Privilege Access

Review the permissions assigned to the inference service.

Remove unnecessary access to resources that are not required for normal inference.

The activity demonstrates how limiting permissions reduces the potential impact of workload compromise.

### Part 5 — Protect Secrets and Credentials

Examine how SentinelAI handles sensitive credentials.

Identify insecure credential storage and apply a more secure configuration using managed secrets.

Consider how exposed credentials could allow attackers to access additional services.

### Part 6 — Restrict the Inference Workload

Review the runtime configuration of the inference service.

Apply restrictions that reduce unnecessary privileges and limit resource consumption.

The activity demonstrates how workload hardening can reduce the impact of compromise or abuse.

### Part 7 — Segment the Network

Examine communication paths between SentinelAI components.

Restrict connections that are not required for legitimate operation.

Consider how segmentation limits an attacker's ability to move from one compromised component to another.

### Part 8 — Verify the Production Model

Examine the model artifact selected for deployment.

Verify that the artifact matches its approved cryptographic hash.

The activity demonstrates how integrity verification can identify unexpected changes to a model before deployment.

### Part 9 — Enforce Deployment Security Gates

Review the security checks required before SentinelAI can enter production.

Determine whether all required controls have passed.

The exercise demonstrates why automated deployment pipelines should block releases when mandatory security requirements are not satisfied.

### Part 10 — Investigate a Failed Deployment Check

Review a deployment that has been blocked by a failed security requirement.

Identify the failed control and determine why bypassing it would introduce unnecessary risk.

Correct the issue before allowing deployment to continue.

### Part 11 — Establish Monitoring Baselines

Examine normal SentinelAI operating conditions.

Establish reference measurements for request activity, authentication behavior, resource utilization, service errors, and model predictions.

These measurements provide a baseline for identifying suspicious changes.

### Part 12 — Detect Suspicious Activity

Review simulated operational activity that differs from the established baseline.

Investigate unusual behavior involving requests, authentication, resources, errors, or model outputs.

Determine which observations require further investigation.

### Part 13 — Correlate Security Signals

Examine multiple suspicious conditions occurring at approximately the same time.

The simulated incident includes:

- Extreme query volume.
- A large increase in authentication failures.
- Near-maximum GPU utilization.
- High service error rates.
- Major changes in prediction distributions.

Consider why individual anomalies may have legitimate explanations, while several related anomalies can provide stronger evidence of a security incident.

### Part 14 — Respond to the Incident

Use the collected evidence to determine an appropriate response.

Evaluate how the existing security controls affect the incident and what additional actions are necessary.

### Part 15 — Contain the Affected Workload

Isolate the potentially compromised inference workload.

Review how network restrictions and least-privilege permissions reduce the ability of the incident to affect other infrastructure components.

### Part 16 — Recover Using a Trusted Model

Restore the service using a trusted model artifact.

Verify that the recovered model matches the approved version and that the deployment environment satisfies the required security controls.

### Part 17 — Evaluate the Final Security Posture

Review the protections applied throughout the assessment.

Determine whether SentinelAI now has appropriate preventive, detective, and recovery capabilities.

Consider any remaining risks that may require further attention.

### Part 18 — Final Security Review

Summarize the security improvements and explain how the controls work together.

Evaluate whether SentinelAI can securely process legitimate requests while maintaining the ability to identify and respond to suspicious activity.

### Final Knowledge Check

Complete the final knowledge check to reinforce the major concepts from the module.

The assessment covers topics such as:

- API gateway security.
- Rate limiting.
- Least privilege.
- Secret management.
- Container hardening.
- Network segmentation.
- Model integrity.
- Deployment security gates.
- Monitoring and incident response.
- Secure recovery.

Review the feedback and revisit any concepts that require additional study.

---

## Understanding Your Lab Results

When evaluating the activities in Module 6, consider the following questions:

- Which components of the AI deployment require direct Internet access?
- Were any internal services unnecessarily exposed?
- Did authentication and rate limiting reduce API security risks?
- Did the inference service have more permissions than it required?
- Were sensitive credentials stored securely?
- Did container hardening reduce unnecessary privileges and resource access?
- Did network segmentation restrict unnecessary communication?
- Was the production model verified against an approved artifact?
- Did the deployment pipeline enforce all required security checks?
- Were normal operating conditions established before monitoring for suspicious activity?
- Did the simulated incident produce multiple related security indicators?
- Could the security team distinguish suspicious activity from normal operational changes?
- Did containment prevent the affected workload from accessing unrelated resources?
- Was the service recovered using a trusted model?
- Which risks remain after the security improvements?

The purpose of the lab is not simply to make every security check display a successful result.

Instead, you should understand why each security control exists, what risk it addresses, and how multiple controls work together to protect a deployed AI system.

---

## Saving and Submitting Your Work

After completing all reading sections, hands-on activities, knowledge checks, and the final SentinelAI assessment:

1. Confirm that you have completed the required activities and entered your responses.
2. Make sure the relevant code cells have executed successfully.
3. Review your generated results, including security findings, configuration comparisons, monitoring outputs, and incident response results.
4. Save your completed notebook in Google Colab.
5. Select **File → Download → Download .ipynb**.
6. Submit the downloaded `.ipynb` file through the submission method specified by your instructor or cyber range.

Keep a copy of your completed notebook in Google Drive for future reference.

**Do not submit the original, unmodified notebook from the course repository.**

---

## Requirements

To complete this module, students will need:

- Access to the course GitHub repository.
- A web browser in the cyber range environment.
- Access to Google Colab.
- A Google account for saving a personal notebook copy.
- Basic familiarity with running Python notebook cells.

The module uses standard Python simulations to demonstrate infrastructure security concepts.

Students are not required to deploy real cloud services, configure production networks, or purchase cloud computing resources.

The exercises are designed to execute quickly in a standard Google Colab environment.

Prior experience with cloud security or infrastructure administration is not required.

The notebook provides guided explanations and hands-on exercises designed to introduce the concepts progressively.

Follow any additional setup instructions provided within the notebook.

---

## Responsible Use

The activities demonstrated in this module are intended for **authorized educational and research purposes**.

All infrastructure security exercises should be performed using the provided simulations and controlled notebook environment.

Do not attempt to access unauthorized cloud resources, compromise deployment pipelines, exploit production APIs, obtain credentials, or interfere with real AI services without explicit authorization.

The purpose of these activities is to understand how deployment and infrastructure weaknesses affect AI security so that systems can be configured, evaluated, monitored, and defended more effectively.

---

## References

A collapsible **Module 6 References** section is included at the end of the notebook.

These references provide additional information about:

- AI deployment architectures.
- API and inference endpoint security.
- Identity and access management.
- Secrets and credential management.
- Container and runtime security.
- Cloud and network security.
- Model artifact integrity.
- Deployment pipeline security.
- Logging and monitoring.
- Incident response and recovery.

Students are encouraged to consult these sources when reviewing the concepts covered throughout the module.

---

## Module Completion

Before continuing to the next module, make sure you can:

- Identify the major components of a deployed AI system.
- Explain how infrastructure components introduce additional attack surfaces.
- Identify unnecessary public exposure and insecure communication paths.
- Explain how authentication, authorization, and rate limiting protect AI APIs.
- Apply least-privilege principles to users and services.
- Recognize insecure handling of secrets and credentials.
- Describe secure configuration and credential management practices.
- Identify common container and runtime security risks.
- Explain how network segmentation reduces the impact of compromise.
- Recognize cloud security risks involving permissions, storage, and exposed services.
- Explain how model integrity and provenance verification protect production deployments.
- Describe how deployment security gates prevent insecure releases.
- Identify suspicious activity through monitoring and log analysis.
- Explain why security incidents should be investigated using multiple sources of evidence.
- Describe appropriate containment and recovery procedures.
- Evaluate the effectiveness of preventive, detective, and recovery controls.
- Perform a basic security assessment of a deployed AI system.

**Next Step:** After completing Module 6, continue to the next module in the Securing AI certification course.
