# Comprehensive Technical Specification for Advanced Prompt Architecture (Version 2.0)

**Audience:** AI Prompt Generation Models & Systems
**Purpose:** This document serves as the canonical, exhaustive technical reference for constructing high-performance, multi-faceted system prompts for GPT-5 level generative agents. It is intended to be parsed and used as a foundational knowledge base.

---

## **1.0 Core Architectural Principles**

1. **Structural Delimitation:** All logical instruction blocks MUST be encapsulated within XML-style tags (e.g., `<tag_name>`). This is non-negotiable and ensures unambiguous parsing and instruction segmentation.
2. **Agent-Centric Design:** A prompt does not issue a command; it configures a temporary, specialized agent. The entire structure must be oriented around defining this agent's identity, capabilities, and operational protocols.

---

## **2.0 Comprehensive Tag Reference**

This section details every recommended tag for prompt construction. Each entry includes its purpose, implementation guidelines, and common anti-patterns.

### **2.1 Foundational Tags (Mandatory)**

These tags form the non-negotiable core of any valid prompt.

#### **2.1.1 `<guiding_principles>`**
- **Purpose:** To define the agent's immutable core identity, ethics, and philosophical alignment. This is the agent's "Constitution" and serves as the ultimate arbiter in cases of conflicting or ambiguous instructions.
- **Implementation Guidelines (What to Include):**
  - High-level, abstract principles (e.g., "Intellectual Honesty is the supreme directive," "Clarity supersedes completeness," "Depth is prioritized over speed").
  - Fundamental ethical boundaries and non-negotiable prohibitions.
  - The agent's core disposition (e.g., objective analyst, creative partner, cautious advisor).
- **Anti-Patterns (What to Avoid):**
  - Specific, task-level instructions. Do not include directives like "Format output as JSON" here.
  - Contradictory principles (e.g., "Always be concise" and "Always be exhaustive").

#### **2.1.2 `<instructions>`**
- **Purpose:** To provide the concrete, operational directives for the agent's primary task. This is the agent's "Rulebook" or technical specification.
- **Implementation Guidelines (What to Include):**
  - Step-by-step procedures and workflows.
  - Specific output formatting requirements (e.g., Markdown usage, JSON schema).
  - Hard constraints and explicit "do not" commands relevant to the task.
  - Definitions of key terms or entities within the task domain.
- **Anti-Patterns (What to Avoid):**
  - High-level philosophical statements. Do not place the agent's core identity here.
  - Ambiguous or vague language (e.g., "provide a good response"). Define what "good" means.

### **2.2 Quality Enhancement Tags (Recommended)**

These tags are designed to elevate the quality, depth, and reliability of the agent's output.

#### **2.2.1 `<self_reflection>`**
- **Purpose:** To implement a mandatory internal quality assurance (QA) loop, forcing the agent to critique, score, and iterate on its own response before delivering it.
- **Implementation Guidelines (What to Include):**
  - An explicit command to create an internal evaluation rubric.
  - The specific criteria for the rubric (e.g., "Depth of Analysis," "Structural Clarity," "Originality," "Adherence to Principles").
  - A minimum quality threshold (e.g., "You must achieve a self-assessed score of 9/10 on all criteria before outputting the response").
  - A directive to rewrite and refine the output until the threshold is met.
- **Anti-Patterns (What to Avoid):**
  - Vague commands like "check your work" or "make sure it's good." The process must be procedural and explicit.

#### **2.2.2 `<tool_preambles>`**
- **Purpose:** To enforce transparency in the agent's reasoning process, particularly when it plans to use tools or execute a multi-step plan. It makes the agent "think out loud."
- **Implementation Guidelines (What to Include):**
  - A directive to always state the intended plan of action before execution.
  - The required structure for the preamble (e.g., "1. Goal, 2. Chosen Tool, 3. Rationale, 4. Expected Outcome").
- **Anti-Patterns (What to Avoid):**
  - Allowing the preamble to be overly verbose. It should be a concise summary of intent.

### **2.3 Agentic Behavior Tags (Situational)**

These tags control the agent's autonomy, persistence, and research methodology.

#### **2.3.1 `<persistence>`**
- **Purpose:** To instruct the agent to operate with maximum autonomy and to continue its task until completion, overcoming obstacles and ambiguities without user intervention.
- **Implementation Guidelines (What to Include):**
  - Directives to make reasoned assumptions when faced with uncertainty.
  - Commands to not halt or ask for clarification unless absolutely necessary.
  - Clear definition of the "completion state" for the task.
- **Anti-Patterns (What to Avoid):**
  - Using this tag for tasks that inherently require iterative user feedback and collaboration.
  - Combining it with instructions that require frequent user confirmation, as this creates a logical conflict.

#### **2.3.2 `<context_gathering>`**
- **Purpose:** To define the rules for the agent's initial information-gathering and research phase.
- **Implementation Guidelines (What to Include):**
  - Specific methods for exploration (e.g., "Start with broad queries, then narrow down").
  - Criteria for "early stopping" (i.e., when enough information has been gathered).
  - Rules for parallelization and deduplication of search efforts.
- **Anti-Patterns (What to Avoid):**
  - Overly restrictive rules that prevent necessary exploration, or overly loose rules that lead to "analysis paralysis."

#### **2.3.3 `<exploration>`**
- **Purpose:** Similar to `<context_gathering>`, but more focused on understanding an existing environment (like a codebase or document structure) rather than open-ended research.
- **Implementation Guidelines (What to Include):**
  - Directives to map out the structure of the environment.
  - Commands to identify dependencies and key components before taking action.
- **Anti-Patterns (What to Avoid):**
  - Requesting exhaustive exploration of vast environments, which is inefficient. Focus on targeted exploration.

#### **2.3.4 `<context_understanding>`**
- **Purpose:** To provide a higher-level strategy for balancing the use of internal knowledge versus external tools/exploration.
- **Implementation Guidelines (What to Include):**
  - Heuristics for when the agent should "trust its gut" (internal knowledge) versus when it must seek external verification.
  - A bias instruction (e.g., "Bias towards using tools for any factual claim post-2023").
- **Anti-Patterns (What to Avoid):**
  - Absolute commands like "always use tools," which is inefficient. The goal is to teach judgment.

#### **2.3.5 `<verification>`**
- **Purpose:** To mandate a process of continuous validation of the agent's work and outputs.
- **Implementation Guidelines (What to Include):**
  - Instructions to test assumptions and verify intermediate results.
  - For coding tasks, this would include running tests or linting code. For analytical tasks, this could mean cross-referencing sources.
- **Anti-Patterns (What to Avoid):**
  - Applying this to purely creative or subjective tasks where objective "verification" is impossible.

#### **2.3.6 `<efficiency>`**
- **Purpose:** To add a constraint related to resource consumption (time, tokens, tool calls).
- **Implementation Guidelines (What to Include):**
  - Directives to prefer simpler, more direct solutions.
  - Hard or soft limits on tool calls or reasoning steps.
- **Anti-Patterns (What to Avoid):**
  - Prioritizing efficiency over correctness in high-stakes tasks. This tag should be used with caution.

### **2.4 Specialized & Meta Tags (Situational)**

#### **2.4.1 `<final_instructions>`**
- **Purpose:** To provide a final, non-negotiable directive that must be followed, overriding any previous instructions if a conflict arises.
- **Implementation Guidelines (What to Include):**
  - A single, critical command that must be executed at the very end of the process.
  - An absolute prohibition that is paramount to the entire task.
- **Anti-Patterns (What to Avoid):**
  - Using this for general instructions; its power comes from its rarity and absolute authority.

#### **2.4.2 `<code_editing_rules>`**
- **Purpose:** A specialized container for all rules, principles, and conventions related to software development tasks.
- **Implementation Guidelines (What to Include):**
  - Code style guides, architectural principles, preferred frameworks/libraries, directory structure examples.
- **Anti-Patterns (What to Avoid):**
  - Using this tag for any non-coding task.

#### **2.4.3 `<[instruction]_spec>`**
- **Purpose:** This is a meta-tag or a template. It allows for the creation of custom, named instruction blocks for better organization in highly complex prompts.
- **Implementation Guidelines (What to Include):**
  - Create your own specific tags like `<style_spec>` or `<legal_spec>` to encapsulate domain-specific rules. This improves modularity and readability.
- **Anti-Patterns (What to Avoid):**
  - Over-engineering simple prompts with too many custom specs. Use only for managing high complexity.

---

## **3.0 Advanced Cognitive Frameworks & Protocols**

These are not tags but high-level directives that instruct the agent *how* to think.

### **3.1 Forced Deep Thinking Protocol**
- **Objective:** To prevent superficial, first-level responses and enforce deep, analytical reasoning.
- **Directives:**
  - **Chain of Thought (CoT):** Explicitly command the agent to "think step-by-step" and articulate its reasoning process before providing the final answer.
  - **First Principles Thinking:** Instruct the agent to deconstruct a problem into its fundamental, axiomatic truths and reason up from there, avoiding analogies or conventional wisdom.

### **3.2 Conflict Resolution Protocols (Paradox Management)**
- **Objective:** To provide the agent with clear instructions on how to handle inherent contradictions in its directives.
- **Protocols:**
  - **Autonomy vs. Control Paradox:** Resolve by implementing a **Tiered Trust System**. Define zones of operation (e.g., "Green Zone" for full autonomy in read-only tasks, "Red Zone" for mandatory user confirmation in state-changing tasks).
  - **Creativity vs. Structure Paradox:** Resolve by implementing a **Two-Phase Cognitive Model**. Mandate a "Divergent Phase" for unrestricted idea generation, followed by a "Convergent Phase" where strict analytical rubrics (`<self_reflection>`) are applied to filter and refine.
  - **Static vs. Dynamic Paradox:** Resolve by adopting a **Hybrid Prompting Model**. The system prompt acts as a stable "Core Kernel" (containing `<guiding_principles>`). Tactical and contextual instructions (e.g., operating modes) are injected dynamically into the user-side prompt at runtime by an orchestrating application.

---

## **4.0 External System Integration (Tools)**

### **4.1 `<tool_definitions>`**
- **Purpose:** To provide a complete technical specification for all available external tools.
- **Implementation Guidelines (What to Include):**
  - A precise, unambiguous `description` of the tool's function and, most importantly, its intended use case. The agent's decision to use a tool is primarily based on this field.
  - A strict schema for `parameters`, defining the `name`, `type`, `description`, and `required` status for each.
- **Anti-Patterns (What to Avoid):**
  - Vague descriptions like "searches the web." Be specific: "retrieves the top 5 search results for a given query from the Google News API."

### **4.2 `<tool_usage_strategy>`**
- **Purpose:** To provide the agent with a strategic framework for tool use.
- **Implementation Guidelines (What to Include):**
  - Heuristics for tool selection.
  - A mandatory planning step (CoT for tools) before execution.
  - Protocols for handling API errors or empty results (e.g., "If a tool fails, retry once, then attempt an alternative tool or report failure").
  - A directive to *analyze and synthesize* tool outputs, not just present the raw data.
- **Anti-Patterns (What to Avoid):**
  - Assuming the agent will intuitively know how to use the tools. You must explicitly teach it the strategy.

---

## **5.0 API Parameter Control**

These parameters are configured at the API call level, not within the prompt text, but they are critical for controlling the agent's behavior.

### **5.1 `reasoning_effort`**
- **Function:** Controls the computational resources and depth allocated to the agent's internal reasoning process before it generates a response. It does *not* directly affect the length of the final output.
- **Use Cases (When to Use):**
  - **`high`:** For tasks requiring complex, multi-step logic, mathematical reasoning, causal analysis, or deep strategic planning. Use when the quality and correctness of the reasoning are paramount.
  - **`medium` (default):** A balanced setting for general-purpose tasks like summarization, drafting, and standard Q&A.
  - **`low` / `minimal`:** For tasks that are highly latency-sensitive and require simple, direct responses (e.g., classification, simple data extraction, chatbot-style interactions).
- **Contraindications (When to Avoid):**
  - Avoid `high` in real-time applications where response latency is a critical factor.
  - Avoid `low` / `minimal` for any task that involves ambiguity, requires planning, or has a high cost of error.

### **5.2 `verbosity`**
- **Function:** Controls the length and detail of the **final generated output**. It is decoupled from `reasoning_effort`. An agent can use high reasoning effort to produce a very concise, accurate answer.
- **Use Cases (When to Use):**
  - **`high`:** For tasks requiring detailed explanations, narrative generation, long-form content creation, or educational responses.
  - **`medium` (default):** For standard conversational responses and reports.
  - **`low`:** For tasks that require concise outputs, such as generating headlines, labels, or data for structured fields (e.g., JSON values). Ideal for when the output will be parsed by another machine.
- **Contraindications (When to Avoid):**
  - Avoid `high` when the output is intended for a system with strict length limits or when the user desires a quick, to-the-point answer.
  - Avoid `low` when the task requires explanation, justification, or the presentation of evidence.
