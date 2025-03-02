---
created: 2025-02-13
source: https://app.dataannotation.tech/workers/tasks/cc4586de-9212-4a4d-9e61-6711d469ccc0?task_response_id=c906428f-f310-4f2e-9d0e-c5f452859f0a
banner: 
tags:
  - clippings
---

![Banner]()

***
1.  [Projects](https://app.dataannotation.tech/workers/projects)
2.  \[Qualification\] Maxis: Create Agentic Task and Actions (single-turn) \[Successful submissions grant access to regular $30+/hr work\]

Last draft saved at 1:37 AM

## Introduction

Welcome to the Maxis Project Qualification! In this introductory qualification, you’ll learn the basics of the SIMS-based workflow and how to create and evaluate Scenarios. Each Scenario is composed of:

1.  A **task** (what the user wants the AI to do)
    
2.  A **solution** (the actions the AI must perform to accomplish the task)
    

These Scenarios assess the AI’s ability to replicate an exact chain of actions in various apps—such as emailing, scheduling, messaging, or booking a cab ride—while following specific project requirements and avoiding certain pitfalls. This qualification will guide you through the main concepts and help you practice spotting potential issues, so you can confidently build and evaluate your own Scenarios.

The most up-to-date version of the Maxis Instructions can be found here ([Google Docs](https://docs.google.com/document/d/e/2PACX-1vTEUg4NUrK4DkJEmhT2NYyHDK8SbTzaaPs0ltzp0ujrQLM7wU2558k0l_X8_9X-X0VHJYUZM3yvnQae/pub)).

Be sure to **pay particular attention to the "Do's and Don'ts"** section of the document.

Below is a concise guide to help you navigate the qualification process. During this qualification, you’ll be asked to load a sample Scenario file into the SIMs UI and then evaluate whether it meets the project guidelines.

1.  **Access the SIMS UI**
    
    -   Go to: [SIMS UI Login](https://annotation-server-beta-37040395420.us-central1.run.app/sims/)
        
    -   Log in with:
        
        -   **Username**: `admin`
            
        -   **Password**: `paperclips`
            
2.  **Load the Provided Scenario File**
    
    -   Once in the SIMS UI, click “Load Scenario” and select the JSON file provided for this qualification. This file represents a sample Scenario (task + solution).
        
    -   Inspect the scenario universe data (emails, contacts, events, etc.) to understand the context.
        
3.  **Review the Scenario**
    
    -   **Task**: Check how the user’s request is phrased—does it meet requirements (e.g., it’s a single-turn request, it references existing data properly)?
        
        -   Are the actions correct and strictly necessary?
            
        -   Are they arranged to maximize parallelization where possible?
            
        -   Is the scenario free of ambiguous references or unsupported actions?
            
4.  **Evaluate for Common Issues**  
    Refer to the **Maxis Instructions** provided above. Pay particular attention to:
    
    -   **Task clarity**: Is there any ambiguity in the user request (e.g., “next Monday” vs. “Monday 11th”)?
        
    -   **Parallelization**: Are independent actions run in parallel?
        
    -   **App-Specific Requirements**:
        
        -   For email, is the recipient of the email correct according to the task?
            
        -   For calendar events, is the start and end time unambiguously defined?
            
        -   Are names copied exactly from the ContactsApp data (no typos)?
            
        -   Do the IDs of deleted emails, messages, and calendar events match the ID of the object that **should** be deleted?
            
    -   **Narrative Coherence**: Does the scenario follow a single, logical thread (i.e., all aspects of the task are related to each other)?
        
5.  **Finalize and Submit**
    
    -   You will answer a brief series of questions about the scenario’s task and actions, pointing out any major or minor issues found.
        
    -   Fill out your answers and submit **three** tasks to complete the qualification.
        

### Load this [file](https://projects-uploaded-files.s3.us-east-2.amazonaws.com/production/item_response_files/1f3f9db7-f988-4cbb-b08e-70b5c9fc79ca_a095f27f-fee5-44a8-9ef6-eee58012c60f_b45db811-6d79-4d7a-90ab-29687aa08ba8.json) into the [SIMS UI](https://annotation-server-beta-37040395420.us-central1.run.app/sims/)

-   Download the file by right-clicking and then selecting "Save As"
    

### Use the evaluation guide to answer the following questions about the scenario:

### Did the original scenario have any of these Major issues? If so, tick all that apply.

*Likely requires a significant rewrite or extensive edits to the prompt or action sequence.*

Fundamental date/timeline contradictions

Identity/role inconsistencies

Incorrect reading of the data

Prompt admits more than 1 acceptable solution

Agent not following instructions

No - There were no Major issues in this task

### Did the original scenario have any of these Minor issues? If so, tick all that apply.

*Usually local or small-scale problems that can be fixed quickly with minimal rewriting.*

Missing actions

Unneeded actions

Parallelization/dependency mapping issues

Prompt wording is ambiguous (could have multiple meanings)

Incorrect or unfounded arguments in actions

Missing details in write action arguments

Unprofessional or unnatural agent tone

No - There were no Minor issues in this task

### Optional Comment
