# Features of Gemini Code Assist

Gemini Code Assist leverages Google's Gemini models to provide robust, context-aware coding assistance directly in your IDE.

## Multimodal Capabilities
While primarily focused on code and text, the underlying Gemini architecture inherently understands multiple modalities. This translates to incredibly strong reasoning capabilities when breaking down complex, cross-file logic or answering nuanced architectural questions.

**Coming Soon:** Support for dragging and dropping architecture diagrams directly into the chat pane, allowing Gemini to generate boilerplate infrastructure-as-code or scaffold applications based on visual diagrams.

## Long Context Window & Management
One of Gemini's defining features is its massive context window (1M+ tokens). This allows it to ingest vast amounts of code, documentation, and logs simultaneously.

### Local Codebase Awareness
Because of this large context window, Gemini Code Assist can build a deep understanding of your *entire* local workspace. When you ask a question in the chat interface, it doesn't just look at the open file; it analyzes relevant files across your project to provide highly customized and accurate suggestions.

### Context Indexing
To ensure fast retrieval, Gemini securely indexes your active workspace. You can refine this index by creating a `.geminiignore` file in the root of your project to prevent sensitive or irrelevant files (like compiled binaries or large datasets) from consuming token limits.

## Core Assist Functions
*   **Code Completion:** Multi-line suggestions as you type.
*   **Generate Code:** Write a comment and have Gemini write the code block or function.
*   **Explain Code:** Highlight a complex block of code and ask Gemini to explain what it does step-by-step.
*   **Generate Tests:** Quickly scaffold unit tests for existing functions.
*   **Chat Interface:** A conversational pane inside your IDE to ask questions, solve bugs, or plan out architecture.

> [!TIP]
> When using the chat interface, you can explicitly mention files or symbols (like classes or functions) to ensure Gemini focuses its attention exactly where you need it.
