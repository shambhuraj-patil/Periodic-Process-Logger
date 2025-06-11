# 🖥️ Process Logger and Email Sender

This Python script monitors and logs all running processes on a system at scheduled intervals. It then sends the log file via email if internet connectivity is available.

## 🛠️ Setup

1. Clone the repository or copy the script into your project.

2. Modify the placeholders:
   - Replace `__________@gmail.com` in the `MailSender` function with the sender and recipient Gmail addresses.
   - Replace `'**********'` with the **App Password** (recommended) for your Gmail account.
   - Replace `"xyz"` in the email body with your actual name.

3. Ensure [less secure app access](https://myaccount.google.com/security) is enabled or use [App Passwords](https://support.google.com/accounts/answer/185833) if you have 2FA enabled.

## 🧪 How It Works

- The script uses the `psutil` module to fetch details of all running processes.
- It writes these details into a text file inside a `Processes` directory.
- It then sends this file via email as an attachment using Gmail SMTP.
- The job is scheduled to run every 1 minute continuously using the `schedule` module.

## 📂 Output

- Log files are stored in a `Processes` directory.
- Each log file is timestamped, e.g., `ProcessesLog Wed_Jun_11_14_20_33_2025`.

## 🚀 Running the Script

Run the script using:

python your_script_name.py

## 📧 Email Sample

**Subject:**
Process log generated at: Wed Jun 11 14:20:33 2025

**Body:**
Hello receiver_email@gmail.com,

Please find attached document which contains log of Running process
Log file created at : Wed Jun 11 14:20:33 2025

This is auto generated mail.
Thanks & Regards,
xyz
