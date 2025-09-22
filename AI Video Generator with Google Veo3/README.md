# AI Video Generator with Google Veo3

## What It Does

This workflow creates viral video content at scale using Google Veo3 AI. It generates creative video concepts, produces hyper-realistic videos, and automatically distributes them across 9 social media platforms simultaneously.

## How It Works

### The Complete Process

1. **Daily Trigger** - Automatically runs on schedule to generate new content
2. **AI Concept Generation** - Uses GPT-4.1 to create viral video ideas with gaming/entertainment themes
3. **Script Creation** - Generates captions with trending hashtags and engaging descriptions
4. **Prompt Engineering** - Converts concepts into Veo3-compatible cinematic prompts
5. **Video Production** - Calls Google Veo3 API via FAL.ai to create realistic video content
6. **Content Management** - Stores concepts and results in Google Sheets for tracking
7. **Multi-Platform Distribution** - Uses Blotato API to post simultaneously to all platforms

### Supported Platforms

The workflow automatically posts to:
- Instagram
- YouTube (unlisted by default)
- TikTok
- Facebook
- Twitter/X
- LinkedIn
- Threads
- BlueSky
- Pinterest

## Setup Requirements

### API Credentials You'll Need

1. **OpenAI API Key** - For GPT-4.1 concept generation
2. **FAL.ai API Key** - For Google Veo3 video generation
3. **Blotato API Key** - For multi-platform social media posting
4. **Google Sheets OAuth** - For content tracking and management

### Platform Account Setup

1. **Blotato Configuration**
   - Connect all 9 social media accounts to Blotato
   - Get account IDs for each platform
   - Configure posting permissions

2. **Google Sheets Setup**
   - Create tracking spreadsheet with columns:
     - id, idea, caption, production, environment_prompt, final_output, STATUS, row_number

### Configuration Steps

1. **Import Workflow** - Load the JSON into your n8n instance
2. **API Keys** - Configure all credential connections
3. **Social Media IDs** - Update the "Assign Social Media IDs" node with your Blotato account IDs
4. **Google Sheets** - Connect to your tracking spreadsheet
5. **Schedule** - Set your desired trigger frequency (daily recommended)

## Customization Options

### Video Themes
Modify the AI concept generation prompt to focus on different topics:
- Gaming content (default)
- Business/productivity
- Lifestyle content
- Educational content
- Entertainment

### Platform Selection
Disable specific platforms by removing connections from the "Upload Video to Blotato" node.

### Generation Frequency
Adjust the schedule trigger for different posting frequencies:
- Daily (recommended)
- Multiple times per day
- Weekly batches

### Video Style
Customize the Veo3 prompt engineering to create different video styles:
- Documentary style (default)
- Professional presentation
- Casual vlog format
- Cinematic storytelling

## Performance & Costs

### Processing Time
- Concept generation: ~30 seconds
- Video creation: ~5 minutes (Veo3 processing)
- Distribution: ~2-3 minutes
- **Total cycle time**: ~6-8 minutes per video

### API Costs (Estimated)
- OpenAI GPT-4.1: ~$0.02 per video
- Google Veo3 (via FAL.ai): ~$1.50 per video
- Blotato posting: ~$0.10 per video across all platforms
- **Total cost per video**: ~$1.62

### Rate Limits
- Veo3: 10 videos per day (free tier)
- Blotato: Varies by platform
- Consider platform-specific posting limits

## Content Strategy

### Viral Video Concepts
The AI generates ideas focused on:
- Gaming moments and reactions
- Trending topics and hashtags
- Character-driven storytelling
- Engaging visual scenarios

### Hashtag Strategy
Each video gets 12 optimized hashtags:
- 4 topic-relevant tags
- 4 all-time popular tags  
- 4 currently trending tags

### Multi-Platform Optimization
- Instagram: Visual-first with hashtags
- YouTube: SEO-optimized titles and descriptions
- TikTok: Trend-focused with AI generation disclosure
- LinkedIn: Professional angle on content
- Other platforms: Platform-specific optimizations

## Monitoring & Analytics

### Google Sheets Tracking
- Video concepts and prompts
- Generation status and URLs
- Publishing status across platforms
- Performance metrics (manual entry)

### Workflow Monitoring
- n8n execution logs
- Failed generation alerts
- API usage tracking
- Content approval workflow

## Use Cases

Perfect for:
- Content creators scaling video production
- Social media agencies managing multiple accounts
- Businesses needing consistent content output
- Gaming and entertainment brands
- Anyone wanting to test viral video concepts

## Advanced Features

### Quality Control
- Preview videos before distribution
- Manual approval workflow option
- Content moderation integration
- A/B testing different concepts

### Content Variations
- Generate multiple concepts per trigger
- Create platform-specific versions
- Seasonal or event-based themes
- Audience-targeted content variations

## Troubleshooting

**Videos not generating?**
- Check FAL.ai API key and credits
- Verify Veo3 queue status
- Review prompt complexity

**Social media posting failed?**
- Validate Blotato account connections
- Check platform-specific requirements
- Verify content format compatibility

**Low engagement?**
- Analyze hashtag performance
- Adjust concept generation prompts
- Review posting timing and frequency

This workflow transforms the time-intensive process of video creation into a fully automated, scalable content machine that produces professional-quality videos daily across all major social platforms.