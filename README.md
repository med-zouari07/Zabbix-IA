# Zabbix-Gemini AI Integration

## Overview
This repository provides a guide and script to integrate Zabbix, a powerful IT infrastructure monitoring tool, with Google's Gemini AI model. By leveraging Gemini's AI capabilities, users can enhance Zabbix's alerting system by receiving possible causes and solutions for triggered alerts. This integration helps IT teams resolve incidents more efficiently.

### Benefits
- **Mitigate alerts** by providing possible causes and solutions.
- **Reduce incident resolution time.**
- **Enhance decision-making** with AI-driven insights.

This guide explains how to:
- Set up the Google Gemini API.
- Configure a custom script in Zabbix.
- Use the AI assistant in the Zabbix problem panel.

## Prerequisites
- **Zabbix 7.0 or higher:** Ensure you have access to the Zabbix frontend and administrative privileges.
- **Google AI Studio Account:** Create an account and generate an API key for the Gemini model.
- **API Key:** Obtain the API key from Google AI Studio for authentication.

## Steps for Integration

### 1. Set Up Google Gemini API
1. Go to [Google AI Studio](https://ai.google.com/studio/).
2. Create an account and generate an API key for the Gemini model.
3. Save the API key securely; it will be used in the Zabbix script.

### 2. Configure the Script in Zabbix
1. Log in to your Zabbix frontend.
2. Navigate to:
   - **Alerts > Scripts > Create Script**
3. Configure the script as follows:
   - **Name:** Possible cause and solution
   - **Type:** Script
   - **Execute on:** Zabbix server
   - **Script:** Copy and paste the script from this repository.
4. Add the following parameters:
   - `{EVENT.ID}`: Trigger event ID.
   - `{API_KEY}`: Your Google Gemini API key.
5. Save the script.

### 3. Use the AI Assistant in the Problem Panel
1. Navigate to the **Problems** panel in Zabbix.
2. Select a specific alert.
3. Click on **AI Assistant**.
4. Choose the **Possible cause and solution** script.
5. The AI will analyze the alert and provide possible causes and solutions.

## Script Details
The script uses the Google Gemini API to analyze Zabbix alerts. It sends the alert details to the AI model and retrieves a response containing:
- Possible causes of the issue.
- Recommended solutions.

### Script Parameters
- `{EVENT.ID}`: The ID of the triggered event.
- `{API_KEY}`: Your Google Gemini API key.

## Contributing
Contributions are welcome! Feel free to open an issue or submit a pull request if you have improvements or bug fixes.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

