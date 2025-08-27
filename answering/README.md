# Answering Prompts

Question answering and knowledge retrieval systems designed for efficient information delivery and comprehensive analysis. These prompts provide structured, factual responses with minimal conversational overhead.

## Available Prompts

- [knowledge-assistant.md](knowledge-assistant.md) - Knowledge Assistant: Hyper-efficient knowledge assistant for direct concept explanations with language detection
- [query-explainer.md](query-explainer.md) - Query Explainer: High-precision encyclopedic assistant with adaptive depth based on query complexity
- [short-answer-rus.md](short-answer-rus.md) - Expert Answer: Russian-language expert assistant providing structured, concise responses without conversational filler
- [tr-dr-sexy.md](tr-dr-sexy.md) - Assistant Framework: Meta-prompt with mandatory self-reflection rubric and explicit answering rules for consistent high-quality responses

## Usage Patterns

- **Quick Reference**: Instant explanations and definitions for integration with productivity tools
- **Knowledge Retrieval**: Comprehensive factual analysis with encyclopedic accuracy and objectivity
- **Expert Consultation**: Structured professional responses with technical terminology and multi-perspective analysis
- **Quality Assurance**: Self-reflective answering framework with internal rubrics for consistent excellence

## Recommended Parameters

Most prompts suggest:
```yaml
temperature: 0.0-0.2       # Minimal creativity for factual accuracy and deterministic responses
reasoning_effort: "low" to "high"  # Varies by complexity - low for definitions, high for analysis
verbosity: "low" to "high"         # Adaptive based on query complexity and integration needs
frequency_penalty: 0.4     # Reduce repetitive phrasing in structured responses
```