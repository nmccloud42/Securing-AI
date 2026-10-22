# Module 3 — Supply Chain and Data-Level Attacks

## Module Overview

Welcome to **Module 3: Supply Chain and Data-Level Attacks** of the Securing AI certification course.

In Module 2, you learned how to identify threats, evaluate risks, and develop security controls for AI systems. This module builds on those concepts by examining how attackers can compromise the resources and training data used to develop machine learning models.

Modern AI systems depend on datasets, pretrained models, software libraries, development environments, and third-party services. Together, these resources form the **AI supply chain**.

A security weakness introduced anywhere in this supply chain can influence the trustworthiness of the final AI system.

This module focuses primarily on **data poisoning**, a category of attacks in which adversaries manipulate training information to influence how a machine learning model behaves.

You will explore:

- AI supply chain components, dependencies, and trust relationships.
- Data poisoning techniques and attacker objectives.
- Label-flipping attacks.
- Clean-label poisoning.
- Data injection and duplication attacks.
- Data drift and distribution manipulation.
- Techniques for detecting and mitigating poisoned training data.
- Defense-in-depth strategies for protecting AI training pipelines.

Throughout the module, you will use Google Colab to examine how manipulated training data affects model performance and experiment with defensive techniques.

The module concludes with an investigation of a compromised machine learning training pipeline.

---

## Learning Objectives

By the end of this module, you should be able to:

1. Explain the AI supply chain and identify the components involved in developing and deploying machine learning systems.
2. Identify supply chain risks associated with datasets, pretrained models, software dependencies, third-party services, and infrastructure.
3. Explain data poisoning and how manipulated training information can influence model behavior.
4. Distinguish between targeted and untargeted poisoning attacks.
5. Demonstrate how label-flipping attacks affect machine learning classification.
6. Explain clean-label poisoning and examine how feature manipulation can influence a model without changing training labels.
7. Demonstrate how data injection and duplication can change the composition of a training dataset.
8. Explain how distribution manipulation and data drift can affect model performance.
9. Evaluate poisoning attacks using accuracy, balanced accuracy, recall, and other performance measurements.
10. Apply anomaly detection and data filtering techniques to identify and mitigate suspicious training samples.
11. Explain defense-in-depth strategies for securing training data and AI development pipelines.
12. Investigate a potentially compromised training dataset and evaluate whether defensive measures improve model performance.

---

## Module Contents

| Section | Topic | What You Will Learn |
|---|---|---|
| 1 | Understanding the AI Supply Chain | Identify AI supply chain components, important assets, third-party dependencies, trust relationships, and attack surfaces. |
| 2 | Introduction to Data Poisoning | Understand how poisoning works, attacker objectives, poisoning rates, and methods for measuring attack impact. |
| 3 | Label-Flipping Attacks | Manipulate training labels and observe how incorrect labels influence model performance. |
| 4 | Clean-Label Poisoning | Examine attacks that manipulate training features while preserving their original labels. |
| 5 | Data Injection and Duplication Attacks | Explore how adding or duplicating training samples can influence machine learning behavior. |
| 6 | Data Drift & Distribution Manipulation | Investigate how changes to training-data distributions affect model reliability. |
| 7 | Detecting and Mitigating Poisoned Data | Apply anomaly detection and mitigation techniques to suspicious training datasets. |
| 8 | Defense in Depth for Training Data | Identify multiple security controls that protect training data throughout the AI lifecycle. |
| 9 | End-of-Module Lab | Investigate a compromised training pipeline, identify suspicious changes, and evaluate defensive measures. |

---

## Getting Started

**Notebook:** [Module3_SupplyChain_DataLevelAttacks.ipynb](./Module3_SupplyChain_DataLevelAttacks.ipynb)

To begin Module 3:

1. Open the Module 3 folder in the course's GitHub repository using your cyber range browser.
2. Select `Module3_SupplyChain_DataLevelAttacks.ipynb`.
3. Open the notebook in Google Colab. If an **Open in Colab** option is unavailable, visit [Google Colab](https://colab.research.google.com/), select the **GitHub** tab, and locate the notebook in the course repository.
4. Select **File → Save a copy in Drive** to create your own editable version.
5. Begin with the Module Overview and Learning Objectives.
6. Complete each section in order, including the reading material, code demonstrations, hands-on activities, and knowledge checks.

> **Important:** This module is designed for Google Colab. Some code cells use Colab-specific collapsible titles and interactive settings that may not display the same way in other notebook environments.

---

## How to Work Through the Notebook

### Reading Sections

Each instructional section contains collapsible reading material labeled **Click to Expand**.

Expand the main section and its subsections to review the concepts, examples, attack descriptions, and defensive techniques.

Read the material before completing the associated activities.

### Interactive Code Cells

The notebook includes Python code cells that demonstrate how different data-level attacks affect machine learning models.

These activities may involve:

- Loading and preparing training datasets.
- Training baseline machine learning classifiers.
- Modifying training labels or features.
- Injecting or duplicating training samples.
- Comparing clean and poisoned datasets.
- Evaluating model performance before and after an attack.
- Detecting suspicious observations.
- Filtering training data and retraining models.

Run each code cell using the **play button** beside the cell.

Some activities allow you to modify variables controlling the simulated attack. Experiment with these values when instructed and observe how the results change.

### Hands-On Learning Context

Hands-on activities include instructional explanations describing what the exercise demonstrates and why the concept matters for AI security.

Read these explanations before running the related experiments.

### Knowledge Checks

Complete the knowledge checks and interactive questions throughout the notebook.

These exercises reinforce the concepts introduced in the reading material and help prepare you for the final lab.

Review the explanations provided when an answer is incorrect.

### Working in Google Colab

- Run code cells in the intended order.
- Allow each cell to finish executing before continuing.
- Change only the variables or settings identified in the activity instructions.
- Review generated tables, metrics, and visualizations.
- Compare results against the clean baseline when appropriate.
- Save your notebook periodically.
- If the runtime disconnects or restarts, rerun the necessary setup and earlier code cells.

Some experiments may produce different results when attack settings change. This is expected and is part of the learning process.

---

## Hands-On Activities

### Section 3 — Label-Flipping Attacks

In this activity, you will manipulate training labels to simulate a data poisoning attack.

You will train a classifier using legitimate training data, modify selected labels, and compare the results.

The exercise demonstrates how an attacker can influence model behavior without directly changing the model's source code.

### Section 4 — Clean-Label Poisoning

This activity introduces a simplified clean-label poisoning scenario.

Instead of changing training labels, you will modify selected feature values while preserving their original labels.

You will examine how feature manipulation can influence a classifier and why some poisoning attempts may be difficult to identify through label inspection alone.

### Section 5 — Data Injection and Duplication Attacks

This activity explores how attackers can influence training by changing the number and representation of samples.

You will experiment with duplicated or injected training examples and observe how the altered dataset affects model behavior.

The exercise demonstrates that poisoning does not always require changing existing labels.

### Section 6 — Data Drift & Distribution Manipulation

In this activity, you will examine how manipulating training feature distributions can influence model performance.

You will compare a clean baseline with a model trained using modified data and review the resulting performance measurements.

The exercise also reinforces the distinction between naturally occurring data drift and intentional distribution manipulation.

### Section 7 — Detecting and Mitigating Poisoned Data

This activity introduces the defensive side of data poisoning.

You will examine a suspicious dataset, apply anomaly detection techniques, and evaluate whether filtering potentially poisoned observations improves model performance.

The exercise demonstrates why detecting unusual data is only one part of a larger security investigation.

### Section 8 — Defense in Depth for Training Data

This activity focuses on securing the machine learning training pipeline.

You will examine a pipeline that relies on an external data source and lacks several important security controls.

Through interactive security decisions, you will select appropriate safeguards and receive feedback explaining their relevance.

The activity demonstrates why protecting training data requires multiple complementary controls rather than a single defensive technique.

---

## End-of-Module Lab — Investigating a Compromised Training Pipeline

In **Section 9**, you will complete a guided investigation involving a machine learning system whose performance decreased after new training information was introduced.

The organization's model previously demonstrated strong performance. After retraining with an updated dataset, the security team discovered unexpected changes in model behavior.

The training process completed successfully, and the new data passed basic format validation. However, the results suggest that the training pipeline may have been manipulated.

Your task is to investigate the suspicious dataset, determine what changed, and evaluate possible defenses.

### Part 1 — Investigation Scenario

Review the organization's training pipeline and the circumstances surrounding the unexpected model performance degradation.

Identify the information that should be investigated before concluding that a poisoning attack occurred.

### Part 2 — Establish the Trusted Baseline

Load the dataset and train a model using trusted training information.

Record baseline performance measurements that can be used for comparison later in the investigation.

### Part 3 — Examine the Suspicious Training Data

Investigate the modified training information introduced into the pipeline.

Consider what type of manipulation may have occurred and how it could affect the learning process.

### Part 4 — Compare Dataset Statistics

Compare the trusted dataset against the suspicious dataset.

Examine changes in dataset size, labels, and feature statistics to identify potential indicators of manipulation.

### Part 5 — Train Using the Suspicious Dataset

Train a new classifier using the suspicious training information.

Compare its performance against the trusted baseline to determine whether the changes affected model behavior.

### Part 6 — Identify the Attack and Select a Defense

Use the evidence collected during the investigation to identify the likely poisoning technique.

Complete the interactive investigation questions and select an appropriate technique for identifying suspicious observations.

### Part 7 — Apply Anomaly Detection and Mitigation

Use anomaly detection to flag unusual training samples.

Evaluate how removing suspicious observations changes the dataset and prepare the filtered data for retraining.

### Part 8 — Evaluate the Mitigated Model

Train a model using the mitigated dataset.

Compare the clean, attacked, and mitigated models using performance measurements such as accuracy and balanced accuracy.

Determine whether the defensive technique improved performance and consider any remaining limitations.

---

## Understanding Your Lab Results

When evaluating your results, consider the following questions:

- How did the suspicious dataset differ from the trusted dataset?
- Were training labels changed, or were the feature values manipulated?
- Did the poisoning attack reduce overall accuracy?
- Were some classes affected more than others?
- Did anomaly detection identify suspicious observations?
- Did removing flagged samples improve model performance?
- Could legitimate samples have been removed during filtering?
- What additional security controls could help prevent similar attacks?

The purpose of the investigation is not simply to achieve a particular accuracy score.

Instead, you should understand how the attack influenced the training process, what evidence supports your conclusions, and whether the selected defensive measures were effective.

---

## Saving and Submitting Your Work

After completing all reading sections, activities, knowledge checks, and the final lab:

1. Confirm that you have completed the required activities and entered your responses.
2. Make sure the relevant code cells have executed successfully.
3. Review the generated results, including performance metrics and visualizations.
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

The module uses common Python machine learning libraries, including:

- NumPy
- Matplotlib
- Scikit-learn

The notebook includes guided examples and activities intended for learners who are new to AI security.

Students do not need extensive machine learning experience to complete the exercises.

Follow any additional setup instructions provided within the notebook.

---

## Responsible Use

The attacks demonstrated in this module are intended for **authorized educational and research purposes**.

All poisoning experiments should be performed using the provided datasets and controlled notebook environments.

Do not attempt to poison datasets, compromise machine learning pipelines, or interfere with AI systems without explicit authorization.

The purpose of these activities is to understand how attacks work so that AI systems can be designed, evaluated, and defended more effectively.

---

## References

A collapsible **Module References** section is included at the end of the notebook.

These references provide additional information about AI supply chain security, data poisoning, label manipulation, clean-label attacks, distribution manipulation, and defensive techniques.

Students are encouraged to consult these sources when reviewing the concepts covered throughout the module.

---

## Module Completion

Before continuing to the next module, make sure you can:

- Explain how the AI supply chain introduces security dependencies.
- Describe several common data poisoning techniques.
- Distinguish between targeted and untargeted poisoning.
- Explain the differences between label flipping and clean-label poisoning.
- Describe how injection, duplication, and distribution manipulation affect training data.
- Compare clean and poisoned model performance.
- Explain how anomaly detection can help identify suspicious training samples.
- Recognize the limitations of automated poisoning detection.
- Identify appropriate defense-in-depth controls for AI training pipelines.
- Investigate suspicious training data and evaluate whether mitigation improved model performance.

**Next Step:** After completing Module 3, continue to the next module in the Securing AI certification course.
