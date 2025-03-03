---
created: 2025-02-12
source: https://app.dataannotation.tech/workers/tasks/44b61432-036d-43e6-8a5e-3f362bb0074a?task_response_id=792910c7-0a22-4ae4-a79e-4615c23e3ec4
banner: 
tags:
  - clippings
---

![Banner]()

***
[DataAnnotation](https://app.dataannotation.tech/) Toggle navigation

       

-   [Work on projects](https://app.dataannotation.tech/workers/projects)
-   [Transfer Funds](https://app.dataannotation.tech/workers/payments)
-   [Inbox](https://app.dataannotation.tech/workers/inbox)                

-   [Jonathan Wagner](https://app.dataannotation.tech/workers/tasks/44b61432-036d-43e6-8a5e-3f362bb0074a?task_response_id=792910c7-0a22-4ae4-a79e-4615c23e3ec4#)
    [Profile](https://app.dataannotation.tech/me) [Support](https://app.dataannotation.tech/workers/support) [Code of Conduct](https://docs.google.com/document/d/e/2PACX-1vQRSbcK0ctnOVqPC58qNzxW3vssF4-oPNueAh4TStPTpj5rxNDYHbsZyEJOroP-0V7nB1PDQff4Sqzi/pub) [FAQ](https://docs.google.com/document/u/1/d/e/2PACX-1vQenBfiMZrBL-_wilNXu0paSnRVKYsNk_dGgOvztj8ZKZ0ciWnfBNE_gq3WuFR_jaWgoBNPA72L3A-q/pub) [Log out](https://app.dataannotation.tech/users/sign_out)

1.  [Projects](https://app.dataannotation.tech/workers/projects)
2.  Raven - Images, Non-STEM - Create Fine-Grained Criteria and Rate Responses from Two Models (02/12/25)

Last draft saved at 6:24 PM

Clear Response

### **Make sure to read the project instructions / attached documents thoroughly before starting.**

### **You can log the time spent reading the instructions.**

### **WARNING: There may be adversarial or harmful tasks (prompt and images).**

### **A new flag has been added so you can skip them and remove them from the queue!**

-   **We want to avoid keeping adversarial or harmful tasks, so filtering them out is exactly what we need. Thanks!**
    

## **Important Updates (Last Update: 12/19 11:00 PT)**

**Here’s an FAQ we put together (and we’ll keep updating as new questions come up) to help address some of your doubts. As always, if anything isn’t clear, feel free to reach out to us in chat!**

## [**\-> FAQ Document <-**](https://docs.google.com/document/d/e/2PACX-1vQ4GTj3elY3001yLO-9JDXY6M-_FrOts_yZHO8gKoY15sG9gCtma3bZxPZEZGwxjhrXtczscaH1pUJS/pub)

### **Minor Update (12/19 11:00 PT)**

Hey everyone!

Thanks for the great work - keep it up! We just wanted to clarify something:

-   Criteria that come from previous turns and apply to the current one should be considered **explicit**.
    
-   Also, please remember to follow the criteria distribution (70% explicit, 30% implicit) when possible.
    
-   Lastly, be sure to incorporate the feedback from 11/12 when creating your criteria!
    
-   **Reminders:**
    
    -   If making a criterion fully self-contained takes over 20 minutes, aim for a reasonable level of self-containment instead.
        
    -   Adding examples or similar elements can help make a criterion more self-contained without overloading it.
        

### **Major Update (11/26 22:00 PT):**

Hey everyone!

We’ve added some new info to the "Original Worker’s Ratings and Explanation" section so you can better understand what the original worker thought about the model responses.

Here are the axes the original worker could have used to flag the response, along with a brief explanation to clarify what they mean:

### **Response Axes - Explanation**

The original worker who created the prompt and generated the responses had the option to flag each response with issues they believed were present.

This is primarily to help guide you in creating the criteria, as it provides context about the issues and gives you an idea of which criteria might be more relevant.

**Writing Quality**

-   Focuses on the clarity and correctness of the language used. Issues include grammar mistakes, spelling errors, unclear phrasing, or awkward sentence construction.
    
-   A high-quality response should be fluent, free of errors, and easy to understand, regardless of its visual presentation.
    

**Format**

-   Focuses on the structure and visual presentation of the response.
    
-   Issues include improper organization, inconsistent use of formatting elements (e.g., headings, bullet points, paragraphs), or failure to adhere to the prompt’s specific layout requirements.
    
-   A well-formatted response should make the content easy to read and visually aligned with the prompt’s expectations.
    

**Verbosity**

-   Evaluates whether the response is concise and to the point. Issues occur when a response is overly wordy, redundant, or excessively brief, leaving out important details.
    

**Instruction Following**

-   Checks how well the response adheres to the prompt’s instructions. Issues include partial completion, misinterpretation of the prompt, or ignoring explicit requirements.
    

**Correctness**

-   Focuses on factual accuracy and logical consistency. Issues arise from incorrect information, flawed reasoning, or technical errors in the response.
    

**Turn Memory**

-   Measures the ability to retain and build on prior context in a multi-turn interaction. Issues include forgetting key details, contradicting earlier turns, or misinterpreting prior context.
    

You should also see tasks without any issues. There aren’t many, but we’re still looking to create criteria for them, even if they’re all correct!

**Great job last week! We hit the implicit criteria percentage (and even surpassed it!), so keep up the good work!**

Here’s the target criteria distribution for your tasks, but remember, if it feels forced in a specific case, there’s no need to strictly follow it:

-   **Objective:** No specific requirement
    
-   **Subjective:** No specific requirement
    
-   **Implicit:** 30%
    
-   **Explicit:** 70%
    

**IMPORTANT! Finally, we wanted to address one of the FAQs: "How self-contained is self-contained enough?"**

-   In general, we expect you to make criteria as self-contained as possible, but we understand it can be challenging at times.
    
-   To address this, **if making a criterion fully self-contained would take more than 20 minutes, it’s fine to aim for a reasonable level of self-containment instead.**
    
    -   Adding examples or similar elements can help make a criterion more self-contained without overloading it.
        
-   We don’t expect you to paste 20+ lines of text into a single criterion - that would definitely be excessive.
    
    -   Around 5-10 lines is usually fine, but it could probably be condensed even further in most cases.
        

Thanks for keeping this in mind as you work, and don’t forget to read the feedback below!

### **Feedback: Make sure to read everything thoroughly to avoid these issues** **(11/17 20:30 PT)**

Hey everyone!

We've been seeing some issues in the criteria creation, and we want to address them by giving you more examples and extra instructions which might help.

1.  **Phrase Criteria Using "Should"**
    
    -   Each criterion should clearly state how a *good response* should behave.
        
    -   Use “should” to maintain consistency and clarity
        
    -   **Example:** "The response should include a clear introduction to the topic."
        
2.  **Make Criteria Self-Contained**
    
    -   Criteria must be understandable on their own, without needing to reference the original prompt or rely on external knowledge.
        
    -   This ensures any person can judge the response based solely on the criteria.
        
        ### Self-Contained Criteria Examples
        
3.  **Create Explicit, Objective Criteria**
    
    -   Explicit criteria specify exactly what the response needs to contain or address, with objective points that can be checked directly.
        
    -   These are particularly helpful for prompts where factual accuracy and completeness are crucial.
        
    -   **Example:**
        
        -   **Prompt:** “I want a funny short story about a man named Bob who has a pet unicorn. I want to read this to my 5 year old son out loud before bedtime, so it should be under 500 words.”
            
        -   **Answer Key Criteria:**
            
            -   The response should contain a short story.
                
            -   The short story should contain a male character.
                
            -   In the story, the male character should be named Bob.
                
            -   In the story, Bob should have a pet unicorn.
                
            -   The story should be under 500 words.
                
            -   The story should be funny.
                

4.  **IMPORTANT! Implicit or Subjective Criteria with General Principles and Examples**
    
    -   Some criteria aren’t directly specified in the prompt but are likely expected by 80%+ users, and would make some responses better than others.
        
    -   For these, provide a general principle and follow it with an example.
        
        ### **IMPORTANT!** Implicit or Subjective Criteria Examples
        
        **Example 1:**
        
        -   **Prompt:** “Write me a list of the heaviest animals in the world”
            
        
        -   **Criteria:**
            
            -   The list should be ordered in a clear way. **For example, it should be ordered by the heaviest animals to the least heavy.**
                
                -   Note that this was **NOT** an explicit requirement.
                    
                -   However, if you had an ordered list vs. an unordered list, you would probably prefer the ordered list.
                    
            -   The list should contain the average weights for the animals.
                
                -   This was **NOT** an explicit requirement either.
                    
                -   80%+ of people would probably expect a list to contain the weights too, and not just the names.
                    
            -   The list should not be too short or too long. **For example, it should contain at least 3 animals and under 20 animals.**
                
                -   Note that this is fairly subjective.
                    
                -   We probably don’t want a list of over 20 animals – that would be too long to read.
                    
                -   And we probably don’t want a list of under 3 animals – that wouldn’t be informative enough.
                    
                -   Because there isn’t an exact criteria, we describe a general principle (“The list should not be too short or too long”) that the list should satisfy, and then give some examples (“For example, it should contain at least 3 animals and under 20 animals”).
                    
                -   This idea of describing a **general principle**, followed by an **example**, is one you can use liberally!
                    
        
        **Example 2:**
        
        -   **Prompt:** “Write an essay about quantum mechanics for a 10 year old.”
            
        
        -   **Criteria:**
            
            -   The response should look like an essay. **For example, it should not contain bullet points.**
                
                -   We included this criteria because often, when you ask models to create essays, they create bullet points.
                    
            -   The essay should be understandable to a 10 year old. **For example, it should not use complex vocabulary without explaining them.**
                
            -   The essay should explain key concepts in quantum mechanics. **For example, it should explain the Uncertainty Principle and the duality of particles and waves.**
                
            -   The essay should capture a 10 year old’s attention. **For example, it could use metaphors to connect concepts in quantum mechanics to concepts a 10-year old would understand.**
                
            -   The essay should not be too long. **For example, it should be under 5 paragraphs.**
                
        
        **Example 3:**
        
        -   **Prompt:** “Write a story about cheese.”
            
        
        -   **Criteria:**
            
            -   The story should be about cheese.
                
            -   The story should be interesting. **For example, it should have a climax, interesting characters, and a clear plot.**
                
        
5.  **Differentiate Between Good and Ideal Responses**
    
    -   Criteria should distinguish between a merely acceptable response and an outstanding one
        
    -   For instance, identify extra elements that would turn a good response into an excellent one.
        
    -   **Example:**
        
        -   For a bedtime story:
            
            -   The story should be engaging for children, with interesting characters and a simple, clear plot.
                
            -   An ideal response might include a gentle moral or lesson.
                

6.  **Avoid Overfitting to Specific Responses**
    
    -   Each criterion should be specific enough to identify high-quality responses yet general enough to apply to a variety of acceptable answers.
        
    -   Aim to create criteria that will not only assess current responses but also distinguish ideal future ones
        

### **Checklist to Make Sure your Criteria Are Good**

1.  Does each criterion use “should” or "should not"?
    
2.  Are criteria self-contained and understandable on their own?
    
3.  Are criteria detailed enough to judge good vs. bad responses, and even distinguish ideal from good?
    
4.  Do the criteria include examples where subjective or implicit preferences are involved?
    

### **More Examples of Good Criteria**

### **Major Update (11/04 16:30 PT)**

## **Project Overview (Updated 11/17 20:30 PT)**

This project aims to evaluate model responses using fine-grained criteria analysis instead of traditional rating systems (N-axis, etc.)

The goal is to break prompts into specific, measurable criteria -- whether **implicit, explicit, subjective, or objective** -- that reflect what you would expect from an ideal response to the prompt.

-   These criteria serve as the benchmark for assessing how effectively the model fulfills the requirements.
    

In this version, you’ll also find images uploaded by the original worker at the start of the conversation, alongside the initial prompt. **The model had access to these images throughout the entire conversation.**

### **IMPORTANT (11/17 20:30 PT): Ensuring Self-Containedness in Visual Recognition**

You should not assume the verifier is perfect in visual recognition. To test whether a rubric is well-constructed and self-contained, consider this approach: "Can a text model, without relying on external context or visual inputs, accurately assess correctness by only referencing the text prompt, response, and the rubric?"

**Example:**

-   **Prompt**: \[image of a pair of Nike shoes\] “What’s this?”
    
-   **Response**: “This is a pair of Nike shoes, specifically Nike Men’s Flex Control 4 Training Shoes.”
    

**Criteria Evaluation:**

-   ✔️ **Good Rubric**: The response should mention that the shoes are *Nike Men’s Flex Control 4 Training Shoes*.
    
    -   *Reason*: This criterion is clear and matches the expected information explicitly present in the response.
        
-   ❌ **Bad Rubric**: The response should mention the exact specific version of the Nike shoe.
    
    -   *Reason*: This assumes external visual verification or knowledge, making it dependent on information not directly derived from the text prompt and response alone.
        

**We ask you to be thorough with your ratings, explanations and criteria creation.**

### **Section 0: Instructions, examples, and Step-by-Step**

This section includes five items that can be referenced throughout the task **(except for the last one)**:

1.  **Images:**
    
    -   These are provided primarily for reference. Use them to evaluate your criteria and ensure they are self-contained.
        
    -   The original worker uploaded them at the start of the conversation, so all turns had access to them.
        
2.  **User Prompt**
    
    -   This is what you should be creating fine-grained criteria for.
        
    -   If you think the instructions are unclear, contrived, or there are any other issues you can flag it at the start of the task, but don’t let that affect your ratings.
        
3.  **Conversation History**
    
    -   This contains all the original turns from the task, including the worker’s prompts and their selected responses.
        
    -   You should mainly use this for context - like when the current prompt references something from an earlier turn.
        
        -   **For example, if there are criteria from previous turns that still should apply to the current one, you can use them!**
            
    -   Don’t factor this into your ratings either.
        
4.  **Two Model Responses**
    
    -   These are the models' original responses, which you’ll evaluate using the fine-grained criteria.
        
    -   At the end of the task, you’ll need to choose one. Be sure to take all your ratings into account!
        
5.  **NEW! Original Worker's Ratings and Explanation**
    
    -   **IMPORTANT: Do not mention these in your explanation or criteria.**
        
    -   These are just for reference, so you can understand what the original worker was thinking and what they expected from the prompt.
        
    -   Ideally, your overall ratings and preferences should align with what the original worker chose.
        

### **Section 1: Instructions, examples, and Step-by-Step**

You need to select the number of criteria you will be creating. Once you’ve done that, new questions will appear where you can write the criteria and select their types.

-   Criteria **SHOULD NOT** be ambiguous.
    
    -   **Avoid** criterion that just says the response should be good on a certain aspect **without saying what that means concretely.**
        
    -   **Example:**
        
        -   **Correct:** 'The summary should mantain the original structure and order of chapters and sections'
            
        -   **Incorrect:** 'The summary should have a good structure and be properly formatted'
            
-   Criteria **SHOULD** be **SELF-CONTAINED**
    
    -   If the prompt requests for something to be added or similar, then it should appear in the criterion.
        
    -   If the prompt is expecting a piece of information, then it should be added to the criterion.
        
    -   If the prompt wants something extracted or summarized from a text, then that should be added to the criterion, even if it ends up being quite long.
        
    -   You should do this in any similar situations, as long as you think it's reasonable.
        
    -   **Example:**
        
        -   **Correct:** 'The essay should correctly list Obama's birth date: August 4, 1961'
            
        -   **Incorrect:** 'The essay should correctly list Obama’s birth date'
            
        -   **Correct:** 'All the following adjectives should be extracted from the essay into a bulleted list: happy, sad, funny, great'
            
        -   **Incorrect:** 'All of the adjectives should be extracted from the essay into a bulleted list'
            
-   Criteria **SHOULD** be **OBJECTIVE** or **SUBJECTIVE.**
    
-   Criteria **SHOULD** be **IMPLICIT** or **EXPLICIT.**
    
-   **NEW!** For **SUBJECTIVE** and/or **IMPLICIT** criteria, provide a general principle and follow it with an example.
    
    -   **Example:** "Write a story about cheese."
        
    -   **Good** Criteria: "The story should be interesting. **For example, it should have a climax, interesting characters, and a clear plot."**
        
    -   For more examples, check the latest feedback update.
        
-   You **SHOULD** **omit any criteria** you'd think the **model would get correct 95% of the time.**
    
    -   **NEW! We’re being more flexible with this. If you're unsure, just add it anyway!**
        
    -   We still want you to focus on the harder criteria.
        
    -   This doesn’t mean you shouldn’t include criteria marked as "No Issues", just try to avoid those that the model will consistently get right.
        

Here's another example, using a simple prompt:

**Prompt:**

> Write me 400 words about the Civil War in an essay format. Be sure to mention the most common cause of death.

**Generated Response:**

> The American Civil War, fought from 1861 to 1865, remains one of the most pivotal and bloody conflicts in the history of the United States. It was primarily a clash between the Northern and Southern states, pivoting around the issues of slavery, states' rights, and the economic and social divergence between the industrial North and the agrarian South.
> 
> At its core, the Civil War was ignited by the long-standing controversy over the enslavement of Black people. The election of Abraham Lincoln in 1860, who was known for his anti-slavery stance, was the catalyst for Southern states to secede from the Union, fearing that their way of life, built on slavery, was under threat. This led to the formation of the Confederate States of America, comprising eleven Southern states, setting the stage for conflict.
> 
> The war itself was characterized by massive battles like Gettysburg, Antietam, and Shiloh, which resulted in staggering casualties due to advancements in weaponry, such as the rifled musket, combined with outdated military tactics like massed infantry assaults.
> 
> The battlefield took its toll through direct combat. The introduction of more accurate and deadly firearms meant that soldiers faced greater risks in open combat than in previous wars. Furthermore, the Civil War saw some of the first uses of trench warfare, particularly during the Siege of Petersburg, which foreshadowed the static, brutal warfare of World War I. Firearms were one of the main causes of death.
> 
> The war concluded with the surrender of the Confederate forces at Appomattox Court House on April 9, 1865, leading to the abolition of slavery with the Thirteenth Amendment. The aftermath saw a period of Reconstruction, aimed at reintegrating the Southern states and establishing rights for the newly freed slaves, though this process was fraught with challenges and resistance.
> 
> The Civil War reshaped the nation, affirming the indivisible nature of the Union, but at a tremendous human cost, with an estimated 620,000 to 750,000 soldiers dead, along with an undetermined number of civilian casualties. It left a legacy of both division and unity, shaping American identity, politics, and social structure for generations to come.

Your main objective in this section is to create criteria that test instructions the model consistently fails to get correct.

**Possible Criteria + Answers:**

-   The response <u>should</u> be 400 words. <-- **OBJECTIVE** criteria
    
    -   **Major issues.** This response is 341 words, fewer than 400 words.
        
-   The response should mention the most common cause of death, <u>disease</u>. <-- **OBJECTIVE, SELF-CONTAINED** criteria
    
    -   **Minor issues.** There's mention of one of the main causes, but not the main cause itself.
        
-   The response should be an essay. <-- **OBJECTIVE** criteria
    
    -   **No issues.** It has the structure of an essay.
        

### **Objective and Self-Contained Criteria Examples:**

Imagine you have the following prompt:

> My kids have been obsessed with animatronics since the Five Nights at Freddy's movie came out. What are 5 real life places where I could take them to see real working animatronics? Provide a paragraph description of each along with some midwest U.S. locations. Only include actual robot/animated electronic characters, not people in costumes.

A good **SUBJECTIVE**, **SELF-CONTAINED** criteria would be:

> The model should prioritize locations that provide an exciting and immersive experience for children when selecting places to visit

**Why is it SUBJECTIVE?**

-    This criterion is based on an opinion or interpretation of what is “exciting” and “immersive” for children, which can vary from person to person.
    

**Why is it SELF-CONTAINED?**

-   It can be understood and acted upon in isolation without needing additional context or information.
    
-   It provides all the necessary details for the model to follow that specific instruction without relying on other instructions or prior knowledge
    

A good **OBJECTIVE**, **SELF-CONTAINED** criteria would be:

> The model should exclude places with people in costumes

**Why is it OBJECTIVE?**

-   This is objective because it’s based on a concrete condition: places with people in costumes are not allowed.
    
-   There’s **NO** **<u>ambiguity</u>** or **<u>interpretation</u>** needed - it’s a straightforward rule that can be factually verified.
    

**More examples:**

-   **Prompt:** "Give me a list of cities that are a short day trip away from London."
    
    -   ***Explanation:*** *"short" may be subjective, but some models may give responses that are way too far away, so "Each city in the list should be a short day trip away from London" is still a* ***good Subjective*** *criteria.*
        
-   **Prompt:** "Give me a list of child-friendly foods that my 10 year old son could eat for lunch."
    
    -   ***Explanation:*** *"child-friendly" may be subjective, but some models may give poor choices of foods, so "Each food item in the list should be appropriate for a 10-year old boy" is still a* ***good Subjective*** *criteria.*
        

### **Section 2: Instructions, examples, and Step-by-Step**

This is the final section you’ll complete each turn.

It’s essentially about evaluating whether each model’s response meets the criteria listed in the previous section and deciding which one is the better option.

You should use the number of **"No issues"**, **"Minor issues"** and **"Major Issues"** ratings for the criteria to determine which response is better.

Once you’ve made your decision, you’ll need to explain the reasoning behind your ratings.

Remember, your explanation should meet the following guidelines:

-   Be **2-5+ sentences** long, with clear rationale, proper grammar, and structure.
    
-   Be **self-contained**, so that **by reading the explanation alone**, one can **understand the basis for your ratings.**
    
-   **Be as thorough as possible.** We’re looking for a **detailed** explanation that **addresses all relevant issues.**
    
-   **DO NOT MENTION** the platform (DAT) or any of the instructions you've been given.
    
-   **DO NOT MENTION/REFERENCE** the original worker's ratings or explanation.
    

*Thank you for your help with this project! :)*

Collapse Instructions

## **Section 0:** **Task Data**

### **Images (use them to create & rate criteria)**

## **<u>IMPORTANT:</u> IF THERE ARE NO IMAGES, SELECT THE FIRST FLAG AND SUBMIT.**

<table style="minWidth: 25px"><colgroup><col></colgroup><tbody><tr><th rowspan="1" colspan="1"><p>Images <span style="color: rgb(204, 0, 0); --darkreader-inline-color: var(--darkreader-text-cc0000, #ff3d3d);" data-darkreader-inline-color="">(can be empty, click to view full size)</span></p></th></tr><tr><td rowspan="1" colspan="1"><p></p><div class="rendered-markdown"><div align="center"><table style="border-collapse: collapse; width: auto;"><tbody><tr><td style="border: 1px solid rgb(198, 198, 198); padding: 4px; --darkreader-inline-border-top: var(--darkreader-border-c6c6c6, #404548); --darkreader-inline-border-right: var(--darkreader-border-c6c6c6, #404548); --darkreader-inline-border-bottom: var(--darkreader-border-c6c6c6, #404548); --darkreader-inline-border-left: var(--darkreader-border-c6c6c6, #404548);" data-darkreader-inline-border-top="" data-darkreader-inline-border-right="" data-darkreader-inline-border-bottom="" data-darkreader-inline-border-left=""><a rel="noopener noreferrer" href="https://projects-uploaded-files.s3.us-east-2.amazonaws.com/production/item_response_files/a98ef15b-b79f-4a71-b270-0fadc42644e0_a2616633-e0f2-4db8-8ec0-f42676461bde_e45fc769-c039-47d0-bc98-249834a71d33.jpg" target="_blank"><img src="Raven%20-%20Images,%20Non-STEM%20-%20Create%20Fine-Grained%20Criteria%20and%20Rate%20Responses%20from%20Two%20Models%20(021225)/a98ef15b-b79f-4a71-b270-0fadc42644e0_a2616633-e0f2-4db8-8ec0-f42676461bde_e45fc769-c039-47d0-bc98-249834a71d33.jpg" alt="Organic_Moderated_Reactor_Experiment_Piping_and_Instrumentation_Diagram.jpg" style="display: block; height: 200px; margin: 0 auto;"></a></td></tr></tbody></table></div></div><p></p></td></tr><tr><td rowspan="1" colspan="1"><p></p><div class="rendered-markdown"></div><p></p></td></tr><tr><td rowspan="1" colspan="1"><p></p><div class="rendered-markdown"></div><p></p></td></tr><tr><td rowspan="1" colspan="1"><p></p><div class="rendered-markdown"></div><p></p></td></tr><tr><td rowspan="1" colspan="1"><p></p><div class="rendered-markdown"></div><p></p></td></tr></tbody></table>

### **Conversation (can be empty)**

### 👤 User (Turn 1)

Does the primary coolant pumps flow to or from the heat exchanger? What type of heat exchanger is it?

***

### 🤖 Assistant (Turn 1)

Based on the diagram:

1.  **Flow Direction**: The primary coolant pumps flow **to** the heat exchanger. This can be seen from the flow lines leading from the primary coolant pumps (labeled as "PRIMARY COOLANT PUMPS") towards the heat exchanger (labeled as "AIR BLAST EXCHANGER").
    
2.  **Type of Heat Exchanger**: The heat exchanger is labeled as "AIR BLAST EXCHANGER," indicating it is an air blast type of heat exchanger.
    

***

<table style="minWidth: 50px"><colgroup><col><col></colgroup><tbody><tr><td rowspan="1" colspan="2"><h3><strong>Prompt</strong></h3></td></tr><tr><td rowspan="1" colspan="2"><p>We are needing to rearrange some of the equipment. Please identify the 3 largest tanks. List them in order from biggest to smallest. If had to move one of these three, which one would be the best one to move?</p></td></tr><tr><th rowspan="1" colspan="1"><h3><strong><span style="color: rgb(103, 78, 167); --darkreader-inline-color: var(--darkreader-text-674ea7, #7e67b8);" data-darkreader-inline-color="">Response A </span><span style="color: rgb(204, 0, 0); --darkreader-inline-color: var(--darkreader-text-cc0000, #ff3d3d);" data-darkreader-inline-color="">(pre-edits)</span></strong></h3></th><th rowspan="1" colspan="1"><h3><strong><span style="color: rgb(166, 28, 0); --darkreader-inline-color: var(--darkreader-text-a61c00, #ff7458);" data-darkreader-inline-color="">Response B </span><span style="color: rgb(204, 0, 0); --darkreader-inline-color: var(--darkreader-text-cc0000, #ff3d3d);" data-darkreader-inline-color="">(pre-edits)</span></strong></h3></th></tr><tr><td rowspan="1" colspan="1"><p></p><div class="rendered-markdown"><p>To identify the three largest tanks and determine which one would be best to move, let's analyze the diagram:</p><ol><li><p><strong>Largest Tank</strong>:</p><ul><li><strong>CORE REACTOR VESSEL</strong>: This is the largest tank, with a capacity of 300,000 gallons.</li></ul></li><li><p><strong>Second Largest Tank</strong>:</p><ul><li><strong>DISTILLATE TANK</strong>: This tank has a capacity of 7,000 gallons.</li></ul></li><li><p><strong>Third Largest Tank</strong>:</p><ul><li><strong>FEED TANK</strong>: This tank has a capacity of 3,000 gallons.</li></ul></li></ol><h3>Order from Biggest to Smallest:</h3><ol><li><strong>CORE REACTOR VESSEL</strong> (300,000 gallons)</li><li><strong>DISTILLATE TANK</strong> (7,000 gallons)</li><li><strong>FEED TANK</strong> (3,000 gallons)</li></ol><h3>Which One to Move:</h3><p>Considering the sizes and potential complexity of moving such large equipment:</p><ul><li><strong>FEED TANK</strong> (3,000 gallons) would be the best one to move. It is significantly smaller than the other two, making it easier to handle and less disruptive to the overall system. Moving the largest tank (CORE REACTOR VESSEL) would be highly complex and likely impractical due to its size and critical role in the system. The DISTILLATE TANK, while smaller than the CORE REACTOR VESSEL, is still quite large compared to the FEED TANK, making the latter the most feasible option for relocation.</li></ul></div><p></p></td><td rowspan="1" colspan="1"><p></p><div class="rendered-markdown"><p>Based on the provided diagram, the three largest tanks are:</p><ol><li><strong>Core Tank</strong> - Labeled as "CORE TANK" with a capacity of 3700 GALS.</li><li><strong>Waste Storage Tank</strong> - Labeled as "WASTE STORAGE TANK" with a capacity of 3000 GALS.</li><li><strong>Drain Tank</strong> - Labeled as "DRAIN TANK" with a capacity of 6000 GAL.</li></ol><p>Listing them from biggest to smallest:</p><ol><li><strong>Drain Tank</strong> (6000 GAL)</li><li><strong>Core Tank</strong> (3700 GALS)</li><li><strong>Waste Storage Tank</strong> (3000 GALS)</li></ol><p>If you had to move one of these three tanks, the <strong>Waste Storage Tank</strong> would be the best one to move. Here’s why:</p><ul><li><strong>Waste Storage Tank</strong> is the smallest of the three largest tanks, making it easier to handle and relocate.</li><li>It is not directly connected to the core processes like the Core Tank, which is integral to the primary operations.</li><li>The Drain Tank, while larger, is likely used for critical drainage purposes, which might make moving it more disruptive.</li></ul><p>Thus, moving the Waste Storage Tank would likely cause the least disruption to the overall system.</p></div><p></p></td></tr></tbody></table>

### **Original Worker's Ratings and Explanation (just for reference)**

On this table, you’ll either see different axes where the worker identified issues with one or both responses, or no axes if the worker believed that neither response had any issues. This should help you develop and evaluate your criteria!

## Ratings

*(✅ = No issues found, ❌ = Issues found)*

| Dimension | Response A | Response B |
| --- | --- | --- |
| **Verbosity** | ❌ | ❌ |
| **Correctness** | ❌ | ❌ |

**Final Preference:**

> Model B is better

**Explanation (can be empty if neither response had issues):**

> Both models referenced actual tanks on the page, but they changed the clearly labels tank sizes. Neither the listed volume nor calculated volume (determined from the visible dimension matched the models, with the exception of of the tanks mentioned by Model B. Model B identified the 3 largest tanks but put them in the wrong order.

## **Prompt Flags**

**These flags let us know if the prompt is contrived, overly simple, or if you think it has other issues.**

-   **Flags 1 and 2 will hide all other questions**, as those shouldn’t be completed
    
-   The other flags are just for extra information
    

One or both responses are empty / There are no attached images / Task is STEM-related

The prompt and/or images are adversarial, harmful, NSFW, non-English, or depict DataAnnotation in some way

The prompt’s main issues are tied to visual recognition

Prompt is contrived

Other issues

## **Section 1: Prompt Criteria Breakdown**

## **IMPORTANT: Do not copy these verbatim. If you plan to use one, make sure to write it in your own words.**

### **THIS TOOL DOESN'T HAVE ACCESS TO THE ATTACHED IMAGES.**

### **Instruction Breakdown: Criteria Creation Helper #1 (MAINLY FOR INSPIRATION)**

**This tool will generate a batch of detailed criteria to give you some inspiration.**

***The model can be unreliable, so take its responses with a grain of salt.***

**Important Reminders:**

-   These generated responses might be **inconsistent** and **contain errors** - this is mainly to give you a general idea or some **inspiration for creating the criteria**
    
    -   Make sure to double-check the generated criteria before using them. **You should also include your own; this is just a starting point.**
        
-   The model won’t leave out criteria it gets right 95% of the time, so it’s up to you to decide which ones should stay and which should go.
    

Generate

## **IMPORTANT: Do not copy these verbatim. If you plan to use one, make sure to write it in your own words.**

### **THIS TOOL DOESN'T HAVE ACCESS TO THE ATTACHED IMAGES.**

### **Instruction Breakdown: Criteria Creation Helper #2**

Criteria Creation Helper #1 can be dumb in various ways. We think this model is better, but slower. Try BOTH to make sure you understand what good criteria might be!

One thing the models are NOT good at is making sure the "answer key criteria" are self-contained. Basically, given a response, you should be able to judge whether or not it satisfies a criterion WITHOUT seeing the original prompt and WITHOUT external knowledeg.

For example:

-   **Prompt:** Extract all the adjectives from the following paragraph. Beneath the towering, emerald-green trees of the ancient forest, a gentle breeze whispered through the vibrant foliage. Sunlight filtered through the dense canopy, casting dappled, golden patterns on the soft, mossy ground.
    
-   **Bad Criteria (not self-contained):** “The model should extract all the adjectives from the paragraph.”
    
    -   This is not a good answer key since we don’t know what all the adjectives are without seeing the prompt.
        
-   **Good Criteria:** “The model should extract the following adjectives: towering, emerald-green, ancient, gentle, vibrant, dense, dappled, golden, soft, mossy”
    

Generate

### **REMINDER: You need to select the number of criteria you will be creating.**

### **\- Once you’ve done that, new questions will appear where you can write the criteria and select their types.**

### **Instruction Breakdown: Possible Criteria**

How many **ATOMIC** and **objective/subjective** criteria can be derived from the **explicit** and **implicit** instructions in your prompt?

1

2

3

4

5

6

7

8

9

10

11

12

13

14

15

### **Task Analyzer V0.1 - VERY NEW, JUST RUN IT TO TEST AND GIVE FEEDBACK**

### **THIS TOOL DOESN'T HAVE ACCESS TO THE ATTACHED IMAGES.**

Hey! You’re about to use the pilot version of Task Analyzer. This tool is still in its early stages, so it **WILL NOT** get things right.

-   **Run it, test it, and share your thoughts!** This tool is in the feedback phase, and we’d love any insights, suggestions, or general impressions you have.
    
-   **Give it a try, but rely on your expertise.** Task Analyzer is a support tool, not a replacement for your judgment or expertise.
    

### **<u>IMPORTANT:</u>** **<u>Don’t rely solely on this - IT MAKES A LOT OF MISTAKES!</u>** **<u>Always use your own judgment.</u>**

Generate

## **Section 2: Criteria Ratings and Model Preference**

## **Criteria Ratings and Model Preference: Response A ratings**

### **Criteria Ratings and Model Preference: Response A Overall Rating**

### **Your Response A ratings:**

<table style="minWidth: 75px"><colgroup><col><col><col></colgroup><tbody><tr><th rowspan="1" colspan="1"><p>Criterion ID</p></th><th rowspan="1" colspan="1"><p>Criterion Text <span style="color: rgb(204, 0, 0); --darkreader-inline-color: var(--darkreader-text-cc0000, #ff3d3d);" data-darkreader-inline-color="">(can be empty)</span></p></th><th rowspan="1" colspan="1"><p><span style="color: rgb(103, 78, 167); --darkreader-inline-color: var(--darkreader-text-674ea7, #7e67b8);" data-darkreader-inline-color="">Response A</span> Criterion Rating <span style="color: rgb(204, 0, 0); --darkreader-inline-color: var(--darkreader-text-cc0000, #ff3d3d);" data-darkreader-inline-color="">(can be empty)</span></p></th></tr><tr><td rowspan="1" colspan="1"><p><strong>1</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>2</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>3</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>4</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>5</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>6</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>7</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>8</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>9</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>10</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>11</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>12</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>13</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>14</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>15</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(142, 124, 195); --darkreader-inline-color: var(--darkreader-text-8e7cc3, #9280c5);" data-darkreader-inline-color=""></span></strong></p></td></tr></tbody></table>

**How good is the model's response overall?**

*Consider all your previous ratings.*

Amazing

Pretty Good

Okay

Pretty Bad

Horrible

## **Criteria Ratings and Model Preference: Response B ratings**

### **Criteria Ratings and Model Preference: Response B Overall Rating**

### **Your overall ratings:**

<table style="minWidth: 75px"><colgroup><col><col><col></colgroup><tbody><tr><th rowspan="1" colspan="1"><p>Criterion ID</p></th><th rowspan="1" colspan="1"><p>Criterion Text <span style="color: rgb(204, 0, 0); --darkreader-inline-color: var(--darkreader-text-cc0000, #ff3d3d);" data-darkreader-inline-color="">(can be empty)</span></p></th><th rowspan="1" colspan="1"><p><span style="color: rgb(166, 28, 0); --darkreader-inline-color: var(--darkreader-text-a61c00, #ff7458);" data-darkreader-inline-color="">Response B</span> Criterion Rating <span style="color: rgb(204, 0, 0); --darkreader-inline-color: var(--darkreader-text-cc0000, #ff3d3d);" data-darkreader-inline-color="">(can be empty)</span></p></th></tr><tr><td rowspan="1" colspan="1"><p><strong>1</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>2</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>3</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>4</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>5</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>6</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>7</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>8</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>9</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>10</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>11</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>12</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>13</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>14</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr><tr><td rowspan="1" colspan="1"><p><strong>15</strong></p></td><td rowspan="1" colspan="1"><p></p></td><td rowspan="1" colspan="1"><p><strong><span style="color: rgb(204, 65, 37); --darkreader-inline-color: var(--darkreader-text-cc4125, #dd5f45);" data-darkreader-inline-color=""></span></strong></p></td></tr></tbody></table>

**How good is the model's response overall?**

*Consider all your previous ratings.*

Amazing

Pretty Good

Okay

Pretty Bad

Horrible

### **Criteria Ratings and Model Preference: Which response is better?**

### **Your overall ratings:**

**You can use the number of 'No Issues', 'Minor Issues', and ‘Major Issues’ ratings for the criteria to determine which response is better, but it's always up to how you feel about each response!**

Response A is much better

Response A is better

Response A is slightly better

Unsure or Response A is negligibly better

Unsure or Response B is negligibly better

Response B is slightly better

Response B is better

Response B is much better

### **Criteria Ratings and Model Preference: Preference Rationale**

**Explain the reasoning for your previous ratings.**

Remember, this explanation should have the following characteristics:

-   Be **2-5+ sentences** long, aim for a good rationale with proper grammar and structure.
    
-   Be **self-contained**, so that **by reading the explanation alone**, one can **understand the basis for your ratings.**
    
-   **Try to be as thorough as possible. We’re looking for a <u>detailed explanation that addresses all the issues</u>.**
    
-   **DO NOT MENTION** the platform (DAT) or any of the instructions you've been given.
    
-   **IMPORTANT: DO NOT MENTION/REFERENCE** the original worker's ratings or explanation.
    

**Reminder:**

-   The main goal of your explanation is to <u>make it easy for reviewers to assess whether your ratings are correct.</u>
    

-   If possible, make it easier for reviewers to double-check your rating. For example, if there’s a factual error in a long text, quote the specific part instead of just saying, “Response A has a factuality error.”
    
-   **Being specific helps clarify your reasoning.**
    
    -   **Example:** If the user asks for “10 exercises I can do from my couch,” don’t just say, “Response A has an exercise that can’t be done from the couch.” Instead, specify which one, like “the jumping jack, 3rd on the list”.
        
-   If you fact-checked information online, include the links you used.
    

### **Criteria Ratings and Model Preference: Rating Agreement**

**Do your ratings align with the original worker’s ratings? (Ideally, they should always match)**

*By "align" we mean whether they are similar. They don’t need to be exactly the same, but as long as you chose the same response as the better one, it would be considered similar.*

Yes, they align

No, they DON'T align

**\[Optional\]** **Task Comments**

Submit

                                                                                                      .circle-stroke-red circle:first-child{stroke:#d02d2d}.circle-stroke-green circle:first-child{stroke:#38b724}.circle-stroke-orange circle:first-child{stroke:#fcd34d} input\[type=text\]\[role=combobox\]:focus{box-shadow:none} .tippy-box\[data-theme~=suggestion\] .tippy-content{padding:0} document.addEventListener("DOMContentLoaded", function(event) { const url = new URL(window.location.href); url.searchParams.set("task\_response\_id", "792910c7-0a22-4ae4-a79e-4615c23e3ec4"); window.history.replaceState(null, null, url); }) document.addEventListener("DOMContentLoaded", function(event) { const taskData = {"id":"70a5ae42-e9b2-4f45-87af-a28fcc2a2ac3\_T2","project\_id":"ead144a1-ddcd-4510-99f1-06c16d43d679","prompt":"We are needing to rearrange some of the equipment. Please identify the 3 largest tanks. List them in order from biggest to smallest. If had to move one of these three, which one would be the best one to move?","response\_a":"To identify the three largest tanks and determine which one would be best to move, let's analyze the diagram:\\n\\n1. \*\*Largest Tank\*\*:\\n - \*\*CORE REACTOR VESSEL\*\*: This is the largest tank, with a capacity of 300,000 gallons.\\n\\n2. \*\*Second Largest Tank\*\*:\\n - \*\*DISTILLATE TANK\*\*: This tank has a capacity of 7,000 gallons.\\n\\n3. \*\*Third Largest Tank\*\*:\\n - \*\*FEED TANK\*\*: This tank has a capacity of 3,000 gallons.\\n\\n### Order from Biggest to Smallest:\\n1. \*\*CORE REACTOR VESSEL\*\* (300,000 gallons)\\n2. \*\*DISTILLATE TANK\*\* (7,000 gallons)\\n3. \*\*FEED TANK\*\* (3,000 gallons)\\n\\n### Which One to Move:\\nConsidering the sizes and potential complexity of moving such large equipment:\\n\\n- \*\*FEED TANK\*\* (3,000 gallons) would be the best one to move. It is significantly smaller than the other two, making it easier to handle and less disruptive to the overall system. Moving the largest tank (CORE REACTOR VESSEL) would be highly complex and likely impractical due to its size and critical role in the system. The DISTILLATE TANK, while smaller than the CORE REACTOR VESSEL, is still quite large compared to the FEED TANK, making the latter the most feasible option for relocation.","response\_b":"Based on the provided diagram, the three largest tanks are:\\n\\n1. \*\*Core Tank\*\* - Labeled as \\"CORE TANK\\" with a capacity of 3700 GALS.\\n2. \*\*Waste Storage Tank\*\* - Labeled as \\"WASTE STORAGE TANK\\" with a capacity of 3000 GALS.\\n3. \*\*Drain Tank\*\* - Labeled as \\"DRAIN TANK\\" with a capacity of 6000 GAL.\\n\\nListing them from biggest to smallest:\\n\\n1. \*\*Drain Tank\*\* (6000 GAL)\\n2. \*\*Core Tank\*\* (3700 GALS)\\n3. \*\*Waste Storage Tank\*\* (3000 GALS)\\n\\nIf you had to move one of these three tanks, the \*\*Waste Storage Tank\*\* would be the best one to move. Here’s why:\\n\\n- \*\*Waste Storage Tank\*\* is the smallest of the three largest tanks, making it easier to handle and relocate.\\n- It is not directly connected to the core processes like the Core Tank, which is integral to the primary operations.\\n- The Drain Tank, while larger, is likely used for critical drainage purposes, which might make moving it more disruptive.\\n\\nThus, moving the Waste Storage Tank would likely cause the least disruption to the overall system.","ow\_preference":"Model B is better","ow\_ratings":"## Ratings\\n\\n\*(✅ = No issues found, ❌ = Issues found)\*\\n\\n| Dimension | Response A | Response B |\\n|-----------|------------|------------|\\n| \*\*Verbosity\*\* | ❌ | ❌ |\\n| \*\*Correctness\*\* | ❌ | ❌ |\\n","image\_name1":"Organic\_Moderated\_Reactor\_Experiment\_Piping\_and\_Instrumentation\_Diagram.jpg","image\_url1":"\\u003cdiv align=\\"center\\"\\u003e\\n \\u003ctable style=\\"border-collapse: collapse; width: auto;\\"\\u003e\\n \\u003ctr\\u003e\\n \\u003ctd style=\\"border: 1px solid #c6c6c6; padding: 4px;\\"\\u003e\\n \\u003ca href=\\"https://projects-uploaded-files.s3.us-east-2.amazonaws.com/production/item\_response\_files/a98ef15b-b79f-4a71-b270-0fadc42644e0\_a2616633-e0f2-4db8-8ec0-f42676461bde\_e45fc769-c039-47d0-bc98-249834a71d33.jpg\\" target=\\"\_blank\\"\\u003e\\n \\u003cimg src=\\"https://projects-uploaded-files.s3.us-east-2.amazonaws.com/production/item\_response\_files/a98ef15b-b79f-4a71-b270-0fadc42644e0\_a2616633-e0f2-4db8-8ec0-f42676461bde\_e45fc769-c039-47d0-bc98-249834a71d33.jpg\\" alt=\\"Organic\_Moderated\_Reactor\_Experiment\_Piping\_and\_Instrumentation\_Diagram.jpg\\" style=\\"display: block; height: 200px; margin: 0 auto;\\"\\u003e\\n \\u003c/a\\u003e\\n \\u003c/td\\u003e\\n \\u003c/tr\\u003e\\n \\u003c/table\\u003e\\n\\u003c/div\\u003e","image\_name2":null,"image\_url2":null,"image\_name3":null,"image\_url3":null,"image\_name4":null,"image\_url4":null,"image\_name5":null,"image\_url5":null,"conversation\_history":"### 👤 User (Turn 1)\\n\\nDoes the primary coolant pumps flow to or from the heat exchanger? What type of heat exchanger is it?\\n\\n---\\n\\n### 🤖 Assistant (Turn 1)\\n\\nBased on the diagram:\\n\\n1. \*\*Flow Direction\*\*: The primary coolant pumps flow \*\*to\*\* the heat exchanger. This can be seen from the flow lines leading from the primary coolant pumps (labeled as \\"PRIMARY COOLANT PUMPS\\") towards the heat exchanger (labeled as \\"AIR BLAST EXCHANGER\\").\\n\\n2. \*\*Type of Heat Exchanger\*\*: The heat exchanger is labeled as \\"AIR BLAST EXCHANGER,\\" indicating it is an air blast type of heat exchanger.\\n\\n---\\n\\n","model\_with\_issue":"A+B","ow\_explanation":"Both models referenced actual tanks on the page, but they changed the clearly labels tank sizes. Neither the listed volume nor calculated volume (determined from the visible dimension matched the models, with the exception of of the tanks mentioned by Model B. Model B identified the 3 largest tanks but put them in the wrong order.","response\_a\_title":"Response A","response\_b\_title":"Response B (selected by original worker)","has\_issues":true,"issue\_count":"both"}; if (taskData.hasOwnProperty("json\_url")){ fetch(taskData\["json\_url"\]) .then(res => res.json()) .then((taskData) => { const fieldsText = $(".fields-text") const questionForms = $(".form-group") for (const \[key, value\] of Object.entries(taskData)) { const injectData = function() { var templateHTML = $(this).html(); templateHTML = templateHTML.replace("{{" + key + "}}", value) $(this).html(templateHTML); } // Inject data from s3 into the fields text and questions fieldsText.each(injectData); questionForms.each(injectData); } }).catch(err => console.error(err)) // catch error from GET request } })

  

Please only leave messages if you have questions about performing the task that you need the poster to answer, if the project is broken in some way, or if you have tips or answers for other workers. If you are facing technical difficulties, have feedback about pay, or have other suggestions, please email DataAnnotation instead. Thanks!

-   Instructions say that ideally, the original worker's rating lines up with our own. Are we supposed to be writing our criterion in such a way that sort of engineers that possibility? Eg, a worker marks Response B down a peg because they didn't like its formatting. Formatting was not specified at all in the original prompt. IMO, neither response had better formatting than the other (they were both meh). Should I be writing a criterion about formatting that would give B a better score for that criterion in order to get my rating to match up with the original worker's?
    
    **Catherine**
    
    var timestamp = "2025-02-13T00:12:02Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-a9ba1508-c7ac-45be-978c-05706129f8b6").appendChild(newParagraph);
    
    2/12/2025, 06:12 PM
    
-   If its a really simple prompt like "what is this?" and the image is an apple, I'd select that flag. There are probably other criteria but i'm not sure.
    
    **Christopher**
    
    var timestamp = "2025-02-13T00:11:18Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-ad8ef355-63a3-46ee-a51f-ca822928d319").appendChild(newParagraph);
    
    2/12/2025, 06:11 PM
    
-   Does anyone know when we would select the third flag option? The one labeled "the prompt's main issues are tied to visual recognition"
    
    **JosephT-6MFWMCC2**
    
    var timestamp = "2025-02-12T22:45:34Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-944bf770-47d3-4cd4-81b3-1d65b2358122").appendChild(newParagraph);
    
    2/12/2025, 04:45 PM
    
-   I've got a prompt that includes, 'Feel free to draw a diagram to better illustrate your response.' Both responses utterly failed to draw any sort of comprehensible diagram. Would it be appropriate to create a critereon instructing the model to not attempt to draw a diagram?
    
    **ElijahS-J2QJ9ZKR**
    
    var timestamp = "2025-02-12T22:17:46Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-801d2f9c-f3fc-4303-87b4-83ee7b059de1").appendChild(newParagraph);
    
    2/12/2025, 04:17 PM
    
-   Does anyone know if it is within the model's capabilities to provide links? I saw in the FAQ that they can follow links, but it doesn't say anything about providing them.
    
    **Raphael**
    
    var timestamp = "2025-02-12T21:50:23Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-00e23baa-905e-44fc-a3bd-050885508a63").appendChild(newParagraph);
    
    2/12/2025, 03:50 PM
    
-   @Allison I usually give a range of what I feel would best meet the needs of the user. So like 2-3 sentences, 3-5 examples, etc. It's more explicit that way.
    
    **OliviaB-R6G3XHRW**
    
    var timestamp = "2025-02-12T21:16:22Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-318a6de8-a4fc-4e35-9b07-a9c72567ba72").appendChild(newParagraph);
    
    2/12/2025, 03:16 PM
    
-   @OliviaB-R6G3XHRW I think this is a good criterion as long as it's self-contained. So I think you'd want to specify that it needs to "organize XYZ from previous response", not just "organize based on previous response".
    
    **Christian**
    
    var timestamp = "2025-02-12T20:59:05Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-9f3d2cf7-f1eb-4423-8603-dd1a3f5eefc7").appendChild(newParagraph);
    
    2/12/2025, 02:59 PM
    
-   @Katrina Hmm, is this for a situation where the model just isn't seeing the image that's there? If so, I find it confusing that it's listed as a "Prompt flag", since the issue is with the model, not the prompt.
    
    **Christian**
    
    var timestamp = "2025-02-12T20:49:33Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-a3320628-d404-4958-ac81-6730a2a459ce").appendChild(newParagraph);
    
    2/12/2025, 02:49 PM
    
-   Good God, it finally clicked. I'm such a... yep, I read through it again. Thank you, @Mindy! I think I was doing that while you were sending me the message!
    
    **KarenP-DTNX9XJY**
    
    var timestamp = "2025-02-12T20:36:48Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-3da69d5d-3983-4d25-b7e9-c636f4110bc2").appendChild(newParagraph);
    
    2/12/2025, 02:36 PM
    
-   @Karen, if you read through all of the information listed on the left side of the screen starting from the top, it should give you direction. You may have to hit the small down arrows if each block isn't already open for you.
    
    **Mindy**
    
    var timestamp = "2025-02-12T20:13:33Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-290e7661-41c2-4b15-a4d9-7cddfbcfdacf").appendChild(newParagraph);
    
    2/12/2025, 02:13 PM
    
-   @Karen, if you read through all of the information listed on the left side of the screen starting from the top, it should give you direction. You may have to hit the small down arrows if each block isn't already open for you.
    
    **Mindy**
    
    var timestamp = "2025-02-12T20:13:33Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-76097ad9-b5ac-4eb4-ba4c-c43670f0043a").appendChild(newParagraph);
    
    2/12/2025, 02:13 PM
    
-   @Christian i believe that it’s the second one. If the model isn’t recognizing the image, that’s a visual recognition issue.
    
    **Katrina**
    
    var timestamp = "2025-02-12T20:02:01Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-9e4feebf-9f82-4114-831e-af4a4c11683f").appendChild(newParagraph);
    
    2/12/2025, 02:02 PM
    
-   Can the chatbots use judgment with the word several? For example, if I say it should include several examples, is that enough or do you have to explicitly say "For example, at least 4 categories should be used."
    
    **AllisonH-RTNFY7ND**
    
    var timestamp = "2025-02-12T19:57:48Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-f619e03d-6682-42bc-9b69-5a3f85de2a27").appendChild(newParagraph);
    
    2/12/2025, 01:57 PM
    
-   If the prompt asks to organize XYZ from the bots previous response can we include "should organize based on previous response" in our criterion? that may sound like a stupid question but for some reason im thinking we arent supposed to that?
    
    **OliviaB-R6G3XHRW**
    
    var timestamp = "2025-02-12T19:55:57Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-163f865f-e8d4-46bf-b410-9407dfe8aa4c").appendChild(newParagraph);
    
    2/12/2025, 01:55 PM
    
-   @Adinai, to add to what Alan said, try not to overthink the criterion too much. I have found it helps to approach them with my own expectations in mind first (what I would want out of the response based on the prompt) and then go back to the checklist afterwards to make sure they also meet the standards.
    
    **GavinP-NXQJX4MR**
    
    var timestamp = "2025-02-12T19:50:48Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-8ff6a4ee-0086-477f-a656-0f8741aaf312").appendChild(newParagraph);
    
    2/12/2025, 01:50 PM
    
-   Hi. I need some clarification. I feel a little clueless right now. What is my task here? I THINK I'm filling in the criteria, after I choose how many I will generate. Is that correct? Then what I am I supposed to do? I have three choices that come up, but I'm not getting any model responses. Should I be comparing them to the Model A & B that are already there under the Prompt? I'm so confused. I feel a little bit like an idiot. I think life has sucked my brain out. Can anyone help me?
    
    **KarenP-DTNX9XJY**
    
    var timestamp = "2025-02-12T19:43:07Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-6153548d-d108-4250-8a30-fa239297746d").appendChild(newParagraph);
    
    2/12/2025, 01:43 PM
    
-   Are we allowed to put the images into Google Lens?
    
    **KarinaW-X2HFKZC2**
    
    var timestamp = "2025-02-12T19:38:52Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-b5700653-4ba2-4051-b893-05fb24d3b6dc").appendChild(newParagraph);
    
    2/12/2025, 01:38 PM
    
-   "Lastly, be sure to incorporate the feedback from 11/12 when creating your criteria!" am I missing something here? what's 11/12
    
    **OliviaB-R6G3XHRW**
    
    var timestamp = "2025-02-12T19:30:00Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-f7af6de5-9172-41c6-a8f8-d25c34d8ab1d").appendChild(newParagraph);
    
    2/12/2025, 01:30 PM
    
-   I have a question about the Prompt Flag: "The prompt’s main issues are tied to visual recognition" - Does this mean that the previous worker created a bad prompt by simply asking the model to identify things in an image (I've seen many image prompt projects where we are asked to challenge the model beyond simple recognition)? - Or does it mean that the issues with the responses the worker received had mostly to do with the model failing to recognize things in the image?
    
    **Christian**
    
    var timestamp = "2025-02-12T18:59:13Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-7191193a-3da2-43e1-bbfa-4f148e482c89").appendChild(newParagraph);
    
    2/12/2025, 12:59 PM
    
-   Nvm, tried it again a couple minutes later and it worked
    
    **EzraS-3926RM24**
    
    var timestamp = "2025-02-12T18:10:10Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-ad57d99a-ace3-47ad-8e59-8bcb45465ee8").appendChild(newParagraph);
    
    2/12/2025, 12:10 PM
    
-   Did anyone else get the "This request would exceed your organization’s rate limit of 20,000,000 prompt bytes per hour" message in the Task Analyzer? Is there any workaround for this?
    
    **EzraS-3926RM24**
    
    var timestamp = "2025-02-12T18:07:44Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-5f777c1e-7827-4c34-ae10-d14db04a13a7").appendChild(newParagraph);
    
    2/12/2025, 12:07 PM
    
-   @Jessica thanks - I'll stick to this approach
    
    **AlexC-WC3YCQ4T**
    
    var timestamp = "2025-02-12T17:35:25Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-e9796f0f-bc4d-41d3-8a31-dcd97341f747").appendChild(newParagraph);
    
    2/12/2025, 11:35 AM
    
-   @adinai the instructions say to give 30% implicit criterion. so basically yes
    
    **OliviaB-R6G3XHRW**
    
    var timestamp = "2025-02-12T17:17:31Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-ce9ef65c-5e61-4af6-b9e8-93b89496191d").appendChild(newParagraph);
    
    2/12/2025, 11:17 AM
    
-   @Adinai so think of it like : the bots response would have no mistakes if it were to follow the criteria YOU are writing. so include anything that you think the bot needs. That's how I've been going about these projects, but anyone can correct me if I am wrong! The instructions are verrrrrry lengthy.
    
    **OliviaB-R6G3XHRW**
    
    var timestamp = "2025-02-12T17:12:19Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-d21cf262-4d42-494a-b655-c3893b2e19af").appendChild(newParagraph);
    
    2/12/2025, 11:12 AM
    
-   Should I be generating criteria that doesn't necessarily appear in the actual response?
    
    **AdinaiB-P7PPMRTF**
    
    var timestamp = "2025-02-12T17:06:14Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-fc9bb7c5-09a3-4fc2-8c94-f93b7e619280").appendChild(newParagraph);
    
    2/12/2025, 11:06 AM
    
-   can our criterion direct the model to provide links?
    
    **OliviaB-R6G3XHRW**
    
    var timestamp = "2025-02-12T17:05:24Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-a0180151-804e-4827-89b1-2bf7b223b7d6").appendChild(newParagraph);
    
    2/12/2025, 11:05 AM
    
-   @britten @Mindy I believe you also need to delete any text in the criteria you are removing, if it's not blank. I had this the other day where I just reduced it from 9 to 8, but then the Task Analyzer still produced results for 9, so I had to go back to 9, delete the text, and then try again with 8.
    
    **AlanT-NYVJWVPP**
    
    var timestamp = "2025-02-12T16:58:36Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-38c53a21-2b47-48d2-9fbe-7d09fd7973a3").appendChild(newParagraph);
    
    2/12/2025, 10:58 AM
    
-   @Adinai, the criteria should be a representation of what you expect in a perfect response to the prompt both explicitly stated in the prompt and implicitly expected by the user.
    
    **Alan**
    
    var timestamp = "2025-02-12T16:47:50Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-baa9f0a1-8478-4224-9b98-66565af8641d").appendChild(newParagraph);
    
    2/12/2025, 10:47 AM
    
-   I am new to this project. I have read the instructions and the FAQ but I am still having a hard time wrapping my head around what this is trying to accomplish. I know it'll probably come after I do a few but thought it best to just ask...Are we giving criteria that define what is already in the model's response or criteria for what should have been in the response but was missing or both? For example, if the response gave some very general information but we know the model has access to the internet, could we define criteria for a more explicit response?
    
    **AdinaiB-P7PPMRTF**
    
    var timestamp = "2025-02-12T16:00:49Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-3eafeed1-2916-4a12-9daf-67840684f7e0").appendChild(newParagraph);
    
    2/12/2025, 10:00 AM
    
-   @AlexC-WC3YCQ4T I would split those into 2 criteria, one explicit and one implicit. The explicit could be 'the response should include health benefits of carrots...'. The implicit could be 'the response should be an appropriate length. For example, it could list at least 3 but no more than 8 benefits.' Or words to that effect. That's been my approach so far.
    
    **Jessica**
    
    var timestamp = "2025-02-12T15:59:53Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-a0805ec7-1069-4198-b24e-8be1f864cb36").appendChild(newParagraph);
    
    2/12/2025, 09:59 AM
    
-   @britten, just go back to the selector where you chose 6 and change it to 5
    
    **Mindy**
    
    var timestamp = "2025-02-12T15:17:57Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-2c7829a5-158b-46f7-84a9-cf5fdf1cf45a").appendChild(newParagraph);
    
    2/12/2025, 09:17 AM
    
-   Is there any way to remove a criterion? I clicked "6" but realized that I only needed 5. I cannot submit the task without filling in all text fields, but I don't need 6 criteria!
    
    **Britten**
    
    var timestamp = "2025-02-12T15:13:43Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-1c8539fa-7353-4bb2-843a-3afa6b429a87").appendChild(newParagraph);
    
    2/12/2025, 09:13 AM
    
-   Quick question - if some info is requested in the prompt and I give a criterion which has a minimum number of points that need to be given in relation to this, is it considered explicit or implicit? For example, if the prompt asks 'please tell me the health benefits of the vegetable in this image' and my criterion is 'the response should include at least 3 health benefits of carrots, for example...' is this considered explicit or implicit? The user explicitly asks for the health benefits of carrots, but doesn't explicitly say that there should be at least 3. I'm going to split this into 2 criterion for the time being but I feel that I'm running the risk of my criteria being too similar/repetitive.
    
    **AlexC-WC3YCQ4T**
    
    var timestamp = "2025-02-12T14:02:43Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-288ec1bf-673e-4b82-a9d9-f2887a398849").appendChild(newParagraph);
    
    2/12/2025, 08:02 AM
    
-   @Susan, The model should provide self-contained responses (only use what's given in the prompt and the image), from what I understand anyhow. I haven't run into anything needing too specific information in the past couple of hours but I can't say it would be the same for all the tasks.
    
    **AlexandriaW-KPEFZTPD**
    
    var timestamp = "2025-02-12T08:20:24Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-f3e01a28-a0e0-4451-8029-f36cce4f74ff").appendChild(newParagraph);
    
    2/12/2025, 02:20 AM
    
-   @Susan, As far as I know, this model has internet access and can check information. You can probably assume it is up to date.
    
    **Christopher**
    
    var timestamp = "2025-02-12T05:06:50Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-913568ee-e1a8-4324-ba1c-d87053fb5310").appendChild(newParagraph);
    
    2/11/2025, 11:06 PM
    
-   Does the model have up to date information? I don't see this mentioned anywhere, in the instructions or the FAQ.
    
    **Susan**
    
    var timestamp = "2025-02-12T03:25:34Z" var localTimestamp = new Date(timestamp); // Check if the timestamp is valid var options = { year: 'numeric', month: 'numeric', day: 'numeric', hour: '2-digit', minute: '2-digit' }; var formattedTimestamp = localTimestamp.toLocaleDateString(undefined, options); // Create a new paragraph element var newParagraph = document.createElement("p"); newParagraph.textContent = formattedTimestamp; // Append the new paragraph to the output container document.getElementById("my-container-0c35759c-2f82-400f-a906-e0d110c529bd").appendChild(newParagraph);
    
    2/11/2025, 09:25 PM
    

.message\_text { min-width: 100% !important; }  
  

       

       

       

Expires in: 3 hours 58 minutes

     

[$16.17](https://app.dataannotation.tech/workers/payments)

      

***

[Code of Conduct](https://docs.google.com/document/d/e/2PACX-1vQRSbcK0ctnOVqPC58qNzxW3vssF4-oPNueAh4TStPTpj5rxNDYHbsZyEJOroP-0V7nB1PDQff4Sqzi/pub) [Support](https://app.dataannotation.tech/workers/support)

© 2025 DataAnnotation. All rights reserved.
