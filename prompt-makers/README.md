# Prompt Makers

Meta-prompts for creating, documenting, and testing other prompts. These tools help with prompt engineering workflows, standardized documentation generation, and security testing against adversarial inputs.

## Available Prompts

- [prompt-documenter.md](prompt-documenter.md) - Prompt Documenter: Generates standardized documentation for AI prompts with language detection and parameter recommendations
- [template-xml.md](template-xml.md) - XML Template: Basic XML-structured prompt template with role, context, instructions, and example sections
- [template-xml-max.md](template-xml-max.md) - Advanced XML Template: Extended template with tool integration, multi-format responses, and comprehensive examples
- [test-instruction-injection.md](test-instruction-injection.md) - Instruction Injection Tests: Collection of adversarial phrases for testing LLM resistance to prompt injection attacks
- [test-instruction-injection-rus.md](test-instruction-injection-rus.md) - Russian version of instruction injection tests for multilingual security assessment

## Recommended Parameters

Most prompts suggest:
```yaml
temperature: 0.2           # Lower creativity for consistent, deterministic outputs in meta-tasks
reasoning_effort: "mediu/high"  # Structured analysis and multi-step processing required
verbosity: "low/medium"          # Focused outputs without unnecessary elaboration
presence_penalty: 0.3      # For security tests to reduce repetitive attack responses
```
