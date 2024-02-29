# Sample Code for UR5 Robot 
- [Sample Code for UR5 Robot](#sample-code-for-ur5-robot)
  - [1 Installation](#1-installation)
  - [2 Getting Started](#2-getting-started)
    - [2.1 Windows](#21-windows)

## 1 Installation 

Please refer to the [Lab 4 Handout](https://github.com/mit212/lab4_2024?tab=readme-ov-file#02-ur5-rtde) for instructions on how to install the UR Real-Time Data Exchange (RTDE) package. 

## 2 Getting Started

Clone this repository and run `test_import.py`. It should print `Yay! Your import was successful!`. If not, try the following steps. 

### 2.1 Windows

Opening the file in VSCode and clicking "Run" will probably result in a `ModuleNotFoundError`. Since you installed `ur_rtde` via WSL, you also need to run your code via WSL. There are two ways to do this.

**Option 1: VS Code (Recommended)**

1. Open VSCode and install the "WSL" extension by Microsoft.
2. Type "> WSL" in the search bar at the top of the screen. Select "WSL: Open Folder in WSL..." from the dropdown that appears.
3. Navigate to this repository and click "Select Folder". In the pop-up window asking whether you trust the authors of the files in the folder, click "Yes, I trust the authors".
4. Open `test_import.py`. VSCode may ask if you want to install the "Python" extension by Microsoft. Click "Install".
5. Click the play icon at the top-right corner of the screen to run `test_import.py`. VSCode may ask you to choose an interpreter first. Select the option from the dropdown that says "Recommended" on the right side. You should see the success print! 

Note: Only this folder has been opened in WSL, and only in this window. In the future, if you want to open another folder without WSL, you can open it as usual by clicking "File" then "Open Folder...". Similarly, if you want to open another folder with WSL, you can open it by repeating these steps.

**Option 2: WSL Terminal**

1. Open a WSL terminal by entering `wsl` in Command Prompt. Your terminal should say something like `LAPTOP_NAME: mnt/c/Users/yourname$`. This is the current directory. 
2. Since the file you want to run is likely in another folder, we will change the current directory to be that folder. Open File Explorer and navigate to that folder.
3. Right-click the address bar at the top of the screen and select "Copy Address" from the dropdown that appears.

    <details> <summary> Where is the address bar? </summary>


    It is located to the left of the search bar. It should say something like "Documents > MIT > ur_2024".

    </details>

4. Go back to the WSL terminal and type `cd "`. Right-click to paste the address you copied and type `"` at the end. **Don't hit enter yet!**
5. Replace all the `\` with `/` and replace `C:` with `/mnt/c`. Your command should now look like 

    ```
    cd "/mnt/c/Users/yourname/Documents/MIT/ur_2024"
    ```

6. Hit enter. Your terminal should show a new current directory.
   <details> <summary> Directory not found error? </summary>

    Make sure you included the `/` before `mnt`. Also, if your original current directory had a different disk letter, make sure to use that instead of `c`, e.g. `/mnt/e`.
    </details>
7. Enter `python3 test_import.py`. You should see the success print! 

Note: In these steps, we navigated to our desired directory by entering its exact address. In the future, you may prefer to navigate incrementally via the terminal using the basic commands below.
- `ls`: returns the contents of your current directory
- `cd example`: goes to `example` subfolder **within the current directory**
- `cd ..`: goes to the folder that contains your current directory, think of this as going up by a level
