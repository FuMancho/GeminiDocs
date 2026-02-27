# Getting Started with Gemini Code Assist

Gemini Code Assist is a powerful development companion integrated directly into your IDE through the Google Cloud Code plugin. It assists throughout the software development lifecycle.

## Supported Environments
Gemini Code Assist is available in:
*   Visual Studio Code (VS Code)
*   JetBrains IDEs (IntelliJ, PyCharm, WebStorm, etc.)
*   Android Studio
*   Google Cloud Workstations
*   Google Cloud Shell Editor

## Installation (VS Code / JetBrains)

1. Open your IDE's Extensions or Plugins marketplace.
2. Search for **Google Cloud Code**.
3. Install the extension.
4. Restart your IDE if prompted.

## Connecting and Authenticating

Once the Cloud Code plugin is installed, you must connect it to a Google Cloud project with the necessary APIs enabled.

1. Click on the **Gemini** icon in your IDE's activity bar or status bar.
2. You will be prompted to "Sign in to Google Cloud".
3. Authenticate with your Google account via the browser pop-up. Ensure your browser is not blocking popups from localhost during this step.
4. When prompted by the IDE, select a Google Cloud project where the **Gemini for Google Cloud API** is enabled. If you do not have a project, you must create one in the Google Cloud Console and enable the billing account associated with it.

### Verifying Authentication
To confirm successful authentication, look for the Gemini spark icon in your IDE status bar. It should be fully lit (not grayed out) and hovering over it should display "Gemini: Ready".

> [!IMPORTANT]
> For enterprise users, your organization administrator must have assigned a license to you and granted the appropriate IAM roles before you can use the service.

## First Steps: Interactive Prompting

Gemini provides multiple ways to interact. Here are a few initial examples to test your setup:

### Example 1: Inline Code Generation
Try writing a descriptive comment above a new function:
```python
# Create a Python function to parse a CSV file, calculate the average of the 'price' column, and return a dictionary grouping items by 'category'
```
Press `Enter`, and Gemini Code Assist will suggest the implementation in gray text. Press `Tab` to accept it.

### Example 2: Explaining Code
Highlight an existing block of complex code. Right-click and select **Gemini > Explain this**. The Gemini chat pane will open with a step-by-step breakdown of what the highlighted code does.

### Example 3: Chatting with your Codebase
Open the Gemini chat pane and ask a project-wide question:
> *"Where is the authentication logic handled in this repository, and what JWT library are we using?"*
