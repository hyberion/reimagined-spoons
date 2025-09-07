# Writer's Companion - Project Plan

## Vision
A web-based storytelling tool designed for overwhelmed, self-doubting writers who struggle to finish projects. Built to gently guide writers through the creative process without judgment, helping them stay engaged with their stories and actually complete them.

## Core Problem
Writers (especially those with ADHD, low self-esteem, perfectionism) abandon projects due to:
- Overwhelming blank page syndrome
- Getting lost in details and losing the big picture
- Internal critic causing premature project abandonment
- Difficulty tracking complex story elements
- Lack of encouraging, non-judgmental support

## Key Principles
- **Helpful, not rigid** - Support writer's natural process rather than imposing dogmatic structure
- **Organic growth** - Let stories and worlds develop naturally
- **Gentle encouragement** - Combat internal critic with supportive guidance
- **Modular flexibility** - Start anywhere, connect everything
- **"Story as metaphor"** - Interface unfolds like a narrative as writer develops their work

## Data Structure

### Hierarchy
```
World (reusable foundation)
├── Story (multiple stories can share same world)
│   ├── Characters (reusable across stories)
│   ├── Structure (story-specific framework)
│   ├── Plot (sequence of events)
│   ├── Themes (why things happen)
│   ├── Scenes (what hangs on structure)
│   └── NPCs (story-specific minor characters)
```

### Core Components
1. **World** - Environment/stage where stories take place
   - Modular containers (history, culture, geography, rules)
   - Research buckets for contemporary/historical fiction
   - Flexible depth (detailed fantasy worlds vs. simple contemporary settings)

2. **Characters** - Reusable, fully-developed people
   - Character ledger automatically tracking actions/development through story
   - Intended character arc vs. organic arc tracking
   - Reusable across multiple stories

3. **Story** - Container that pulls worlds and characters together
   - References world and characters
   - Contains story-specific structure, plot, themes
   - Includes minor NPCs that don't need full character development

4. **Structure** - Narrative framework for the story
5. **Scenes** - Individual story beats that advance plot and develop characters
6. **Themes** - Underlying meaning and message

## Features

### World Building
- Wizard-driven setup based on genre/story type
- "Is this good?" / "Dig deeper" progressive enhancement
- Modular containers that grow with story needs
- Research organization for historical/contemporary fiction
- Multiple stories can share same world

### Character Management
- Automatic character ledger tracking story actions
- Character arc intention vs. reality comparison
- Consistency checking across story appearances
- Reusable characters across multiple stories
- NPC vs. full Character distinction

### Story Development
- Flexible entry points (start with any component)
- "Session 0" guided onboarding
- Interconnected "rooms" for different story aspects
- Conspiracy board visualization of connections
- Progress tracking without pressure

### AI Agents (Specialized)
- **Character Tracker**: Logs character appearances and actions
- **Arc Analyzer**: Compares intended vs. actual character development
- **Continuity Checker**: Flags contradictions and inconsistencies
- **Pacing Monitor**: Identifies momentum issues
- **Theme Tracker**: Identifies emerging thematic elements

### Writing Support
- Daily writing goals with gentle nudging
- Writer's block assistance and prompts
- Scene planning and rearrangement
- National Novel Writing Month integration
- Short story prompt generation
- Craft improvement suggestions

## Technical Stack

### Core Platform
- **Frontend**: React with Vite
- **Backend**: Node.js/Express
- **Database**: PostgreSQL (Digital Ocean Managed)
- **ORM**: Prisma
- **Development Environment**: Wappler (for rapid development, database integration)
- **Hosting**: Digital Ocean (droplets, managed DB, Spaces storage)
- **Containerization**: Docker (via Wappler)

### AI Integration
- **Approach**: Specialized agents rather than monolithic AI
- **Initial**: External APIs (OpenAI, Anthropic) for prototyping
- **Future**: Local models via Ollama for cost control and privacy
- **Target Models**: Llama 3.1 8B, Mistral 7B for basic agents
- **Architecture**: Independent services communicating via REST APIs

### Deployment Strategy
- Use Wappler for core app (CRUD, user management, database relationships)
- Build AI agents as separate Node services
- Clean separation allows independent iteration and testing
- Digital Ocean provides clear scaling path

## Development Phases

### Phase 1: Foundation
- Set up basic Wappler project structure
- Implement core data models (World, Character, Story)
- Basic CRUD operations for all entities
- Simple user authentication

### Phase 2: Core Features
- World building wizard and modular containers
- Character management and basic tracking
- Story creation and organization
- Basic scene management

### Phase 3: AI Integration
- Character ledger tracking (first AI agent)
- Simple continuity checking
- Basic character arc analysis
- API architecture for agent communication

### Phase 4: Enhancement
- Advanced AI agents
- Writing prompts and assistance
- Gamification elements
- NaNoWriMo integration

### Phase 5: Polish
- UI/UX refinement
- Performance optimization
- Local AI model integration
- Advanced visualization features

## Success Metrics
- Writers completing more projects than they abandon
- Reduced time between writing sessions
- Increased confidence in creative decisions
- Active engagement with character and world development tools
- Positive feedback on "gentle encouragement" approach

## Repository Purpose
This document serves as the living specification for development. All architectural decisions, feature requirements, and technical considerations should be tracked here as the project evolves.
