# Module 5 — LLM Security and Prompt Injection

## Module Overview

Welcome to **Module 5: LLM Security and Prompt Injection** of the Securing AI certification course.

In Module 4, you examined attacks that target trained machine learning models, including adversarial examples, model extraction, membership inference, model inversion, and API-based exploitation.

This module builds on those concepts by examining the unique security challenges associated with **Large Language Models (LLMs)** and the applications built around them.

LLM-powered applications often do more than generate text. They may retrieve information from external documents, access internal knowledge bases, process sensitive information, interact with APIs, and execute actions through connected tools.

These capabilities introduce security risks that extend beyond the underlying language model.

One of the most important threats is **prompt injection**, in which an attacker attempts to influence an LLM-powered application's behavior by placing malicious instructions into content the application processes.

This module examines several important LLM security topics, including:

- LLM attack surfaces and threat modeling.
- Direct prompt injection.
- Indirect prompt injection.
- Jailbreaking and adversarial prompt attacks.
- Prompt leakage and sensitive information disclosure.
- Retrieval-Augmented Generation (RAG) security.
- Knowledge base poisoning.
- LLM agents and tool exploitation.
- AI security testing, monitoring, and defense.
- Defense-in-depth strategies for LLM applications.

Throughout the module, you will investigate a fictional AI assistant called **SecureAssist**.

SecureAssist is an LLM-powered application designed to help employees access company policies, retrieve documents, and interact with internal services.

As the module progresses, SecureAssist will gain additional capabilities, introducing new security risks that you will investigate through guided exercises.

The module concludes with a comprehensive security assessment in which you will identify vulnerabilities, test security controls, and evaluate whether the application can perform legitimate tasks without exposing sensitive information or executing unauthorized actions.

---

## Learning Objectives

By the end of this module, you should be able to:

1. Identify the attack surfaces of LLM-powered applications, including prompts, retrieval systems, tools, APIs, memory, and external data sources.
2. Develop a basic threat model for an LLM application by identifying assets, trust boundaries, attacker capabilities, and potential security impacts.
3. Explain direct prompt injection and how malicious user instructions can conflict with an application's intended behavior.
4. Explain indirect prompt injection and how malicious instructions embedded in external content can influence an LLM application.
5. Distinguish between prompt injection and jailbreaking techniques.
6. Identify security risks associated with prompt leakage and sensitive information disclosure.
7. Explain how Retrieval-Augmented Generation systems can be affected by malicious documents and knowledge base poisoning.
8. Identify security risks associated with LLM agents, connected tools, and excessive permissions.
9. Explain how unauthorized tool execution can affect confidentiality, integrity, and availability.
10. Apply basic security testing techniques to evaluate LLM application behavior.
11. Interpret attack success rates and legitimate task success measurements.
12. Identify suspicious activity through security logs and application monitoring.
13. Recommend defensive controls such as access restrictions, trusted retrieval, tool authorization, human approval, and output validation.
14. Explain why LLM security requires protecting the complete application rather than relying exclusively on the model.
15. Perform a security assessment of a simulated LLM application and evaluate the effectiveness of defensive improvements.

---

## Module Contents

| Section | Topic | What You Will Learn |
|---|---|---|
| 1 | LLM Attack Surface & Threat Modeling | Identify important LLM application components, assets, trust boundaries, and potential attack paths. |
| 2 | Direct Prompt Injection | Understand how attacker-controlled user prompts can attempt to override an application's intended behavior. |
| 3 | Indirect Prompt Injection | Investigate malicious instructions embedded in external documents and other lower-trust content. |
| 4 | Jailbreaking and Adversarial Prompt Attacks | Examine how adversarial prompts attempt to bypass an application's behavioral restrictions. |
| 5 | Prompt Leakage and Sensitive Information Disclosure | Explore how LLM applications may expose hidden instructions or protected information. |
| 6 | RAG Security and Knowledge Poisoning | Investigate how manipulated knowledge base documents can influence retrieved information and application responses. |
| 7 | LLM Agents and Tool Exploitation | Examine the risks associated with connected tools, excessive permissions, and unauthorized actions. |
| 8 | AI Security Testing, Monitoring, and Defense | Evaluate adversarial behavior, security testing results, defensive controls, and suspicious activity. |
| 9 | End-of-Module Security Assessment | Perform a security review of SecureAssist, identify vulnerabilities, implement defenses, and retest the application. |

---

## Getting Started

**Notebook:** [Module5_LLMSecurity&PromptInjection.ipynb](./Module5_LLMSecurity%26PromptInjection.ipynb)

To begin Module 5:

1. Open the Module 5 folder in the course's GitHub repository using your cyber range browser.
2. Select `Module5_LLMSecurity&PromptInjection.ipynb`.
3. Open the notebook in Google Colab. If an **Open in Colab** option is unavailable, visit [Google Colab](https://colab.research.google.com/), select the **GitHub** tab, and locate the notebook in the course repository.
4. Select **File → Save a copy in Drive** to create your own editable version.
5. Begin with the Module Overview and Learning Objectives.
6. Complete each section in order, including the reading material, interactive demonstrations, hands-on activities, and knowledge checks.

> **Important:** This module is designed for Google Colab. Some code cells use Colab-specific collapsible titles and interactive settings that may display differently in other notebook environments.

---

## How to Work Through the Notebook

### Reading Sections

Each instructional section contains collapsible reading material labeled **Click to Expand**.

Expand the main section and its subsections to review the concepts, examples, attack scenarios, and defensive techniques.

Read the instructional material before completing the associated activities.

### Hands-On Learning Context

Hands-on activities include explanations describing what the exercise demonstrates and why the security concept matters.

Read the **Hands-On Learning Context** before completing the associated activity when it is provided.

These explanations connect the simulated behavior to real-world LLM application security challenges.

### Interactive Code Cells

The notebook contains Python code cells that simulate vulnerable and defended LLM application behavior.

These activities may involve:

- Identifying LLM application components and trust boundaries.
- Testing malicious instructions against simulated assistants.
- Processing attacker-controlled documents.
- Comparing legitimate and adversarial requests.
- Simulating sensitive information disclosure.
- Manipulating retrieved knowledge base content.
- Testing connected tool permissions.
- Measuring attack success rates.
- Comparing vulnerable and defended applications.
- Reviewing suspicious security events.

Run each code cell using the **play button** beside the cell.

Review the results and accompanying explanations before continuing.

### Knowledge Checks

Complete the knowledge checks and interactive questions throughout the notebook.

These activities reinforce the security concepts introduced in each section.

Review any feedback or explanations provided when an answer is incorrect.

### Working in Google Colab

- Run code cells in the intended order.
- Allow each cell to finish executing before continuing.
- Follow the instructions provided for each activity.
- Modify only the variables or inputs identified for experimentation.
- Review generated outputs and security observations.
- Save your notebook periodically.
- If your runtime disconnects or restarts, rerun any necessary setup cells.

Most of the exercises use lightweight simulations rather than requiring access to a live commercial LLM.

This allows you to examine security concepts in a controlled environment without relying on external model APIs.

---

## Hands-On Activities

### Section 1 — LLM Attack Surface & Threat Modeling

In this activity, you will examine the architecture of a fictional LLM-powered assistant called **SecureAssist**.

SecureAssist helps employees retrieve company information and interact with internal services.

The application includes several components, such as:

- User prompts.
- System instructions.
- An LLM.
- A RAG knowledge base.
- Internal company documents.
- Policy search.
- Employee records.
- A messaging system.

You will identify important assets, examine the application's architecture, and determine where trust boundaries exist.

The activity demonstrates why security analysis must consider the entire LLM application rather than only the language model.

### Section 2 — Direct Prompt Injection

This activity introduces direct prompt injection through a simplified SecureAssist simulation.

You will interact with an application that has defined behavioral restrictions.

The exercise demonstrates how attacker-controlled user prompts may attempt to override those restrictions.

You will compare legitimate requests with malicious instructions and examine whether the application follows its intended security rules.

The activity demonstrates why user-provided text should not automatically be treated as trusted instructions.

### Section 3 — Indirect Prompt Injection

In this lab, SecureAssist has been given the ability to summarize external documents.

You will compare a legitimate document with a malicious document containing an embedded instruction.

Unlike direct prompt injection, the attacker does not place the malicious instruction directly into the user's request.

Instead, the malicious instruction enters through an external document processed by the application.

You will examine how an insecure document processor may mistake attacker-controlled document content for an instruction.

The activity demonstrates the importance of maintaining trust boundaries between external information and application instructions.

### Section 4 — Jailbreaking and Adversarial Prompt Attacks

This lab uses a fictional assistant responsible for protecting a castle.

The assistant knows a fictional secret phrase that it must not reveal to unauthorized users.

You will:

- Establish normal assistant behavior.
- Test several adversarial prompt styles.
- Examine whether the secret phrase is exposed.
- Calculate an Attack Success Rate.
- Introduce a simple defensive measure.
- Compare results before and after the defense.

The activity demonstrates how attackers may attempt to bypass application restrictions using adversarial prompts.

It also introduces the importance of measuring whether an attack achieved its intended objective.

### Section 5 — Prompt Leakage and Sensitive Information Disclosure

In this lab, SecureAssist has been connected to a simulated employee information system.

The system contains both public and private employee information.

You will examine a vulnerable design in which the assistant can access complete employee records and is expected to determine which information should be disclosed.

The exercise demonstrates why relying on the assistant alone to protect sensitive information can create security risks.

You will investigate unauthorized information disclosure and examine how application-level authorization controls can reduce exposure.

The activity reinforces the importance of separating access to sensitive information from the model's ability to generate responses.

### Section 6 — RAG Security and Knowledge Poisoning

In this lab, SecureAssist uses a knowledge base to answer employee questions.

The application retrieves relevant documents and uses their contents to produce responses.

An attacker has gained the ability to introduce a document into the knowledge base.

You will investigate how this attacker-controlled information may influence the application's responses.

The activity demonstrates how an attacker can manipulate an LLM application without modifying the underlying model.

You will also examine why document trust, retrieval controls, and knowledge base integrity are important for secure RAG systems.

### Section 7 — LLM Agents and Tool Exploitation

In this lab, SecureAssist has been upgraded into a simplified LLM agent.

The application can access three tools:

- Policy Search.
- Employee Lookup.
- Message Sender.

The vulnerable application assumes that a tool should execute whenever the assistant requests it.

You will investigate why this design creates security risks.

The exercise demonstrates how attacker-controlled instructions can potentially influence actions involving connected tools.

You will examine the importance of tool authorization, permission boundaries, and approval requirements.

The activity reinforces the principle that an LLM's request to execute a tool should not automatically be treated as authorization.

### Section 8 — AI Security Testing, Monitoring, and Defense

This lab combines several concepts from the earlier sections.

You will act as a security tester evaluating a simplified version of SecureAssist.

The application will receive both legitimate and adversarial requests.

You will:

- Create or use a security test suite.
- Evaluate normal application behavior.
- Test adversarial requests.
- Measure Attack Success Rate.
- Measure Benign Task Success Rate.
- Introduce a defensive improvement.
- Repeat the security tests.
- Examine security logs for suspicious activity.

The activity demonstrates why defenders must evaluate both security and functionality.

A defensive control should reduce unauthorized behavior while allowing legitimate tasks to continue.

---

## End-of-Module Lab — SecureAssist Security Assessment

In **Section 9**, you will complete a comprehensive security assessment of SecureAssist before the application is deployed.

SecureAssist is designed to:

- Answer company policy questions.
- Retrieve internal documents.
- Access employee information.
- Send internal messages.

The development team reports that the application is functioning correctly, but it has not yet undergone a complete security review.

Your responsibility is to examine the application, identify security weaknesses, test potentially malicious requests, introduce defensive controls, and determine whether the application can continue performing legitimate tasks securely.

### Part 1 — Examine SecureAssist

Review the application's initial configuration, knowledge base, employee records, and connected tools.

Identify important assets and consider which information or actions require protection.

Pay particular attention to the difference between trusted company policies and information that may have been uploaded from less-trusted sources.

### Part 2 — Load Vulnerable SecureAssist

Examine the intentionally vulnerable version of SecureAssist.

The application contains several weak security decisions that may allow unauthorized information disclosure, untrusted retrieval, or unsafe tool behavior.

Before implementing defenses, understand how the vulnerable application processes requests.

### Part 3 — Establish Baseline

Submit normal employee requests to the vulnerable application.

Observe how SecureAssist responds to legitimate questions.

This establishes a baseline for comparing the application's behavior before and after security improvements.

### Part 4 — Run Security Tests

Test the application using several security-focused requests.

The tests examine whether SecureAssist:

- Reveals hidden system instructions.
- Exposes private employee information.
- Returns untrusted policy information.
- Performs unauthorized messaging actions.

Review each response and determine which security property may have been violated.

### Part 5 — Classify the Findings

Examine the security issues discovered during testing.

Classify the findings according to the relevant vulnerability or attack category.

These may include:

- Prompt or information disclosure.
- Sensitive information disclosure.
- Unsafe retrieval and knowledge poisoning.
- Tool exploitation.

The activity demonstrates why a complete security assessment should identify multiple weaknesses rather than focusing on only one attack.

### Part 6 — Secure the Application

Examine and implement defensive improvements to SecureAssist.

The defended application introduces different controls for different security risks.

These include:

- Restricting access to hidden configuration information.
- Requiring authorization for sensitive employee data.
- Retrieving information from trusted policy sources.
- Requiring approval before performing certain external actions.

The exercise demonstrates how independent security controls can work together to reduce the impact of multiple attack types.

### Part 7 — Retest After Defense

Repeat the security tests against the defended version of SecureAssist.

Compare the results with the original vulnerable application.

Determine whether the new controls prevented the previously observed unauthorized behavior.

The activity demonstrates why defensive measures should be validated through repeatable security testing.

### Part 8 — Test Legitimate Access

Evaluate whether the defended application can still perform authorized tasks.

These tests examine whether:

- Employees can retrieve approved company policies.
- Authorized personnel can access protected information.
- Approved external actions can still occur.

The exercise demonstrates that security should not simply block all functionality.

Effective security controls should restrict unauthorized behavior while preserving legitimate application capabilities.

### Part 9 — Final Module Assessment

Complete the final assessment questions covering the major concepts from Module 5.

Apply your understanding of:

- LLM attack surfaces.
- Prompt injection.
- Information disclosure.
- RAG security.
- Knowledge poisoning.
- Tool exploitation.
- Authorization.
- Defense in depth.
- Security testing.

Review the results to identify concepts that may require additional study.

---

## Understanding Your Lab Results

When evaluating the activities in Module 5, consider the following questions:

- What was the attacker's objective?
- Which application component introduced the security weakness?
- Did the attack originate from a user prompt or an external information source?
- Did the application treat untrusted content as an instruction?
- Was hidden or sensitive information disclosed?
- Did the application retrieve information from a trustworthy source?
- Did the assistant request or execute an unauthorized tool action?
- Which trust boundary was crossed?
- Did the attack succeed against the vulnerable application?
- Which defensive control addressed the observed weakness?
- Did the defense prevent the same behavior during retesting?
- Could legitimate users still complete their tasks after the defense was introduced?

The goal is not simply to cause an application to produce an unexpected response.

Instead, you should understand which security property was violated, how the attack crossed a trust boundary, and whether the implemented defense reduced the associated risk.

---

## Saving and Submitting Your Work

After completing all reading sections, hands-on activities, knowledge checks, and the final security assessment:

1. Confirm that you have completed the required activities and entered your responses.
2. Make sure the relevant code cells have executed successfully.
3. Review the generated results, including attack outcomes, defensive comparisons, and assessment feedback.
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

The module primarily uses lightweight Python simulations to demonstrate LLM application security concepts.

A paid LLM subscription or external model API key is not required for the simulated activities described in this module.

Prior experience with LLM security is not required.

The notebook provides guided explanations and experiments designed to introduce the concepts progressively.

Follow any additional setup instructions provided within the notebook.

---

## Responsible Use

The attacks demonstrated in this module are intended for **authorized educational and research purposes**.

All prompt injection, jailbreaking, information disclosure, knowledge poisoning, and tool exploitation experiments should be performed using the provided simulated applications and controlled notebook environment.

Do not attempt to access confidential information, bypass security controls, manipulate production knowledge bases, or execute unauthorized actions against real AI applications.

The purpose of these activities is to understand LLM security vulnerabilities so that applications can be designed, evaluated, and defended more effectively.

---

## References

A collapsible **References** section is included at the end of the notebook.

These references provide additional information about:

- Adversarial machine learning.
- LLM application security.
- Prompt injection.
- Jailbreaking.
- Sensitive information disclosure.
- Retrieval-Augmented Generation security.
- Knowledge poisoning.
- LLM agent and tool security.
- AI security testing and defensive architecture.

Students are encouraged to consult these sources when reviewing the concepts covered throughout the module.

---

## Module Completion

Before continuing to the next module, make sure you can:

- Identify the major components and attack surfaces of an LLM-powered application.
- Explain why LLM security requires protecting more than the underlying model.
- Distinguish between direct and indirect prompt injection.
- Explain how adversarial prompts attempt to bypass application restrictions.
- Recognize the risks associated with prompt leakage and sensitive information disclosure.
- Describe how attacker-controlled documents can affect RAG systems.
- Explain how knowledge poisoning can influence application responses.
- Identify security risks associated with LLM agents and connected tools.
- Explain why tool execution requires independent authorization.
- Evaluate an application's behavior using both adversarial and legitimate requests.
- Interpret Attack Success Rate and Benign Task Success Rate.
- Recognize suspicious application activity through security testing and monitoring.
- Recommend defensive controls that protect sensitive information, retrieval systems, and external actions.
- Explain the importance of defense in depth for LLM applications.
- Perform a basic security assessment of an LLM-powered application and validate defensive improvements.

**Next Step:** After completing Module 5, continue to the next module in the Securing AI certification course.
