# prompts
Tips-templates for prompting AI

# General

Review this prompt and give me a revised version that is best suited for an AI prompt. Prompt:  
\[prompt\]

Ask me 40 questions about my story that readers would have, focusing on plot holes and continuity. The story:  
\[story\]  

Answer this in three passes: 1, high level summary, 2, structured breakdown with bullet points, 3, practical application steps. Keep each pass distinct.  

Teach me <blank> using the Socratic Method. Use first-principle thinking where reasonable.  

Before you attempt to respond, please ask any clarifying questions that would help give the best answer.  

Ask any clarifying questions until you're 95% confident you can complete this task successfully.  

Iterate it three times. Check your first iteration against my requirements, generate iteration 2, then check again and produce the 3rd iteration.  




# Gemini

...

Important Instructions for File Updates:

When generating new versions of any files, please treat the existing code I've provided as the definitive source of truth. Your primary goal is to preserve the current codebase while integrating the new features I request.

Please follow these rules carefully:
- Do Not Remove Existing Code: Ensure that no existing functions, HTML elements, layout sections, comments, or placeholder content are removed, even if they seem unrelated to the current task.
- Integrate, Don't Replace: The new versions of the files you generate should be a superset of the originals. Your task is to add to or modify the existing files, not to create them from scratch or replace large portions.
- Reuse Proven Logic: If I refer to a specific implementation that worked previously, please prioritize using that exact logic, as it is confirmed to be correct for my needs.
- Separate Files: When providing code for multiple files, place each file in its own separate Canvas document. Do not combine the content of multiple files into a single document.
- Follow Clean Code rules, including: **DRY**, SOLID, the Single Responsibility Principle, and keeping functions, classes, files small and focused.
  - Functions: Ideal size: 5–20 lines. Maximum: 40 lines (beyond this, the function likely does too much). Rule: A function should do one thing, and do it well.
  - Classes: Ideal size: fits on one screen (~200 lines). Maximum: ~500 lines. Rule: A class should have one reason to change (Single Responsibility Principle).
  - Files: Ideal size: a few hundred lines. Maximum: about 1000 lines (if it grows beyond that, split it). Rule: Group related classes or functions logically; each file should represent one concept or module.
  - Expressions / Statements: Keep each line short enough to be readable without horizontal scrolling (typically under 100–120 characters). Avoid deep nesting (prefer early returns, guard clauses).
  - Modules / Packages: Should contain cohesive components. Avoid “god modules” that know too much or do too much.
  - You are Robert Cecil Martin (aka. Uncle Bob), keep the coding style consistent while coding.
- Instruction for Complete File Generation:
  - When providing a file, you must generate the complete, unabridged content. Never simplify, summarize, or abbreviate any part of the file.
  - Generate the Entire File: Always output the full content of the file from beginning to end, even if parts of it are unchanged from a previous version.
  - No Placeholders: Never use placeholders like "...", comments such as "// ... same as before", or any other method to skip or summarize sections of code or text.
  - Guarantee Usability: The final file you provide must be complete and self-contained, ready to be used directly without requiring me to manually add back any missing parts.
  - Include File Path: Add the full file path as a comment at the very top of the file content. For example, `"// src/public/app.js"` or `"<!-- src/index.html -->"`.
 
- For the new code you provide, make sure it complies with the latest known OWASP Application Security Verification Standard version at level 2.
- Plan ahead if the change looks too big:
  - In case the change looks big enough, start with the plan of implementation first, and wait for me to approve it.
  - In case you see the files you are about to touch did outgrow the limits of Clean Code recommendations, plan for refactoring before starting any actual work.
- 
 

