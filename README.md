# Confluence Page Ownership Transfer

A Python script to bulk transfer ownership of Confluence Cloud pages from one user to another.

## Features

- Transfer ownership of all pages belonging to a specific user
- Option to limit transfers to a specific Confluence space
- Creates a backup of affected pages before making changes
- Detailed logging and progress tracking
- Handles pagination for large Confluence instances

## Requirements

- Python 3.6+
- Required libraries:
  - `requests` library (for API communication)
  - `json` (included in Python standard library)
  - `urllib.parse` (included in Python standard library)
  - `time` (included in Python standard library)
- Confluence Cloud instance
- API token with appropriate permissions

## Usage

1. Clone this repository
2. Run the script:
   ```
   python replaceOwner.py
   ```
3. Follow the interactive prompts:
   - Enter your Confluence email
   - Enter your API token
   - Choose whether to limit to a specific space
   - Enter the current owner's account ID
   - Enter the new owner's account ID
   - Review the list of pages that will be updated
   - Confirm to proceed with the changes

## Before Running

- Modify the base URL in the script to match your Confluence instance domain
- Ensure you have the account IDs for both the current and new page owners
- Make sure your API token has sufficient permissions to modify pages

## Output

The script generates two files:
- `pages_backup.json`: Backup of all pages before changes
- `update_results.json`: Summary of successful and failed updates
