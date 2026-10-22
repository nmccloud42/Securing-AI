# Module 2 — Threat Modeling AI Systems

## Module Overview

Welcome to **Module 2: Threat Modeling AI Systems** of the Securing AI certification course.

In Module 1, you explored foundational AI security concepts. This module builds on that knowledge by introducing **threat modeling**: a structured process for identifying valuable assets, understanding where attacks could occur, assessing risks, and selecting security controls before an incident happens.

You will examine the AI/ML lifecycle and practice three complementary approaches:

- **STRIDE** — Identify and categorize potential security threats.
- **DREAD** — Score and prioritize identified risks.
- **Failure Modes and Effects Analysis (FMEA)** — Examine possible system failures and their consequences.

The module includes guided explanations, interactive Python activities, knowledge checks, and an end-of-module threat-modeling lab.

---

## Learning Objectives

By the end of this module, you should be able to:

1. Explain the purpose of threat modeling in AI security.
2. Identify important AI system assets, components, data flows, and trust boundaries.
3. Recognize attack surfaces throughout the AI/ML lifecycle.
4. Use STRIDE to identify and classify security threats.
5. Use DREAD-style scoring to prioritize risks.
6. Apply FMEA to analyze failures and their effects.
7. Explain how STRIDE, DREAD, and FMEA work together.
8. Recommend security controls for identified threats and failures.
9. Build a basic threat model for an AI-enabled system.

---

## Module Contents

| Section | Topic | What You Will Learn |
|---|---|---|
| 1 | Foundations of Threat Modeling | Why threat modeling matters and how to begin identifying risks. |
| 2 | Understanding the AI/ML Attack Surface | Where vulnerabilities can arise across data, training, inference, and deployment. |
| 3 | STRIDE for AI Systems | How to classify threats using STRIDE. |
| 4 | DREAD Risk Prioritization | How to compare and prioritize identified threats. |
| 5 | Failure Modes and Effects Analysis (FMEA) | How to identify potential failures and evaluate their consequences. |
| 6 | Combining STRIDE, DREAD, and FMEA | How to integrate the three approaches in a single threat analysis. |
| 7 | From Threat Model to Security Controls | How to match identified risks with appropriate defenses. |
| 8 | Threat Modeling Best Practices and Continuous Review | Why threat models must be maintained as systems change. |
| 9 | End-of-Module Lab | Develop a threat model for an AI-based malware detection system. |

---

## Getting Started

**Notebook:** [Module2_ThreatModelingAISystems.ipynb](./Module2_ThreatModelingAISystems.ipynb)

1. Open this Module 2 folder in the course's GitHub repository using your cyber range browser.
2. Select `Module2_ThreatModelingAISystems.ipynb`.
3. Use **Open in Colab** if available. Alternatively, open [Google Colab](https://colab.research.google.com/), choose the **GitHub** tab, and locate the notebook in the course repository.
4. In Colab, select **File → Save a copy in Drive** so you can work on your own copy without modifying the original course notebook.
5. Follow the notebook from top to bottom, expanding the reading sections and running the activities as directed.

> **Important:** Use Google Colab for this module. Some code cells use Colab-specific collapsible titles and display settings that may appear differently in other notebook environments.

---

## How to Work Through the Notebook

### Reading Sections

Instructional text is organized into collapsible sections labeled **Click to Expand**. Expand each section and its subsections, read the material, and review the examples before moving to the related activities.

### Hands-On Activities

Interactive code cells let you explore attack surfaces, identify STRIDE threats, calculate DREAD and FMEA scores, and recommend security controls.

Run each activity using the **play button** beside its code cell. Read the accompanying **Hands-On Learning Context** and explanations where provided.

### Knowledge Checks

Complete the section checkpoints as you encounter them. These checks help reinforce the concepts before you continue.

Read any feedback or explanations displayed by the notebook and revisit the relevant reading when needed.

### Working in Colab

- Run cells in the intended order, especially when a later activity depends on earlier work.
- Allow each cell to finish before moving to the next one.
- Follow instructions in the notebook when entering or changing responses.
- Save your notebook periodically to preserve your work.
- If your runtime disconnects, reconnect and rerun any cells needed to restore the notebook state.

---

## End-of-Module Lab — AI-Based Malware Detection System

In **Section 9**, you will apply the module's threat-modeling techniques to a fictional AI-based malware detection service.

The system collects and labels file samples, trains and tests a model, stores approved versions, and serves predictions through an API.

The lab contains eight parts:

### Part 1 — Identify Important Assets

Determine which resources require protection within the AI-based malware detection system.

### Part 2 — Identify Trust Boundaries

Locate points where data or control crosses between different trust levels.

### Part 3 — Identify Threats with STRIDE

Identify potential security threats and classify them using the STRIDE framework.

### Part 4 — Prioritize Threats with DREAD

Assess identified threats using DREAD-style risk scoring and compare their relative priority.

### Part 5 — Analyze Failure Modes with FMEA

Identify potential system failures, examine their consequences, and evaluate their relative risk.

### Part 6 — Recommend Security Controls

Propose safeguards and defensive measures that address the threats and failures identified during the analysis.

### Part 7 — Consider Residual Risk

Evaluate the risks that may remain after security controls have been implemented.

### Part 8 — Final Reflection

Summarize what the threat-modeling exercise revealed about the security of the AI-based malware detection system.

Complete the lab in your own notebook copy. Use the review sections to check your reasoning where the notebook provides them.

---

## Saving and Submitting Your Work

After completing the readings, activities, checkpoints, and final lab:

1. Confirm that your responses are entered and the required code cells have been run.
2. Save your work in Google Colab.
3. Select **File → Download → Download .ipynb**.
4. Submit the downloaded `.ipynb` notebook through the submission method specified by your instructor or cyber range.

Keep a copy in Google Drive for your own records.

**Do not submit the unmodified notebook from the course repository.**

---

## Requirements

To complete this module, students will need:

- Access to the course GitHub repository.
- A web browser in the cyber range environment.
- Access to Google Colab and a Google account for saving their own copy.
- Basic familiarity with running notebook cells.

Prior experience with threat modeling is not required.

The notebook includes guided Python demonstrations and scoring activities. Follow any additional setup instructions displayed within the notebook itself.

---

## Responsible Use

All threat-modeling scenarios and exercises are intended for authorized educational use.

Analyze only the fictional or explicitly permitted systems and data supplied for the course.

The purpose is to understand risk and select appropriate security controls, not to attack real systems.

---

## References

A collapsible **Module References** section is included at the end of the notebook.

Consult it for the sources supporting the module's threat-modeling concepts and AI security discussions.

---

**Next Step:** After completing Module 2, continue to the next module in the Securing AI certification course.
