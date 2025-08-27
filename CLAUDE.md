# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a comprehensive collection of AI prompts organized by category and use case. The repository contains structured prompt templates for various applications including coding assistance, text processing, research, and specialized tasks. All prompts are stored as Markdown files with consistent documentation patterns.

## Repository Structure

### Core Directories
- `coding/` - Programming and development assistance prompts
- `answering/` - General-purpose question answering and knowledge retrieval
- `prompt-makers/` - Meta-prompts for creating other prompts (including UPA framework)
- `prompt-snippets/` - Reusable prompt components and modular elements
- `research/` - Academic and analysis-focused prompts
- `summarization/` - Content summarization and analysis tools
- `dictation/` - Speech-to-text and voice command processing
- `image-to-text/` - OCR and image analysis prompts
- `raycast/` - Quick automation and text processing utilities
- `snippets/` - Utility prompt fragments
- `one-liners/` - Simple, single-purpose prompt examples
- `!_guides/` - Comprehensive prompt engineering guides and documentation

### Key Architecture Patterns

#### File Organization
- Each prompt is a standalone `.md` file with descriptive filename
- Russian language prompts use `-rus.md` suffix
- Files follow consistent documentation structure with title, description, key features, and prompt sections

#### Prompt Structure Standards
Most prompts follow this XML-based structure:
```xml
<role>
  [Defines the AI persona and expertise level]
</role>

<context>
  [Provides background information and constraints]
</context>

<instructions>
  [Core operational directives and task definitions]
</instructions>

<help>
  [Usage guidance for end users]
</help>

<example>
  [Input/output demonstrations when applicable]
</example>
```

#### Multi-Language Support
- English prompts: standard naming convention
- Russian prompts: `-rus.md` suffix
- Bilingual prompts available for key use cases
- Language-specific examples and cultural adaptations

## Key Framework: Ultimate Prompt Architect (UPA)

The repository's centerpiece is the UPA framework (`UPA.md`), which defines a comprehensive system for prompt creation with:
- Mandatory clarification loops (up to 5 rounds)
- Deep reasoning protocols with 4-step execution
- Positive reframing rules for converting negative constraints
- Self-critique and verification mechanisms
- Structured output with metadata and parameter recommendations

## Common Development Patterns

### Prompt Engineering Best Practices
1. **XML Structure**: Use consistent XML tags for organization and robustness
2. **Persona Definition**: Clear role assignment with specific expertise levels
3. **Context Awareness**: Include relevant background and constraint information
4. **Example-Driven**: Provide concrete input/output examples where beneficial
5. **Positive Framing**: Convert negative constraints to positive directives when possible

### File Creation Guidelines
- Follow existing naming conventions (`kebab-case.md` or `kebab-case-rus.md`)
- Include structured documentation with title, description, and key features
- Use XML tags for prompt organization
- Provide parameter recommendations when applicable
- Include usage examples and help sections
- End all list items with periods for consistency
- Use only hyphen-minus (-) character instead of em dash (—) or en dash (–)

### Modification Approach
- Preserve exact formatting and whitespace for version control compatibility
- Make surgical changes that only affect intended modifications
- Follow the UPA modification protocol for existing prompts
- Test prompt modifications for logical consistency

## Special Considerations

### Security and Safety
- Prompts include defensive design patterns against injection attacks
- Clear demarcation between trusted and untrusted content
- Explicit input validation and formatting requirements
- Role-based constraints to maintain intended behavior

### Language-Specific Features
- Russian prompts adapted for cultural context and linguistic patterns
- Specialized technical terminology translations
- Regional compliance and usage considerations

### Multi-Language README Synchronization
**CRITICAL REQUIREMENT:** This repository maintains three README files that must be kept synchronized:
- `README.md` (English - primary)
- `README_RUS.md` (Russian)
- `README_ZH.md` (Traditional Chinese)

**Mandatory Protocol:**
- Any changes to content, structure, or information in one README MUST be reflected in all three versions
- When updating any README, immediately update the other two to maintain consistency
- Ensure cultural and linguistic adaptation while preserving core information
- All three files should have identical structure and equivalent content coverage
- Never leave README files out of sync - this creates confusion for international users

### No Build/Test Commands
This repository contains only documentation and text files. There are no build processes, dependency management, or test suites to run. All validation is manual through prompt testing in target AI systems.

# Important Instruction Reminders
- Do what has been asked; nothing more, nothing less.
- NEVER create files unless they're absolutely necessary for achieving your goal.
- ALWAYS prefer editing an existing file to creating a new one.
- NEVER proactively create documentation files (*.md) or README files. Only create documentation files if explicitly requested by the User.
