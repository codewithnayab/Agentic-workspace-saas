# Outpost Agent

### AI-Powered Collaborative Workspace for Intelligent Workflows

Outpost Agent is an AI-powered collaborative workspace that brings together intelligent AI agents, interactive canvases, and structured documentation in one place. It helps users organize ideas, visualize complex systems, and work with AI to turn concepts into structured, actionable workflows.

Instead of switching between multiple tools, Outpost provides a unified environment where users can interact with AI, design diagrams, document ideas, and collaborate on projects.

##  Features

- **AI Agent Assistant** — Interact with an AI assistant powered by Google Gemini to generate ideas, answer questions, and assist with workspace tasks.
- **Interactive Canvas** — Create and edit diagrams, visualize relationships, and organize ideas using an interactive canvas.
- **AI-Powered Canvas Actions** — Allow the AI agent to assist with canvas-related operations and structured visual workflows.
- **Collaborative Workspace** — Organize work in dedicated workspaces with support for collaborative editing.
- **Rich Text Documentation** — Write, edit, and organize project documentation using a rich text editor.
- **Real-Time Collaboration** — Keep workspace content synchronized for collaborative workflows.
- **Workspace Management** — Manage projects and workspace content from a centralized dashboard.
- **Authentication & Organizations** — Secure user authentication and organization management.
- **Modern UI** — A responsive interface built with modern web technologies.

## 🛠️ Tech Stack

| Category           | Technologies                 |
| ------------------ | ---------------------------- |
| Frontend           | Next.js, React, TypeScript   |
| Styling            | Tailwind CSS, shadcn/ui      |
| Authentication     | Clerk                        |
| AI Integration     | Google Gemini, Vercel AI SDK |
| Interactive Canvas | tldraw                       |
| Real-Time Sync     | Yjs, Supabase Realtime       |
| Rich Text Editor   | BlockNote                    |
| Database           | PostgreSQL, Supabase         |
| ORM                | Prisma                       |
| Deployment         | Vercel                       |

## 🏗️ Architecture

Outpost Agent combines AI capabilities with interactive workspace tools.

```
                  ┌──────────────────────┐
                  │      User            │
                  └──────────┬───────────┘
                             │
                  ┌──────────▼───────────┐
                  │   Next.js Frontend   │
                  │  React + TypeScript  │
                  └──────────┬───────────┘
                             │
             ┌───────────────┼───────────────┐
             │               │               │
     ┌───────▼──────┐ ┌──────▼──────┐ ┌──────▼──────┐
     │  AI Agent    │ │ Interactive │ │  Workspace  │
     │  Gemini      │ │   Canvas    │ │ Documents   │
     └───────┬──────┘ └──────┬──────┘ └──────┬──────┘
             │               │               │
             └───────────────┼───────────────┘
                             │
                  ┌──────────▼───────────┐
                  │  Backend Services    │
                  │ Prisma + PostgreSQL  │
                  │ Real-Time Sync       │
                  └──────────────────────┘
```

## 🚀 Getting Started

Follow these steps to run Outpost Agent locally.

### 1. Clone the Repository

```
git clone https://github.com/codewithnayab/outpost-agent.git
cd outpost-agent
```

### 2. Install Dependencies

```
npm install
```

### 3. Configure Environment Variables

Create a `.env` file in the root directory:

```
# Database
DATABASE_URL=

# Clerk Authentication
NEXT_PUBLIC_CLERK_PUBLISHABLE_KEY=
CLERK_SECRET_KEY=

# AI Integration
GOOGLE_GENERATIVE_AI_API_KEY=

# Supabase
NEXT_PUBLIC_SUPABASE_URL=
NEXT_PUBLIC_SUPABASE_ANON_KEY=
SUPABASE_SERVICE_ROLE_KEY=
```

Add any additional environment variables required by your project's configuration.

### 4. Set Up the Database

Generate the Prisma client and apply your database migrations:

```
npx prisma generate
npx prisma migrate dev
```

### 5. Start the Development Server

```
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

## 📁 Project Structure

```
outpost-agent/
├── app/
│   ├── (main)/
│   │   └── workspace/
│   │       └── [id]/
│   ├── api/
│   │   └── agent/
│   └── ...
├── actions/
├── lib/
│   ├── agent-tools.ts
│   ├── agent-canvas.ts
│   ├── agent-doc.ts
│   └── ...
├── prisma/
├── components/
├── public/
├── package.json
└── README.md
```

## 🧠 AI Agent Workflow

The AI agent is designed to work alongside the workspace rather than functioning only as a standalone chatbot.

It can assist with:

- Understanding user instructions
- Generating structured content
- Supporting canvas-related operations
- Helping create and organize documentation
- Connecting AI assistance with workspace functionality

The goal is to make AI a practical part of the user's workflow.

## 🔐 Authentication & Data

Outpost Agent uses Clerk for authentication and user management.

Workspace data is managed through PostgreSQL and Prisma, while real-time collaboration is supported through synchronization technologies.

## 🎯 Project Goals

Outpost Agent aims to:

- Make AI-assisted work more interactive
- Simplify the creation of complex diagrams and workflows
- Combine documentation, collaboration, and AI assistance
- Provide a scalable foundation for intelligent workspace applications

## 👨‍💻 Author

**MD Nayab Akhtar**

Full Stack Developer | MERN Stack | GenAI & AI Agents

- GitHub: [@codewithnayab](https://github.com/codewithnayab)

---

⭐ If you find this project interesting, consider giving it a star!

**Before publishing:** Replace the repository URL if your GitHub repository uses a different name, and verify the environment variable names and available npm scripts against your actual project.
