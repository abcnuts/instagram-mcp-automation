# Instagram MCP Automation

> MCP-powered Instagram automation system for @brandonio31 - AI content generation, scheduling, analytics, and engagement management

## 🎯 Overview

This project is a comprehensive Instagram automation system built using the Model Context Protocol (MCP). It enables natural language commands to manage your entire Instagram presence, from content creation to analytics.

## ✨ Features

### Content Generation
- AI-powered caption generation using Claude
- Content idea generation based on pillars
- Caption refinement and optimization
- Hook-Story-Lesson template support
- Consistent brand voice maintenance

### Publishing & Scheduling
- Automated post scheduling
- Optimal time posting (Mon/Wed/Fri 7 PM, Tue/Thu 9 AM, Sat 2 PM)
- Batch scheduling for weeks/months
- Instagram Graph API integration

### Analytics & Insights
- Performance tracking (likes, comments, reach, engagement rate)
- Growth monitoring
- Content comparison and analysis
- AI-powered insights and recommendations

### Engagement Management
- Comment monitoring and suggested replies
- DM management
- Engagement analytics
- Automated response suggestions

### Calendar Management
- View and manage content calendar
- Update posting schedules
- Content compliance checks
- Weekly/monthly planning

## 🏗️ Architecture

### Tech Stack
- **MCP SDK**: Model Context Protocol for tool orchestration
- **Instagram Graph API v22.0**: Content publishing and analytics
- **Claude API**: AI content generation
- **PostgreSQL**: Database for content and analytics
- **TypeScript + Node.js**: Core implementation

### MCP Tools (15+)
1. `generate_caption` - Create AI-powered captions
2. `generate_content_ideas` - Generate post ideas
3. `refine_caption` - Improve existing captions
4. `schedule_post` - Schedule single posts
5. `schedule_week` - Schedule week of content
6. `schedule_batch` - Batch schedule multiple posts
7. `get_performance` - Get post performance metrics
8. `get_insights` - Get AI-powered insights
9. `compare_posts` - Compare post performance
10. `get_comments` - Retrieve recent comments
11. `suggest_replies` - AI-suggested comment replies
12. `get_dms` - Retrieve direct messages
13. `view_calendar` - View content calendar
14. `update_calendar` - Update calendar entries
15. `check_compliance` - Ensure content compliance

## 🚀 Quick Start

### Prerequisites
- Node.js 18+
- PostgreSQL database
- Instagram Business Account
- Facebook Page (linked to Instagram)
- Claude API key
- Instagram Access Token

### Installation

```bash
# Clone the repository
git clone https://github.com/abcnuts/instagram-mcp-automation.git
cd instagram-mcp-automation

# Install dependencies
npm install

# Set up environment variables
cp .env.example .env
# Edit .env with your credentials

# Initialize database
npm run db:init

# Build the project
npm run build

# Start the MCP server
npm start
```

### Configuration

Create a `.env` file with:

```env
# Instagram API
INSTAGRAM_ACCESS_TOKEN=your_access_token
INSTAGRAM_USER_ID=your_instagram_user_id

# Claude API
CLAUDE_API_KEY=your_claude_api_key

# Database
DATABASE_URL=postgresql://user:password@localhost:5432/instagram_mcp

# Content Calendar
CALENDAR_PATH=./data/content-calendar.json
HASHTAGS_PATH=./data/hashtags.json
```

### Claude Desktop Integration

Add to your Claude Desktop config (`~/Library/Application Support/Claude/claude_desktop_config.json` on Mac):

```json
{
  "mcpServers": {
    "instagram-automation": {
      "command": "node",
      "args": ["/path/to/instagram-mcp-automation/dist/index.js"]
    }
  }
}
```

## 💬 Usage Examples

Once configured, use natural language commands in Claude:

```
"Create captions for Week 1 of my content calendar"
"Schedule this week's posts at optimal times"
"How did my posts perform this month?"
"Check my recent comments and suggest replies"
"Generate 5 content ideas about AI consciousness"
"What's on my calendar for next week?"
```

## 📁 Project Structure

```
instagram-mcp-automation/
├── src/
│   ├── index.ts              # Main MCP server
│   ├── tools/                # MCP tool implementations
│   ├── services/             # Core services
│   │   ├── instagram.ts      # Instagram API service
│   │   ├── claude.ts         # Claude AI service
│   │   └── database.ts       # Database service
│   ├── types/                # TypeScript types
│   └── utils/                # Utility functions
├── data/
│   ├── content-calendar.json # Your content calendar
│   ├── hashtags.json         # Hashtag collections
│   └── brand-voice.json      # Brand voice profile
├── database/
│   └── schema.sql            # Database schema
├── .env.example              # Environment template
├── package.json
├── tsconfig.json
└── README.md
```

## 🔐 Security

- Never commit `.env` or credentials to Git
- Use environment variables for all secrets
- Instagram Access Tokens expire - refresh regularly
- Follow Instagram's Terms of Service and rate limits
- Store sensitive data in PostgreSQL with encryption

## 📊 Content Strategy

**Posting Schedule**: 3x per week
- Monday, Wednesday, Friday: 7 PM
- Tuesday, Thursday: 9 AM
- Saturday: 2 PM

**Content Pillars**:
1. AI & Technology
2. Philosophy & Consciousness
3. Personal Growth
4. Creativity & Innovation

## 🛠️ Development

### Build
```bash
npm run build
```

### Development Mode
```bash
npm run dev
```

### Testing
```bash
npm test
```

### Linting
```bash
npm run lint
```

## 📝 License

MIT License - See LICENSE file for details

## 🤝 Contributing

This is a personal project, but suggestions and improvements are welcome!

## 📧 Contact

Instagram: [@brandonio31](https://instagram.com/brandonio31)
GitHub: [@abcnuts](https://github.com/abcnuts)

---

**Note**: This system respects Instagram's API rate limits and Terms of Service. Always review content before publishing.
