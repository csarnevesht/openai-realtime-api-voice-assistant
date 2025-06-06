# OpenAI Realtime API Voice Assistant

This project implements an AI-powered inbound call agent for Bart's Automotive, a fictional automotive business. It uses OpenAI's new realtime API and integrates with Twilio to handle incoming phone calls.

## Video Instructions

- https://youtu.be/AZ0WziqO_QA?si=HORqrwjrbKnsuRZY  Part 1
- https://www.youtube.com/watch?v=ffDm4HVGuTM&t=11s Part 2

## Features

- Handles incoming calls using Twilio's voice services
- Utilizes OpenAI's realtime API for natural language processing
- Transcribes user speech and generates AI responses in real-time
- Extracts customer details (name, availability, and special notes) from the conversation
- Sends extracted information to a webhook for further processing

## Technologies Used

- Node.js
- Fastify (web framework)
- WebSocket (for real-time communication)
- OpenAI GPT-4 Realtime API
- Twilio (for telephony services)
- dotenv (for environment variable management)

## Setup

1. Clone the repository:
   ```
   git clone https://github.com/Barty-Bart/openai-realtime-api-voice-assistant.git
   cd openai-realtime-api-voice-assistant
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Set up environment variables:
   Create a `.env` file in the root directory and add the following:
   ```
   OPENAI_API_KEY=your_openai_api_key
   ```
   Replace `your_openai_api_key` with your actual OpenAI API key.

4. Update the webhook URL:
   Open the `index.js` file and locate the `WEBHOOK_URL` constant. Replace the existing URL with your own webhook URL:
   ```javascript
   const WEBHOOK_URL = "https://your-webhook-url.com";
   ```

5. Start the server:
   ```
   npm start
   ```

## Usage

Once the server is running, it will handle incoming Twilio calls. The AI agent will engage with callers, transcribe their speech, generate appropriate responses, and extract relevant information from the conversation.

## Note

This project is a demonstration and should be adapted for production use, including proper error handling, security measures, and compliance with relevant regulations.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## Other notes

This project uses n8n with a workflow that has a webhook url and is connected to Google sheets api.
n8n is self-hosted in render.com at:
https://dashboard.render.com/web/srv-d000gcuuk2gs73dohd50
The n8n url is: https://n8n-i718.onrender.com/workflow/k9wFsw1vXaKmv6JQ
The workflow json is in file n8n_contact_spreadsheet.json
The twillio phone number is: (833) 702-6167
OpenAPI info: https://platform.openai.com/api-keys
Google sheet: openai-realtime-api-voice-assistant




