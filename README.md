# Using V2D - Voice Documentation Tool

## Overview
Voice2Docs is a voice-to-documentation tool that allows you to create and update documentation by speaking naturally. The tool transcribes your speech and converts it into properly formatted markdown.

## Installation of FFmpeg

`ffmepg` is required to be installed on your system to do any audio recording. To install:

- Mac: `brew install ffmpeg`
- Windows: `winget install ffmpeg`
- Linux: `sudo apt install ffmpeg`

## Installation

1. Clone this repository onto your local machine. Take note of where the latest release is in this repository.
1. Open any project in Visual Studio Code or Cursor
2. Navigate to the extensions pane and click the 3 dots in the upper right corner (...)
3. Select the .vsix file in this repository.

Note: This can be installed into Cursor as well.

## Initial Setup

### Authentication
First, log in using your GitHub account. In the Accounts window of your Voice2Docs panel:
1. Select "Login with GitHub" 
2. A new browser window will open
3. Sign in with your GitHub account
4. Complete the authentication process

Once logged in, the accounts section displays:
- Your name
- Current plan/tier
- Usage for this month
- Options to upgrade plan or sign out

> **Important:** Username and password sign-in has not been tested. Use GitHub account authentication only for the time being.

> **Note:** Currently, there is no direct way to upgrade your plan through the interface. Plan upgrades can be processed manually if needed.

### Setting Up Documentation Location
- The documentation route should be auto-detected
- If not detected, right-click and select "Change Docs Location" under the Documentation tab
- The application currently supports markdown files only

## Recording Interface

### Getting Started
Under "Recording and Usage," you'll see a microphone with "Ready to Record" status and a countdown timer. 

**Important limitations:**
- Three-minute recording limit per session to prevent API abuse and protect API keys
- When recording begins, the interface shows "Stop and Process" or "Cancel Recording" options

### Creating New Files and Folders
- Hover over your documentation root
- Click the "New File" button to create a new file
- Click "New Folder" button to create a new folder

### Recording Methods

#### Method 1: General Recording
Use the blue button underneath "Recording and Usage" to select a file to record to.

Note: *this functionality may be deprecated in the future*

#### Method 2: Document-Specific Recording
1. Navigate to the documentation roots section (contains all documents)
2. Hover over any document to reveal a microphone icon
3. Click the microphone icon to start recording immediately for that specific document
4. Alternatively, right-click and select "Record"

### Recording Process
1. Recording starts automatically once initiated
2. The interface updates to show a red "Stop and Process" or "Cancel Recording" bar
3. Record your documentation and edits (3-minute limit)
4. Click "Stop and Process" when finished
5. Wait a few seconds for the diff pop-up to appear
6. Approve or deny the proposed changes

## Processing Workflow

When you stop and process a recording, the following happens automatically:

1. **Upload**: The audio file uploads to the server
2. **Transcription**: Audio gets transcribed to text
3. **Conversion**: Content gets cleaned and converts to markdown format
4. **Integration**: The markdown overwrites the content in the selected target file

## Usage Limits and Notes

### Recording Limits
- There is currently a 3-minute limit per recording session to prevent abuse
- There is a 15-minute total talk limit per month. As part of testing, you can request this to increase if needed.
- Canceled recordings do not count toward usage
- Higher limits may be available in future versions
- Monthly limits can be increased upon request

### Technical Limitations
- The application is not context-aware - it doesn't know other documentation and codebase. This is planned for future iterations.
- The application supports markdown files only currently. Future iterations may support other file types.

## Getting Help

### Bug Reports and Feature Requests
Open an [issue in GitHub](https://github.com/WxBDM/Voice2Docs-Issues/blob/main/README.md) for any bugs encountered or desired features.

For assistance or support issues, reach out directly for help.

---