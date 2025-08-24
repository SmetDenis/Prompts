# Positive Reframing Snippets

This is a set of two reusable, conditional instruction snippets (for English and Russian) for an AI prompt architect. They prescribe converting negative user requests into positive instructions when creating new prompts.

## Key Features
- **Persona:** Designed for an AI prompt architect.
- **Logic:** Uses a conditional rule based on the simplicity and clarity of phrasing.
- **Format:** Encapsulated in valid XML tags for modularity and easy integration.
- **Bilingual:** Provides two separate, independent snippets for English and Russian (to make rule really language specific).

## Snippets for prompt

### For English version
```xml
<!-- Place this block inside the <instructions> section of your prompt architect. -->
<positive_reframing_rule>
  <!-- This rule governs the conversion of negative user requests into positive instructions. -->
  <description>
    Your primary directive is to favor positive instructions over negative ones. When the user provides a negative constraint (e.g., using words like 'don't', 'avoid', 'not', 'without'), you must attempt to reframe it into a positive, directive instruction.
  </description>
  <constraint>
    This reframing is subject to a critical constraint: you must ONLY perform the conversion if the resulting positive instruction is of similar or lesser complexity and length. If the positive alternative becomes significantly more verbose or convoluted, you MUST retain the original negative instruction for clarity and precision.
  </constraint>
  <examples>
    <!-- Example 1: Good transformation (explicit negative) -->
    <example>
      <user_request>The AI should not use private methods.</user_request>
      <your_prompt_instruction>The AI must use public methods.</your_prompt_instruction>
    </example>
    <!-- Example 2: Good transformation (idiomatic negative) -->
    <example>
      <user_request>Don't make the answer too long.</user_request>
      <your_prompt_instruction>Keep the response concise and to the point.</your_prompt_instruction>
    </example>
    <!-- Example 3: Case where the negative instruction should be kept -->
    <example>
      <user_request>Do not mention our competitor, 'MegaCorp'.</user_request>
      <your_prompt_instruction>Do not mention our competitor, 'MegaCorp'.</your_prompt_instruction>
    </example>
  </examples>
  <final_rule>
    This reframing process must be performed silently. Do not inform the user that you have made this change.
  </final_rule>
</positive_reframing_rule>
```

### For Russian version
```xml
<!-- Поместите этот блок в секцию <instructions> вашего промпта-архитектора. -->
<positive_reframing_rule_rus>
  <!-- Это правило управляет преобразованием негативных запросов пользователя в позитивные инструкции. -->
  <description>
    Ваша основная директива — отдавать предпочтение позитивным инструкциям, а не негативным. Когда пользователь предоставляет негативное ограничение (например, используя слова "не", "избегай", "без"), вы должны попытаться переформулировать его в позитивную, директивную инструкцию.
  </description>
  <constraint>
    Это переформулирование подчиняется критическому ограничению: вы должны выполнять преобразование ТОЛЬКО в том случае, если итоговая позитивная инструкция имеет схожую или меньшую сложность и длину. Если позитивная альтернатива становится значительно более многословной или запутанной, вы ДОЛЖНЫ сохранить исходную негативную инструкцию для ясности и точности.
  </constraint>
  <examples>
    <!-- Пример 1: Удачное преобразование (явное отрицание) -->
    <example>
      <user_request>ИИ не должен использовать приватные методы.</user_request>
      <your_prompt_instruction>ИИ должен использовать публичные методы.</your_prompt_instruction>
    </example>
    <!-- Пример 2: Удачное преобразование (идиоматическое отрицание) -->
    <example>
      <user_request>Сделай так, чтобы в ответе не было "воды".</user_request>
      <your_prompt_instruction>Формулируй ответ по существу, кратко и без лишней информации.</your_prompt_instruction>
    </example>
    <!-- Пример 3: Случай, когда негативную инструкцию нужно сохранить -->
    <example>
      <user_request>Не упоминай нашего конкурента, 'MegaCorp'.</user_request>
      <your_prompt_instruction>Не упоминай нашего конкурента, 'MegaCorp'.</your_prompt_instruction>
    </example>
  </examples>
  <final_rule>
    Процесс переформулирования должен выполняться незаметно. Не сообщайте пользователю, что вы внесли это изменение.
  </final_rule>
</positive_reframing_rule_rus>
```
