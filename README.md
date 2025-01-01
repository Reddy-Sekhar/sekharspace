Generative AI practised files

import openai  # Assuming the Gemini API is OpenAI GPT-based

# Set up the Gemini API key
openai.api_key = "YOUR_GEMINI_API_KEY"

# Use the API to summarize the text
response = openai.Completion.create(
    engine="text-davinci-003",  # Choose the appropriate model
    prompt=f"Summarize the following text:\n{text}",
    max_tokens=100
)

# Extract and print the summary
summary = response.choices[0].text.strip()
print("Text Summary (via Gemini API):", summary)