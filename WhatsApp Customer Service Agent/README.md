# WhatsApp Customer Service Agent

24/7 AI-powered WhatsApp assistant that answers customer questions using your company's internal knowledge from Google Docs. Perfect for businesses that need instant customer support without human intervention.

## How it works

Customers text questions to your WhatsApp Business number, and the AI reads your company's Google Doc in real-time to provide accurate, contextual responses. All conversations are logged for reporting and the system handles WhatsApp's 24-hour messaging window automatically.

**Key Features:**
- Real-time Google Docs integration for up-to-date information
- Smart date awareness (understands closures, schedules, etc.)
- Automatic conversation logging to Google Sheets
- 24-hour messaging window compliance
- Memory across conversations for better context
- Clean, professional responses without AI disclaimers

## Setup Requirements

### WhatsApp Business API
- Meta WhatsApp Cloud API account
- Verified phone number ID
- Webhook configuration

### Google Services
- Google Docs with your company information
- Google Sheets for conversation logging
- Appropriate OAuth permissions

### AI Model
- Anthropic Claude API key (or OpenAI alternative)
- Configured chat model in n8n

## Configuration

1. **Update WhatsApp credentials** in both trigger and action nodes
2. **Set your Google Doc ID** in the "company's knowledge" node
3. **Configure Google Sheets** for logging (update spreadsheet ID)
4. **Customize the AI system message** to match your brand voice
5. **Set up webhook URL** with Meta WhatsApp API

## Usage

Once configured, customers can:
- Send free-form questions to your WhatsApp number
- Get instant responses based on your documentation
- Receive date-aware information (e.g., current hours, closures)
- Continue conversations with context memory

The system automatically:
- Checks messaging window compliance
- Logs all interactions to Google Sheets
- Handles template messages for window reopening
- Cleans responses for professional formatting

## Technical Details

**Nodes used:**
- WhatsApp Trigger (incoming messages)
- Google Docs (knowledge retrieval)
- AI Transform (prompt preparation)
- Anthropic Chat Model (response generation)
- Code nodes (date handling, formatting)
- Google Sheets (logging)
- WhatsApp (outgoing messages)

**File:** `whatsapp-customer-service-agent.json`