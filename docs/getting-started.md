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
3. Authenticate with your Google account via the browser pop-up.
4. Select a Google Cloud project where the **Gemini for Google Cloud API** is enabled.

> [!IMPORTANT]
> For enterprise users, your organization administrator must have assigned a license to you and granted the appropriate IAM roles before you can use the service.

## First Steps
Try writing a comment above a new function:
```python
# Create a Python function to parse a CSV and return a list of dictionaries
```
Press `Enter`, and Gemini Code Assist will suggest the implementation. Press `Tab` to accept it!
