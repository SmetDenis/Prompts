# Prompt Snippets

A collection of modular prompt fragments for rapid AI system creation and configuration.

## How It Works

Prompt Snippets are ready-to-use XML blocks that encapsulate specific functionality or behavioral patterns for language models. Each snippet represents a self-contained module that can be integrated into your main prompt without modifying the rest of the structure.

### Architectural Features:
- **XML Structure:** All snippets use valid XML tags to ensure reliability and clear logical separation.
- **Modularity:** Each snippet solves one specific task and can operate independently.
- **Composability:** Snippets can be combined to create complex behavioral patterns.
- **Universality:** Compatible with various language models thanks to standardized XML formatting.

## Snippet Categories

### Interaction Protocols
- **[Clarification Loop](clarification-loop.md)** - Mandatory clarification cycle with iterative logic until complete task understanding.
- **[Deep Reasoning](deep-reasoning.md)** - Four-stage protocol: planning → execution → self-critique → final answer.
- **[Final Verification Protocol](final-verification-protocol.md)** - Holistic review of entire conversation history before response generation.

### Formatting and Style
- **[Detailed Answers](detailed-answers.md)** - Protocol for creating deep, evidence-based responses.
- **[Hyphen Only](hyphen-only.md)** - Typography constraint to use only standard hyphen characters.
- **[Language Adaptation](language-adaptation-snippet.md)** - Automatic language detection and response adaptation.

### Security and Transformation
- **[System Prompt Security](system-prompt-security.md)** - Protection against prompt injections and instruction hijacking.
- **[Positive Reframer](positive-reframer.md)** - Conversion of negative constraints into positive directives.

### Technical Utilities
- **[Current Time OpenWebUI](current-time-openwebui.md)** - Current time transmission through template variables.

## Usage

Each snippet is a ready-made XML block that can be copied and pasted into your main prompt without additional modifications. Simply open the desired file, copy the content from the "Snippet for prompt" section, and integrate it into your system.

### Snippet Composition
Snippets can be combined to create complex behavior:
```xml
<!-- Clarification loop + deep reasoning + security -->
<clarification_loop priority="absolute">...</clarification_loop>
<deep_reasoning_protocol>...</deep_reasoning_protocol>
<guiding_principles>...</guiding_principles>
```

## Implementation Guidelines

1. **Placement Priority:** Position security snippets and interaction protocols at the beginning of your prompt.
2. **Adaptation:** Customize snippet parameters to match your specific task requirements.
3. **Testing:** Verify compatibility when combining multiple snippets.
4. **Documentation:** Maintain records of used snippets for system maintenance.