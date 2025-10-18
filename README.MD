# 🤖 AI Template: Next.js Application Starter

A structured template for building Next.js applications using AI assistance with proper documentation and workflow management.

## 📋 Overview

This template provides a comprehensive system for developing Next.js applications with AI guidance. It includes organized documentation, phased development approach, and clear workflow management to ensure successful project completion.

## 🚀 Quick Start

### Prerequisites
- Node.js 18+ installed
- Git initialized repository
- Claude Code or similar AI assistant

### Setup Steps

1. **Create your PRD**
   ```bash
   # Create a Product Requirements Document (PRD.md) in the root directory
   # Define your application requirements, features, and technical specifications
   ```

2. **Initialize with AI**
   ```bash
   # Open Claude Code and run:
   "Create me an application based on the PROMPT.md"
   ```

3. **Project Structure Setup**
   - AI will create a nested project structure
   - Main application will be in `/project-name` folder
   - Documentation will be organized in `/docs` folder
   - Control file (`CLAUDE.md`) will be at root level

4. **Configure Git**
   ```bash
   # Update your .gitignore to include the new project structure
   echo "/project-name/" >> .gitignore
   ```

## 📁 Project Structure

```
/your-repository
├── README.md              # This file
├── PRD.md                 # Product Requirements Document (you create this)
├── PROMPT.md              # AI implementation prompt
├── CLAUDE.md              # AI control and status file
├── .gitignore             # Git ignore rules
└── /docs                  # Documentation folder
    ├── PHASES.md          # Development phases breakdown
    ├── TASKS.md           # Detailed task list
    └── PROGRESS.md        # Progress tracking
```

After AI initialization:
```
/your-repository
├── README.md
├── PRD.md
├── PROMPT.md
├── CLAUDE.md
├── .gitignore
├── /docs
│   ├── PHASES.md
│   ├── TASKS.md
│   └── PROGRESS.md
└── /project-name          # ← Your Next.js application
    ├── /app
    ├── /components
    ├── /lib
    ├── package.json
    └── ... (standard Next.js files)
```

## 🛠️ Tech Stack

- **Framework**: Next.js 14+ (App Router)
- **Database**: Supabase
- **Authentication**: Better Auth
- **UI Components**: shadcn/ui
- **Styling**: Tailwind CSS
- **Language**: TypeScript

## 📖 How It Works

### 1. Preparation Phase
- Create your `PRD.md` with detailed requirements
- Review the `PROMPT.md` to understand the AI workflow
- Ensure your repository is properly initialized

### 2. AI-Assisted Development
- AI reads your PRD and creates a structured project plan
- Development is broken into logical phases with clear milestones
- Progress is tracked in real-time through documentation files

### 3. Workflow Management
- Use simple commands to control the AI assistant:
  - `"next"` - Move to next task
  - `"status"` - Check current progress
  - `"review"` - Review implementation
  - `"continue"` - Resume work on current task

### 4. Documentation Updates
- All progress is automatically tracked
- Phase completion is documented
- Task status is maintained in real-time

## 🎯 Key Features

- **Structured Development**: Organized phases with clear objectives
- **Progress Tracking**: Real-time status updates and milestone tracking
- **AI-Powered**: Intelligent code generation and problem-solving
- **Best Practices**: Following Next.js and TypeScript best practices
- **Production Ready**: Built with deployment in mind

## 📝 Required Files

Before starting, ensure you have:

1. **PRD.md** - Your Product Requirements Document
   - Project overview and objectives
   - Feature requirements
   - Technical specifications
   - User stories and acceptance criteria

2. **.gitignore** - Proper git ignore rules
   ```gitignore
   # Dependencies
   node_modules/

   # Environment variables
   .env.local

   # Build output
   .next/
   out/

   # Project folder (if you want to keep repo clean)
   /project-name/
   ```

## 🔄 Development Workflow

1. **Planning**: AI analyzes PRD and creates development phases
2. **Setup**: Initializes Next.js project with proper configuration
3. **Implementation**: Builds features incrementally with proper testing
4. **Documentation**: Maintains up-to-date progress and task tracking
5. **Review**: Regular code reviews and optimization suggestions

## 💡 Tips for Success

- **Be Specific**: The more detailed your PRD, the better the AI implementation
- **Follow Commands**: Use the predefined commands for smooth workflow
- **Check Progress**: Regularly review `PROGRESS.md` and `CLAUDE.md`
- **Iterate**: Don't hesitate to ask for reviews and improvements

## 🤝 Contributing

This template is designed to evolve with feedback. Feel free to suggest improvements to the workflow or documentation structure.

## 📄 License

This template is open source and available under the [MIT License](LICENSE).

---

**Ready to build your next application with AI assistance?** 🚀

1. Create your `PRD.md`
2. Run the AI prompt
3. Watch your application come to life!