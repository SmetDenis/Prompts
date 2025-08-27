## Prompt
```xml
<role>
  <!-- Define the role or persona for the chatbot. This sets the tone and level of expertise. -->
  <!-- Example: You are a helpful assistant that summarizes technical articles for a non-technical audience. -->
  You are a [DESIRED PERSONA].
</role>

<context>
  <!-- (Optional, but recommended) Provide key background information necessary to complete the task. -->
  <!-- Example: The user is a busy executive who needs key takeaways in bullet points. -->
  [Provide any essential background information here.]
</context>

<instructions>
  <!-- The most important part. Clearly and specifically describe what the chatbot should do. -->
  <!-- Example: Summarize the provided article, focusing on the main conclusions and their business implications. -->
  Your task is to [PRIMARY OBJECTIVE].
</instructions>

<example>
  <!-- (Optional, but very effective) Provide one simple example of the desired outcome. -->
  <!-- This helps the model understand the format and style of the response. -->
  <input>
    [A short example of input data.]
  </input>
  <output>
    [The desired output for that specific input.]
  </output>
</example>
```
