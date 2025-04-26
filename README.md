# agenticMCP
Setup agent MCP's
Agentic Coding MCPs

Overview

Powered by composio this guide provides detailed information on Management Control Panel (MCP) integration capabilities. MCP enables seamless agent workflows by connecting to more than 80 servers, covering development, AI, data management, productivity, cloud storage, e-commerce, finance, communication, and design. Each server offers specialized tools, allowing agents to securely access, automate, and manage external services through a unified and modular system. This approach supports building dynamic, scalable, and intelligent workflows with minimal setup and maximum flexibility.

Install via NPM

npx create-sparc init --force
Available MCP Servers

🛠️ Development & Coding

Service	Description
🐙	GitHub	Repository management, issues, PRs
🦊	GitLab	Repo management, CI/CD pipelines
🧺	Bitbucket	Code collaboration, repo hosting
🐳	DockerHub	Container registry and management
📦	npm	Node.js package registry
🐍	PyPI	Python package index
🤗	HuggingFace Hub	AI model repository
🧠	Cursor	AI-powered code editor
🌊	Windsurf	AI development platform
🤖 AI & Machine Learning

Service	Description
🔥	OpenAI	GPT models, DALL-E, embeddings
🧩	Perplexity AI	AI search and question answering
🧠	Cohere	NLP models
🧬	Replicate	AI model hosting
🎨	Stability AI	Image generation AI
🚀	Groq	High-performance AI inference
📚	LlamaIndex	Data framework for LLMs
🔗	LangChain	Framework for LLM apps
⚡	Vercel AI	AI SDK, fast deployment
🛠️	AutoGen	Multi-agent orchestration
🧑‍🤝‍🧑	CrewAI	Agent team framework
🧠	Huggingface	Model hosting and APIs
📈 Data & Analytics

Service	Description
🛢️	Supabase	Database, Auth, Storage backend
🔍	Ahrefs	SEO analytics
🧮	Code Interpreter	Code execution and data analysis
📅 Productivity & Collaboration

Service	Description
✉️	Gmail	Email service
📹	YouTube	Video sharing platform
👔	LinkedIn	Professional network
📰	HackerNews	Tech news discussions
🗒️	Notion	Knowledge management
💬	Slack	Team communication
✅	Asana	Project management
📋	Trello	Kanban boards
🛠️	Jira	Issue tracking and projects
🎟️	Zendesk	Customer service
🎮	Discord	Community messaging
📲	Telegram	Messaging app
🗂️ File Storage & Management

Service	Description
☁️	Google Drive	Cloud file storage
📦	Dropbox	Cloud file sharing
📁	Box	Enterprise file storage
🪟	OneDrive	Microsoft cloud storage
🧠	Mem0	Knowledge storage, notes
🔎 Search & Web Information

Service	Description
🌐	Composio Search	Unified web search for agents
🛒 E-commerce & Finance

Service	Description
🛍️	Shopify	E-commerce platform
💳	Stripe	Payment processing
💰	PayPal	Online payments
📒	QuickBooks	Accounting software
📈	Xero	Accounting and finance
🏦	Plaid	Financial data APIs
📣 Marketing & Communications

Service	Description
🐒	MailChimp	Email marketing platform
✉️	SendGrid	Email delivery service
📞	Twilio	SMS and calling APIs
💬	Intercom	Customer messaging
🎟️	Freshdesk	Customer support
🛜 Social Media & Publishing

Service	Description
👥	Facebook	Social networking
📷	Instagram	Photo sharing
🐦	Twitter	Microblogging platform
👽	Reddit	Social news aggregation
✍️	Medium	Blogging platform
🌐	WordPress	Website and blog publishing
🌎	Webflow	Web design and hosting
🎨 Design & Digital Assets

Service	Description
🎨	Figma	Collaborative UI design
🎞️	Adobe	Creative tools and software
🗓️ Scheduling & Events

Service	Description
📆	Calendly	Appointment scheduling
🎟️	Eventbrite	Event management and tickets
📅	Calendar Google	Google Calendar Integration
📅	Calendar Outlook	Outlook Calendar Integration
🧩 Using MCP Tools

To use an MCP server:

Connect to the desired MCP endpoint or install server (e.g., Supabase via npx).
Authenticate with your credentials.
Trigger available actions through Roo workflows.
Maintain security and restrict only necessary permissions.
mcp.json
{
  "mcpServers": {
    "supabase": {
      "command": "npx",
      "args": [
        "-y",
        "@supabase/mcp-server-supabase@latest",
        "--access-token",
        "${env:SUPABASE_ACCESS_TOKEN}"
      ],
      "alwaysAllow": [
        "list_tables",
        "execute_sql",
        "listTables",
        "list_projects",
        "list_organizations",
        "get_organization",
        "apply_migration",
        "get_project",
        "execute_query",
        "generate_typescript_types",
        "listProjects"
      ]
    },
    "composio_search": {
      "url": "https://mcp.composio.dev/composio_search/abandoned-creamy-horse-Y39-hm?agent=cursor"
    },
    "mem0": {
      "url": "https://mcp.composio.dev/mem0/abandoned-creamy-horse-Y39-hm?agent=cursor"
    },
    "perplexityai": {
      "url": "https://mcp.composio.dev/perplexityai/abandoned-creamy-horse-Y39-hm?agent=cursor"
    },
    "codeinterpreter": {
      "url": "https://mcp.composio.dev/codeinterpreter/abandoned-creamy-horse-Y39-hm?agent=cursor"
    },
  "gmail": {
    "url": "https://mcp.composio.dev/gmail/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "youtube": {
    "url": "https://mcp.composio.dev/youtube/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "ahrefs": {
    "url": "https://mcp.composio.dev/ahrefs/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "linkedin": {
    "url": "https://mcp.composio.dev/linkedin/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "hackernews": {
    "url": "https://mcp.composio.dev/hackernews/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "notion": {
    "url": "https://mcp.composio.dev/notion/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "slack": {
    "url": "https://mcp.composio.dev/slack/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "asana": {
    "url": "https://mcp.composio.dev/asana/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "trello": {
    "url": "https://mcp.composio.dev/trello/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "jira": {
    "url": "https://mcp.composio.dev/jira/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "zendesk": {
    "url": "https://mcp.composio.dev/zendesk/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "dropbox": {
    "url": "https://mcp.composio.dev/dropbox/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "box": {
    "url": "https://mcp.composio.dev/box/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "onedrive": {
    "url": "https://mcp.composio.dev/onedrive/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "google_drive": {
    "url": "https://mcp.composio.dev/google_drive/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "calendar": {
    "url": "https://mcp.composio.dev/calendar/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "outlook": {
    "url": "https://mcp.composio.dev/outlook/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "salesforce": {
    "url": "https://mcp.composio.dev/salesforce/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "hubspot": {
    "url": "https://mcp.composio.dev/hubspot/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "airtable": {
    "url": "https://mcp.composio.dev/airtable/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "clickup": {
    "url": "https://mcp.composio.dev/clickup/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "monday": {
    "url": "https://mcp.composio.dev/monday/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "linear": {
    "url": "https://mcp.composio.dev/linear/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "intercom": {
    "url": "https://mcp.composio.dev/intercom/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "freshdesk": {
    "url": "https://mcp.composio.dev/freshdesk/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "shopify": {
    "url": "https://mcp.composio.dev/shopify/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "stripe": {
    "url": "https://mcp.composio.dev/stripe/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "paypal": {
    "url": "https://mcp.composio.dev/paypal/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "quickbooks": {
    "url": "https://mcp.composio.dev/quickbooks/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "xero": {
    "url": "https://mcp.composio.dev/xero/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "mailchimp": {
    "url": "https://mcp.composio.dev/mailchimp/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "sendgrid": {
    "url": "https://mcp.composio.dev/sendgrid/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "twilio": {
    "url": "https://mcp.composio.dev/twilio/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "plaid": {
    "url": "https://mcp.composio.dev/plaid/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "zoom": {
    "url": "https://mcp.composio.dev/zoom/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "calendar_google": {
    "url": "https://mcp.composio.dev/calendar_google/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "calendar_outlook": {
    "url": "https://mcp.composio.dev/calendar_outlook/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "discord": {
    "url": "https://mcp.composio.dev/discord/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "telegram": {
    "url": "https://mcp.composio.dev/telegram/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "facebook": {
    "url": "https://mcp.composio.dev/facebook/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "instagram": {
    "url": "https://mcp.composio.dev/instagram/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "twitter": {
    "url": "https://mcp.composio.dev/twitter/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "reddit": {
    "url": "https://mcp.composio.dev/reddit/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "medium": {
    "url": "https://mcp.composio.dev/medium/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "wordpress": {
    "url": "https://mcp.composio.dev/wordpress/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "webflow": {
    "url": "https://mcp.composio.dev/webflow/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "figma": {
    "url": "https://mcp.composio.dev/figma/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "adobe": {
    "url": "https://mcp.composio.dev/adobe/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "calendly": {
    "url": "https://mcp.composio.dev/calendly/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "eventbrite": {
    "url": "https://mcp.composio.dev/eventbrite/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "huggingface": {
    "url": "https://mcp.composio.dev/huggingface/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "openai": {
    "url": "https://mcp.composio.dev/openai/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "replicate": {
    "url": "https://mcp.composio.dev/replicate/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "cohere": {
    "url": "https://mcp.composio.dev/cohere/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "stabilityai": {
    "url": "https://mcp.composio.dev/stabilityai/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "groq": {
    "url": "https://mcp.composio.dev/groq/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "llamaindex": {
    "url": "https://mcp.composio.dev/llamaindex/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "langchain": {
    "url": "https://mcp.composio.dev/langchain/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "vercelai": {
    "url": "https://mcp.composio.dev/vercelai/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "autogen": {
    "url": "https://mcp.composio.dev/autogen/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "crewai": {
    "url": "https://mcp.composio.dev/crewai/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "cursor": {
    "url": "https://mcp.composio.dev/cursor/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "windsurf": {
    "url": "https://mcp.composio.dev/windsurf/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "python": {
    "url": "https://mcp.composio.dev/python/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "nodejs": {
    "url": "https://mcp.composio.dev/nodejs/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "typescript": {
    "url": "https://mcp.composio.dev/typescript/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "github": {
    "url": "https://mcp.composio.dev/github/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "gitlab": {
    "url": "https://mcp.composio.dev/gitlab/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "bitbucket": {
    "url": "https://mcp.composio.dev/bitbucket/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "dockerhub": {
    "url": "https://mcp.composio.dev/dockerhub/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "npm": {
    "url": "https://mcp.composio.dev/npm/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "pypi": {
    "url": "https://mcp.composio.dev/pypi/abandoned-creamy-horse-Y39-hm?agent=cursor"
  },
  "huggingfacehub": {
    "url": "https://mcp.composio.dev/huggingfacehub/abandoned-creamy-horse-Y39-hm?agent=cursor"
  }
  }
}