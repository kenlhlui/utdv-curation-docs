---
title: Installation
description: Instructions for installing the U of T Dataverse Curation Tool

---
!!! note

    The below instruction is for the testing phase use only.


To install the U of T Dataverse Curation Tool on a Windows local machine, follow the steps below:

# Prerequisites
1. [Git](https://git-scm.com/)
2. [uv](https://docs.astral.sh/uv/)
3. [VS Code](https://code.visualstudio.com/)

# Steps
1. First, install the prerequisites if you haven't already. You can download Git from [here](https://git-scm.com/downloads) and uv from [here](https://pypi.org/project/uv/). For VS Code, you can download it from [here](https://code.visualstudio.com/).
   1. Remember to select the option 'Git Credential Manager' during Git installation.
2. If the tool's GitHub repository remains private, you will need to request access from Ken. Authenticate with Github using the Git Credential Manager when prompted.
3. Clone the repository to your local machine using the in a PowerShell terminal:
   ```powershell
   git clone https://github.com/kenlhlui/pydatacuration-p.git
   ```
4. Navigate to the cloned repository:
   ```powershell
    cd pydatacuration-p
   ```
5. Make a directory called 'workdir' for the tool to use as a workspace:
   ```powershell
   mkdir workdir
   ```
6. Install the required dependencies using uv:
   ```powershell
   uv sync
   ```
7. Open the project in VS Code and create a `.env` file in the root directory. Populate it with the required environment variables, referring to [app_settings.py](https://github.com/kenlhlui/pydatacuration-p/blob/main/pydatacuration/backend/models/app_settings.py). For faster testing, you may also include default values from [setup_form.py](https://github.com/kenlhlui/pydatacuration-p/blob/main/pydatacuration/backend/models/setup_form.py).
:
   ```env
    # App Settings
    app_title='U of T Dataverse Curation Tool'
    log_level='DEBUG'

    # Default values for setup form (for faster testing)
    base_url='https://borealisdata.ca/'
    api_token='YOUR_API_TOKEN'
    curator_name='YOUR_NAME'
    curator_email='YOUR_EMAIL'
    collection_alias='toronto' # The alias for U of T Dataverse collection on Borealis
   ```

8. Run the application using uv:
   ```powershell
   uv run --env-file .env app.py
   ```

You should be able to access the tool at `http://localhost:9005` in your web browser.

Go to the next page for the testing instructions: [Testing](./testing.md)