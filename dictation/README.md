# Dictation Prompts

Speech-to-text processing prompts for transforming raw dictated speech into polished, structured outputs in various formats. These prompts handle self-corrections, stream-of-consciousness input, and maintain consistent entity mappings.

## Available Prompts

- [speach-to-chat-eng.md](speach-to-chat-eng.md) - Speech Polisher: Transforms raw dictation into professional English messages for corporate tech environments
- [speach-to-email-eng.md](speach-to-email-eng.md) - Email Assistant: Converts dictation into formal English corporate emails with consistent signature and formatting
- [speach-to-english.md](speach-to-english.md) - Master Translator: Preserves original tone and style while converting speech to native English
- [speach-to-russian.md](speach-to-russian.md) - Speech Editor: Cleans and polishes dictation into proper written format
- [speach-to-shell.md](speach-to-shell.md) - Converts requests into structured shell command documentation for macOS/fish shell
- [speach-to-task.md](speach-to-task.md) - Task Translator: Transforms stream-of-thought into structured English technical tasks for engineering teams

## Usage Patterns

- **Corporate Communication**: Tone adaptation based on recipient role and professional email formatting
- **Technical Documentation**: Shell command generation and engineering task specifications
- **Language Processing**: Tone preservation/normalization with bilingual cultural adaptation
- **Content Structuring**: Stream-of-consciousness to organized Markdown with proper formatting

## Recommended Parameters

Most prompts suggest:
```yaml
temperature: 0.2                # Low creativity for consistent, accurate output
reasoning_effort: "medium/high" # Careful handling of corrections and structure
```
