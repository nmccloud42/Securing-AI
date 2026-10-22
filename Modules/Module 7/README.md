# Module 7 — AI Security Operations & Defense

## Module Overview

Welcome to **Module 7: AI Security Operations & Defense** of the Securing AI certification course.

In Module 6, you examined how to securely deploy AI systems and protect the infrastructure supporting them. You explored API security, identity and access management, container hardening, network segmentation, model integrity, and deployment security controls.

This module builds on those concepts by examining how organizations **continuously monitor, detect, investigate, respond to, and recover from security threats affecting AI systems**.

Securing an AI system does not end when the model is deployed.

Once an AI system enters production, defenders must maintain visibility into its components, monitor its behavior, identify suspicious activity, investigate potential attacks, and respond when security controls fail.

AI systems introduce operational security challenges because attackers may target not only traditional infrastructure but also training datasets, model artifacts, prediction interfaces, retrieval systems, and AI agents.

This module focuses on the processes, technologies, and security practices required to defend AI systems throughout their operational lifecycle.

You will explore:

- AI security operations and continuous defense.
- AI asset inventories and security baselines.
- Security monitoring, logging, and telemetry.
- Detecting attacks against AI systems.
- AI security detection engineering.
- AI incident response and containment.
- Model recovery, rollback, and operational resilience.
- AI red teaming and continuous security testing.
- Defense-in-depth strategies and security controls.
- Security playbooks, metrics, and operational readiness.

Throughout the module, you will complete guided Python simulations, hands-on security investigations, detection exercises, incident response scenarios, and knowledge checks.

The module concludes with a comprehensive capstone lab titled **Defend an AI System**, where you will investigate a simulated security incident, analyze evidence, contain the threat, restore trusted operation, and document your findings.

---

## Learning Objectives

By the end of this module, you should be able to:

1. Explain the purpose of AI security operations and continuous defense.
2. Identify important AI assets and maintain security inventories.
3. Establish trusted security baselines for AI systems.
4. Identify important telemetry sources for monitoring deployed AI applications.
5. Distinguish between normal operational behavior and potentially suspicious activity.
6. Identify indicators associated with AI-specific attacks.
7. Develop and evaluate security detection rules.
8. Explain the importance of detection thresholds, alert severity, and false positives.
9. Apply incident response procedures to AI security incidents.
10. Identify appropriate containment strategies for compromised AI systems.
11. Explain how trusted model artifacts and recovery procedures support operational resilience.
12. Evaluate model rollback, canary deployment, and fallback strategies.
13. Explain the role of AI red teaming and continuous security testing.
14. Evaluate the effectiveness of layered security controls.
15. Develop AI security playbooks for common attack scenarios.
16. Interpret security operations metrics and evaluate operational readiness.
17. Apply relevant security frameworks to AI security operations.
18. Investigate a simulated AI security incident and produce a final incident report.

---

## Module Contents

| Section | Topic | What You Will Learn |
|---|---|---|
| 1 | Introduction to AI Security Operations | Understand the AI security operations lifecycle and the responsibilities involved in defending deployed AI systems. |
| 2 | AI Asset Inventory & Security Baselines | Identify important AI assets, document their relationships, and establish trusted system baselines. |
| 3 | AI Security Monitoring & Telemetry | Collect, classify, and analyze operational security data from AI systems. |
| 4 | Detecting AI Attacks | Identify indicators associated with model extraction, data poisoning, prompt injection, backdoors, and resource exhaustion. |
| 5 | AI Security Detection Engineering | Develop, test, evaluate, and improve security detection rules. |
| 6 | AI Incident Response | Investigate security incidents, preserve evidence, contain threats, and coordinate recovery. |
| 7 | Model Recovery, Rollback & Resilience | Restore trusted models and evaluate recovery strategies, canary deployments, and fallback mechanisms. |
| 8 | AI Red Teaming & Continuous Security Testing | Test AI systems for vulnerabilities and validate defensive controls through repeatable assessments. |
| 9 | Defense-in-Depth & AI Security Controls | Combine preventive, detective, and recovery controls to protect AI systems. |
| 10 | AI Security Playbooks, Metrics & Operational Readiness | Develop response procedures, measure security performance, and evaluate organizational readiness. |
| Capstone Lab | Defend an AI System | Investigate a simulated incident, analyze security evidence, contain the threat, restore trusted operation, and document findings. |

---

## Getting Started

**Notebook:** [Module7_AISecurityOperations&Defense.ipynb](./Module7_AISecurityOperations%26Defense.ipynb)

To begin Module 7:

1. Open the Module 7 folder in the course's GitHub repository using your cyber range browser.
2. Select `Module7_AISecurityOperations&Defense.ipynb`.
3. Open the notebook in Google Colab. If an **Open in Colab** option is unavailable, visit [Google Colab](https://colab.research.google.com/), select the **GitHub** tab, and locate the notebook in the course repository.
4. Select **File → Save a copy in Drive** to create your own editable version.
5. Begin with the Module Overview and Learning Objectives.
6. Complete each section in order, including the reading material, visualizations, hands-on labs, and knowledge checks.

> **Important:** This module is designed for Google Colab. Some code cells use Colab-specific collapsible titles and interactive settings that may display differently in other notebook environments.

---

## How to Work Through the Notebook

### Reading Sections

Each instructional section contains collapsible reading material labeled **Click to Expand**.

Expand the main section and its subsections to review the security concepts, examples, operational procedures, and defensive techniques.

Read the instructional material before completing the associated activities.

### Hands-On Labs

Each of the ten instructional sections includes a hands-on lab.

These labs introduce practical AI security operations concepts through simulated environments and security scenarios.

You will investigate security events, establish baselines, develop detection rules, analyze attack indicators, and evaluate defensive controls.

The exercises build on one another to prepare you for the final capstone investigation.

### Interactive Code Cells

The notebook contains Python code cells that simulate different aspects of AI security operations.

These activities may involve:

- Creating AI asset inventories.
- Mapping AI system dependencies.
- Establishing trusted baselines.
- Collecting and analyzing telemetry.
- Identifying suspicious model behavior.
- Detecting query-based model extraction.
- Investigating data poisoning indicators.
- Detecting prompt injection attempts.
- Building rule-based detections.
- Evaluating false positives and false negatives.
- Reconstructing incident timelines.
- Applying containment controls.
- Validating trusted model artifacts.
- Testing recovery procedures.
- Conducting red-team assessments.
- Developing security playbooks.
- Calculating operational security metrics.

Run each code cell using the **play button** beside the cell.

Review the output and accompanying explanations before continuing.

### Hands-On Learning Context

Hands-on activities include explanations describing what the exercise demonstrates and why the security concept matters.

Read the instructional context before running each activity when it is provided.

These explanations connect the simulated behavior to real-world AI security operations.

### Knowledge Checks

Complete the knowledge checks and interactive questions throughout the notebook.

These exercises reinforce the concepts introduced in each section and help prepare you for the final capstone lab.

Review the feedback and explanations provided when an answer is incorrect.

### Working in Google Colab

- Run code cells in the intended order.
- Allow each cell to finish executing before continuing.
- Follow the instructions provided for each activity.
- Modify only the variables or configurations identified for experimentation.
- Review generated tables, security findings, detection results, and visualizations.
- Save your notebook periodically.
- If your runtime disconnects or restarts, rerun the necessary setup cells.

The labs use simulated AI systems and security events rather than requiring access to production infrastructure.

This allows you to practice security operations in a controlled environment without requiring paid cloud services or access to real organizational systems.

---

## Hands-On Activities

### Section 1 — Introduction to AI Security Operations

In this lab, you will examine how security operations protect deployed AI systems.

You will explore the responsibilities involved in identifying suspicious activity, investigating security events, and maintaining trusted operation.

You will:

- Examine a simulated AI service.
- Identify normal operational conditions.
- Review security events.
- Identify suspicious behavior.
- Determine whether an event requires investigation.
- Examine incident severity.
- Respond to a security event.
- Evaluate recovery and improvement activities.

The activity demonstrates why AI security requires continuous monitoring and operational defense rather than relying exclusively on controls implemented during development.

### Section 2 — AI Asset Inventory & Security Baselines

This lab focuses on identifying and documenting the components that make up an AI system.

You will:

- Build an initial AI asset inventory.
- Evaluate inventory coverage.
- Create a model record.
- Document training datasets.
- Generate trusted artifact hashes.
- Map AI asset lineage.
- Trace downstream dependencies.
- Establish trusted security baselines.
- Identify deviations from expected conditions.
- Detect untrusted system states.
- Locate trusted recovery options.

The activity demonstrates why defenders must understand which assets exist, how they are connected, and what their trusted states should look like.

### Section 3 — AI Security Monitoring & Telemetry

This lab examines how security teams collect and analyze operational information from AI systems.

You will:

- Collect simulated AI security telemetry.
- Identify different telemetry sources.
- Establish normal operating conditions.
- Monitor expected activity.
- Examine abnormal events.
- Compare normal and suspicious telemetry.
- Correlate multiple security signals.
- Monitor model performance.
- Validate telemetry protection.

The activity demonstrates why effective AI monitoring requires visibility into both traditional infrastructure behavior and AI-specific model activity.

### Section 4 — Detecting AI Attacks

This lab focuses on identifying indicators associated with attacks against AI systems.

You will investigate several simulated attack scenarios, including:

- Adversarial prediction instability.
- Query-based model extraction.
- Data poisoning.
- Trigger-dependent backdoor behavior.
- Prompt injection.
- Suspicious AI agent actions.
- Resource exhaustion.

You will also evaluate detection errors, measure detection quality, and examine how multiple signals can strengthen an investigation.

The activity demonstrates why defenders should use multiple forms of evidence rather than relying on a single alert or performance measurement.

### Section 5 — AI Security Detection Engineering

This lab introduces the process of developing and improving security detections.

You will:

- Develop a detection hypothesis.
- Create rule-based detections.
- Identify unusual query volumes.
- Analyze session behavior.
- Correlate multiple security signals.
- Assign alert severity.
- Test detection quality.
- Measure detection performance.
- Compare detection thresholds.
- Examine detection evasion.
- Improve detection coverage.
- Document detection logic.
- Review the detection engineering lifecycle.

The activity demonstrates why detection rules must be tested, measured, documented, and continuously improved.

### Section 6 — AI Incident Response

This lab introduces the procedures used to investigate and respond to security incidents affecting AI systems.

You will:

- Validate a suspected security incident.
- Determine incident scope.
- Preserve evidence.
- Apply containment controls.
- Reconstruct the incident timeline.
- Identify the likely entry point.
- Remove untrusted components.
- Select trusted recovery artifacts.
- Restore production operation.
- Validate recovery.
- Enable enhanced monitoring.
- Document lessons learned.
- Review the incident response lifecycle.

The activity demonstrates why incident response must address both the compromised infrastructure and the trustworthiness of the AI system itself.

### Section 7 — Model Recovery, Rollback & Resilience

This lab examines how organizations restore AI systems after a security incident.

You will:

- Identify the last known-good system state.
- Examine model and dataset lineage.
- Select an appropriate recovery strategy.
- Verify recovery information.
- Validate a recovered model.
- Perform a simulated canary redeployment.
- Detect a failed canary deployment.
- Activate a safe fallback mode.
- Prioritize recovery activities.
- Evaluate operational resilience.
- Conduct a recovery drill.
- Review the AI recovery lifecycle.

The activity demonstrates why recovery requires more than restarting a service.

Defenders must ensure that the restored model, associated data, and supporting infrastructure can be trusted.

### Section 8 — AI Red Teaming & Continuous Security Testing

This lab examines how organizations proactively test AI systems for security weaknesses.

You will:

- Define the scope of a red-team assessment.
- Conduct model-level security tests.
- Conduct system-level security tests.
- Perform manual adversarial testing.
- Examine automated security testing.
- Implement continuous testing concepts.
- Conduct security regression tests.
- Test AI agent security.
- Evaluate detection and monitoring.
- Measure red-team results.
- Identify testing limitations.
- Review the AI red-team lifecycle.

The activity demonstrates how security testing helps identify weaknesses before they are exploited and validates whether defensive improvements are effective.

### Section 9 — Defense-in-Depth & AI Security Controls

This lab focuses on combining multiple security controls to protect AI systems.

You will:

- Build layered security defenses.
- Combine complementary security controls.
- Classify preventive, detective, and recovery controls.
- Apply least-privilege access.
- Separate model decisions from authorization.
- Protect Retrieval-Augmented Generation systems.
- Test security control failures.
- Map threats to appropriate controls.
- Validate AI supply chain components.
- Apply human oversight.
- Develop a complete defense-in-depth architecture.
- Test layered defenses.
- Examine continuous security improvement.

The activity demonstrates why no single security control can protect an AI system against every possible attack.

Effective security requires multiple independent safeguards.

### Section 10 — AI Security Playbooks, Metrics & Operational Readiness

This lab examines how organizations prepare to respond consistently to AI security incidents.

You will:

- Evaluate operational readiness.
- Develop a model extraction response playbook.
- Add AI-specific incident response actions.
- Assign incident responsibilities.
- Define escalation procedures.
- Measure security operations performance.
- Calculate detection and response metrics.
- Examine security testing metrics.
- Conduct a tabletop exercise.
- Assess operational readiness.
- Identify continuous improvement opportunities.
- Map activities to the NIST AI Risk Management Framework.
- Examine MITRE ATLAS mappings.
- Review the complete AI security operations lifecycle.
- Complete a capstone readiness check.

The activity demonstrates why operational security depends on documented procedures, trained personnel, measurable outcomes, and continuous improvement.

---

## End-of-Module Capstone Lab — Defend an AI System

At the end of Module 7, you will complete a comprehensive security investigation involving a fictional AI system.

The organization operates an AI-powered service that processes requests, uses a trained machine learning model, and relies on several supporting infrastructure components.

The security team has observed suspicious activity that may indicate an attempted compromise.

Your responsibility is to investigate the available evidence, identify the likely security issue, contain the incident, restore trusted operation, and document the results.

The capstone combines concepts from all ten instructional sections.

### Part 1 — AI Asset Inventory

Review the fictional AI environment and identify the important assets involved in operating the system.

Document the components that require protection and consider how they relate to one another.

Use the provided analysis check to evaluate your understanding of the system.

### Part 2 — Establish the Security Baseline

Examine the expected behavior and trusted configuration of the AI service.

Establish reference conditions that can be used to identify suspicious changes.

The baseline provides a comparison point for the remainder of the investigation.

### Part 3 — Analyze Security Telemetry

Review simulated security telemetry collected from the AI system.

Identify unusual activity involving API requests, system behavior, and operational measurements.

Determine which observations may require additional investigation.

### Part 4 — Run Detection Rules

Apply security detection rules to the available telemetry.

Review the alerts generated by the detection logic and determine which conditions were identified.

Complete the detection check to reinforce your understanding of the findings.

### Part 5 — Investigate API Credentials

Examine API credentials associated with the suspicious activity.

Identify the credential that requires investigation and consider how unauthorized use could affect the AI service.

This exercise demonstrates why identity and credential information are important sources of incident evidence.

### Part 6 — Build the Incident Timeline

Use the available security events to reconstruct the sequence of suspicious activity.

Identify when important events occurred and how they may be related.

The timeline helps establish a clearer understanding of the incident.

### Part 7 — Incident Classification

Review the available evidence and classify the suspected security incident.

Determine which attack category best explains the observed behavior.

Use the concepts introduced throughout the course to support your decision.

### Part 8 — Determine Incident Severity

Evaluate the seriousness of the incident.

Consider the potential impact on the AI service, affected assets, and the organization's ability to continue normal operation.

Determine an appropriate severity classification.

### Part 9 — Contain the Incident

Select and apply appropriate containment measures.

The objective is to limit further unauthorized activity while preserving the information needed for investigation.

Consider how containment decisions may affect legitimate service availability.

### Part 10 — Recover Trusted Operation

Restore the AI system to a trusted operating state.

Use the available recovery information to select appropriate components and restore normal operation.

The activity demonstrates why recovery must consider system integrity rather than simply returning a service to an operational state.

### Part 11 — Validate Recovery

Evaluate whether the recovery process was successful.

Confirm that the restored system satisfies the expected security conditions.

Review whether suspicious activity has been addressed and whether additional monitoring is necessary.

### Part 12 — Red-Team Validation

Conduct a simulated security validation exercise against the recovered environment.

Determine whether the defensive improvements address the previously identified weaknesses.

The activity demonstrates why security controls should be tested after recovery.

### Part 13 — Improve Defense-in-Depth

Review the existing security controls and identify opportunities for improvement.

Select additional safeguards that reduce the likelihood or impact of similar incidents.

Consider how preventive, detective, and recovery controls complement one another.

### Part 14 — Calculate Security Metrics

Use the investigation results to calculate security operations measurements.

Evaluate how metrics can help an organization understand detection effectiveness, response performance, and security improvement.

### Part 15 — Generate Lessons Learned

Review the investigation and identify important findings.

Consider which security weaknesses contributed to the incident and how future incidents could be prevented or detected more effectively.

Document recommendations for improving the organization's AI security practices.

### Part 16 — Final Incident Report

Generate a final incident report summarizing the investigation.

The report should communicate the important findings, including:

- The affected AI system.
- Relevant assets.
- Suspicious activity.
- Detection results.
- Incident classification.
- Severity assessment.
- Containment actions.
- Recovery procedures.
- Validation results.
- Recommended security improvements.

The activity demonstrates the importance of communicating security findings in a structured and understandable format.

### Part 17 — Final Knowledge Check

Complete the final knowledge check covering the major concepts from the capstone investigation.

Review the feedback and revisit any concepts that require additional study.

---

## Understanding Your Lab Results

When evaluating the activities in Module 7, consider the following questions:

- Which AI assets were important to the investigation?
- Did the organization have a complete asset inventory?
- Were trusted system baselines available?
- Which telemetry sources revealed suspicious behavior?
- Did the detection rules identify the relevant security events?
- Were any legitimate activities incorrectly flagged?
- Did the investigation reveal multiple related indicators?
- Was the likely attack identified using sufficient evidence?
- Were the affected credentials or components properly investigated?
- Was the incident severity appropriate?
- Did containment reduce further exposure?
- Was the system restored using trusted components?
- Did recovery validation confirm that the system was operating securely?
- Did red-team testing reveal remaining weaknesses?
- Which defense-in-depth controls provided the greatest benefit?
- How could the organization improve its security playbooks and operational readiness?
- What lessons should be carried forward into future AI security operations?

The goal is not simply to generate successful detection or recovery results.

Instead, you should understand how security operations connect monitoring, investigation, response, recovery, and continuous improvement.

---

## Saving and Submitting Your Work

After completing all reading sections, hands-on labs, knowledge checks, and the final capstone:

1. Confirm that you have completed the required activities and entered your responses.
2. Make sure the relevant code cells have executed successfully.
3. Review your generated results, including asset inventories, telemetry, detection results, incident timelines, recovery outcomes, and security metrics.
4. Complete the final incident report.
5. Save your completed notebook in Google Colab.
6. Select **File → Download → Download .ipynb**.
7. Submit the downloaded `.ipynb` file through the submission method specified by your instructor or cyber range.

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

The module uses Python-based simulations to demonstrate AI security operations concepts.

Students are not required to access production monitoring systems, deploy real AI services, or connect to external security platforms.

The exercises are designed to run in a standard Google Colab environment.

Prior experience with AI security operations is not required.

The notebook provides guided explanations and activities designed to introduce the concepts progressively.

Follow any additional setup instructions provided within the notebook.

---

## Responsible Use

The activities demonstrated in this module are intended for **authorized educational and research purposes**.

All detection engineering, incident response, red teaming, and recovery exercises should be performed using the provided simulations and controlled notebook environment.

Do not attempt to access unauthorized AI systems, compromise production services, interfere with monitoring infrastructure, or conduct security testing against systems without explicit permission.

The purpose of these activities is to develop the knowledge and skills needed to detect, investigate, respond to, and recover from AI security threats.

---

## References

A collapsible **Module 7 References** section is included at the end of the notebook.

These references provide additional information about:

- AI security operations.
- AI asset inventories.
- Security monitoring and telemetry.
- AI attack detection.
- Detection engineering.
- Incident response.
- Model recovery and resilience.
- AI red teaming.
- Defense-in-depth strategies.
- Security operations metrics.
- Operational readiness.
- NIST AI Risk Management Framework.
- MITRE ATLAS.

Students are encouraged to consult these sources when reviewing the concepts covered throughout the module.

---

## Module Completion

After completing Module 7, make sure you can:

- Explain the purpose of continuous AI security operations.
- Identify and document important AI assets.
- Establish trusted security baselines.
- Collect and analyze AI security telemetry.
- Recognize indicators associated with AI-specific attacks.
- Develop and evaluate security detection rules.
- Explain the importance of detection thresholds and alert quality.
- Investigate suspicious AI system behavior.
- Apply appropriate incident response procedures.
- Preserve evidence and reconstruct incident timelines.
- Select containment strategies for compromised AI systems.
- Restore models and infrastructure using trusted recovery information.
- Evaluate recovery and rollback procedures.
- Explain how AI red teaming supports continuous security testing.
- Recommend layered security controls.
- Develop incident response playbooks.
- Interpret security operations metrics.
- Evaluate operational readiness.
- Apply relevant AI security frameworks.
- Complete an AI security investigation and produce a final incident report.

---

## Course Completion

**Congratulations on reaching the final module of the Securing AI certification course.**

Throughout this course, you have explored the security challenges associated with developing, training, deploying, and operating artificial intelligence systems.

Across the modules, you have examined:

- Foundations of AI security.
- Threat modeling AI systems.
- Supply chain and data-level attacks.
- Model exploitation techniques.
- LLM security and prompt injection.
- Secure deployment and infrastructure.
- AI security operations and defense.

You have also completed hands-on activities involving attack simulations, security analysis, detection, defensive controls, and incident response.

The knowledge and skills developed throughout this course provide a foundation for understanding and addressing security risks across the AI lifecycle.

**Final Step:** Complete the Module 7 capstone, save your finished notebook, and follow your instructor's directions for final course submission and certification completion.
