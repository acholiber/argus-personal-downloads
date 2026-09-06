# ARGUS Personal — private tester downloads

Download the Mac or Windows program from [Releases](https://github.com/acholiber/argus-personal-downloads/releases). Choose the asset for your computer, along with START-HERE.txt. The automatically generated “Source code” archives contain this distribution repository's documentation, not the application.

This repository is private. Testers need a GitHub account and an invitation from the owner before they can download. A copied link alone does not grant access.

## Install

- **Mac:** Apple Silicon (M1 or newer), macOS 14+. Extract the ZIP, move ARGUS Personal.app into Applications, and open it. Intel Macs are not supported.
- **Windows:** x64 Windows 10/11. Extract the entire ZIP into a folder you own. Open ARGUS Personal.exe inside the ARGUS Personal folder. Keep the executable and its app folder together.

Python and application dependencies are bundled.

1. Start ARGUS Personal. Its setup page opens in your browser.
2. Choose **Download Ollama**, install that separate program, then return to the ARGUS page. You do not need to select a model inside Ollama.
3. Click the gold **Download local models** button in ARGUS. This authorizes the download. Keep ARGUS open until it says Ready.
4. Choose **Open ARGUS**.

The button is in ARGUS, not inside Ollama or this document. If you lose the page, open **http://127.0.0.1:8789/personal** on the same computer while ARGUS is running. Pilot 2 called the button “Prepare local models”; pilot 3 calls it “Download local models.”

This explicit setup step requires internet and downloads Qwen2.5 7B and nomic-embed-text. Plan for at least 16 GB RAM and 15 GB free storage; speed varies by computer.

**These pilot apps are unsigned and the Mac app is not notarized.** Security software may block them. Report the exact message to the owner; do not disable system-wide security protections. A clean antivirus scan is not a guarantee that software is harmless.

## Test and share feedback

Use nonsensitive examples first and check the answers. Try real questions or documents you deliberately choose to add. In Personal setup, write what you tried, expected, actually received, and whether the result was repeatable or too slow. Choose “Save feedback file,” inspect it, and send it manually through your agreed channel with the owner.

There is no remote support connection, automatic feedback upload, or automatic update check. Feedback does not automatically attach chats, documents, logs, names, or device identifiers. GitHub is used to distribute downloads; it is not connected to the running app. Web search and home-device actions are disabled; voice setup is not included.

## Update or quit

Choose “Quit ARGUS” in Personal setup before replacing the complete application with a newer release. Keep your data folder. Closing the browser tab alone does not quit the program.

- Mac data: `~/Library/Application Support/Argus Personal`
- Windows data: `%LOCALAPPDATA%\Argus Personal`

There is no automatic installation or remote access to your computer. The included program files contain readable Python source. This repository does not contain the development repository or its history.

## Validation

Each release includes checksums and a scan/validation summary. Windows native startup was tested on Windows Server 2022 for pilot 1; Windows 10/11 hardware and inference performance still require tester validation. Read each release's notes for what was checked again.
