# Positive Reframer

Converts negative or prohibitive user constraints into concise positive directives when the positive alternative is of similar or lesser complexity; includes explicit examples and a silent-operation requirement. Designed for prompt-engineering rules that must check complexity, preserve precision when needed, and avoid notifying the user about the reframing.

## Key Features
- **Purpose:** Converts negative instructions (e.g., "don't", "avoid", "not") into equivalent positive directives when feasible.
- **Rule:** Only reframe if the positive alternative is similar or shorter in complexity and length; otherwise keep the original negative phrasing.
- **Examples:** Provides explicit good/bad transformation examples to guide behavior.


Вы совершенно правы. Приношу извинения за ошибку в предыдущем ответе — XML действительно был невалидным из-за случайного включения лишнего текста. Это моя оплошность. Спасибо, что указали на это.

Я полностью пересмотрю структуру, исправлю XML и разделю сниппеты на независимые блоки с более идиоматичными примерами для каждого языка, как вы и просили.

### **ЭТАП 1: ПЛАНИРОВАНИЕ И ГИПОТЕЗА**

1.  **Цель:** Исправить, улучшить и реструктурировать ранее созданный сниппет.
2.  **Задача 1: Исправление XML.** Основная задача — обеспечить 100% валидность XML в обоих сниппетах. Я тщательно проверю каждый открывающий и закрывающий тег, чтобы гарантировать синтаксическую корректность.
3.  **Задача 2: Разделение блоков.** Вместо одного общего блока я создам два полностью независимых. Это повысит читаемость и упростит копирование нужной версии. В итоговом файле они будут размещены под отдельными подзаголовками.
4.  **Задача 3: Улучшение примеров.** Я заменю прямые переводы на более культурно и лингвистически релевантные примеры для английского и русского языков.
    *   **Для английского:** Я добавлю пример, связанный с распространенной просьбой о краткости (`"Don't make it too long"` -> `"Keep the response concise and to the point."`).
    *   **Для русского:** Я добавлю идиоматичный пример, характерный для русского языка, например, просьбу избегать "воды" в тексте (`"Сделай так, чтобы в ответе не было 'воды'"` -> `"Формулируй ответ по существу, кратко и без лишней информации."`).
5.  **Сохранение логики:** Основная логика правила — преобразование негативных инструкций в позитивные только при сохранении простоты и длины — останется неизменной, так как она была сформулирована верно.

### **ЭТАП 2: ПОШАГОВОЕ ВЫПОЛНЕНИЕ И КОНСТРУИРОВАНИЕ**

1.  **Создание английского сниппета.** Я создаю первый блок. Тщательно прописываю структуру: `<positive_reframing_rule>` содержит `<description>`, `<constraint>`, `<examples>` и `<final_rule>`. Внутри `<examples>` размещаю три `<example>`, каждый из которых содержит `<user_request>` и `<your_prompt_instruction>`. Вставляю новые, более идиоматичные примеры. Проверяю валидность.

2.  **Создание русского сниппета.** Я создаю второй, полностью независимый блок по той же схеме. Использую тег `<positive_reframing_rule_rus>`. Перевожу основную логику и добавляю специфичные для русского языка примеры, включая идиому про "воду". Снова тщательно проверяю валидность всей структуры.

3.  **Обоснование дизайна.** Разделение на два блока напрямую выполняет требование пользователя и является лучшей практикой для модульности. Новые примеры не просто иллюстрируют правило, но и лучше калибруют модель для понимания нюансов каждого языка, что повышает общую надежность инструкции.

### **ЭТАП 3: САМОКРИТИКА И ПРОВЕРКА**

1.  **Валидность XML:** Я мысленно и визуально парсю оба XML-блока. Все теги открыты и закрыты корректно. Вложенность соблюдена. Ошибок, подобных предыдущей, нет. XML теперь валиден.
2.  **Соответствие требованиям:**
    *   XML исправлен? — Да.
    *   Блоки разделены? — Да.
    *   Примеры улучшены с учетом специфики языков? — Да.
    *   Все исходные требования сохранены? — Да.
3.  **Потенциальные сбои:** Риск неверной интерпретации "сложности" остается, но он значительно снижен благодаря более качественным и разнообразным примерам, которые служат лучшей калибровочной базой для модели.

Проверка пройдена. Результат полностью соответствует исправленному запросу.

### **ЭТАП 4: ГЕНЕРАЦИЯ ИТОГОВОГО ПРОМПТА**

Suggested Filename: `positive-reframing-snippets-rus.md`

# Positive Reframing Snippets

Это набор из двух переиспользуемых, условных фрагментов инструкций (для английского и русского языков) для AI-архитектора промптов. Они предписывают преобразовывать негативные запросы пользователя в позитивные инструкции при создании новых промптов.

## Key Features
- **Persona:** Разработан для AI-архитектора промптов.
- **Logic:** Использует условное правило, основанное на простоте и ясности формулировок.
- **Format:** Инкапсулирован в валидные XML-теги для модульности и легкой интеграции.
- **Bilingual:** Предоставляет два отдельных, независимых сниппета для английского и русского языков.

## Prompts

### English Snippet
```markdown
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

### Russian Snippet
```markdown
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
