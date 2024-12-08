# LLM Prompt Templates for Rapid Software Prototyping

This guide provides a series of prompt templates designed to help developers rapidly prototype software applications using LLM-assisted coding agents. These templates follow a systematic approach from idea conception to working prototype, incorporating best practices for documentation, testing, and error handling. These templates are starting points. Adapt them to your specific needs. Use the templates to create as many prompts as needed. The main goal is to enable the software application to be built stage by stage to ensure each feature works correctly whilst maintaining a balance between rapid development and code quality through consistent documentation, automated testing and continuous refinement.

## How to Use These Templates

1. Replace text in {curly braces} with your specific details
2. When referencing files/directories, use @{path/to/file} syntax
3. Follow the templates in sequence for best results
4. Iterate through the process as needed, using the feedback loops described
5. Use the templates to create as many prompts as needed to build the software
6. Include brief instructions on how to build the software (deploy locally)

## Tips for Success

1. **Template Customization**
   - Adapt templates to your specific needs
   - Add project-specific sections
   - Remove irrelevant parts
   - Keep templates updated with lessons learned

2. **Effective Communication**
   - Be specific in your requests
   - Provide context and references
   - Ask for clarification when needed
   - Document decisions and rationales

3. **Quality Maintenance**
   - Regular code reviews
   - Continuous testing
   - Documentation updates
   - Performance monitoring

4. **Feedback Integration**
   - Collect user feedback early
   - Document issues and solutions
   - Update templates based on experience
   - Share learning with team members

## 1. Initial Idea Validation Template

```
I have an idea for {product_type}: {product_name}. Core features include:
{feature_1}
{feature_2}
{feature_3}

Please evaluate this idea considering:
1. Market viability and unique value proposition
2. Technical feasibility for MVP development
3. Potential challenges and limitations
4. Suggested additional features or modifications
5. High-level steps required for prototype development
```

## 2. Technical Architecture Planning Template

```
For the {product_name} MVP, I need guidance on technology selection and architecture.

Current technical assumptions:
- Frontend: {frontend_technology}
- Backend: {backend_technology}
- Key APIs/Services: {apis_or_services}
- Infrastructure: {infrastructure_choices}

Please provide:
1. Validation or alternatives for technology choices
2. Required third-party services and APIs
3. Development environment setup
4. Initial project structure
5. Core technical components and their interactions
```

## 3. MVP Feature Specification Template

```
For {product_name}, I need to define the MVP feature set and implementation approach.

Core user flow:
{describe_main_user_journey}

For each feature, please specify:
1. Technical implementation details
2. Required APIs/libraries
3. Data models and storage requirements
4. User interface components
5. Testing requirements
```

## 4. Development Process Template

```
Project: {product_name}
Current Stage: {development_stage}
Reference Files: @{path/to/relevant/files}

Please help with:
1. Creating/updating project documentation
2. Implementing automated tests
3. Setting up error logging
4. Code review and optimization
5. Integration testing
```

## 5. Prototype Deployment Template

```
For {product_name}, I need to deploy a testable prototype:

Environment:
- Target Platform: {mobile/web/desktop}
- Development Approach: {native/cross-platform/hybrid}
- Testing Platform: {testing_environment}
- Device Requirements: {specific_hardware_requirements}

Please provide:
1. Development environment setup instructions
2. Build and deployment process
3. Testing environment configuration
4. Hardware access requirements (camera, sensors, etc.)
5. Performance optimization guidelines
```

### Mobile-Specific Deployment Considerations
```
For {mobile_app_name}, please specify:
1. Platform-specific requirements (iOS/Android)
2. Device permissions and hardware access
3. Testing environment setup (TestFlight/Android Testing)
4. Performance optimization for:
   - Battery usage
   - Memory management
   - Hardware resource access
5. App store deployment requirements
```

## Best Practices for LLM-Assisted Development

### Documentation Generation
- Request inline documentation for all new code
- Ask for README updates with each significant change
- Generate API documentation automatically
- Maintain a changelog

### Testing Strategy
```
For {component_name} in @{path/to/component}, please:
1. Generate unit tests covering core functionality
2. Create integration tests for external service interactions
3. Add error case testing
4. Implement performance benchmarks
```

### Error Handling and Logging
```
Please implement error handling and logging for {feature_name} that includes:
1. Structured error messages
2. Error categorization
3. Logging levels
4. Recovery procedures
```

### Rapid Iteration Cycle
1. **Development Phase**
   ```
   Please implement {feature_name} with:
   - Modular code structure
   - Built-in error handling
   - Automated tests
   - Documentation
   ```

2. **Testing Phase**
   ```
   For @{path/to/test_results}:
   1. Analyze test failures
   2. Propose fixes
   3. Implement solutions
   4. Verify fixes
   ```

3. **Refinement Phase**
   ```
   Based on @{path/to/feedback}:
   1. Optimize performance
   2. Enhance error handling
   3. Improve user experience
   4. Update documentation
   ```

## Tips for Effective LLM Collaboration

1. **Be Specific**
   - Provide clear context
   - Reference specific files and line numbers
   - Define expected outcomes

2. **Iterative Development**
   - Start with small, focused changes
   - Review and refine incrementally
   - Maintain consistent communication

3. **Quality Control**
   - Request automated tests with new features
   - Ask for error handling strategies
   - Verify security considerations

4. **Documentation First**
   - Request documentation with each feature
   - Keep README and API docs updated
   - Document design decisions

5. **Platform-Specific Considerations**
   - Define target platforms early
   - Consider hardware requirements
   - Plan for platform-specific testing
   - Address performance optimization

## Detailed Example Usage: End-to-End Process

This section demonstrates how to use these templates in sequence to develop a prototype, using a Business Intelligence Dashboard app as an example.

### Stage 1: Initial Idea Validation

```
Initial Prompt:
I have an idea for a web application: DataInsight Dashboard. Core features include:
- Real-time data visualization from multiple sources
- AI-powered trend analysis and predictions
- Customizable dashboard layouts
- Automated report generation
- Team collaboration features

Please evaluate this idea considering:
1. Market viability and unique value proposition
2. Technical feasibility for MVP development
3. Potential challenges and limitations
4. Suggested additional features or modifications
5. High-level steps required for prototype development
```

After receiving positive validation and suggestions, proceed to technical planning.

### Stage 2: Technical Architecture

```
For the DataInsight Dashboard MVP, I need guidance on technology selection and architecture.

Current technical assumptions:
- Frontend: React with D3.js for visualizations
- Backend: Python (FastAPI) for data processing
- Key APIs/Services: OpenAI API for predictions, MongoDB for storage
- Infrastructure: AWS (EC2, Lambda)

Please provide:
1. Validation or alternatives for technology choices
2. Required third-party services and APIs
3. Development environment setup
4. Initial project structure
5. Core technical components and their interactions
```

### Stage 3: MVP Feature Specification

```
For DataInsight Dashboard, I need to define the MVP feature set and implementation approach.

Core user flow:
1. User connects data source (CSV/API)
2. System processes and visualizes data
3. AI generates insights and predictions
4. User customizes dashboard layout
5. User generates and shares reports

For each feature, please specify:
1. Technical implementation details
2. Required APIs/libraries
3. Data models and storage requirements
4. User interface components
5. Testing requirements
```

### Stage 4: Development Process

```
Project: DataInsight Dashboard
Current Stage: Initial Development
Reference Files: @{src/components/Dashboard.js}

Please help with:
1. Creating component documentation
2. Implementing unit tests for data processing
3. Setting up error logging for API calls
4. Code review of visualization components
5. Integration testing for data pipeline
```

### Stage 5: Deployment Planning

```
For DataInsight Dashboard, I need to deploy a testable prototype:

Environment:
- Target Platform: web-based
- Development Approach: modern web stack
- Testing Environment: staging environment on AWS
- Device Requirements: modern web browsers

Please provide:
1. Development environment setup instructions
2. Build and deployment process
3. Testing environment configuration
4. Browser compatibility requirements
5. Performance optimization guidelines
```

### Iterative Development Example

#### 1. Feature Implementation
```
Please implement the data source connection feature with:
- Modular code structure for different data source types
- Error handling for connection failures
- Unit tests for connection validation
- Documentation for supported data formats
```

#### 2. Testing and Refinement
```
For @{tests/integration/data_source_tests.js}:
1. Analyze connection timeout failures
2. Propose retry mechanism
3. Implement connection pooling
4. Verify fixes with large datasets
```

#### 3. Documentation Update
```
Based on @{docs/README.md}:
1. Update data source connection guide
2. Add troubleshooting section
3. Include performance recommendations
4. Document security considerations
```