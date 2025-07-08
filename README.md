# Context Management - Large File Refactoring Challenge

##  Challenge Overview
You have a monolithic Python file (`monolithic_data_processor.py`) that contains over 500 lines of code doing EVERYTHING in one place. Your job is to use Cursor's context management features to break this monster into proper modular components.

##  The Problem
The `monolithic_data_processor.py` file contains:
- Database operations (connection, queries, schema creation)
- File I/O operations (CSV, JSON, Excel handling)
- Data transformations (cleaning, scaling, encoding)
- Reporting logic (HTML, text, email reports)
- Configuration management (settings, environment variables)
- Backup and maintenance utilities
- Logging and error handling
- Email notifications
- Data visualizations
- Statistics calculations

**This is a maintenance nightmare!** It violates the Single Responsibility Principle and makes the code hard to test, debug, and maintain.

##  Your Mission
Use Cursor's context management to refactor this monolithic file into a proper modular structure:


##  Success Criteria

### Phase 1: Context Analysis 
1. **Add the monolithic file to Cursor's context**
2. **Ask Cursor to analyse the file structure** and identify the main responsibilities
3. **Document what modules you should create** based on the analysis

### Phase 2: Module Creation 
1. **Use Cursor to extract database-related code** into `database/` modules
2. **Create file handler modules** for different file types
3. **Separate data transformation logic** into dedicated modules
4. **Extract reporting functionality** into its own module
5. **Create configuration management** module
6. **Set up utilities** for logging, backup, validation

### Phase 3: Integration 
1. **Create a new main.py** that orchestrates all the modules
2. **Ensure all imports work correctly**
3. **Test that the refactored version maintains the same functionality**

### Phase 4: Context Strategy Documentation 
Document your context management strategy:
- What did you include/exclude from context at each step?
- How did you manage context size when working with large files?
- What challenges did you face with context management?

##  Submission Requirements

### 1. Refactored Code Structure
- All modules properly separated
- Clean imports and dependencies
- Working main.py that orchestrates everything

### 2. Context Management Report
```markdown
## Context Management Strategy Report

### Phase 1: Initial Analysis
- **Context Used**: [What files/sections you included]
- **Cursor Prompts**: [Key questions you asked]
- **Insights Gained**: [What you learned about the structure]

### Phase 2: Module Extraction
- **Context Strategy**: [How you managed context for each module]
- **Challenges**: [Context size issues, complexity problems]
- **Solutions**: [How you solved context management issues]

### Phase 3: Integration
- **Context Decisions**: [What you included when creating main.py]
- **Testing Approach**: [How you verified functionality]

### Lessons Learned
- **Context Management Best Practices**: [What worked well]
- **What I'd Do Differently**: [Improvements for next time]
- **Key Insights**: [Understanding gained about modular architecture]
```

### 3. Before/After Comparison
- Screenshot or summary of the original monolithic structure
- Screenshot or summary of the new modular structure
- Brief explanation of the benefits gained

##  Advanced Challenge 
1. **Add proper error handling** to each module
2. **Create unit tests** for each module
3. **Add type hints** throughout the codebase
4. **Create a proper package structure** with setup.py
5. **Add documentation** for each module

##  Context Management Tips
- **Start Small**: Don't try to include the entire file at once
- **Focus on One Module**: Work on one logical component at a time
- **Use Specific Selections**: Highlight specific functions/classes rather than entire files
- **Document Dependencies**: Keep track of what each module needs
- **Test Incrementally**: Verify each module works before moving to the next


## Target Structure:
```
refactored_project/
├── database/
│   ├── __init__.py
│   ├── connection.py
│   └── schemas.py
├── file_handlers/
│   ├── __init__.py
│   ├── csv_processor.py
│   ├── json_processor.py
│   └── excel_processor.py
├── transformers/
│   ├── __init__.py
│   ├── data_cleaner.py
│   ├── data_scaler.py
│   └── feature_engineer.py
├── reports/
│   ├── __init__.py
│   ├── generator.py
│   ├── html_formatter.py
│   └── email_sender.py
├── config/
│   ├── __init__.py
│   └── settings.py
├── utils/
│   ├── __init__.py
│   ├── logging_setup.py
│   ├── backup_manager.py
│   └── file_validator.py
├── visualizations/
│   ├── __init__.py
│   └── chart_generator.py
└── main.py
```


---

**This challenge teaches you to use Cursor's context management strategically for large-scale refactoring projects.** 
