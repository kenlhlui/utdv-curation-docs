---
title: Restart the tool
description: Instructions for restarting the U of T Dataverse Curation Tool

---

Restart instructions
===



To restart the U of T Dataverse Curation Tool on a Windows local machine, follow the steps below:

# Steps
1. Open a PowerShell terminal.
   
      <video width="100%" controls>
      <source src="assets/videos/open-powershell.mp4" type="video/mp4">
      Your browser does not support the video tag.
      </video>

2. Type (or copy and paste) the following command to change your terminal's directory to the *pydatacuration-p* folder:
   ```powershell
   cd pydatacuration-p
   ```

      <video width="100%" controls>
      <source src="assets/videos/cd-pydatacuration.mp4" type="video/mp4">
      Your browser does not support the video tag.
      </video>


3. Run the following command in the PowerShell terminal to start VS Code in the current directory:
   ```powershell
   code .
   ```
      <video width="100%" controls>
      <source src="assets/videos/enter-vs-code.mp4" type="video/mp4">
      Your browser does not support the video tag.
      </video>

4. Open the `.env` file in VS Code using the left panel. Change the value of `API_TOKEN` to your latest API token, especially if you have revoked or generated a new one. Also change the `CURATOR_NAME` and `CURATOR_EMAIL` if necessary.

      <video width="100%" controls>
      <source src="assets/videos/change-env.mp4" type="video/mp4">
      Your browser does not support the video tag.
      </video>

5. Finally, run the application in the PowerShell terminal using the following command:
   ```powershell
   uv run --env-file .env app.py
   ```

      <video width="100%" controls>
      <source src="assets/videos/uv-run-apppy.mp4" type="video/mp4">
      Your browser does not support the video tag.
      </video>

      You should be able to access the tool at http://localhost:9005 in your web browser.

# Close the application
To close the application, simply press `Ctrl + C` in the PowerShell terminal.

!!! danger "API Token security tip"

    A best security practice is revoke the API Token in Borealis after you are done using the tool. You can generate a new API token for the next time you use the tool.

