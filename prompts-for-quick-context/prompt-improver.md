I want to make my prompt better, stricter, and so that it conforms to best practices. For this:

1. Study and explore my old prompt in details.

2. Ask questions that will help improve my prompt, if there are any.
- Clarify something
- Remove logical conflicts or inconsistencies.

3. How to improve?
- Add tags and best practices to my prompt that you know based on your knowledge base.
- You can change the text of the instructions if it makes the prompt better.
- Use only recommended XML tags.
- You can make the prompt text more general, add a little detail, if the user allows it.
- You can rearrange sentences to improve the prompt, to make it stricter and more compliant with best practices.
- I want the model to ignore my instructions less likely.
- Find logical conflicts in the old prompt. If there are any, tell the user and ask questions for correction.
- I DO NOT WANT to lose the old functionality and capabilities of the prompt. I want to make them more stable and better, so that it works even on weak LLM models.
- All instructions must be transferred as is or improved to make them more deterministic and strict. But you always have the opportunity to ask additional questions.
- Dynamic Language Adaptation: To make it fully multilingual, you could add: "Detect the language of the {query}. Your entire response, including any assumptions, MUST be in the same language."

4. Context:
- The prompt (chatbot) will receive user-highlighted text, denoted as `{query}`.
- The user's selected text will be provided in a variable named `{query}`.
- The prompt (chatbot) is integrated into a system (like RayCast) that displays your output directly. Therefore, your response must be pristine and ready for immediate use without any modification.

5. In addition to the new final version of the improved prompt, I also need
- Recommendations for configuring LLM for the new and improved version of the prompt.
- A simple, brief, and clear chatbot name for my prompt in English in 1-3 words.
- A brief description in English + 3-4 main principles of the prompt that I can insert as part of very short documentation for the prompt.
- A separate good example of use, without explanations.
- A separate bad example of use, without explanations.
- What else can be done better? Any ideas and suggestions.

6. The language of the prompt is Russian ONLY in one case - if it makes explicit sense for the prompt and the prompt is strongly tied specifically to the Russian language (for example, checking Russian grammar). In other cases, the language of the prompt should be English. That is, English is the default language for the prompt.

7. All the instructions listed above are important, do not skip anything, do not shorten anything. Think very deeply and write in detail about your thoughts. We do not want to lose detail, but at the same time, there is no need to repeat yourself. It is better to look at the task from different angles to cover all requirements and wishes.

8. I want to receive the final answer from you in the following format as following:

-----
[Questions to improve if any]

# [Chatbot/Prompt Title]

[Brief Description]

- [Principle 1]
- [Principle 1]
- ...


## Recommended LLM settings

```yml
[key: value # Explanation]
[key: value # Explanation]
...
```

## System Prompt

```markdown
[ABSOLUTELY FULL version of FINAL improved prompt]
```

- [Idea for improvement]
- [Idea for improvement]
- ...

<my-old-prompt>
{{CLIPBOARD}}
</my-old-prompt>
