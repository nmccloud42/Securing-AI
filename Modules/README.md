# Securing AI — AI System Security Certification Course

## Course Overview

Welcome to the **Securing AI: AI System Security Certification Course**.

This course provides an introduction to the security challenges associated with developing, training, deploying, and operating artificial intelligence (AI) and machine learning (ML) systems.

As artificial intelligence becomes increasingly integrated into modern applications, cybersecurity tools, business operations, and critical infrastructure, protecting these systems becomes an important responsibility.

Traditional cybersecurity practices remain essential, but AI introduces additional security challenges involving training data, model behavior, prediction interfaces, external dependencies, and automated decision-making.

Attackers may attempt to manipulate training datasets, influence model predictions, extract sensitive information, exploit Large Language Models (LLMs), compromise deployment infrastructure, or disrupt AI services.

Understanding these threats requires examining the **entire AI lifecycle**, rather than focusing on a single model or application component.

The Securing AI course introduces learners to these challenges through a combination of instructional readings, guided demonstrations, interactive Python activities, knowledge checks, and practical security assessments.

Throughout the course, you will learn how attackers target AI systems, how defenders identify vulnerabilities, and how security controls can reduce the associated risks.

The course is designed for individuals interested in AI security, cybersecurity, machine learning, and the protection of AI-powered applications.

**No previous experience with AI security is required.**

---

## Course Objectives

By the end of this course, you should be able to:

1. Explain the fundamental concepts of artificial intelligence, machine learning, and AI system security.
2. Identify important security risks associated with AI development, training, deployment, and operation.
3. Apply threat modeling techniques to identify AI assets, attack surfaces, trust boundaries, and potential vulnerabilities.
4. Explain how supply chain weaknesses and manipulated training data can compromise AI systems.
5. Demonstrate common data poisoning techniques and evaluate their effects on machine learning performance.
6. Explain model exploitation techniques, including adversarial examples, model extraction, membership inference, model inversion, and backdoor attacks.
7. Identify security vulnerabilities associated with Large Language Models and LLM-powered applications.
8. Explain direct and indirect prompt injection, jailbreaking, knowledge poisoning, and tool exploitation.
9. Identify security controls for protecting AI APIs, infrastructure, credentials, containers, and deployment pipelines.
10. Explain how logging, monitoring, and detection engineering support AI security operations.
11. Apply incident response and recovery procedures to simulated AI security incidents.
12. Evaluate the effectiveness of preventive, detective, and recovery controls.
13. Analyze attack scenarios and recommend appropriate defense-in-depth strategies.
14. Perform basic AI security assessments using controlled Python simulations.
15. Explain how security should be maintained throughout the complete AI system lifecycle.

---

## Course Structure

The course consists of **seven instructional modules**, progressing from foundational AI security concepts to advanced attack scenarios and operational defense.

Each module builds on the concepts introduced in previous modules.

| Module | Title | Primary Focus |
|---|---|---|
| Module 1 | Introduction to AI Security | AI/ML fundamentals, security risks, and real-world AI failures. |
| Module 2 | Threat Modeling AI Systems | AI attack surfaces, STRIDE, DREAD, FMEA, and security risk analysis. |
| Module 3 | Supply Chain and Data-Level Attacks | AI supply chain risks, data poisoning, label flipping, clean-label attacks, and mitigation. |
| Module 4 | Model Exploitation Techniques | Adversarial attacks, model extraction, membership inference, model inversion, backdoors, and attack chains. |
| Module 5 | LLM Security and Prompt Injection | Prompt injection, jailbreaking, RAG security, information disclosure, and LLM agent exploitation. |
| Module 6 | Secure Deployment and Infrastructure | AI API security, identity management, container hardening, model integrity, and secure deployment. |
| Module 7 | AI Security Operations and Defense | Monitoring, detection engineering, incident response, recovery, red teaming, and operational readiness. |

---

## Course Roadmap

### Module 1 — Introduction to AI Security

**Focus: Understanding why artificial intelligence systems require specialized security protections.**

Module 1 introduces the fundamental concepts needed to understand AI security.

You will examine the differences between artificial intelligence, machine learning, and deep learning, along with the ways these technologies are used in modern systems.

The module also introduces common AI security threats and examines real-world examples of AI failures and misuse.

**Topics Covered:**

- Introduction to artificial intelligence.
- Machine learning and deep learning fundamentals.
- The importance of securing AI systems.
- AI security risks and attack surfaces.
- Adversarial examples.
- Data poisoning.
- Prompt injection.
- Model information leakage.
- AI security incidents and real-world examples.
- AI applications in cybersecurity.

**What You Will Learn:**

By completing this module, you will understand the foundational concepts of AI security and recognize why AI systems require protections beyond traditional software security controls.

---

### Module 2 — Threat Modeling AI Systems

**Focus: Identifying security threats before they are exploited.**

Module 2 introduces structured techniques for identifying and evaluating security risks throughout the AI lifecycle.

You will learn how to identify important assets, examine system components, recognize trust boundaries, and evaluate potential threats.

The module introduces several security analysis frameworks that help organizations prioritize risks and select appropriate defenses.

**Topics Covered:**

- Foundations of threat modeling.
- AI/ML attack surfaces.
- AI system assets and trust boundaries.
- STRIDE threat modeling.
- DREAD risk prioritization.
- Failure Modes and Effects Analysis (FMEA).
- Combining threat modeling frameworks.
- Selecting appropriate security controls.
- Continuous threat model review.

**Hands-On Focus:**

You will apply threat modeling techniques to a simulated AI system and evaluate its potential security weaknesses.

**What You Will Learn:**

By completing this module, you will be able to identify potential AI security threats, prioritize risks, and recommend appropriate controls.

---

### Module 3 — Supply Chain and Data-Level Attacks

**Focus: Protecting the information and dependencies used to train AI systems.**

Module 3 examines security risks associated with the AI supply chain and training datasets.

Machine learning systems depend on data quality and the integrity of the resources used during development.

If attackers manipulate training information, they may influence model predictions or introduce hidden behaviors.

**Topics Covered:**

- Understanding the AI supply chain.
- Third-party dependencies and trust relationships.
- Introduction to data poisoning.
- Targeted and untargeted poisoning.
- Label-flipping attacks.
- Clean-label poisoning.
- Data injection and duplication.
- Data drift and distribution manipulation.
- Detecting suspicious training data.
- Anomaly detection and mitigation.
- Defense in depth for training pipelines.

**Hands-On Focus:**

You will manipulate training datasets in controlled experiments, compare clean and poisoned model performance, and evaluate techniques for detecting suspicious observations.

**What You Will Learn:**

By completing this module, you will understand how data-level attacks influence machine learning systems and how defenders can improve training-data security.

---

### Module 4 — Model Exploitation Techniques

**Focus: Understanding how attackers target trained machine learning models.**

Module 4 examines security threats against models after training, including attacks that manipulate predictions, extract model behavior, and expose sensitive information.

You will investigate how attackers can exploit model interfaces even when they cannot directly access the original training dataset or model parameters.

**Topics Covered:**

- Introduction to model exploitation.
- White-box, gray-box, and black-box attacks.
- Adversarial examples and evasion.
- Fast Gradient Sign Method (FGSM).
- Projected Gradient Descent (PGD).
- Model extraction and model stealing.
- Membership inference.
- Model inversion.
- Transfer attacks and surrogate models.
- Model backdoors and Trojans.
- API and query-based exploitation.
- Model denial of service.
- Multi-stage attack chains.

**Hands-On Focus:**

You will conduct controlled model exploitation experiments, examine attack outcomes, and evaluate security controls intended to reduce model-level risks.

**What You Will Learn:**

By completing this module, you will understand how attackers exploit trained models and how model robustness, privacy protections, and operational safeguards can improve security.

---

### Module 5 — LLM Security and Prompt Injection

**Focus: Securing Large Language Models and the applications built around them.**

Module 5 examines the security challenges associated with LLM-powered applications.

These systems often process untrusted text, retrieve external information, access sensitive records, and interact with connected tools.

Attackers may attempt to manipulate the instructions followed by an application, influence retrieved information, or trigger unauthorized actions.

**Topics Covered:**

- LLM attack surfaces and threat modeling.
- Direct prompt injection.
- Indirect prompt injection.
- Jailbreaking and adversarial prompts.
- Prompt leakage.
- Sensitive information disclosure.
- Retrieval-Augmented Generation (RAG) security.
- Knowledge base poisoning.
- LLM agents and tool exploitation.
- AI security testing.
- Security monitoring and defensive architecture.

**Hands-On Focus:**

You will investigate a fictional LLM-powered assistant called SecureAssist.

Through guided simulations, you will test application behavior, identify security weaknesses, evaluate defensive controls, and determine whether legitimate functionality remains available.

**What You Will Learn:**

By completing this module, you will understand how LLM applications can be manipulated and how trust boundaries, authorization controls, and defense in depth reduce security risks.

---

### Module 6 — Secure Deployment and Infrastructure

**Focus: Protecting the infrastructure supporting deployed AI systems.**

Module 6 examines the security challenges associated with operating AI models in production environments.

AI systems depend on APIs, containers, networks, cloud resources, databases, credentials, and automated deployment pipelines.

Weaknesses in these components can compromise an AI application even when the underlying model is functioning correctly.

**Topics Covered:**

- AI deployment architectures.
- Infrastructure attack surfaces.
- AI API and inference endpoint security.
- Authentication and authorization.
- Identity and access management.
- Least privilege.
- Secrets and credential management.
- Container and runtime security.
- Network segmentation.
- Cloud infrastructure security.
- Model artifact integrity.
- Secure deployment pipelines.
- Logging and monitoring.
- Incident response and recovery.

**Hands-On Focus:**

You will evaluate a fictional AI deployment called SentinelAI.

You will examine its infrastructure, implement security controls, verify model integrity, investigate suspicious activity, and restore trusted operation.

**What You Will Learn:**

By completing this module, you will understand how infrastructure security practices protect AI systems during deployment and operation.

---

### Module 7 — AI Security Operations and Defense

**Focus: Continuously monitoring, defending, and recovering AI systems.**

Module 7 brings together the security concepts introduced throughout the course.

You will examine how organizations maintain visibility into deployed AI systems, detect suspicious behavior, investigate incidents, and restore trusted operation.

The module emphasizes the importance of continuous security rather than treating deployment as the final stage of protection.

**Topics Covered:**

- Introduction to AI security operations.
- AI asset inventories.
- Trusted security baselines.
- Security logging and telemetry.
- Detecting AI-specific attacks.
- Detection engineering.
- AI incident response.
- Model recovery and rollback.
- Operational resilience.
- AI red teaming.
- Continuous security testing.
- Defense-in-depth strategies.
- Security playbooks.
- Security metrics.
- Operational readiness.

**Hands-On Focus:**

You will complete a capstone investigation titled **Defend an AI System**.

The assessment requires you to analyze security telemetry, identify suspicious activity, investigate credentials, classify an incident, apply containment measures, restore trusted operation, and prepare a final incident report.

**What You Will Learn:**

By completing this module, you will understand how AI security concepts can be applied throughout an organization's operational security lifecycle.

---

## How the Course Works

The Securing AI course is delivered through **Google Colab notebooks**.

Each module contains instructional material and interactive activities designed to help you understand and apply AI security concepts.

### Instructional Readings

Each module includes structured reading sections that introduce important concepts, explain security risks, and describe defensive techniques.

Reading sections are organized using collapsible headings so that you can expand the material you are currently studying.

### Interactive Demonstrations

Python code cells demonstrate how different AI security concepts work.

These demonstrations may include:

- Training machine learning models.
- Manipulating training datasets.
- Generating adversarial examples.
- Simulating vulnerable AI applications.
- Evaluating model behavior.
- Analyzing security telemetry.
- Applying defensive controls.

The demonstrations allow you to observe security concepts through practical examples rather than relying exclusively on written explanations.

### Hands-On Labs

Each module includes guided hands-on activities.

These exercises provide opportunities to experiment with attack scenarios, investigate security weaknesses, and evaluate defensive techniques.

Most activities use simulated environments or publicly available educational datasets.

The labs are designed to introduce practical concepts without requiring access to production AI systems.

### Knowledge Checks

Throughout the course, you will encounter interactive knowledge checks.

These activities help reinforce important concepts and provide feedback on your understanding.

Complete the knowledge checks before proceeding to the next section.

### End-of-Module Assessments

Each instructional module concludes with a practical lab or security assessment.

These activities combine concepts introduced throughout the module and allow you to apply them to a larger scenario.

The final module includes a capstone investigation that brings together concepts from across the course.

---

## Getting Started

### Step 1 — Access the Course Repository

Open the course GitHub repository using your cyber range browser or another supported web browser.

The repository contains the instructional notebooks and supporting materials for each module.

### Step 2 — Select a Module

Begin with **Module 1 — Introduction to AI Security**.

The modules are intended to be completed in numerical order because later material builds on earlier concepts.

Open the appropriate module folder and review its README for instructions specific to that module.

### Step 3 — Open the Notebook in Google Colab

Select the module's `.ipynb` notebook file.

Open the notebook using Google Colab.

If an **Open in Colab** option is unavailable:

1. Visit [Google Colab](https://colab.research.google.com/).
2. Select the **GitHub** tab.
3. Locate the course repository.
4. Select the notebook you want to open.

### Step 4 — Save Your Own Copy

Before beginning the activities, select:

**File → Save a copy in Drive**

This creates an editable copy of the notebook in your Google Drive.

Use your personal copy to complete the exercises and record your work.

### Step 5 — Complete the Module

Work through the notebook in order.

For each section:

1. Read the instructional material.
2. Expand any additional subsections.
3. Review the hands-on learning context.
4. Run the associated Python code cells.
5. Examine the generated results.
6. Complete the knowledge checks.
7. Finish the section's activities before moving forward.

### Step 6 — Complete the Final Lab

At the end of the module, complete the practical lab or security assessment.

Review the instructions carefully and complete all required questions, experiments, and analysis tasks.

### Step 7 — Save and Submit Your Work

When you have completed the module:

1. Confirm that your responses and activities are complete.
2. Save your notebook in Google Colab.
3. Select **File → Download → Download .ipynb**.
4. Submit the completed notebook through the method specified by your instructor or cyber range.

Keep a copy of your completed notebook for future reference.

---

## Course Requirements

To participate in this course, you will need:

- Access to the course GitHub repository.
- A modern web browser.
- Access to Google Colab.
- A Google account for saving notebook copies.
- A stable Internet connection.
- Basic computer literacy.
- A willingness to experiment with Python-based activities.

### Recommended Background

The course is designed for beginners interested in AI security.

Previous experience with machine learning, AI security, or advanced Python programming is not required.

However, basic familiarity with cybersecurity concepts, such as authentication, access control, vulnerabilities, and network security, may be helpful.

Students who are new to Python can follow the provided code examples and experiment with the variables identified in the notebook instructions.

---

## Software and Technologies

The course uses several common technologies and educational tools.

| Technology | Purpose |
|---|---|
| Google Colab | Execute Python notebooks and complete interactive labs. |
| GitHub | Access course materials and instructional notebooks. |
| Python | Perform simulations, data analysis, and security experiments. |
| NumPy | Support numerical operations and dataset manipulation. |
| Pandas | Organize and analyze structured data. |
| Matplotlib | Generate graphs and security visualizations. |
| Scikit-learn | Train and evaluate machine learning models. |
| TensorFlow / Keras | Support neural network demonstrations where applicable. |

Additional libraries may be used in specific modules.

Follow the setup instructions included in each notebook.

---

## Course Assessment and Completion

The course emphasizes practical understanding and the ability to apply AI security concepts.

Learners are expected to:

- Review the instructional material in each module.
- Complete the interactive demonstrations.
- Participate in hands-on activities.
- Complete the knowledge checks.
- Finish the end-of-module assessments.
- Document observations and results when requested.
- Complete the final capstone assessment.

### Final Capstone

The final capstone is located in **Module 7 — AI Security Operations and Defense**.

In this assessment, you will investigate a simulated AI security incident and apply concepts introduced throughout the course.

You will:

- Identify important AI assets.
- Establish security baselines.
- Analyze operational telemetry.
- Detect suspicious activity.
- Investigate potential compromise.
- Classify the incident.
- Determine incident severity.
- Apply containment measures.
- Restore trusted operation.
- Validate recovery.
- Evaluate defensive improvements.
- Calculate security metrics.
- Document lessons learned.
- Prepare a final incident report.

The capstone demonstrates how different areas of AI security work together to protect an operational system.

### Certification Completion

Successful completion of the course requires satisfying the learning and assessment requirements established by the course instructor or program administrator.

Completion of individual notebooks does not automatically establish certification eligibility unless the required assessments and submission procedures have been satisfied.

---

## Responsible Use and Ethical Guidelines

The Securing AI course includes demonstrations of techniques that may be used to attack or exploit AI systems.

These exercises are provided for **authorized educational and research purposes only**.

All activities should be performed using the provided datasets, simulated applications, and controlled learning environments.

Students must not:

- Attempt to compromise AI systems without authorization.
- Poison datasets belonging to other organizations.
- Extract proprietary machine learning models without permission.
- Access private or confidential training information.
- Exploit production AI APIs.
- Perform unauthorized prompt injection or tool exploitation against real applications.
- Disrupt operational AI services.
- Interfere with cloud infrastructure or deployment pipelines.

The purpose of studying these techniques is to understand how attacks work so that AI systems can be evaluated, secured, and defended more effectively.

---

## Additional Learning Resources

The course incorporates concepts from established cybersecurity and AI security research.

Individual modules include reference sections containing relevant publications, standards, frameworks, and supporting resources.

Important resources for further study include:

- [NIST AI Risk Management Framework](https://www.nist.gov/itl/ai-risk-management-framework)
- [NIST Adversarial Machine Learning: A Taxonomy and Terminology of Attacks and Mitigations](https://csrc.nist.gov/pubs/ai/100/2/e2025/final)
- [MITRE ATLAS](https://atlas.mitre.org/)
- [OWASP Top 10 for Large Language Model Applications](https://genai.owasp.org/)
- [OWASP Machine Learning Security Top 10](https://owasp.org/www-project-machine-learning-security-top-10/)
- [Google Colab Documentation](https://colab.research.google.com/)
- [Scikit-learn Documentation](https://scikit-learn.org/stable/)

Students are encouraged to review the references included in each module for more detailed information about the topics being studied.

---

## Course Completion Checklist

Use the following checklist to track your progress through the course.

- [ ] **Module 1 — Introduction to AI Security**
- [ ] **Module 2 — Threat Modeling AI Systems**
- [ ] **Module 3 — Supply Chain and Data-Level Attacks**
- [ ] **Module 4 — Model Exploitation Techniques**
- [ ] **Module 5 — LLM Security and Prompt Injection**
- [ ] **Module 6 — Secure Deployment and Infrastructure**
- [ ] **Module 7 — AI Security Operations and Defense**
- [ ] Complete all required knowledge checks.
- [ ] Complete all end-of-module assessments.
- [ ] Complete the final capstone investigation.
- [ ] Submit all required course materials.

---

## Final Course Outcomes

After completing the Securing AI certification course, you should have a foundational understanding of how AI systems can be attacked and how security controls can reduce those risks.

You should be able to:

- Recognize security weaknesses throughout the AI lifecycle.
- Identify important AI assets and attack surfaces.
- Apply threat modeling techniques.
- Explain common data poisoning and model exploitation attacks.
- Identify security risks associated with LLM-powered applications.
- Evaluate deployment and infrastructure security.
- Recognize suspicious AI system behavior.
- Recommend appropriate defensive controls.
- Explain incident response and recovery procedures.
- Conduct basic AI security investigations.
- Understand the importance of continuous security testing and improvement.

The course is intended to provide a foundation for further study, research, and practical work in artificial intelligence security.

**Begin with Module 1 — Introduction to AI Security and progress through the course in numerical order.**
