# CertOrganizer: Automate Your Participation Certificate Management

This Python script streamlines the process of moving your participation certificates from your Downloads folder to a dedicated folder.

**Benefits:**

* Simplifies organization of your certificates.
* Saves time by automating repetitive tasks.
* Reduces the risk of losing certificates in cluttered Downloads.

**Prerequisites:**

* Python 3 (You can check your version by running `python --version` in your terminal.)

**Instructions:**

1. **Download and Save the Script:**
   - Download the script and save it as a Python file (e.g., `cert_organizer.py`).

2. **Customize Paths:**
   - Open the script in a text editor.
   - Update `source_folder` and `destination_folder` variables with the actual paths on your system.
     - Replace `"C:/Users/YourUsername/Downloads"` with your Downloads folder path.
     - Replace `"C:/MyCertificates"` with your desired destination folder path (create it if it doesn't exist).

3. **Run the Script:**
   - Open a terminal or command prompt, navigate to the directory where you saved the script.
   - Run the script using `python cert_organizer.py`.

**Explanation:**

The script utilizes the `os` module to interact with your operating system's file system. Here's a breakdown of the key steps:

* **Import:** The `import os` line imports the `os` module.
* **Folder Paths:** `source_folder` and `destination_folder` variables define the source and destination paths for certificate files (replace with your actual paths).
* **File Loop:** The `for filename in os.listdir(source_folder)` loop iterates through all files in the source folder.
* **Certificate Check:** The `if "Participation Certificate" in filename:` condition checks if the filename contains the phrase "Participation Certificate" (ignoring case).
* **File Paths Construction:** `os.path.join()` constructs the full paths for the source (`source_path`) and destination (`destination_path`) files using the filename and folder paths.
* **File Movement:** The `try...except` block attempts to move the file using `os.replace()`.
   - If successful, a message indicating successful movement is printed.
   - If an error occurs, an error message is printed along with the error details.
* **Completion Message:** The `print("Done!")` line indicates that the script has finished processing the files.

**Additional Notes:**

* This script moves files containing the exact phrase "Participation Certificate" (case-insensitive). You can modify the condition to match your specific certificate filenames.
* Consider adding error handling for cases where the source folder doesn't exist or the destination folder can't be accessed.

**Enjoy the automated organization of your participation certificates!**
