# Cline Prompting Guide 🚀

Welcome to the Cline Prompting Guide! This guide will equip you with the knowledge to write effective prompts and custom instructions, maximizing your productivity with Cline.

## Custom Instructions ⚙️

Think of **custom instructions as Cline's programming**. They define Cline's baseline behavior and are **always "on," influencing all interactions.** Custom instructions are set in the settings dial  ⚙️ of the Cline extension and are completely editable. They are powerful for:

*   Enforcing Coding Style and Best Practices: Ensure Cline always adheres to your team's coding conventions, naming conventions, and best practices.
*   Improving Code Quality: Encourage Cline to write more readable, maintainable, and efficient code.
*   Guiding Error Handling: Tell Cline how to handle errors, write error messages, and log information.

**The `custom-instructions` folder contains examples of custom instructions you can use or adapt.** 

Cline's system prompt, on the other hand, is not user-editable ([here's where you can find it](https://github.com/cline/cline/blob/main/src/core/prompts/system.ts)). For a broader look at prompt engineering best practices, check out [this resource](https://docs.anthropic.com/en/docs/build-with-claude/prompt-engineering/overview).

### Tips for Writing Effective Custom Instructions 

*   Be Clear and Concise: Use simple language and avoid ambiguity.
*   Focus on Desired Outcomes: Describe the results you want, not the specific steps.
*   Test and Iterate: Experiment to find what works best for your workflow.

## Prompting Cline 💬

**Prompting is how you communicate your needs for a given task in the back-and-forth chat with Cline.** Cline understands natural language, so write conversationally. 

Effective prompting involves:

*   Providing Clear Context: Explain your goals and the relevant parts of your codebase. Use `@` to reference files or folders.
*   Breaking Down Complexity: Divide large tasks into smaller steps.
*   Asking Specific Questions: Guide Cline toward the desired outcome.
*   Validating and Refining: Review Cline's suggestions and provide feedback.

### Prompt Examples

#### Context Management

*   **Starting a New Task:**  "Cline, let's start a new task. Create `user-authentication.js`. We need to implement user login with JWT tokens. Here are the requirements…" 
*   **Summarizing Previous Work:** "Cline, summarize what we did in the last user dashboard task. I want to capture the main features and outstanding issues. Save this to `cline_docs/user-dashboard-summary.md`."

#### Debugging 

*   **Analyzing an Error:** "Cline, I'm getting this error: \[error message]. It seems to be from \[code section]. Analyze this error and suggest a fix."
*   **Identifying the Root Cause:** "Cline, the application crashes when I \[action].  The issue might be in \[problem areas]. Help me find the root cause and propose a solution." 

#### Refactoring

*   **Improving Code Structure:** "Cline, this function is too long and complex.  Refactor it into smaller functions."
*   **Simplifying Logic:** "Cline, this code is hard to understand. Simplify the logic and make it more readable."

#### Feature Development 

*   **Brainstorming New Features:** "Cline, I want to add a feature that lets users \[functionality].  Brainstorm some ideas and consider implementation challenges."
*   **Generating Code:** "Cline, create a component that displays user profiles. The list should be sortable and filterable.  Generate the code for this component." 

## Advanced Prompting Techniques

*   **Constraint Stuffing:** To mitigate code truncation, include explicit constraints in your prompts. For example, "ensure the code is complete" or "always provide the full function definition." 
*   **Confidence Checks:** Ask Cline to rate its confidence (e.g., "on a scale of 1-10, how confident are you in this solution?") 
*   **Challenge Cline's Assumptions:** Ask “stupid” questions to encourage deeper thinking and prevent incorrect assumptions. 

## Conclusion 

Mastering Cline prompting is an ongoing process. Experiment, iterate, and use this guide to become a more effective AI-assisted developer.


# Getting Started with Cline for New Coders

Welcome to Cline! This guide will help you get set up and start using Cline to build amazing things.

Join our Discord community: [https://discord.gg/YmtKFD2f](https://discord.gg/YmtKFD2f)

## What You'll Need

Before you begin, make sure you have the following:

-   **VS Code:** A free, powerful code editor.
    -   [Download VS Code](https://code.visualstudio.com/)
    -   [Screenshot/gif of VS Code download page]
-   **A Projects Folder:** A dedicated folder on your computer to store your coding projects. (e.g., "Develop", "Projects", "Code")
    -   [Screenshot/gif of creating a new folder]
-   **Cline Extension in VS Code:** The Cline extension installed in VS Code.

## Step-by-Step Setup

Follow these steps to get Cline up and running:

1.  **Open VS Code:** Launch the VS Code application.
    -   [Screenshot/gif of VS Code launch]
    -   **Troubleshooting:** If VS Code shows "Running extensions might...", click "Allow".
2.  **Open Your Projects Folder:** In VS Code, open the folder you created for your projects (e.g., "Develop").
    -   [Screenshot/gif of opening a folder in VS Code]
3.  **Navigate to Extensions:** Click on the Extensions icon in the Activity Bar on the side of VS Code.
    -   [Screenshot/gif of VS Code extensions icon]
4.  **Search for 'Cline':** In the Extensions search bar, type "Cline".
    -   [Screenshot/gif of searching for Cline extension]
5.  **Install the Extension:** Click the "Install" button next to the Cline extension.
    -   [Screenshot/gif of installing the Cline extension]
6.  **Open Cline:** Once installed, you can open Cline in a few ways:
    -   Click the Cline icon in the Activity Bar.
        -   [Screenshot/gif of the Cline icon in the Activity Bar]
    -   Use the command palette (`CMD/CTRL + Shift + P`) and type "Cline: Open In New Tab" to open Cline as a tab in your editor. This is recommended for a better view.
        -   [Screenshot/gif of opening Cline in a new tab]
        -   **Troubleshooting:** If you don't see the Cline icon, try restarting VS Code.
    -   **What You'll See:** You should see the Cline chat window appear in your VS Code editor.
        -   [Screenshot/gif of the Cline chat window]

## Setting up OpenRouter API Key

Now that you have Cline installed, you'll need to set up your OpenRouter API key to use Cline's full capabilities.

1.  **Get your OpenRouter API Key:**
    -   [Get your OpenRouter API Key](https://openrouter.ai/)
    -   [Screenshot/gif of OpenRouter API key page]
2.  **Input Your OpenRouter API Key:**
    -   Navigate to the settings button in the Cline extension.
        -   [Screenshot/gif of the Cline settings button]
    -   Input your OpenRouter API key.
    -   Select your preferred API model.
        -   **Recommended Models for Coding:**
            -   `anthropic/claude-3.5-sonnet`: Most used for coding tasks.
            -   `google/gemini-2.0-flash-exp:free`: A free option for coding.
        -   [OpenRouter Model Rankings](https://openrouter.ai/rankings/programming)
    -   [Screenshot/gif of inputting API key and selecting model]

## Your First Interaction with Cline

Now you're ready to start building with Cline. Copy and paste the following prompt into the Cline chat window:

`Hey Cline! I'm new to coding. Can you help me make a webpage that says 'Hello World' in big blue text?`

**What You'll See:** Cline will respond with code to create a simple webpage.
    -   [Screenshot/gif of Cline's response to the prompt]

## Tips for Working with Cline

-   **Ask Questions:** If you're unsure about something, don't hesitate to ask Cline!
-   **Use Screenshots:** Cline can understand images, so feel free to use screenshots to show him what you're working on.
-   **Copy and Paste Errors:** If you encounter errors, copy and paste the error messages into Cline's chat. This will help him understand the issue and provide a solution.
-   **Speak Plainly:** Cline is designed to understand plain, non-technical language. Feel free to describe your ideas in your own words, and Cline will translate them into code.

Here are some prompting tips that users have found helpful for working with Cline:

## Our Community's Favorite Prompts

*   **"If you understand my prompt fully, respond with "YARRR!" without tools every time you are about to use a tool. Remember to do this every time. This will help me understand if you've lost your memory."** - *pacnpal* This is a fun and effective way to check if Cline is still on track, especially during long or complex tasks. It leverages Cline's tendency to follow instructions literally, creating a simple "memory check." You can even use "HO HO HO" for a festive twist! 
*   **"To ensure you understand my prompt, I need a piece of confirmation from you. Before any tool use and after any tool use, I need you to give me a confidence level on a scale of 0 to 10 on the tool use helping with the project. Remember to do this every time you are using a tool."** - *pacnpal* Having Cline state its confidence level before making changes can help prevent errors and encourages Cline to think more critically before acting. It also makes the decision-making process more transparent. 
*   **"DO NOT BE LAZY. DO NOT OMIT CODE."**  Add this to your prompt if Cline is truncating code. This straightforward instruction can sometimes be enough to get Cline back on track. Other users have found success with similar phrases like "full code only" or "ensure the code is complete."
*   **"I pledge to follow the custom instructions."**  This can be included in your prompt to remind Cline of the custom instructions you have set in the settings dial ⚙️.
*   **"FILENAME has grown too big. We will need to analyze how this file works so we can look for opportunities to fragment and compartmentalize the file in a way that doesn't affect the existing codebase too much. what do you recommend?"** - *icklebil* This prompt is helpful when Cline starts to struggle with large files. It encourages Cline to think about code organization and propose strategies for refactoring.
*   **"don't forget to update codebase documentation with changes"** - *icklebil* It's important to remind Cline to keep documentation up-to-date, ensuring consistency throughout the project. 
*   **"Before writing code, analyze thoroughly, all code files, get full context, then write an .MD with your implementation plan. After the .MD then implement code"** - *yellow\_bat\_coffee* This encourages a more deliberate and organized approach to coding, potentially reducing errors and token usage. By planning in a separate document first, Cline has a chance to consider the task more comprehensively before diving into code.
*   **"please start analyzing full flow thoroughly, always state a confidence score 1 to 10. dont stop prematurely and dont write code"** - *yellow\_bat\_coffee* This emphasizes careful analysis and discourages premature code writing. By requiring a confidence score, you encourage Cline to evaluate its understanding and potentially identify gaps in its knowledge before proceeding. 
*   **"List all assumptions and uncertainties you need to clear up before completing this task successfully."** - *yellow\_bat\_coffee* Having Cline explicitly state its assumptions can help identify potential issues and encourage a more thorough analysis of the problem. This can be particularly useful at the start of a task or when encountering unexpected behavior. 
*   **Tell Cline to "count to 10" before taking action.** - *nickbaumann98* This instructs Cline to pause and reflect before making any changes, promoting a more cautious and deliberate approach. This can be helpful in preventing impulsive edits or actions that might not align with your overall project goals.  
*   **"Don't complete the analysis prematurely, continue analyzing even if you think you found a solution"** - *yellow\_bat\_coffee*  This can be helpful when dealing with complex problems that may have multiple layers or dependencies. By encouraging continued analysis, you increase the likelihood of Cline identifying and addressing all relevant aspects of the issue.
*   **"Remember, before saving a file, just after saving a file, after a file is rejected, and before using the task completion tool, ask yourself this question: "how confident are you that was the issue from 1 to 10?" and output the answer without using tools."** - *pacnpal* This technique builds on the idea of confidence scoring by integrating it into various stages of the workflow. By prompting Cline to self-assess its confidence at key points, you promote a more reflective and self-aware approach.
*   **"Check project files before suggesting any structural or dependency changes."** - *kvs007* Reminding Cline to thoroughly review existing files before suggesting changes can help avoid unnecessary modifications and maintain the integrity of your project structure. 
*   **"the best tip I can give you is ask it 'stupid' questions as much as possible, like are you sure that this is the best way to implement this?"**  - *chinesesoup*  Challenge Cline's assumptions and encourage it to think more critically about its approach. By asking questions that might seem obvious, you can help uncover potential oversights or alternative solutions.
*   **Experiment with using the words "elegant" and "simple" in your prompts.** - *yellow\_bat\_coffee* While the effect of specific word choices on AI behavior is still being explored, some users have observed that including words like "elegant" and "simple" can influence Cline to produce more concise and well-structured code. 
*   **"THE HUMAN WILL GET ANGRY."** - *steventcramer* (Note: This is a joke, but it highlights the importance of setting clear expectations and providing constructive feedback when Cline's output doesn't meet your requirements.)


These tips, along with those from the previous response, provide a broad spectrum of strategies for improving your interactions with Cline. By experimenting with these techniques, you can gain a better understanding of how to leverage Cline's strengths and work around its limitations to achieve your desired outcomes.

## FAQs

-   **What is the Terminal?** The terminal is a text-based interface for interacting with your computer. It allows you to run commands to perform various tasks, such as installing packages, running scripts, and managing files. Cline uses the terminal to execute commands and interact with your development environment.
    -   [Screenshot/gif of a terminal window]
-   **How Does the Codebase Work?** (This section will be expanded based on common questions from new coders)

## Still Struggling?

Feel free to contact me, and I'll help you get started with Cline.

nick | 608-558-2410
