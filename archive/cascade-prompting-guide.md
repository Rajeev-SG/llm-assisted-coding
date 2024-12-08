# Rapid LLM-Assisted Software Development with Cascade: A Workflow Guide

*Learn how to accelerate your software development process using prompt templates and the Cascade LLM-assisted coding agent, with a comprehensive and optimized workflow. Cascade is a llm-assisted coding agent that can read/write code/other text files, create files, suggest terminal commands and edit code. Cascade can also look at files and directories by including statements like this: @[directory/filename.md]*

---

## Introduction

The advent of Large Language Models (LLMs) has revolutionized software development, enabling rapid prototyping and efficient coding practices. Cascade, an LLM-assisted coding agent, takes this a step further by allowing developers to interact with their codebase through natural language prompts. This guide provides a scrutinized and improved workflow for leveraging Cascade in your software development process, ensuring optimal productivity and code quality.

---

## Workflow Overview

The optimized workflow consists of the following steps:

1. [Idea Exploration and Planning](#1-idea-exploration-and-planning)
2. [Compiling Discussion into Markdown](#2-compiling-discussion-into-markdown)
3. [Generating the Promptfile with Cascade](#3-generating-the-promptfile-with-cascade)
4. [Executing Initial Development Prompts](#4-executing-initial-development-prompts)
5. [Iterative Development and Testing](#5-iterative-development-and-testing)
6. [Documentation and Change Management](#6-documentation-and-change-management)
7. [Effective Context Management](#7-effective-context-management)
8. [Adding Components with Refined Prompts](#8-adding-components-with-refined-prompts)
9. [Continuous Scrutiny and Instruction Adherence](#9-continuous-scrutiny-and-instruction-adherence)
10. [Live Testing and Deployment](#10-live-testing-and-deployment)
11. [Cascade Prompt Template Example](#11-cascade-prompt-template-example)

---

## 1. Idea Exploration and Planning

**Objective:** Define and refine your application idea, functionality, user experience (UX), and key features.

### Actions:

- **Brainstorm with an LLM:** Use a conversational LLM like Claude to discuss your app idea.
- **Scrutinize and Optimize:** Critically evaluate the idea for feasibility and potential improvements.
- **Plan:** Outline the application's core features, user flow, and technical requirements.

### Considerations:

- **Clarity:** Ensure your idea is well-defined and achievable.
- **User-Centered Design:** Focus on the UX to provide value to your end-users.
- **Technical Feasibility:** Assess whether the technology stack and resources are appropriate.

---

## 2. Compiling Discussion into Markdown

**Objective:** Consolidate your brainstorming session into a markdown file for future reference and LLM consumption.

### Actions:

- **Request Compilation:** Ask the LLM to compile the key points of your discussion into a single markdown file.
- **Organize Content:** Structure the document with clear headings, bullet points, and sections.

### Considerations:

- **Comprehensiveness:** Include all relevant details that will inform the development process.
- **Reusability:** Save this file for later use in generating prompts and providing context to Cascade.

---

## 3. Generating the Promptfile with Cascade

**Objective:** Create a comprehensive set of development prompts (the "promptfile") covering the entire development lifecycle.

### Actions:

- **Input the Discussion Outcome:** Provide the compiled markdown file to Cascade.
- **Use the Cascade Prompt Template:** Utilize the following prompt to guide Cascade in generating the promptfile:

    > I want to build the app discussed in @{markdown file from step 2} that {briefly mention key features}. Please create a comprehensive set of development prompts in a markdown file, the 'promptfile', that covers the entire development lifecycle. The prompts should follow the structure from @{[LLM Prompt Templates for Rapid Prototyping](llm-prompt-templates-for-rapid-prototyping.md)} and include:

    > [Include Core Features, Technical Requirements, Implementation Phases, and Project Structure as specified in the Cascade prompt.] ... See complete example in section 11.

- **Customize Placeholders:** Replace `{app idea}`, `{key features}`, `{feature 1}`, etc., with your specific details.

### Considerations:

- **Specificity:** Be as detailed as possible to ensure Cascade generates accurate and useful prompts.
- **Alignment:** Ensure the prompts align with your development goals and standards.

---

## 4. Executing Initial Development Prompts

**Objective:** Begin the development process by executing the first prompt from the promptfile.

### Actions:

- **Run the First Prompt:** Provide the initial prompt to Cascade.
- **Review Output:** Carefully examine the code and suggestions generated.

### Considerations:

- **Accuracy:** Verify that the output meets the requirements specified in the prompt.
- **Quality Standards:** Ensure code adheres to best practices and coding standards.
- **Understanding:** Make sure you understand the generated code for effective implementation and future maintenance.

---

## 5. Iterative Development and Testing

**Objective:** Develop and refine your application through continuous testing and debugging.

### Actions:

- **Implement Code:** Integrate the generated code into your project.
- **Test Functionality:** Regularly test each feature to identify and address bugs.
- **Log Issues:** Document any bugs or issues encountered in `BUGS.md`.

### Considerations:

- **Debugging:** Utilize Cascade to assist in debugging by providing context from error logs.
- **Performance:** Monitor application performance and make optimizations as needed.
- **Feedback Loop:** Continuously provide feedback to Cascade to improve future outputs.

---

## 6. Documentation and Change Management

**Objective:** Maintain accurate and up-to-date documentation throughout the development process.

### Actions:

- **Update `README.md`:** Include project overview, installation instructions, development setup, and contributing guidelines.
- **Maintain `CHANGELOG.md`:** Document all features, updates, bug fixes, and changes.
- **Record in `BUGS.md`:** Keep a detailed log of all issues, warnings, and their resolutions.

### Considerations:

- **Consistency:** Ensure documentation is updated alongside code changes.
- **Transparency:** Provide clear and detailed explanations for changes to assist future development.
- **Accessibility:** Organize documentation for easy reference by all team members.

---

## 7. Effective Context Management

**Objective:** Manage Cascade's context window to prevent overload and maintain efficiency.

### Actions:

- **Start New Sessions:** Begin new Cascade sessions when necessary to keep context manageable.
- **Provide Essential Context:** Ensure Cascade has access to relevant `BUGS.md`, `README.md`, and `CHANGELOG.md` files in new sessions by referencing them (e.g., `@[directory/filename.md]`).

### Considerations:

- **Context Limitations:** Be mindful of the LLM's context window limits to avoid losing important information.
- **Efficient Communication:** Provide concise and relevant context to Cascade to maintain performance.

---

## 8. Adding Components with Refined Prompts

**Objective:** Enhance your application by adding new components and features using improved prompts.

### Actions:

- **Tweak Prompts:** Adjust prompts based on previous feedback and outcomes to improve the quality of Cascade's outputs.
- **Execute New Prompts:** Provide the refined prompts to Cascade to generate code for additional components.
- **Integrate Components:** Carefully integrate new components, ensuring compatibility with existing code.

### Considerations:

- **Incremental Development:** Add features in manageable increments to simplify testing and integration.
- **Prompt Clarity:** Ensure prompts are clear and specific to guide Cascade effectively.
- **Review and Test:** Scrutinize generated code and test thoroughly before moving on.

---

## 9. Continuous Scrutiny and Instruction Adherence

MUST EXPAND HERE RE RECENT ISSUES: AGENT DELETES STUFF, MAKES STUFF YOU DIDNT ASK FOR, DELETING SWATHES OF README?, DELETING UI ELEMENTS - SUMMARISE ISSUES FROM PREVIOUS 2 COMMITS AND INCLUDE HERE

**Objective:** Ensure all instructions are accurately followed and maintain the project's direction.

### Actions:

- **Review Outputs:** Regularly check Cascade's outputs against your instructions and project requirements.
- **Provide Feedback:** Communicate any discrepancies or deviations to Cascade for correction.
- **Update Promptfile:** Incorporate feedback and improvements into the original promptfile for future reference.

### Considerations:

- **Quality Control:** Implement a review process to maintain high code quality.
- **Documentation:** Keep detailed records of feedback and changes for accountability and learning.
- **Alignment:** Keep the development aligned with the project's goals and standards.

---

## 10. Live Testing and Deployment

**Objective:** Test the application in a live environment and prepare for deployment.

### Actions:

- **Conduct Live Testing:** Test the application in a production-like environment to identify any remaining issues.
- **Optimize Performance:** Make necessary optimizations based on testing results.
- **Prepare for Deployment:** Finalize documentation, deployment scripts, and ensure all features are ready.

### Considerations:

- **User Experience:** Evaluate the application's performance from an end-user perspective.
- **Scalability:** Ensure the application can handle expected user load.
- **Post-Deployment Monitoring:** Plan for ongoing monitoring and maintenance after deployment.

---

## 11. Cascade Prompt Template Example

> I want to build the app discussed in @{markdown file from step 2} that {briefly mention key features}. Please create a comprehensive set of development prompts in a markdown file, the 'promptfile', that covers the entire development lifecycle. The prompts should follow the structure from @{[LLM Prompt Templates for Rapid Prototyping](llm-prompt-templates-for-rapid-prototyping.md)} and include:

>Core Features:
>1. Beautiful, modern UI with unobtrusive guidance system

>Technical Requirements:

>3. Implement comprehensive error logging and handling
>4. Maintain detailed CHANGELOG.md for all features and updates
>5. Include beautiful, responsive design
>6. Ensure frictionless UX with minimal latency

>For each implementation phase, include:
>1. Specific error handling and logging requirements
>2. CHANGELOG.md update instructions
>3. Documentation requirements
>4. Performance considerations
>5. Testing requirements

>Project Structure:
>1. Include detailed README.md with:
>   - Project overview
>   - Installation instructions
>   - Development server setup
>   - Contributing guidelines
>2. Organize prompts into sequential development phases
>3. Include project directory structure
>4. Specify error logging infrastructure

>The prompts should cover:
>1. Initial setup and architecture
>2. {feature 1}
>3. {feature 2}
>4. {feature 3}
>5. Testing and optimization
>6. Documentation and deployment

>Each prompt should explicitly require:
>1. Feature implementation details
>2. Error handling and logging specifics
>3. Documentation of ALL errors and fixes in CHANGELOG.md
>4. The updating of BUGS.md with all issues and warnings
>5. Verification all directories and files exist
>6. The updating of README.md to reflect current project state including successfully implemented features
>7. Testing procedures
>8. Project Context: (e.g.'You are assisting with development on {project_name}, a {project_description}. Before proceeding, analyze the following documentation to understand the project:
>README Location: {readme_path}
>CHANGELOG Location: {changelog_path}
>BUGS Location: {bugs_path}
>9. Development Guidelines: Code Preservation, Maintain existing UI layout and styling exactly as is, Do not modify working code unless specifically required, Preserve all existing functionality, Keep current component structure intact
>10. Feature Implementation: Add only features explicitly requested, Implement changes incrementally, one at a time

## Additional Improvements and Considerations

### Error Handling and Logging

- **Implement Early:** Integrate comprehensive error logging and handling from the beginning.
- **Standardization:** Use consistent error handling practices across the application.
- **Monitoring:** Set up tools to monitor logs and alert you to critical issues.

### Performance Optimization

- **Minimize Latency:** Aim for a frictionless UX with minimal response times.
- **Responsive Design:** Ensure the UI is responsive and adapts to different devices and screen sizes.
- **Resource Management:** Optimize resource usage to improve performance.

### Development Best Practices

- **Version Control:** Use a system like Git to track changes and collaborate.
- **Code Reviews:** Regularly review code to maintain quality and share knowledge.
- **Automated Testing:** Set up automated tests to catch issues early.

### Effective Communication with Cascade

- **Specificity in Prompts:** The more specific your prompts, the better Cascade can assist.
- **Context Awareness:** Provide necessary context to Cascade to improve output relevance.
- **Feedback Loop:** Continuously refine your communication with Cascade for better results.

---

## Conclusion

By following this optimized workflow, you can leverage the power of Cascade and LLMs to accelerate your software development process. Continuous scrutiny, effective context management, and adherence to best practices are crucial for maximizing productivity and achieving high-quality outcomes. Embrace this workflow to enhance your development capabilities and bring your application ideas to life efficiently.

---

*Happy coding!*