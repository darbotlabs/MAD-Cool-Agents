# Copilot Instructions for Microsoft 365 Agents SDK

## Repository Overview

This repository contains the Microsoft 365 Agents SDK, which enables developers to create agents deployable to various Microsoft 365 channels including Microsoft 365 Copilot, Microsoft Teams, Web & Custom Apps, and more. The SDK provides scaffolding for agent communication and supports integration with AI services of choice.

## Project Structure

- `/samples/` - Example implementations and demos
  - `/basic/` - Simple agent examples
  - `/complex/` - Advanced agent implementations
  - `/compat/` - Compatibility samples
- `/specs/` - Specifications and schema definitions
  - `/manifest/` - Bot manifest specifications and schemas
  - `/activity/` - Activity protocol specifications
- `/docs/` - Additional documentation
- `/experimental/` - Experimental features and prototypes

## Technology Stack

- **Languages**: TypeScript/JavaScript (Node.js), C#/.NET, Python
- **Frameworks**: Microsoft Bot Framework, React (for web components)
- **AI Integration**: Semantic Kernel, Azure AI Foundry, custom AI services
- **Channels**: Microsoft 365 Copilot, Microsoft Teams, SharePoint Embedded

## Development Guidelines

### Code Style and Standards

1. **Linting**: Use ESLint configuration defined in `/samples/package.json`
   - Run `npm run lint` in the samples directory to check and fix code style
   - Follow the neostandard configuration

2. **TypeScript**: 
   - Use strict TypeScript configuration
   - Prefer explicit types over `any`
   - Follow Microsoft's TypeScript guidelines

3. **File Naming**:
   - Use camelCase for TypeScript/JavaScript files
   - Use PascalCase for React components
   - Use kebab-case for configuration files

### Architecture Patterns

1. **Agent Structure**:
   - Implement agent logic in dedicated classes
   - Separate concerns: routing, processing, and response generation
   - Use dependency injection where appropriate

2. **Manifest Files**:
   - Follow the schema versions defined in `/specs/manifest/schemas/`
   - Use semantic versioning for manifest versions
   - Include proper metadata and capability declarations

3. **Authentication**:
   - Implement proper OAuth flows for Microsoft 365 integration
   - Use secure token handling practices
   - Support both user and application authentication

### Sample Development

When creating new samples:

1. **Structure**: Follow the pattern in existing samples
   - Include proper README.md with setup instructions
   - Provide package.json with appropriate dependencies
   - Include manifest files for channel deployment

2. **Documentation**: 
   - Explain the scenario being demonstrated
   - Provide step-by-step setup instructions
   - Include troubleshooting section

3. **Testing**:
   - Include unit tests where applicable
   - Provide manual testing instructions
   - Test against multiple channels when relevant

### Channel Integration

1. **Microsoft 365 Copilot**:
   - Use proper manifest schema v2.1 or v2.2
   - Implement appropriate activity handlers
   - Follow Microsoft 365 Copilot UX guidelines

2. **Microsoft Teams**:
   - Support Teams-specific features like adaptive cards
   - Handle Teams-specific events and activities
   - Follow Teams app development best practices

3. **Web Integration**:
   - Use React components for web experiences
   - Implement proper CORS handling
   - Support responsive design patterns

### AI Service Integration

1. **Flexibility**: Design agents to work with multiple AI providers
2. **Configuration**: Use environment variables for API keys and endpoints
3. **Error Handling**: Implement robust error handling for AI service failures
4. **Rate Limiting**: Respect AI service rate limits and implement backoff strategies

### Security Best Practices

1. **Secrets Management**:
   - Never commit API keys or secrets to the repository
   - Use environment variables or secure configuration stores
   - Follow Microsoft's security guidelines for agent development

2. **Input Validation**:
   - Validate all user inputs
   - Sanitize data before processing
   - Implement proper content filtering

3. **Authentication**:
   - Use Microsoft identity platform for authentication
   - Implement proper token validation
   - Support principle of least privilege

### Performance Considerations

1. **Response Times**: Keep agent responses under Microsoft's recommended latency thresholds
2. **Resource Usage**: Optimize memory and CPU usage for scalability
3. **Caching**: Implement appropriate caching strategies for AI responses and data

### Common Patterns to Follow

1. **Activity Handling**: Use the activity handler pattern for processing different activity types
2. **State Management**: Implement proper conversation and user state management
3. **Error Recovery**: Provide graceful degradation when services are unavailable
4. **Logging**: Implement comprehensive logging for debugging and monitoring

### Contribution Guidelines

1. **Pull Requests**: 
   - Follow the existing code style and patterns
   - Include tests for new functionality
   - Update documentation as needed

2. **Issues**:
   - Use the appropriate repository for language-specific issues
   - Provide detailed reproduction steps
   - Include environment information

3. **Documentation**:
   - Keep README files up to date
   - Document breaking changes
   - Provide migration guides when needed

## Useful Commands

- `npm run lint` - Run ESLint in samples directory
- `npm install` - Install dependencies in samples directory
- Check individual sample README files for specific build and run instructions

## Related Resources

- [Microsoft 365 Agents SDK Documentation](https://aka.ms/M365-Agents-SDK-Docs)
- [Semantic Kernel Documentation](https://learn.microsoft.com/en-us/semantic-kernel/overview/)
- [Microsoft Bot Framework Documentation](https://docs.microsoft.com/en-us/azure/bot-service/)
- [Microsoft Teams Development Documentation](https://docs.microsoft.com/en-us/microsoftteams/platform/)