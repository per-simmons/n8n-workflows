# Monday.com Lead Enrichment & Email Personalization Workflow

## What It Does

This workflow transforms raw Monday.com leads into qualified opportunities by automatically enriching them with deep company intelligence and generating personalized outreach. It connects directly to your Monday.com board and springs into action whenever a new lead arrives.

## How It Works

### The Process Flow

1. **Webhook Trigger** - Fires when a new lead is added to your Monday.com board
2. **Company Research** - Uses Explorium MCP to gather comprehensive company intelligence
3. **AI Opportunity Analysis** - Identifies specific automation opportunities based on the company's profile
4. **Email Personalization** - Generates a concise, targeted outreach message (under 120 words)
5. **Gmail Integration** - Saves the personalized draft directly to your Gmail drafts folder
6. **Monday.com Update** - Enriches your CRM with all gathered insights and recommendations

### What Gets Enriched

For each lead, the workflow captures:
- **Company Intelligence**: Industry positioning, recent developments, technology stack
- **Business Context**: Current priorities, growth indicators, operational pain points
- **AI Opportunities**: Specific automation use cases tailored to their business model
- **Personalized Outreach**: Draft email that references their actual challenges and proposes relevant solutions
- **Actionable Insights**: Clear recommendations for next steps in the sales process

## Setup Requirements

### Services You'll Need

1. **Monday.com Account** - With webhook permissions
2. **OpenAI API Key** - For GPT-4 processing
3. **Explorium MCP** - For company data enrichment
4. **Gmail OAuth** - For saving email drafts
5. **n8n Instance** - Self-hosted or cloud

### Configuration Steps

1. **Monday.com Setup**
   - Create a webhook integration in your Monday.com board
   - Map the following columns:
     - Lead Email
     - Company Name
     - Company Insights (text column)
     - AI Opportunities (text column)
     - Email Draft (text column)
     - Enrichment Status (status column)
     - Enrichment Date (date column)

2. **OpenAI Configuration**
   - Add your OpenAI API key to n8n credentials
   - Ensure you have GPT-4 access for best results

3. **Gmail Integration**
   - Set up OAuth2 authentication in n8n
   - Grant permissions for draft creation

4. **Webhook URL**
   - Copy the webhook URL from n8n after importing
   - Add it to your Monday.com webhook configuration

## Customization Options

### Adjust Email Length
In the Email Writer Agent node, modify the prompt to change word count limits.

### Add More Data Sources
Extend the Company Researcher Agent to pull from additional APIs or databases.

### Change AI Models
Switch between GPT-4, GPT-4o, or other models based on your needs and budget.

### Modify Enrichment Fields
Add or remove Monday.com columns based on your CRM structure.

## Performance Notes

- **Processing Time**: ~15-30 seconds per lead
- **API Costs**: Approximately $0.05-0.10 per lead (depending on company complexity)
- **Rate Limits**: Consider Monday.com and OpenAI rate limits for bulk processing
- **Webhook Reliability**: Use webhook retry logic for critical leads

## Use Cases

Perfect for:
- B2B sales teams with inbound lead flow
- Companies selling automation or AI solutions
- Teams needing rapid lead qualification
- Organizations prioritizing personalization at scale

## Troubleshooting

**Lead not processing?**
- Check webhook URL configuration
- Verify all API credentials are active
- Ensure Monday.com columns are properly mapped

**Email drafts not appearing?**
- Re-authenticate Gmail OAuth
- Check Gmail API permissions
- Verify email address format

**Enrichment data missing?**
- Validate Explorium MCP connection
- Check company name formatting
- Review API response logs

## Example Output

When a lead for "TechCorp Industries" enters your Monday.com board:

**Company Insights**: "TechCorp Industries is a mid-market manufacturing company with 500+ employees, recently expanded to 3 locations. Uses legacy ERP systems and showing signs of digital transformation initiatives."

**AI Opportunities**: "1) Automated quality control workflows, 2) Predictive maintenance scheduling, 3) Supply chain optimization with real-time alerts"

**Email Draft**: "Hi Sarah, noticed TechCorp's recent expansion to multiple locations. Many manufacturers struggle with maintaining consistent quality control across sites. We've helped similar companies automate their QC workflows, reducing inspection time by 60% while improving accuracy. Worth a quick chat to explore if this could support TechCorp's growth? 15 minutes next Tuesday?"

## Questions or Issues?

This workflow is actively maintained. For issues or suggestions, open an issue in this repository.