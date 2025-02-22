# Web Automation Study Script

## Description
This repository contains a Tampermonkey userscript designed for educational purposes to demonstrate web automation techniques. The script randomly moves a character in a web-based environment, including diagonal movements, every 3 seconds. It includes functionality to detect specific entities and stop movement upon detection. The script uses JavaScript to interact with web elements, simulate clicks, and handle AJAX requests.

**Important Note**: This script is for educational purposes only and should not be used to automate gameplay in violation of any game's terms of service. Using this script in online games may result in account bans, legal consequences, or negative impacts on game communities. Always respect game developers and community guidelines.

## Features
- Random movement in 8 directions (up, down, left, right, NE, NW, SE, SW) using a random number generator
- Movement occurs every 3 seconds
- Detects specific entities and stops movement upon detection
- Toggle button to start/stop automation
- Extensive debugging logs for troubleshooting
- AJAX fallback for movement simulation

## Educational Purpose
This script is intended to help learners understand:
- DOM manipulation and element selection
- Event simulation (e.g., clicking elements)
- Random number generation for decision-making
- AJAX requests for web interactions
- Error handling and debugging techniques

## Prerequisites
- A modern web browser (e.g., Chrome, Firefox, Edge)
- Tampermonkey browser extension installed
- Basic understanding of JavaScript and web development

## Step-by-Step Instructions for Using the Script
Follow these steps to study and test the script in a controlled, educational environment. These instructions are written in simple language so anyone can understand. **Do not use in live games without explicit permission from game operators, as this could break rules and get you in trouble.**

---

### Step 1: Get the Right Tools
Before you start, you need a web browser (like Google Chrome or Firefox) and a special tool called Tampermonkey. This tool lets you run custom scripts on web pages.

1. **Open Your Web Browser**:
   - Use Google Chrome, Firefox, or Microsoft Edge. These are popular browsers.
   - If you don't have one, download Chrome from [google.com/chrome](https://www.google.com/chrome/) or Firefox from [mozilla.org/firefox](https://www.mozilla.org/firefox/).

2. **Find Tampermonkey**:
   - Tampermonkey is like a helper tool that lets you add custom scripts to web pages.
   - Go to your browser's extension store:
     - For Chrome: Open Chrome, click the three dots in the top-right corner, go to "More Tools" > "Extensions", then click "Open Chrome Web Store" at the bottom.
     - For Firefox: Open Firefox, click the three lines in the top-right corner, go to "Add-ons and Themes".
     - For Edge: Open Edge, click the three dots in the top-right corner, go to "Extensions", then click "Get extensions for Microsoft Edge".

3. **Search for Tampermonkey**:
   - In the extension store, type "Tampermonkey" in the search bar and press Enter.
   - Look for the one called "Tampermonkey" (it usually has a black-and-yellow icon).

4. **Install Tampermonkey**:
   - Click "Add to Chrome" (or "Add to Firefox", or "Get" for Edge).
   - A pop-up will ask if you want to add it. Click "Add extension" or "Add".
   - Wait a few seconds. You'll see a message saying Tampermonkey was added.
   - Check the top-right corner of your browser. You should see a new Tampermonkey icon (black-and-yellow).

5. **Make Sure Tampermonkey is Working**:
   - Click the Tampermonkey icon in the top-right corner of your browser.
   - A menu will pop up. Click "Dashboard".
   - A new tab will open with the Tampermonkey Dashboard. This means it's working.
   - If you don't see the icon, go back to the extension store and make sure it's enabled.

---

### Step 2: Add the Script to Tampermonkey
Now that you have Tampermonkey, you need to add the script to it. The script is like a set of instructions for the browser to follow.

1. **Find the Script**:
   - The script is in a file called `script.js` in this repository.
   - Open the repository on GitHub (where you found this README).
   - Click on `script.js` to open it.
   - You'll see a lot of text (code). Don't worry, you don't need to understand it all yet.

2. **Copy the Script**:
   - Click anywhere on the code in `script.js`.
   - Press Ctrl+A (or Cmd+A on a Mac) to select all the text.
   - Press Ctrl+C (or Cmd+C on a Mac) to copy it.
   - Now the script is copied to your computer's clipboard (like copying text in a document).

3. **Open Tampermonkey Dashboard**:
   - Click the Tampermonkey icon in the top-right corner of your browser.
   - Click "Dashboard" from the menu.
   - A new tab will open with the Tampermonkey Dashboard.

4. **Create a New Script**:
   - In the Dashboard, look for a "+" tab at the top (next to "Installed userscripts").
   - Click the "+" tab. This opens a new script editor.
   - You'll see some default text (code) in the editor. You need to replace it.

5. **Paste the Script**:
   - Click anywhere in the editor where the default text is.
   - Press Ctrl+A (or Cmd+A on a Mac) to select all the default text.
   - Press Delete or Backspace to remove it.
   - Now press Ctrl+V (or Cmd+V on a Mac) to paste the script you copied from `script.js`.
   - The editor should now show the new script.

6. **Save the Script**:
   - Press Ctrl+S (or Cmd+S on a Mac) to save the script.
   - Or click "File" in the top-left corner of the editor, then click "Save".
   - You'll see a message saying "Script saved".
   - The script is now ready to use, but only in a test environment.

---

### Step 3: Set Up a Test Environment
The script is designed for learning, not for playing games automatically. You need a safe test environment (like a local web page) to study how it works. Do not use it in real games, as this could break rules and get you banned.

1. **Understand the Script's Purpose**:
   - The script moves a character randomly in 8 directions (up, down, left, right, and diagonals) every 3 seconds.
   - It also looks for specific things (entities) on the page and stops moving if it finds one.
   - For learning, you need to test it on a web page you control, not a real game.

2. **Create a Simple Test Page (Optional)**:
   - If you want to test the script, you can make a simple web page on your computer:
     - Open Notepad (Windows) or TextEdit (Mac).
     - Copy and paste this simple HTML code:
       ```html
       <!DOCTYPE html>
       <html>
       <head>
           <title>Test Page</title>
       </head>
       <body>
           <h1>Test Environment</h1>
           <div id="dr-nw" class="m-move">NW</div>
           <div id="dr-n" class="m-move">N</div>
           <div id="dr-ne" class="m-move">NE</div>
           <div id="dr-e" class="m-move">E</div>
           <div id="dr-w" class="m-move">W</div>
           <div id="dr-se" class="m-move">SE</div>
           <div id="dr-s" class="m-move">S</div>
           <div id="dr-sw" class="m-move">SW</div>
           <div class="wild-pokemon-name">example1</div>
       </body>
       </html>
       ```
     - Save the file as `test.html` on your desktop (make sure it ends with `.html`).
     - Open the file in your browser by double-clicking it.
   - This page has fake movement buttons and an entity for testing.

3. **Change the Script's URL (For Testing)**:
   - Go back to the Tampermonkey Dashboard.
   - Open your script (click on its name in the list).
   - Look for the line that says:
     ```javascript
     // @match        https://example.com/map/*
     ```
   - Change it to match your test page. For example:
     ```javascript
     // @match        https://www.delugerpg.com/map/overworld5
     ```
     - Replace `C:/Users/YourName/Desktop/test.html` with the actual path to your `test.html` file.
   - Save the script (Ctrl+S or File > Save).

4. **Do Not Use in Real Games**:
   - The script has placeholders (like `https://example.com/map/*` and `entities = ['example1', 'example2']`) to avoid game-specific automation.
   - Do not change these to match a real game
