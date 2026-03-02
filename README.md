# sendDuesReminders.py

**Description of the Python Code: Send Dues Reminders**

This Python script, `sendDuesReminders.py`, sends emails to members who have unpaid dues based on their status in a spreadsheet (`duesRecords.xlsx`). The script uses the `openpyxl` library to read the spreadsheet and the `smtplib` library to send emails via Gmail.

**Step-by-Step Explanation:**

1. **Load the Spreadsheet**: The script opens the `duesRecords.xlsx` spreadsheet and loads the data into the `openpyxl` library.
2. **Get Unpaid Members**: The script iterates through each row in the spreadsheet, starting from row 2 (skipping the header row). If a member's payment status is not "paid", their name and email are added to the `unpaidMembers` dictionary.
3. **Log in to Email Account**: The script logs in to a Gmail account using the `smtplib` library, specifying the username (