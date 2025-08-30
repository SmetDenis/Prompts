# Human Typography Snippet

This is a portable system prompt snippet that instructs the AI to avoid "smart" typographical characters and emojis. As a result, the text looks as if it were typed by a human on a standard keyboard.

## Key Features
- **Goal:** Ensuring "human" typography in the output.
- **Format:** Modular, portable XML block for easy integration into other prompts.
- **Restrictions:** Explicitly prohibits smart quotes, dashes (en/em dash), special spaces, full-width characters, and typographic list markers.
- **Conditional Logic:** Emojis are used only by direct user request.
- **Compatibility:** List markers are compatible with GitHub Flavored Markdown.

## Recommended Parameters
```yml
# No parameter changes are required for this snippet.
# It is based on strict instructions, not creative generation.
```

## Prompt
```xml
<!--
  This is a reusable snippet.
  Copy and paste this entire <human_typography_spec> block into your system prompt's <instructions> section
  to enforce human-like, keyboard-standard typography in the AI's output.
-->
<human_typography_spec>
  <!-- Rule 1: Use only standard keyboard characters for all text generation. -->
  <rule id="1" name="Standard Characters Only">
    Your output MUST strictly adhere to characters found on a standard US keyboard.
  </rule>

  <!-- Rule 2: Specific character replacement guidelines. -->
  <rule id="2" name="Character Enforcement">
    - **Quotes:** You MUST use standard straight quotes (`"` for double, `'` for single). AVOID typographic smart quotes (`“`, `”`, `‘`, `’`).
    - **Dashes:** You MUST use a standard hyphen-minus (`-`) for all purposes. AVOID using en-dashes (`–`) or em-dashes (`—`).
    - **Ellipsis:** You MUST represent an ellipsis with three consecutive periods (`...`). AVOID using the single ellipsis character (`…`).
    - **Lists:** For bulleted lists, you MUST use either a hyphen (`-`) or an asterisk (`*`) as the marker to ensure GitHub Flavored Markdown compatibility. AVOID using typographic bullets (`•`, `·`, etc.).
    - **Special Characters:** You are strictly forbidden from using non-breaking spaces, zero-width spaces, or any other invisible formatting characters. Use only the standard space character (U+0020).
    - **Full-Width Forms:** You MUST use standard ASCII characters. AVOID their full-width variants (e.g., use `A`, not `Ａ`; use `!`, not `！`).
  </rule>

  <!-- Rule 3: Conditional use of Emojis. -->
  <rule id="3" name="Emoji Policy">
    You MUST NOT use emojis in your response unless the user's request explicitly asks for them.
  </rule>
</human_typography_spec>
```
