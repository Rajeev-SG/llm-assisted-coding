# 🤖 LLM-Assisted Software Development Guide

> A systematic approach to building software applications with AI assistance

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📚 Table of Contents
- [Getting Started](#getting-started)
- [Development Process](#development-process)
- [Best Practices](#best-practices)
- [Documentation Strategy](#documentation-strategy)
- [Tips & Troubleshooting](#tips--troubleshooting)
- [Coming Soon](#coming-soon)

## Getting Started

Before diving into development, it's crucial to:
1. Clearly define your application concept
2. Map out core functionality
3. Plan the user experience (UX)
4. List and prioritize key features

### Initial Planning Prompt
Use this template to kickstart your project:
```markdown
Help me define and spec out a {insert language i.e. Python} based application using {insert framework i.e. Streamlit}.

Objective: Create a plan that we can use with an LLM-assisted coding agent/IDE to generate code based on our prompts.

Please include:
1. Application concept and core functionality
2. UX/UI requirements and user flow
3. Key features and priority order
4. Required libraries and technical stack
5. Data inputs and user stories
```

This prompt will generate a boilerplate plan that you can refine according to your specific requirements.

## Development Process

The LLM-assisted development process follows these key steps:
1. Plan application and define requirements
2. Generate focused development prompts
3. Implement features incrementally
4. Update documentation after each change
5. Use documentation as context for next steps

### 1. Creating Development Prompts
Use this template to generate focused development prompts:
```markdown
"I have a plan for a {framework} app here: @plan.md
Project scaffolding is described in: @README.md

Please write prompts to build each part of the app, ensure each prompt includes:

1. Implementation Requirements:
   - Feature specifications
   - Error handling approach
   - Testing procedures
   - Documentation updates

2. Project Context:
   - Project: {project_name}
   - Description: {project_description}
   - Documentation Paths:
     README: {readme_path}
     CHANGELOG: {changelog_path}
     BUGS: {bugs_path}

3. Development Guidelines:
   - Preserve existing functionality
   - Maintain UI/UX consistency
   - Implement features incrementally
   - Update documentation continuously"
```

### 2. Implementation Example
Here's a structured prompt for implementing specific features:
```markdown
Project Context:
You are assisting with the Report Insights App, a Streamlit-based application for analyzing ad server reports.

Documentation References:
- README: @README.md 
- CHANGELOG: @CHANGELOG.md 
- BUGS: @BUGS.md
- Framework Docs: @docs/streamlit-docs 

Development Guidelines:
- Preserve existing functionality
- Maintain consistent UI/UX
- Implement features incrementally
- Include comprehensive error handling
- Update documentation after each change
- Add appropriate tests

Feature Implementation:
Implement file upload functionality:
1. Create file uploader (XLSX/CSV support)
2. Add format validation
3. Implement data preview

Technical Requirements:
- Use st.file_uploader with type restrictions
- Show file metadata (name, size, type)
- Display first 5 rows of data
- Handle invalid files gracefully

Testing Requirements:
- Valid XLSX/CSV files
- Invalid file formats
- Error message verification
```

### 3. Documentation Updates
After each feature implementation:
```markdown
1. Update README.md with:
   - New functionality
   - Updated project structure
   - Usage instructions

2. Document in BUGS.md:
   - Known issues
   - Workarounds
   - Future improvements

3. Update CHANGELOG.md:
   - Feature additions
   - Bug fixes
   - Breaking changes
```

## Best Practices

### 1. Context Management
- Define frameworks and libraries upfront
- Keep prompts focused and specific
- Use documentation references instead of copying code
- Break complex features into smaller tasks

### 2. Documentation Strategy
- Maintain comprehensive documentation
- Update docs after each feature implementation
- Include project structure and dependencies
- Document known issues and solutions

### 3. Error Prevention
- Validate LLM outputs against requirements
- Test incrementally
- Keep context window focused
- Use clear, specific prompts

## Tips & Troubleshooting

### Recommended Tools
- [jina.ai](https://jina.ai) - Convert a single URL to an LLM-friendly input (useful for single documentation pages)
- [firecrawl.dev](https://firecrawl.dev) - Crawl multiple URLs and convert page content to LLM-friendly input (useful for multiple documentation pages)
- [llms.txt](https://llmstxt.org/) - A standardised way to provide website information to LLMs, similar to robots.txt for search engines (provide another useful source of LLM-friendly documentation
### Common Issues
1. **Context Overflow**
   - Break down prompts into smaller chunks
   - Reference documentation instead of copying

2. **Inconsistent Output**
   - Provide more specific requirements
   - Include example patterns
   - Use incremental development

3. **Feature Regression**
   - Maintain clear documentation
   - Use documentation as context
   - Implement changes incrementally

## Coming Soon

- Unit testing
- Version control

📝 **Pro Tip**: Always include project structure, component details, and other relevant information in your documentation files. Use these as context for subsequent development prompts to maintain consistency and prevent unintended code changes.

## License
This project is licensed under the MIT License - see the [LICENSE](https://opensource.org/license/MIT) file for details.
