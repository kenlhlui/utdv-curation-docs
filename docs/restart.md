---
title: Restart the tool
description: Instructions for restarting the U of T Dataverse Curation Tool

---

Restart instructions
===


To restart the U of T Dataverse Curation Tool on a Windows local machine, follow the steps below:

# Steps
1. Open a PowerShell terminal. Type (or copy and paste) the following command to change your terminal's directory to the *pydatacuration-p* folder:
   ```powershell
   cd pydatacuration-p
   ```

      You should see the `PS C:\Users\{YourUsername}\pydatacuration-p>` prompt, indicating you are in the correct directory.

2. Run the following command to start VS Code in the current directory:
   ```powershell
   code .
   ```

3. Open the `.env` file in VS Code. Change the value of `API_TOKEN` to your latest API token, especially if you have revoked or generated a new one.

4. Finally, run the application in the PowerShell terminal using the following command:
   ```powershell
   uv run --env-file .env app.py
   ```

# Access the tool
You should be able to access the tool at http://localhost:9005 in your web browser.

# Close the application
To close the application, simply press `Ctrl + C` in the PowerShell terminal.

!!! danger "API Token security tip"

    A best security practice is revoke the API Token in Borealis after you are done using the tool. You can generate a new API token for the next time you use the tool.