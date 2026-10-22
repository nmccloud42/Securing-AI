# Module 4 — Model Exploitation Techniques

## Module Overview

Welcome to **Module 4: Model Exploitation Techniques** of the Securing AI certification course.

In Module 3, you examined attacks against the AI supply chain and training data. This module builds on those concepts by exploring how attackers can target trained machine learning models, their prediction interfaces, and the information they have learned.

A machine learning model can become an attack surface even when an attacker cannot directly access its source code, architecture, parameters, or original training dataset.

By interacting with a model and observing its responses, attackers may attempt to manipulate predictions, approximate the model's functionality, infer sensitive training information, reconstruct learned representations, or exhaust the resources required to operate the system.

This module examines several important **model exploitation techniques**, including:

- Adversarial attacks and evasion.
- Model extraction and model stealing.
- Membership inference attacks.
- Model inversion.
- Transfer attacks and surrogate models.
- Model backdoors and Trojan exploitation.
- API and query-based exploitation.
- Model denial of service and resource exhaustion.
- Multi-stage attack chains.

You will also examine defensive approaches such as adversarial training, differential privacy, access controls, output restriction, query monitoring, rate limiting, and defense in depth.

Throughout the module, you will complete guided Python demonstrations, hands-on experiments, knowledge checks, and security analysis activities.

The module concludes with a comprehensive security assessment of a fictional AI prediction service.

---

## Learning Objectives

By the end of this module, you should be able to:

1. Explain model exploitation and identify the security risks associated with trained machine learning models.
2. Distinguish between white-box, gray-box, and black-box attacks.
3. Explain adversarial evasion and demonstrate how manipulated inputs can influence model predictions.
4. Describe adversarial attack techniques, including FGSM, PGD, and Carlini-Wagner attacks.
5. Explain how model extraction attacks use prediction queries to approximate a target model.
6. Describe membership inference and the privacy risks associated with revealing training-set membership.
7. Explain model inversion and how model behavior can expose information about learned representations.
8. Demonstrate how surrogate models can support transferable adversarial attacks.
9. Explain model backdoors, hidden triggers, and attacker-selected model behavior.
10. Identify security weaknesses associated with prediction APIs and query-based attacks.
11. Explain how model denial-of-service attacks can affect the availability of AI systems.
12. Analyze multi-stage attacks that combine multiple model exploitation techniques.
13. Evaluate defensive controls that reduce model exploitation risks.
14. Interpret experimental results to determine whether an attack achieved its objective.
15. Assess the security of a deployed AI system and recommend improvements.

---

## Module Contents

| Section | Topic | What You Will Learn |
|---|---|---|
| 1 | What Is Model Exploitation? | Understand how trained models become attack surfaces and why model-level security matters. |
| 2 | Adversarial Attacks & Evasion | Explore how adversarial inputs can cause incorrect model predictions. |
| 3 | Model Extraction / Model Stealing | Learn how attackers use prediction queries to approximate a target model's behavior. |
| 4 | Membership Inference | Examine how model confidence and behavior can reveal possible training-set membership. |
| 5 | Model Inversion | Explore how model outputs can be used to reconstruct representative information. |
| 6 | Transfer Attacks & Surrogate Models | Understand how attacks developed against one model may affect another. |
| 7 | Model Backdoors & Trojan Exploitation | Investigate hidden triggers and attacker-controlled model behavior. |
| 8 | API & Query-Based Exploitation | Examine how prediction interfaces can be abused through repeated queries. |
| 9 | Model Denial of Service & Resource Exhaustion | Understand how excessive requests and computational demands can affect availability. |
| 10 | Attack Chains & Multi-Stage AI Attacks | Explore how attackers combine techniques to achieve more complex objectives. |
| Final Lab | End-of-Module Security Assessment | Investigate a fictional AI service, identify weaknesses, analyze attack evidence, and recommend defenses. |

---

## Getting Started

**Notebook:** [Module4_ModelExploitationTechniques.ipynb](./Module4_ModelExploitationTechniques.ipynb)

To begin Module 4:

1. Open the Module 4 folder in the course's GitHub repository using your cyber range browser.
2. Select `Module4_ModelExploitationTechniques.ipynb`.
3. Open the notebook in Google Colab. If an **Open in Colab** option is unavailable, visit [Google Colab](https://colab.research.google.com/), select the **GitHub** tab, and locate the notebook in the course repository.
4. Select **File → Save a copy in Drive** to create your own editable version.
5. Begin with the Module Overview and Learning Objectives.
6. Complete each section in order, including the instructional readings, visualizations, hands-on activities, and knowledge checks.

> **Important:** This module is designed for Google Colab. Some code cells use Colab-specific collapsible titles and display settings that may not appear the same way in other notebook environments.

---

## How to Work Through the Notebook

### Reading Sections

Each instructional section contains collapsible reading material labeled **Click to Expand**.

Expand the main section and its subsections to review the security concepts, attack descriptions, examples, and defensive approaches.

Read the instructional material before completing the associated activities.

### Section Visualizations

Each of the ten instructional sections includes visualizations that demonstrate important concepts.

These graphics may illustrate attack processes, model behavior, security risks, evaluation metrics, or defensive techniques.

Expand the visualization code cells, run them when instructed, and review the generated graphics and explanations.

### Hands-On Activities

Sections 2–10 contain guided hands-on labs that demonstrate different model exploitation techniques.

These activities may involve:

- Training baseline machine learning models.
- Generating adversarial examples.
- Comparing clean and manipulated predictions.
- Constructing surrogate models.
- Simulating model extraction.
- Examining membership inference signals.
- Reconstructing representative model inputs.
- Testing backdoor triggers.
- Simulating prediction APIs.
- Monitoring query activity.
- Evaluating resource exhaustion and defensive rate limits.
- Building multi-stage attack chains.

Run each code cell using the **play button** beside the cell.

Read the accompanying explanations to understand what each experiment demonstrates.

### Student Experiments

Several labs include student experiment sections that allow you to modify attack settings or examine how changing conditions affects model behavior.

When completing these experiments:

- Follow the instructions provided in the notebook.
- Modify only the variables identified for experimentation.
- Compare the resulting outputs.
- Consider why the attack succeeded, failed, or produced different results.

### Knowledge Checks

Complete the section checkpoints and lab checks throughout the notebook.

These activities reinforce the security concepts and help you evaluate your understanding.

Review any feedback or explanations provided when an answer is incorrect.

### Working in Google Colab

- Run code cells in the intended order.
- Allow each cell to finish executing before continuing.
- Some experiments may take longer than others because they involve model training or repeated calculations.
- Review generated tables, graphs, predictions, and performance measurements.
- Save your notebook periodically.
- If your runtime disconnects or restarts, rerun any required setup cells.
- Keep your completed notebook in Google Drive until you are ready to submit it.

---

## Hands-On Activities

### Section 2 — Adversarial Attacks & Evasion

In this lab, you will train a machine learning model and examine how adversarial inputs can influence its predictions.

You will:

- Load a dataset.
- Train a clean model.
- Measure baseline performance.
- Generate adversarial examples using the Fast Gradient Sign Method (FGSM).
- Evaluate predictions on adversarial inputs.
- Compare clean and adversarial images.
- Experiment with attack settings.

The activity demonstrates how small, intentionally selected input changes can cause a model to produce incorrect predictions.

### Section 3 — Model Extraction / Model Stealing

This lab demonstrates how an attacker may approximate a target model by observing its predictions.

You will:

- Create a black-box target model.
- Query the target model.
- Collect prediction information.
- Train a surrogate model.
- Compare target and surrogate behavior.
- Examine how query budgets affect extraction.
- Evaluate prediction fidelity.

The activity demonstrates how access to a prediction interface can reveal information about a model's learned behavior.

### Section 4 — Membership Inference

In this lab, you will investigate whether model behavior can reveal information about training-set membership.

You will:

- Prepare member and non-member datasets.
- Train a target classifier.
- Compare prediction confidence for members and non-members.
- Visualize confidence distributions.
- Perform a simplified membership inference attack.
- Evaluate the resulting predictions.

The activity demonstrates how differences in model behavior may create privacy risks.

### Section 5 — Model Inversion

This lab explores how an attacker may use information from a trained model to reconstruct representative inputs.

You will:

- Load the MNIST dataset.
- Train a target model.
- Select an inversion target.
- Perform a model inversion procedure.
- Visualize the reconstructed representation.
- Compare the reconstruction with real dataset examples.
- Experiment with reconstruction settings.

The activity demonstrates how model outputs and learned representations can expose information associated with training data.

### Section 6 — Transfer Attacks & Surrogate Models

This lab investigates adversarial transferability between machine learning models.

You will:

- Load and prepare a dataset.
- Train a target model.
- Train a surrogate model.
- Measure clean performance.
- Generate adversarial examples using the surrogate.
- Evaluate the attack against the surrogate.
- Test whether the examples also affect the target model.
- Examine transferred adversarial inputs.

The activity demonstrates how an attacker may develop an attack using one model and attempt to apply it against another.

### Section 7 — Model Backdoors & Trojan Exploitation

This lab demonstrates how hidden triggers can influence model behavior.

You will:

- Load a dataset.
- Create a backdoor trigger.
- Poison a selected portion of the training data.
- Train a backdoored model.
- Evaluate normal model performance.
- Apply the trigger to test inputs.
- Examine triggered predictions.
- Experiment with attack settings.

The activity demonstrates how a model may behave normally on clean inputs while producing attacker-desired predictions when a trigger is present.

### Section 8 — API & Query-Based Exploitation

This lab explores how prediction interfaces can become attack surfaces.

You will:

- Create a hidden target model.
- Build a simulated prediction API.
- Select an attack input.
- Perform a query-based attack.
- Compare clean and manipulated inputs.
- Analyze the number of queries used.
- Examine simple query-monitoring techniques.

The activity demonstrates how repeated interactions with a model can reveal useful information and how monitoring can help identify suspicious patterns.

### Section 9 — Model Denial of Service & Resource Exhaustion

This lab examines the availability risks associated with AI inference services.

You will:

- Create an AI service simulator.
- Simulate normal request traffic.
- Introduce a high-demand scenario.
- Compare service conditions.
- Estimate service latency.
- Apply defensive rate limiting.
- Validate expensive requests.
- Experiment with request volume and processing capacity.

The activity demonstrates how excessive computational demand can affect AI service availability and how defensive controls can reduce the impact.

### Section 10 — Attack Chains & Multi-Stage AI Attacks

This lab examines how multiple exploitation techniques can be combined into a larger attack sequence.

You will:

- Examine a target environment.
- Select an initial attack stage.
- Choose subsequent attack stages.
- Construct a complete attack chain.
- Visualize the resulting sequence.
- Evaluate defensive decisions.
- Build a defense-in-depth map.

The activity demonstrates why AI security must consider how individual weaknesses can be combined rather than evaluating every attack in isolation.

---

## End-of-Module Lab — AI Model Security Assessment

At the end of Module 4, you will complete a comprehensive security assessment of a fictional machine learning service.

The organization operates a prediction API that allows users to submit inputs to a machine learning classifier and receive predictions and confidence scores.

The organization wants to evaluate whether its existing security controls are sufficient before expanding the service's deployment.

You will act as an **AI security analyst** responsible for reviewing the system, identifying potential weaknesses, interpreting suspicious activity, and recommending defensive improvements.

Unlike the earlier guided labs, the final assessment requires you to determine which security concepts apply to different situations.

### Part 1 — Examine the Target System

Review the fictional AI service and identify its important components, interfaces, and security characteristics.

Consider how authentication, model access, confidence scores, third-party dependencies, and missing controls may affect the system's security.

### Part 2 — Initial Security Assessment

Evaluate the system's initial security posture.

Identify which characteristics provide protection and which may introduce additional exposure.

### Part 3 — Identify the Attack

Examine the provided scenario and determine which model exploitation technique best explains the observed behavior.

Apply concepts from the instructional sections to support your analysis.

### Part 4 — Analyze Query Activity

Review simulated prediction API activity.

Compare normal and unusual query patterns and consider which exploitation techniques may benefit from repeated requests.

Recognize that unusual activity is an indicator requiring investigation, not automatic proof of an attack.

### Part 5 — Analyze the Evidence

Review the available security observations and determine what they suggest about the AI system's exposure.

Use evidence rather than assumptions when evaluating potential attacks.

### Part 6 — Attack Chain Challenge

Examine how multiple attack techniques may be connected.

Identify a plausible sequence in which one technique provides information or capabilities that enable another.

### Part 7 — Defense Selection Challenge

Select security controls that address the weaknesses and attack scenarios identified during the assessment.

Consider which controls provide preventive, detective, or limiting protections.

### Part 8 — Build the Secured Architecture

Review a defense-in-depth architecture for the AI prediction service.

Consider protections such as:

- Authentication and access controls.
- Rate limiting.
- Input validation.
- Resource controls.
- Model robustness testing.
- Output restrictions.
- Logging and query monitoring.
- Model provenance verification.
- Backdoor testing.
- Privacy evaluation.
- Adversarial testing.

The activity demonstrates how multiple controls work together to reduce model exploitation risks.

### Part 9 — Final Lab Assessment

Complete the final assessment questions using the concepts and observations from the investigation.

Apply what you learned about model exploitation, attack chains, and defensive controls.

### Part 10 — Final Reflection

Reflect on the overall security assessment.

Consider:

- Which model exploitation techniques may be difficult to detect.
- Which security controls can address multiple attack types.
- Why high model accuracy does not necessarily demonstrate security.
- Why defenders should examine combinations of attacks rather than treating every technique independently.

Use the reflection questions to connect the technical exercises to the broader challenge of securing deployed AI systems.

---

## Understanding Your Lab Results

When evaluating the activities in Module 4, consider the following questions:

- Did the attack achieve its intended objective?
- How did the model behave before and after the attack?
- Did overall accuracy change?
- Did the attack affect only selected inputs or classes?
- How closely did a surrogate model reproduce the target model's predictions?
- Could model confidence reveal information about training-set membership?
- What information was reconstructed during model inversion?
- Did an adversarial example transfer between models?
- Did a backdoor trigger produce the intended behavior?
- How did query volume influence the attack or service availability?
- Which security controls reduced the observed risk?
- Could multiple exploitation techniques be combined into an attack chain?

The goal is not simply to execute attack code successfully.

Instead, you should understand what each attack attempts to accomplish, what evidence indicates success, and how defenders can reduce the associated risks.

---

## Saving and Submitting Your Work

After completing the reading sections, visualizations, hands-on activities, knowledge checks, and final lab:

1. Confirm that you have completed the required activities and entered your responses.
2. Make sure the relevant code cells have executed successfully.
3. Review your generated results, including performance measurements, graphs, and attack observations.
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

The module includes demonstrations using Python machine learning and visualization libraries.

Some exercises involve model training, iterative attacks, or repeated prediction queries and may require additional execution time.

A GPU runtime may improve performance for certain activities, but students should follow the notebook's instructions for any specific runtime requirements.

Prior experience with model exploitation is not required.

The module provides guided explanations and experiments designed to introduce the concepts progressively.

---

## Responsible Use

The attacks demonstrated in this module are intended for **authorized educational and research purposes**.

All experiments should be performed using the provided datasets, simulated services, and controlled notebook environments.

Do not attempt to extract proprietary models, infer private training information, exploit prediction APIs, disrupt AI services, or interfere with machine learning systems without explicit authorization.

The purpose of these activities is to understand model exploitation techniques so that AI systems can be evaluated, secured, and defended more effectively.

---

## References

A collapsible **Module References** section is included at the end of the notebook.

These references provide additional information about adversarial machine learning, model extraction, membership inference, model inversion, transfer attacks, model backdoors, API exploitation, resource exhaustion, and related defenses.

Students are encouraged to consult these sources when reviewing the concepts covered throughout the module.

---

## Module Completion

Before continuing to the next module, make sure you can:

- Explain how trained machine learning models become attack surfaces.
- Distinguish between white-box, gray-box, and black-box exploitation.
- Describe how adversarial examples influence model predictions.
- Explain how model extraction and surrogate models work.
- Identify privacy risks associated with membership inference and model inversion.
- Describe how adversarial attacks can transfer between models.
- Explain the relationship between hidden triggers and model backdoors.
- Recognize risks associated with prediction APIs and excessive query activity.
- Explain how resource exhaustion can affect AI service availability.
- Identify how multiple model exploitation techniques can form an attack chain.
- Recommend defensive controls that address model exploitation risks.
- Evaluate AI system security using evidence beyond overall model accuracy.
- Perform a basic security assessment of a deployed AI prediction service.

**Next Step:** After completing Module 4, continue to the next module in the Securing AI certification course.
