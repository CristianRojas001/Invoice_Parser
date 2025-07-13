# Invoice Parser Workflow

This repository contains a single exported **n8n** workflow named `Invoice_Parser_V1.3`.
The workflow automates parsing invoice documents using cloud services and AI nodes.

## Overview

The workflow watches a specific folder on Google Drive. When a new file
appears, it extracts data, processes the content with AI models,
and records the results in Google Sheets. Notifications can be sent via
Slack or Gmail depending on the outcome.

Key node types used in the workflow include:

- `googleDriveTrigger` and `googleDrive` nodes for file handling
- `informationExtractor`, `lmChatGoogleGemini`, and other
  `@n8n/n8n-nodes-langchain` nodes for AI processing
- `googleSheets` to store results
- `gmail` and `slack` for sending notifications

## Importing the Workflow

1. Open your n8n instance.
2. Create a new workflow and choose **Import from File** (or paste the
   contents of `Invoice_Parser_V1.3`).
3. Configure credentials for Google Drive, Google Sheets, Gmail, and Slack
   according to your environment.
4. Activate the workflow when you are ready.

The workflow is inactive by default (`"active": false` in the JSON), so it will
not run until you enable it in n8n.

## File list

```
Invoice_Parser_V1.3  # JSON file with ~1200 lines defining the n8n workflow
```

There is no additional source code in this repository.
