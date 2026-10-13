# Module 1: Foundations of AI Security

## Securing AI Certification Program

Welcome to **Module 1: Foundations of AI Security**!

This module introduces the fundamental concepts of artificial intelligence security, explores real-world AI security failures, and demonstrates how attackers can target AI and machine learning systems.

Students will learn about common AI security threats, examine practical examples, complete interactive exercises, and analyze a real-world AI security incident.

All instructional content and hands-on activities are provided through **Google Colab**.

Students will access the certification through their assigned campus cyber range environment and use GitHub to retrieve the official module notebook.

---

## 1. Module Overview

Artificial intelligence and machine learning systems are increasingly integrated into cybersecurity applications and everyday technologies. As these systems become more widely adopted, understanding their vulnerabilities and security risks becomes essential.

This module introduces AI security by examining how AI systems operate, how attackers exploit weaknesses, and how organizations can evaluate and reduce AI-related security risks.

### Module Topics

| Section | Topic |
|---|---|
| 1 | Foundations of AI Security |
| 2 | Real-World AI Security Failures |
| 3 | Adversarial / Evasion Attacks |
| 4 | Data Poisoning Attacks |
| 5 | Model Privacy and Leakage |
| 6 | Prompt Injection |
| 7 | AI Supply Chain Risk |
| 8 | AI Security Frameworks |
| 9 | End-of-Module Lab: Analyze a Real-World AI Security Failure |

### Learning Objectives

By the end of this module, students should be able to:

- Explain the purpose and importance of securing AI systems.
- Differentiate between using AI for cybersecurity and securing AI itself.
- Identify common attacks against AI and machine learning systems.
- Describe how adversarial examples manipulate model predictions.
- Explain how data poisoning compromises model training.
- Recognize privacy risks associated with AI models.
- Identify direct and indirect prompt injection attacks.
- Understand security risks involving AI datasets and pretrained models.
- Recognize the role of AI security frameworks in managing risk.
- Analyze a real-world AI security incident and recommend appropriate mitigations.

---

## 2. Prerequisites

Before beginning Module 1, students should have:

- Access to the campus cyber range.
- A web browser capable of accessing GitHub and Google Colab.
- A Google account for saving completed notebooks.
- Basic familiarity with navigating websites and running Python code cells.
- An internet connection.

**Prior experience with machine learning is not required.** This module introduces foundational AI security concepts for new learners.

### Required Platforms

| Platform | Purpose |
|---|---|
| Campus Cyber Range | Student learning environment |
| GitHub | Access official certification materials |
| Google Colab | Read module content and complete interactive exercises |
| Google Drive | Save individual student notebooks |

**Important:** Google Colab normally executes Python code on Google's hosted infrastructure, even when accessed through a browser inside the cyber range. Students should use the runtime configuration approved by their instructor.

---

# 3. Student Setup Instructions

Follow the instructions below before beginning the module.

## Step 1 — Access the Campus Cyber Range

1. Navigate to the campus cyber range login page provided by your instructor.
2. Sign in using your assigned credentials.
3. Launch your assigned virtual machine or learning environment.
4. Open the web browser inside the cyber range.

Verify that you can access external websites before continuing.

## Step 2 — Open the GitHub Repository

1. Open a new browser tab.
2. Navigate to the GitHub repository provided by your instructor.

   **Repository URL:**

   `https://github.com/nmccloud42/Securing-AI`

3. Locate the folder containing Module 1.
4. Open the Module 1 folder.
5. Find the notebook:

   `Module1_FoundationsOfAISecurity.ipynb`

This file contains the instructional readings, demonstrations, knowledge checks, and end-of-module laboratory.

**You do not need to download or clone the entire GitHub repository.**

## Step 3 — Open Module 1 in Google Colab

There are two ways to open the notebook.

### Method A — Open from GitHub

If your instructor provides an **Open in Colab** link:

1. Click the link.
2. Wait for Google Colab to load.
3. Sign in to your Google account if prompted.
4. Verify that Module 1 has opened successfully.

### Method B — Open Through Google Colab

If an Open in Colab link is not available:

1. Navigate to https://colab.research.google.com.
2. Select **File → Open notebook**.
3. Select the **GitHub** tab.
4. Enter the repository URL provided by your instructor.
5. Locate `Module1_FoundationsOfAISecurity.ipynb`.
6. Select the notebook to open it.

You should now see the Module 1 notebook inside Google Colab.

## Step 4 — Save Your Personal Copy

**Do not complete activities directly in the original GitHub notebook.**

Each student must create a personal copy.

1. In Google Colab, select **File → Save a copy in Drive**.
2. Wait for the new notebook to open.
3. Rename your notebook using the following format:

   `Module1_YourName.ipynb`

4. Confirm that the notebook is saved in Google Drive.

### Recommended Google Drive Organization

Create a folder named:

`Securing_AI_Certification`

Store all completed certification notebooks inside this folder.

This ensures your progress is saved separately from the instructor's original materials.

## Step 5 — Connect to the Google Colab Runtime

Before executing code:

1. Locate the **Connect** button in the upper-right corner of Google Colab.
2. Click **Connect**.
3. Wait for the runtime to initialize.
4. Confirm that the notebook is connected.

Use the default CPU runtime unless the activity specifies otherwise.

Some cells may install Python packages or download example datasets. Run the required setup cells before attempting later exercises.

---

# 4. How to Complete Module 1

Module 1 combines instructional readings with interactive learning activities.

Students should complete the sections in the order presented.

## Reading Sections

Many instructional sections use collapsible headings.

To access the content:

1. Locate the section heading.
2. Click **Click to Expand**.
3. Read the material inside the section.
4. Expand individual subsections as needed.
5. Continue to the next section after reviewing the content.

Some sections contain nested subsections that must be expanded separately.

## Code Demonstrations

Throughout the module, Python code cells demonstrate AI security concepts.

To execute a code cell:

1. Locate the code cell.
2. Click the Play button on the left side.
3. Wait for execution to finish.
4. Review the generated results, graphs, or explanations.

Some code cells may have hidden source code. These cells are designed to demonstrate a concept without requiring students to modify the underlying implementation.

## Hands-On Activities

Hands-on activities allow students to experiment with AI security techniques.

When completing an activity:

1. Expand the **Hands-On Learning Context** section.
2. Read the explanation and activity instructions.
3. Identify any student-editable variables.
4. Modify the requested parameters.
5. Execute the code cell.
6. Examine the resulting output.
7. Answer any associated questions.

Students should focus on understanding why the results occurred rather than simply executing the code.

## Knowledge Checks

Knowledge checks are included to reinforce important concepts.

When completing a knowledge check:

1. Read each question carefully.
2. Select or enter your answer.
3. Run the provided grading cell if applicable.
4. Review the feedback.
5. Revisit the instructional material if additional clarification is needed.

---

# 5. Module Content

## Section 1 — Foundations of AI Security

Introduces the meaning of AI security and explains the difference between using AI to improve cybersecurity and protecting AI systems from attacks.

Students should understand why AI systems require security considerations throughout their lifecycle.

## Section 2 — Real-World AI Security Failures

Examines real-world AI failures, including the Microsoft Tay incident.

Students will explore how weaknesses in AI system design, deployment, and oversight can lead to undesirable or harmful behavior.

## Section 3 — Adversarial / Evasion Attacks

Introduces adversarial examples and explains how attackers manipulate inputs to influence model predictions.

Students will examine how relatively small input changes can affect machine learning behavior.

Complete the associated hands-on activity and review the results.

## Section 4 — Data Poisoning Attacks

Explores attacks against machine learning training data.

Students will learn how techniques such as label flipping can influence model behavior and reduce prediction reliability.

Complete the associated hands-on activity.

## Section 5 — Model Privacy and Leakage

Introduces privacy-related attacks against machine learning models.

Topics include:

- Membership inference
- Model inversion
- Sensitive information leakage

Students will examine how model behavior can reveal information about training data.

Complete the associated hands-on activity.

## Section 6 — Prompt Injection

Introduces prompt injection attacks against AI systems.

Students will examine the differences between direct and indirect prompt injection and understand how malicious instructions can influence AI behavior.

Complete the associated hands-on activity.

## Section 7 — AI Supply Chain Risk

Examines security risks involving external AI components.

Topics include:

- Dataset security
- Pretrained model security
- Third-party AI dependencies

Students will learn why the security of an AI system depends on the integrity of the resources used to develop and deploy it.

Complete the associated hands-on activity.

## Section 8 — AI Security Frameworks

Introduces frameworks used to understand and manage AI security risks.

The section includes the NIST AI Risk Management Framework and its role in identifying, evaluating, and managing AI-related risks.

Students should understand how security frameworks help organizations develop more structured approaches to AI security.

## Section 9 — End-of-Module Lab: Analyze a Real-World AI Security Failure

The final section applies concepts introduced throughout Module 1.

Students will investigate a real-world AI security incident and analyze the vulnerabilities, consequences, and possible mitigations.

Follow all instructions within the notebook's end-of-module lab.

---

# 6. End-of-Module Laboratory

## Analyze a Real-World AI Security Failure

### Lab Objective

The purpose of this laboratory is to demonstrate your ability to apply foundational AI security concepts to a real-world incident.

Students will investigate an AI security failure and explain how the incident relates to concepts introduced throughout the module.

### Lab Instructions

1. Navigate to **Section 9 — End-of-Module Lab**.
2. Expand the laboratory instructions.
3. Read the lab overview.
4. Complete each of the seven lab parts in the notebook.
5. Provide explanations and observations where requested.
6. Review your responses for completeness.
7. Save your completed notebook.

Your analysis should demonstrate an understanding of the security weaknesses involved, their consequences, and potential defensive measures.

Use credible sources when researching your selected incident and provide references where required.

**Note:** Follow the notebook's specific lab instructions if they differ from this general overview.

---

# 7. Saving Your Progress

Google Colab automatically saves changes to notebooks stored in Google Drive under normal circumstances.

However, students should regularly verify that their changes have been saved.

### Before Ending a Session

1. Confirm that the notebook is saved in Google Drive.
2. Check that your answers and code modifications are present.
3. Allow important code cells to finish executing.
4. Close the notebook when finished.

### Returning to Your Work

To continue your module later:

1. Log back into the campus cyber range.
2. Open your browser.
3. Navigate to https://drive.google.com.
4. Locate your `Securing_AI_Certification` folder.
5. Open your saved Module 1 notebook.
6. Reconnect to the runtime if necessary.
7. Continue where you left off.

**Important:** Always reopen your personal Google Drive copy rather than the original notebook on GitHub.

Google Colab runtimes may disconnect after inactivity. If your runtime resets, you may need to rerun earlier setup cells to restore variables, models, or temporary datasets.

---

# 8. Submitting Your Completed Module

Once you have completed the required readings, knowledge checks, hands-on activities, and end-of-module laboratory, prepare your notebook for submission.

### Step 1 — Review Your Work

Verify that all required activities are complete.

### Step 2 — Download Your Notebook

In Google Colab:

1. Select **File → Download → Download .ipynb**.
2. Save the downloaded notebook to your computer or cyber range environment.
3. Rename the file:

   `Module1_YourName_Completed.ipynb`

### Step 3 — Submit Your Work

Submit your completed notebook using the method specified by your instructor.

**Submission Location:** To be provided by instructor.

Do not upload your completed work to the instructor's master GitHub repository unless specifically instructed.

---

# 9. Module Completion Checklist

Before moving to Module 2, verify that you have completed the following:

- [ ] Accessed the certification repository through the cyber range.
- [ ] Opened Module 1 in Google Colab.
- [ ] Saved a personal copy to Google Drive.
- [ ] Completed Section 1 — Foundations of AI Security.
- [ ] Completed Section 2 — Real-World AI Security Failures.
- [ ] Completed Section 3 — Adversarial / Evasion Attacks.
- [ ] Completed Section 4 — Data Poisoning Attacks.
- [ ] Completed Section 5 — Model Privacy and Leakage.
- [ ] Completed Section 6 — Prompt Injection.
- [ ] Completed Section 7 — AI Supply Chain Risk.
- [ ] Completed Section 8 — AI Security Frameworks.
- [ ] Completed all required knowledge checks.
- [ ] Completed all required hands-on activities.
- [ ] Completed Section 9 — End-of-Module Laboratory.
- [ ] Saved the completed notebook.
- [ ] Downloaded and submitted the notebook as instructed.

---

# 10. Troubleshooting

### Google Colab Will Not Open

Verify that your browser has internet access and that Google Colab is accessible from the cyber range.

If access is blocked, contact your instructor or cyber range administrator.

### GitHub Repository Cannot Be Accessed

Verify that you are using the correct repository URL.

If the repository is private, you must have the appropriate permissions.

### Code Cells Are Not Running

Confirm that your Google Colab runtime is connected.

Run any required setup cells before executing later activities.

### A Python Package Is Missing

Run the installation or setup instructions provided in the notebook.

If the problem continues, report the error to your instructor.

### A Dataset Cannot Be Downloaded

Check your internet connection and verify that the dataset resource is available.

Some cyber range environments may restrict external downloads.

### Previous Results or Variables Are Missing

Your Colab runtime may have restarted.

Reconnect and rerun the necessary setup cells.

### My Completed Work Is Missing

Open Google Drive and locate your personal notebook copy.

Do not reopen the original GitHub notebook when attempting to resume previously completed work.

---

# 11. Important Student Guidelines

- Complete the module using your own Google Colab notebook copy.
- Follow the instructional sections in order.
- Read activity instructions before modifying code.
- Do not modify instructor-provided code unless instructed.
- Run experiments only within the authorized learning environment.
- Do not upload sensitive campus data, credentials, or private information to Google Colab.
- Save your work regularly.
- Complete the required knowledge checks and laboratory activities.
- Submit your completed notebook according to instructor instructions.

---

# 12. Module References

The notebook includes a **Module References** section containing supporting academic literature, security frameworks, and additional learning resources.

Students are encouraged to review these references when completing the end-of-module laboratory or researching AI security concepts.

---

## Next Steps

After successfully completing Module 1, students should proceed to **Module 2: Threat Modeling AI Systems**.

Module 2 builds on the foundational concepts introduced here by examining how to identify, categorize, and evaluate threats throughout the AI system lifecycle.

---

**Securing AI Certification Program**

*Module 1 — Foundations of AI Security*
