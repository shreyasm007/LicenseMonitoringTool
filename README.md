# License Monitoring Tool

## Overview
The **License Monitoring Tool** is a Node.js-based application designed to track software license expiration dates and send automated email reminders to ensure timely renewal. The tool reads license data from an Excel file, checks for upcoming expirations, and sends notifications via email to responsible users.

## Features
- Parses an Excel file to extract license expiration details.
- Calculates remaining days until expiration.
- Sends automated email reminders for licenses expiring within a defined period.
- Logs email notifications to prevent duplicate alerts.
- Provides an API endpoint to fetch license data in JSON format.
- Implements robust error handling for reliability.

## Tech Stack
- **Backend:** Node.js, Express.js
- **Email Handling:** Nodemailer
- **Excel Processing:** xlsx
- **Middleware:** cors, body-parser
- **File System Operations:** fs (File System module)

## Installation
### Prerequisites
Ensure you have the following installed:
- [Node.js](https://nodejs.org/)
- npm (Node Package Manager)

### Steps to Install & Run
1. Clone the repository:
   ```bash
   git clone https://github.com/shreyasm007/LicenseMonitoringTool.git
   cd LicenseMonitoringTool
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Update configuration:
   - Modify `EXCEL_FILE_PATH` in `index.js` to point to your actual Excel file.
   - Configure email SMTP settings in the `transporter` object.
4. Start the server:
   ```bash
   node index.js
   ```
5. The server will run on `http://localhost:3001`.

## API Endpoints
### Fetch License Data
**GET /excel/json**
- Returns license details from the Excel file in JSON format.

## Email Reminder Logic
1. Reads expiration date and email from the Excel file.
2. Calculates remaining days until expiration.
3. Sends an email notification if expiration is within 300 days.
4. Logs sent emails to avoid duplicate reminders.

## Error Handling
- Ensures the Excel file is accessible and properly formatted.
- Catches and logs errors in email sending.
- Handles missing or corrupted log files gracefully.

## Future Enhancements
- Integrate a frontend dashboard for real-time monitoring.
- Support multiple file formats (CSV, JSON, etc.).
- Implement database storage for better scalability.
- Add user authentication and role-based access.

## License
This project is open-source and available under the MIT License.

