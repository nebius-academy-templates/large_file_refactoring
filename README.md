In this task, you'll use Cursor's context management to refactor a monolithic file into a proper modular structure.

## **🔎 Step 1: Understand your context**

<aside>
🛠

Once you log into your GitHub account, the repository for this task will be added automatically. Check that **`monolithic_data_processor.py`** appears in your account.

</aside>

1. Download the file **`monolithic_data_processor.py`**. If you are having issues, try [this link](https://github.com/nebius-academy-templates/monolithic-data-processor) to download the file. 
2. Add the **`monolithic_data_processor.py`** to Cursor's context.
3. Ask Cursor to analyze the file structure and identify its main responsibilities.

## Quiz: Multiple Choice

***Format:** multiple choice*

***Is Blocking:** true*

What does this file do?

- [ ]  Reads data → stores in Postgres → builds dashboards → uploads to S3
- [ ]  Loads CSV/JSON → crunches with Spark → logs to MongoDB → posts reports to Slack
- [ ]  Pulls API data → trains random-forest model → serves predictions via Flask
- [ ]  Ingests data → cleans & plots → records in SQLite → emails + backs up data locally

## 🪄 Step 2: Refactor with Cursor

1. Create a **custom rule** for your project to customize your preferences:
    
    Use Cmd/Ctrl+Shift+P → "Rule" → "Add user rule" or "New Cursor rule" → then create a rule like: `Keep all files under 400 lines`. 
    
    You can also use `@` in chat → Cursor Rules → Add new rules.
    
2. Refactor the code using Cursor.
    
    <aside>
    📌
    
    Please use the **exact** folder names listed below — this is required for the project to pass.
    
    </aside>
    
    - Extract database logic into a `database` folder.
    - Create `file_handlers` modules for different file types.
    - Move data transformation logic into a `transformers` folder.
    - Extract reporting functionality into a `reports` module.
    - Create a configuration management module called `config`.
    - Place utility functions (logging, backup, validation) into a `utils` folder.
    - Create a separate `visualizations` module.
    - Create a new `main.py` that orchestrates all modules.
    - Ensure all imports work correctly.
    - Example structure
        
        This is a reference — it's OK if your solution looks different.
        
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
        
3. **Additionally**:
    - Test that the refactored version maintains the same functionality.
    - Cursor allows you to ignore some files. To use this feature, add a `.cursorignore` file to the root of your codebase and list the directories and files to be ignored. Try it out and test whether Cursor skips the files you've listed.
    - Hint
        
        Check out the [Cursor documentation](https://docs.cursor.com/context/ignore-files) to learn more about how and why you might want to ignore files[.](https://docs.cursor.com/context/ignore-files)
        

## ⬆️ Step 3: Upload for testing

When your files are ready, upload them to GitHub and click "Submit" at the top of the page.
