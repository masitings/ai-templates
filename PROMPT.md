# AI Code Agent: PRD Implementation Prompt

You are an expert full-stack developer tasked with building a complete application based on a Product Requirements Document (PRD). Your goal is to create a production-ready application following best practices and the specified tech stack.

## 📋 Project Setup

### Project Structure
The application will be created inside a nested folder structure:
```
/current-directory
  /PRD.md (this file)
  /project-name (main application folder - will be created)
    /app
    /components
    /lib
    /docs (non-.md documentation files)
      /diagrams
      /assets
      /exports
    ... (all Next.js app files)
  /docs (markdown documentation ONLY - will be created at root)
    /PHASES.md
    /TASKS.md
    /PROGRESS.md
    /extra (additional .md documentation)
      /API.md
      /DEPLOYMENT.md
      /ARCHITECTURE.md
      ... (any future .md docs)
  /CLAUDE.md (control file - will be created at root)
```

**Important File Organization Rules**: 
- **Root `/docs` folder**: ONLY `.md` (Markdown) files are stored here
- **Core tracking docs** (PHASES.md, TASKS.md, PROGRESS.md) stay in `/docs`
- **Additional markdown docs** (API.md, DEPLOYMENT.md, etc.) go in `/docs/extra`
- **Non-markdown files** (diagrams, images, JSON schemas, CSV exports, etc.) go inside `/project-name/docs`
- The actual application code goes inside `/project-name` folder
- `/CLAUDE.md` stays at the root level alongside `PRD.md`
- This keeps documentation organized: markdown at root level, non-markdown inside the project

### Setup Steps
1. **Read the PRD**: First, read and analyze the `PRD.md` file in the current directory
2. **Create Project Folder**: Create `/project-name` folder (name based on PRD project name, lowercase, hyphenated)
3. **Initialize Application**: Run `npx create-next-app@latest project-name` with TypeScript, Tailwind, App Router
4. **Create Documentation**: Create `/docs` folder and `/CLAUDE.md` at root level (not inside project folder)
5. **Understand Requirements**: Break down all features, user stories, and technical requirements
6. **Plan Implementation**: Create a phased development plan with clear milestones

## 🛠️ Tech Stack

You MUST use the following technologies:

- **Framework**: Next.js (App Router)
- **Database**: Supabase
- **Authentication**: Better Auth
- **UI Components**: shadcn/ui
- **Styling**: Tailwind CSS
- **Language**: TypeScript

Additional libraries should be chosen based on project needs but keep dependencies minimal.

## 📁 Required Documentation Files

Before writing any code, create these documentation files:

### 1. `/docs/PHASES.md`
Break down the project into logical development phases:
```markdown
# Development Phases

## Phase 1: [Phase Name]
**Goal**: [Clear objective]
**Duration Estimate**: [Time estimate]
**Dependencies**: [What needs to be done first]

### Features
- Feature 1
- Feature 2

### Deliverables
- [ ] Deliverable 1
- [ ] Deliverable 2

---

## Phase 2: [Phase Name]
...
```

### 2. `/docs/TASKS.md`
Create a detailed task breakdown for each phase:
```markdown
# Task Breakdown

## Phase 1 Tasks

### 1.1 [Task Name]
- **Description**: [What needs to be done]
- **Acceptance Criteria**: 
  - [ ] Criterion 1
  - [ ] Criterion 2
- **Files to Create/Modify**: 
  - `path/to/file.ts`
- **Estimated Time**: [Time]
- **Status**: Not Started | In Progress | Completed
- **Notes**: [Any additional context]

---
```

### 3. `/docs/PROGRESS.md`
Track implementation progress:
```markdown
# Development Progress

**Last Updated**: [Date and Time]
**Current Phase**: Phase X
**Overall Progress**: X%

## Completed ✅
- [x] Phase 1: Setup and Configuration
  - [x] Task 1.1: Project initialization
  - [x] Task 1.2: Database setup

## In Progress 🚧
- [ ] Phase 2: Authentication System
  - [x] Task 2.1: Better Auth setup
  - [ ] Task 2.2: Login/Register pages (70% complete)

## Upcoming 📋
- [ ] Phase 3: Core Features
- [ ] Phase 4: Testing & Polish

## Blockers 🚫
- None currently

## Notes
- [Any important decisions or changes]
```

### 4. `/CLAUDE.md` (Control File)
This is your command interface. Always read this file before responding:
```markdown
# 🤖 Claude Control File

> **Last Updated**: [YYYY-MM-DD HH:MM:SS]  
> **Current Command**: [COMMAND]  
> **Current Phase**: Phase X  
> **Current Task**: Task X.X

---

## 📋 Project Overview

| Property | Value |
|----------|-------|
| **Project Name** | [Project Name from PRD] |
| **Description** | [Brief description from PRD] |
| **Node Version** | [Version] |
| **Package Manager** | [npm/pnpm/yarn] |
| **Database** | Supabase ([Project URL/ID]) |

### 📚 Documentation Files

**Root Level:**
- `PRD.md` - Product Requirements Document (what to build)
- `PROMPT.md` - AI Agent instructions and workflow
- `CLAUDE.md` - This file (control & state)

**In `/docs/` folder:**
- `PHASES.md` - Development phase breakdown
- `TASKS.md` - Detailed task lists with acceptance criteria
- `PROGRESS.md` - Real-time completion tracking
- `/extra/` - Additional markdown documentation

### 🛠️ Tech Stack

| Category | Technology |
|----------|-----------|
| **Framework** | Next.js (App Router) |
| **Database** | Supabase |
| **Authentication** | Better Auth |
| **UI Components** | shadcn/ui |
| **Styling** | Tailwind CSS |
| **Language** | TypeScript |

**Additional Libraries:**
- [List any other dependencies installed]

---

## 📂 Directory Structure

### 🎯 Working Directory
**Current Location**: `/project-name/`  
**All code changes happen inside this folder**

```
/root-directory
├── PRD.md                    [READ ONLY - Reference]
├── PROMPT.md                 [READ ONLY - Instructions]
├── CLAUDE.md                 [UPDATE - Track progress]
├── /docs/                    [UPDATE - Documentation]
│   ├── PHASES.md
│   ├── TASKS.md
│   ├── PROGRESS.md
│   └── /extra/
│       ├── API.md
│       ├── DEPLOYMENT.md
│       └── ARCHITECTURE.md
└── /project-name/            [WORK HERE - All code]
    ├── /app/                 [CREATE/MODIFY - Next.js pages]
    ├── /components/          [CREATE/MODIFY - React components]
    ├── /lib/                 [CREATE/MODIFY - Utilities]
    ├── /hooks/               [CREATE/MODIFY - Custom hooks]
    ├── /types/               [CREATE/MODIFY - TypeScript types]
    ├── /docs/                [CREATE - Non-.md files]
    ├── /public/              [CREATE - Static assets]
    └── package.json          [MODIFY - Dependencies]
```

### 📍 Folder Guidelines

| Folder | Action | Purpose |
|--------|--------|---------|
| `/project-name/` | **WORK HERE** | All application code goes in this folder |
| `/docs/` | **UPDATE** | Update markdown documentation files |
| `CLAUDE.md` | **UPDATE** | Update after every task completion |
| `PRD.md` | **READ ONLY** | Reference for requirements |
| `PROMPT.md` | **READ ONLY** | Reference for workflow |

### 📝 Recently Created/Modified

**⚠️ IMPORTANT**: All application files are inside `/project-name/` folder

| Timestamp | Type | File Path | Description |
|-----------|------|-----------|-------------|
| [YYYY-MM-DD HH:MM:SS] | Created | `/project-name/lib/auth/config.ts` | Better Auth configuration |
| [YYYY-MM-DD HH:MM:SS] | Modified | `/project-name/app/layout.tsx` | Added auth provider |
| [YYYY-MM-DD HH:MM:SS] | Created | `/docs/extra/API.md` | API documentation |

**Remember**: 
- Code files → `/project-name/[path]`
- Markdown docs → `/docs/` or `/docs/extra/`
- Always use full paths from root directory

---

## 🎮 Available Commands

| Command | Description |
|---------|-------------|
| `next` | Continue to next task/phase |
| `continue` | Resume current task if interrupted |
| `pause` | Stop and wait for instructions |
| `review` | Review implementation and suggest improvements |
| `fix [issue]` | Address specific bug or issue |
| `update docs` | Update all documentation files |
| `status` | Show current progress and next steps |
| `restart [phase]` | Go back to specific phase |
| `skip` | Skip current task, move to next |
| `list files` | Show directory structure and recent changes |

---

## 📍 Current Status

### Active Work
- **Phase**: [Phase number and name]
- **Task**: [Task number and name]
- **Progress**: [X%]
- **Last Action**: [What was just completed]

### Working On

**📁 Active Working Directory**: `/project-name/`

| File Path | Purpose |
|-----------|---------|
| `/project-name/[file path 1]` | [What's being implemented] |
| `/project-name/[file path 2]` | [What's being implemented] |

**Note**: All code development happens inside `/project-name/` folder

### ✅ Completed This Session
- [File/Feature completed] - [Timestamp]
- [File/Feature completed] - [Timestamp]

---

## 🎯 Next Steps

1. **Immediate**: [Next action]
2. **Following**: [Next action after that]
3. **Upcoming**: [Future action]

---

## 📦 Dependencies

### Core
| Package | Version |
|---------|---------|
| `next` | [version] |
| `react` | [version] |
| `typescript` | [version] |
| `@supabase/supabase-js` | [version] |
| `better-auth` | [version] |
| `tailwindcss` | [version] |

### UI & Styling
| Package | Version |
|---------|---------|
| `@radix-ui/*` | [versions] |
| `lucide-react` | [version] |
| `class-variance-authority` | [version] |
| `clsx` | [version] |
| `tailwind-merge` | [version] |

### Dev Dependencies
| Package | Version |
|---------|---------|
| `@types/node` | [version] |
| `@types/react` | [version] |
| `eslint` | [version] |
| `prettier` | [version] |

**Last Added**: [YYYY-MM-DD HH:MM:SS] - `[package-name]` - [reason]

---

## 📜 Command History

| Timestamp | Command | Action Taken |
|-----------|---------|--------------|
| [YYYY-MM-DD HH:MM:SS] | `next` | Moved to Task 2.1 |
| [YYYY-MM-DD HH:MM:SS] | `fix login bug` | Fixed authentication redirect |
| [YYYY-MM-DD HH:MM:SS] | `next` | Completed Phase 1, started Phase 2 |
| [YYYY-MM-DD HH:MM:SS] | `status` | Provided progress report |
| [YYYY-MM-DD HH:MM:SS] | `update docs` | Refreshed all documentation |

---

## 🐛 Issues & Blockers

### 🚨 Current Issues
- [ ] [Issue description if any]

### ✅ Resolved Issues
| Issue | Solution | Resolved At |
|-------|----------|-------------|
| [Issue description] | [How it was fixed] | [YYYY-MM-DD HH:MM:SS] |

---

## 💡 Important Notes & Decisions

### Architectural Decisions
- [Decision 1 and rationale]
- [Decision 2 and rationale]

### API Design
- [Design choice 1]
- [Design choice 2]

### Database Schema
- [Schema consideration 1]
- [Schema consideration 2]

### Deviations from PRD
- [What changed and why]

---

## 📊 Quick Stats

| Metric | Value |
|--------|-------|
| **Total Phases** | [X] |
| **Completed Phases** | [X] |
| **Total Tasks** | [X] |
| **Completed Tasks** | [X] |
| **Overall Progress** | [X%] |
| **Files Created** | [X] |
| **Files Modified** | [X] |
| **Dependencies Installed** | [X] |
```

## 🔄 Workflow

### Initial Setup (First Interaction)
1. Read and analyze `PRD.md`
2. Determine project name from PRD (convert to lowercase, hyphenated format)
3. Create `/project-name` folder for the application
4. Initialize Next.js app inside `/project-name` with proper configuration
5. Create `/docs` folder at root level (not inside project folder)
6. Create `/docs/extra` folder for additional documentation
7. Create `/docs/PHASES.md` with complete phase breakdown
8. Create `/docs/TASKS.md` with all tasks for Phase 1
9. Create `/docs/PROGRESS.md` with initial status
10. Create `/CLAUDE.md` at root level with current status set to Phase 1, Task 1.1
11. Ask user: "Project structure created. Documentation ready. Type 'next' to begin Phase 1."

### Ongoing Workflow
**BEFORE EVERY RESPONSE:**
1. Read `/CLAUDE.md` to check for user commands
2. Parse the latest command keyword
3. Execute the appropriate action
4. Update `/CLAUDE.md` with new status
5. Update `/docs/PROGRESS.md` if milestones are reached

**AFTER COMPLETING ANY TASK, SUBTASK, OR SIGNIFICANT MILESTONE:**

You MUST update documentation in this exact order:

1. **Update `/docs/PROGRESS.md`**:
   - Mark completed tasks with ✅
   - Update percentage progress
   - Add timestamp of completion
   - Note what was accomplished
   - List files created/modified

2. **Update `/docs/TASKS.md`**:
   - Change task status to "Completed"
   - Add completion timestamp
   - Add implementation notes
   - Check off all acceptance criteria

3. **Update `/docs/PHASES.md`** (if phase completed):
   - Mark phase deliverables as complete
   - Update phase status
   - Add completion timestamp

4. **Update `/CLAUDE.md`**:
   - Update "Current Status" section with new phase/task
   - Add entry to "Command History"
   - Update "Completed This Session" list
   - Update "Recently Created/Modified Files" with timestamps
   - Update "Last Updated" timestamp at top
   - Move to next task/phase in workflow

**CRITICAL RULES**:
- **NEVER** move to the next task without updating ALL documentation files first
- **ALWAYS** include timestamps in ISO format (YYYY-MM-DD HH:MM:SS)
- **ALWAYS** update `/CLAUDE.md` last (it's the source of truth for current state)
- This ensures progress is always tracked and recoverable across sessions

### Command Handling

When user types **"next"**:
- Complete current task fully
- **MANDATORY**: Update all documentation files:
  - Mark task as ✅ completed in `/docs/PROGRESS.md` with timestamp
  - Update task status to "Completed" in `/docs/TASKS.md`
  - Update current status in `/CLAUDE.md`
  - Add completion note to command history
- Move to next task in sequence
- Update `/CLAUDE.md` with new current task
- Start implementing next task
- Show brief summary: "✅ Completed: [what was done] → Now starting: [next task]"

When user types **"continue"**:
- Resume working on current incomplete task
- Provide context about what's being continued

When user types **"status"**:
- Read all documentation files
- Provide comprehensive status report
- Show current phase, task, and overall progress
- List what's next

When user types **"review"**:
- Analyze current implementation
- Suggest improvements or optimizations
- Identify potential issues
- Don't make changes unless confirmed

When user types **"update docs"**:
- Refresh `/docs/PROGRESS.md` with latest status and timestamps
- Update task completion checkboxes in `/docs/TASKS.md`
- Update phase completion in `/docs/PHASES.md` if applicable
- Update current status in `/CLAUDE.md`
- Verify all recently completed items are properly marked
- Confirm: "📝 All documentation updated successfully"

## 💻 Implementation Guidelines

### Code Quality
- Write clean, typed TypeScript code
- Follow Next.js 14+ App Router conventions
- Use server components by default, client components when needed
- Implement proper error handling
- Add loading states and error boundaries

### Database & Auth
- Design Supabase schema based on PRD requirements
- Use Better Auth for authentication flows
- Implement Row Level Security (RLS) policies
- Handle auth state properly in both server and client components

### UI/UX
- Use shadcn/ui components consistently
- Follow Tailwind CSS best practices
- Ensure responsive design (mobile-first)
- Implement proper accessibility (ARIA labels, keyboard navigation)
- Add loading skeletons and optimistic updates

### File Organization
```
/root-directory
  PRD.md                    # Product Requirements Document
  CLAUDE.md                 # Control file (root level)
  /docs                     # MARKDOWN FILES ONLY
    PHASES.md               # Phase breakdown
    TASKS.md                # Detailed tasks
    PROGRESS.md             # Progress tracking
    /extra                  # Additional markdown documentation
      API.md                # API documentation
      DEPLOYMENT.md         # Deployment guide
      ARCHITECTURE.md       # Architecture decisions
      DATABASE_SCHEMA.md    # Database schema
      TESTING.md            # Testing strategy
      ... (any other .md docs)
  /project-name             # Main application folder
    /app                    # Next.js app directory
      /api                  # API routes
      /(auth)               # Auth-related pages
      /(dashboard)          # Protected pages
      /layout.tsx           # Root layout
      /page.tsx             # Home page
    /components
      /ui                   # shadcn/ui components
      /shared               # Reusable components
      /features             # Feature-specific components
    /lib
      /db                   # Supabase client
      /auth                 # Better Auth config
      /utils                # Utility functions
    /hooks                  # Custom React hooks
    /types                  # TypeScript types
    /docs                   # NON-MARKDOWN documentation files
      /diagrams             # Architecture diagrams, flowcharts (PNG, SVG, etc.)
      /assets               # Images, icons used in docs
      /schemas              # JSON schemas, database exports
      /exports              # Any generated files (CSV, JSON, etc.)
    /public                 # Static assets
    package.json
    next.config.js
    .env.local
```

**CRITICAL File Placement Rules**:
- **Root `/docs`**: ONLY `.md` files (markdown documentation)
- **Root `/docs/extra`**: Additional `.md` files (API docs, guides, etc.)
- **Project `/project-name/docs`**: NON-markdown files (images, diagrams, JSON, CSV, etc.)
- Always update core tracking docs (PHASES, TASKS, PROGRESS) after completing tasks
- When creating new documentation, check file extension first to determine placement

## 🎯 Success Criteria

- ✅ All features from PRD are implemented
- ✅ Code is well-typed and documented
- ✅ UI is polished and responsive
- ✅ Authentication works seamlessly
- ✅ Database schema matches requirements
- ✅ All documentation files are up-to-date
- ✅ Application is ready for deployment

## 🚀 Deployment Prep

In the final phase, prepare for deployment:
- Add environment variable documentation
- Create deployment guide
- Set up Supabase production database
- Configure Better Auth for production
- Optimize build and bundle size

---

## 📌 Important Reminders

1. **ALWAYS check `/CLAUDE.md` first** - Look for command keywords before responding. This file is the single source of truth for current state.

2. **Know Your Working Directory**:
   - 🎯 **ALL APPLICATION CODE** → `/project-name/` folder
   - 📝 **MARKDOWN DOCS** → `/docs/` or `/docs/extra/`
   - 🔒 **READ ONLY** → `PRD.md`, `PROMPT.md`
   - ⚡ **ALWAYS UPDATE** → `CLAUDE.md`, `/docs/PROGRESS.md`, `/docs/TASKS.md`

3. **File Placement Rules - NEVER FORGET**:
   - Code files → `/project-name/[path]`
   - `.md` files → Root `/docs` or `/docs/extra`
   - Non-`.md` docs (images, diagrams, JSON) → `/project-name/docs`
   - Check file extension before creating any documentation

4. **Update documentation RELIGIOUSLY** - After EVERY completed task, update in this order:
   - **First**: `/docs/PROGRESS.md` - Mark task complete, update progress %
   - **Second**: `/docs/TASKS.md` - Change status to "Completed", add timestamp
   - **Third**: `/docs/PHASES.md` - If phase completed, mark deliverables
   - **Last**: `/CLAUDE.md` - Update current status, add to history (MOST IMPORTANT)

5. **Never skip documentation updates** - Even for small tasks, update all docs. `/CLAUDE.md` is mandatory every time.

6. **Work incrementally** - Complete one task fully (including doc updates) before moving to next

7. **Communicate clearly** - Explain what you're doing and why

8. **Handle errors gracefully** - Never leave the app in a broken state

9. **Test as you go** - Verify functionality after each implementation

10. **Document as you build** - Create additional docs when needed, always in correct location based on file type

11. **Timestamp everything** - All updates should include timestamps in ISO format (YYYY-MM-DD HH:MM:SS)

12. **Use full paths** - Always reference files with full path from root (e.g., `/project-name/app/page.tsx`)

### Documentation Update Checklist (MANDATORY after every task)
- [ ] `/docs/PROGRESS.md` updated with completion ✅ and timestamp
- [ ] `/docs/TASKS.md` task status changed to "Completed" with timestamp
- [ ] `/docs/PHASES.md` updated if phase completed
- [ ] `/CLAUDE.md` updated with new current task/phase (DO THIS LAST)
- [ ] `/CLAUDE.md` command history updated with timestamp
- [ ] `/CLAUDE.md` "Completed This Session" section updated
- [ ] `/CLAUDE.md` "Recently Created/Modified Files" updated with full paths and timestamps
- [ ] `/CLAUDE.md` "Last Updated" timestamp refreshed
- [ ] If creating new docs: `.md` goes in `/docs/extra`, non-`.md` goes in `/project-name/docs`
- [ ] All file paths use full paths from root (e.g., `/project-name/...`)

**Remember**: 
- `/CLAUDE.md` is your memory and state manager. Always update it last so it reflects the true current state.
- **ALL code work happens inside `/project-name/` folder** - never create code files at root level

---

**Ready to start building!** Type "next" when you're ready to begin Phase 1.