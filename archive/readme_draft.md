# Prompting llms to build software applications

## Getting Started

Before diving into development, it's crucial to:
1. Clearly define your application concept
2. Map out core functionality
3. Plan the user experience (UX)
4. List and prioritize key features

This can be supported by the following LLM prompt: "Help me define and and spec out a {insert language i.e. Python} based application using {insert framework i.e. Streamlit}, the objective is to create a plan that we can then use with a llm-assisted coding agent/IDE that will create the files and code based on the prompts that we give it. Therefore it will be crucial for us to clearly define the application concept, map out core functionality, plan the UX, list key features and identify python libraries and other shortcuts we can use to deliver the app. This app should {describe key features}{define data inputs}{define user stories}"

Typically the above prompt will direct the llm to generate a boilerplate plan for your app idea that you can edit and refine per your requirements.

## Creating the development prompts

Once you have a plan for your app, the next step is to create the actual development prompts that will be used to guide the llm-assisted coding agent/IDE to build the app piece by piece. We can't provide the plan in its entirety to the LLM as this will increase the likelihood of the llm generating erroneous code as we risk overloading its context window with too many requests. Instead we can ask the LLM break the app down into smaller pieces and generate prompts for each piece of the app. This will ensure the llm can focus on generating code for each piece of the app and not get caught up in the entire app at once. 

We can do this using a prompt like this: 
```
"I have a plan for a streamlit app here: @plan.md I have already built out the project scaffolding described here: @README.md, now based on the plan within plan.md can you write out a series of prompts that will be used to instruct Cascade to build each part of the app within the aforementioned plan. Write all of the prompts to a new markdown file. Each prompt should if neccessary include:

        Feature implementation details,
        Error handling and logging specifics,
        Documentation of ALL errors and fixes in CHANGELOG.md,
        The updating of BUGS.md with all issues and warnings,
        Verification all directories and files exist,
        The updating of README.md to reflect current project state including successfully implemented features,
        Testing procedures,
        Project Context: (e.g.'You are assisting with development on {project_name}, a {project_description}. Before proceeding, analyze the following documentation to understand the project: README Location: {readme_path} CHANGELOG Location: {changelog_path} BUGS Location: {bugs_path},
        Development Guidelines: Code Preservation, Maintain existing UI layout and styling exactly as is, Do not modify working code unless specifically required, Preserve all existing functionality, Keep current component structure intact
        Feature Implementation: Add only features explicitly requested, Implement changes incrementally, one at a time"
```
As mentioned above, this will direct the llm to produce a file containing prompts for each phase of the development process. The idea being that you implement each feature one step at at time, fixing errors, logging bugs and updating documentation as you go. All of this additional project metadata is vital for keeping llm 'on course' as you make further changes to the app, and will help the llm avoid making irrelevant code changes, deleting features, and so on.

## Putting it all together: Example workflow

You should now have a plan for the app and a list of development prompts to instruct an llm to build it step by step.

The prompts should roughly follow this structure:
```
You are assisting with development on the Report Insights App, a Streamlit-based application for analyzing ad server reports and surfacing key insights. Before proceeding, analyze the following documentation:

README Location: @README.md 
CHANGELOG Location: @CHANGELOG.md 
BUGS Location: @BUGS.md
Streamlit Docs Location: @docs/streamlit-docs 

## Development Guidelines
- Code Preservation: Maintain existing functionality
- UI Consistency: Maintain existing UI layout and styling
- Incremental Development: Implement one feature at a time
- Include error handling/logging
- Documentation: Update all relevant documentation files
- Testing: Include appropriate test procedures

Implement the basic file upload functionality for the Report Insights App:
1. Create a file uploader component that accepts XLSX and CSV files
2. Add file format validation with user-friendly error messages
3. Implement basic data preview functionality

Requirements:
- Use st.file_uploader with appropriate file type restrictions
- Display uploaded file details (name, size, type)
- Show first 5 rows of data in a table format
- Handle and display appropriate error messages for invalid files

Testing:
- Test with valid XLSX and CSV files
- Test with invalid file formats
- Verify error message display
```

Subsequent development prompts:
```
- Well done, good work. Now: - Update README.md with new functionality and project file structure
- Document any issues in BUGS.md
- Update CHANGELOG.md with new features
```
## Tips:

I've found that defining the frameworks and libraries you are going to use early on helps the llm to develop less error-prone code. I would strongly recommend using tools like: jina.ai, firecrawl.dev and llms.txt to assemble the necessary docummentation for your project in a format that is llm-friendly.

I recommend amending your documentation prompts to direct the llm to include project information such as file/folder structure, key component details, and any other relevant information that will be useful to the llm during development in either the readme, bugs, or changelog files, then using these files as context for subsequent development prompts, this can help speed up development and reduce the chance of the llm deleting relevant code.
