# Best Practices for Gemini Code Assist

To maximize the quality and accuracy of Gemini Code Assist, follow these prompt engineering best practices and integration guidelines.

## 1. Contextualize Your Prompts

Gemini operates best when given explicit context. Avoid vague instructions.

*   **Bad:** "Fix this."
*   **Good:** "Fix the NullReferenceException in the `calculateTotal` function. It occurs when the `discount_rate` variable is undefined."

## 2. Break Down Complex Tasks

If you need a large feature implemented, ask Gemini to generate it in steps or components rather than all at once.

1.  *"Generate the database schema for a blog application."*
2.  *"Now write the REST API endpoints to fetch those blog posts using Express."*
3.  *"Finally, create a React component that consumes the GET endpoint."*

## 3. Use `@` Mentions in Chat

When using the IDE Chat Pane, take advantage of context variables:
*   Use `@workspace` to force the model to search the entire project for context.
*   Type `@` followed by a filename (e.g., `@utils.js`) to explicitly attach that file to your prompt.
*   Highlight code in your editor; it will automatically be included as context in your next chat message.

## 4. Provide Few-Shot Examples

When generating repetitive code or enforcing a specific styling guideline, provide an example in your prompt.

*"Write a Redux slice for user authentication. Use the following formatting style for actions:*
```javascript
// Example Action Style
export const SET_THEME = 'app/SET_THEME';
```
*"*

## 5. Security and Data Privacy

When working with proprietary codebases:
*   Ensure you understand your organization's data retention policies regarding Cloud Code. Enterprise tiers of Gemini for Google Cloud do not use your proprietary code to train base models.
*   Utilize `.geminiignore` to prevent API keys, `.env` files, or PII from being transmitted to the model during codebase indexing.
