# Prompter - AI Agent Development Assistant

## Welcome to Prompter!

Prompter helps you create specialized AI agents for your development projects using reusable, modular components.

## How This Works

Every command will:
1. **Complete the task** (create project, add agents, etc.)
2. **Show you exactly what was created**
3. **Tell you the specific next command to run**
4. **Explain what that next command will do**

No guessing, no confusion - just clear next steps every time.

## What would you like to do?

**1. 🚀 Create a new project with AI agents**
   - Set up complete project structure (src/, docs/, tests/)
   - Generate specialized AI agents for your tech stack
   - Get ready-to-develop project with documentation
   - **Best for**: Starting a new web app, API, Slack bot, or enterprise project

**2. 🤖 Add AI agents to an existing project**
   - Analyze your existing project structure
   - Generate project-specific AI agents
   - Integrate with your current workflow
   - **Best for**: Adding AI assistance to projects you've already started

**3. 🔧 Build a custom AI agent**
   - Compose agent from reusable components
   - Customize for specific domain or role
   - Advanced agent customization options
   - **Best for**: Creating specialized agents for unique needs

**4. ✅ Validate and improve existing agents**
   - Check agent quality and completeness
   - Identify improvement opportunities
   - Ensure validation protocols are working
   - **Best for**: Quality assurance and optimization

**5. 🔬 Advanced system tools**
   - Component extraction and analysis
   - System validation and optimization
   - Interaction history analysis
   - **Best for**: Prompter system development and research

---

## Choose an option (1-5):

### Option 1: Create New Project
If you want to **start a new project from scratch**, choose this option. You'll get:
- Complete project structure
- Git repository setup
- Project-specific AI agents
- Documentation and workflow guides

**Command**: `.claude/commands/create_new_project.md`

### Option 2: Add Agents to Existing Project
If you have an **existing project** and want to add AI agents, choose this option. You'll get:
- Analysis of your current project
- AI agents configured for your specific codebase
- Integration with existing workflow

**Command**: `.claude/commands/add_agents_to_project.md`

### Option 3: Build Custom Agent
If you need a **specialized AI agent** not covered by standard templates, choose this option. You'll get:
- Component-based agent composition
- Custom role and expertise configuration
- Advanced customization options

**Command**: `.claude/commands/build_custom_agent.md`

### Option 4: Validate and Improve
If you want to **check quality** of existing agents or improve them, choose this option. You'll get:
- Quality assessment of agents
- Improvement recommendations
- Validation protocol verification

**Command**: `.claude/commands/improve_agent_quality.md`

### Option 5: Advanced Tools
If you're working on the **prompter system itself** or need advanced features, choose this option. You'll get:
- Component extraction from existing prompts
- System validation and optimization
- Interaction pattern analysis

**Commands**: See `.claude/commands/system/` directory

---

## Quick Start Examples

### Web Application
```bash
# Direct approach
.claude/commands/create_new_project.md --template web_app --name "my-ecommerce"

# Guided approach
.claude/commands/prompter.md
# → Choose option 1
# → Select web_app template
```

### Slack Bot
```bash
# Direct approach
.claude/commands/create_new_project.md --template slack_app --name "team-bot"

# Guided approach
.claude/commands/prompter.md
# → Choose option 1
# → Select slack_app template
```

### Add Agents to Existing Project
```bash
# Direct approach (from your project directory)
.claude/commands/add_agents_to_project.md --analyze-current

# Guided approach
.claude/commands/prompter.md
# → Choose option 2
# → Follow analysis workflow
```

---

## Need Help?

- **New to Prompter?** Start with Option 1 to see how it works
- **Have a specific project in mind?** Use the direct commands above
- **Not sure what you need?** This guided interface will help you choose
- **Want to learn more?** Check the documentation in `docs/` directory

## Support

- **Documentation**: `docs/QUICK_START.md` and `docs/WORKFLOW_GUIDE.md`
- **Examples**: `examples/` directory for working examples
- **Issues**: Report problems in the GitHub repository
- **Advanced Usage**: Explore `components/` for customization options

---

## After Making Your Choice

When you select an option, I'll guide you through the process and then provide:

1. **Clear completion status** - What was created/accomplished
2. **Specific next commands** - Exactly what to run next
3. **Context explanation** - What each command does for your project

### Example Completion Messages:

**After creating a project:**
```
✅ Project "my-shop" created successfully!

🚀 Next Steps:
1. cd /Users/dawiddutoit/projects/play/my-shop
2. .claude/commands/planner.md
```

**After adding agents:**
```
✅ AI agents added to your project!

🚀 Next Steps:
1. .claude/commands/planner.md
2. .claude/commands/frontend_developer.md
```

---

**Ready to get started?** Choose your option above or run one of the direct commands!