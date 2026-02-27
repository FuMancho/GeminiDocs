# Gemini API Reference

Beyond the IDE extensions, you can integrate Gemini Code and language models directly into your own applications using the Google Cloud Vertex AI API or the Google AI Developer API.

## API Authentication

To call the API, you must obtain an API Key or authenticate via Google Cloud Application Default Credentials (ADC).

### Using an API Key (Google AI Studio)
1. Navigate to Google AI Studio.
2. Click **Get API key** and generate a new key.
3. Export the key in your terminal:
```bash
export GEMINI_API_KEY="your_api_key_here"
```

## Basic REST Endpoint (Generate Content)

The primary endpoint for generating text and code is `generateContent`.

**Endpoint:**
`POST https://generativelanguage.googleapis.com/v1beta/models/gemini-pro:generateContent`

**Sample Request:**
```bash
curl -H 'Content-Type: application/json' \
     -d '{"contents":[{"parts":[{"text":"Write a fast sorting algorithm in Rust."}]}]}' \
     -X POST 'https://generativelanguage.googleapis.com/v1beta/models/gemini-1.5-pro:generateContent?key='${GEMINI_API_KEY}
```

## SDK Integration

Google provides official SDKs for Python, Node.js, Go, and Java.

### Python Example
First, install the SDK:
```bash
pip install -U google-generativeai
```

Then, generate code programmatically:
```python
import google.generativeai as genai
import os

genai.configure(api_key=os.environ["GEMINI_API_KEY"])

model = genai.GenerativeModel('gemini-1.5-pro')
response = model.generate_content("Create a simple Express server in Node.js")

print(response.text)
```

## Handling Responses
The API returns a JSON structure containing the generated candidatures and safety ratings. Ensure your application logic checks the `finishReason` field to confirm the model successfully completed its generation without hitting safety filters or token limits.
