# 🖥️ Process Logger and Email Sender

This Python script monitors and logs all running processes on a system at scheduled intervals. It then sends the log file via email if internet connectivity is available.

---

## 🛠️ Setup

1. Clone the repository or copy the script into your project.

2. Modify the placeholders:
   - Replace `__________@gmail.com` in the `MailSender` function with the sender and recipient Gmail addresses.
   - Replace `'**********'` with the **App Password** (recommended) for your Gmail account.
   - Replace `"xyz"` in the email body with your actual name.

3. Either:
   - ✅ Use **App Passwords** if you have 2FA enabled (recommended), or  
   - ⚠️ Enable **less secure app access** (not recommended).

---

## 🧪 How It Works

🔹 The script uses the `psutil` module to fetch details of all running processes (PID, name, username).  
🔹 It writes these details into a timestamped log file in a `Processes` directory.  
🔹 It checks for internet connectivity by pinging `https://www.google.com`.  
🔹 If connected, it emails the log file as an attachment using Gmail's SMTP server.  
🔹 The task is scheduled to run every 1 minute using the `schedule` module.

---

## 📂 Output

- Log files are stored in a `Processes` directory.  
- Each log file is timestamped, e.g., `ProcessesLog Wed_Jun_11_14_20_33_2025`.

---

## 🚀 Running the Script

Run the script using:

```bash
python your_script_name.py
```
---

## 📧 Email Sample

**Subject:**
Process log generated at: Wed Jun 11 14:20:33 2025

**Body:**
Hello receiver_email@gmail.com,

Please find the attached document containing the log of running processes.
Log file created at: Wed Jun 11 14:20:33 2025

This is auto generated mail.
Thanks & Regards,
xyz

---

## ⚠️ Notes
-✅ Use environment variables or external config files to store sensitive data like passwords.
-✅ Make sure the machine running the script has Python 3.x installed and necessary libraries:

```bash
pip install psutil schedule
```
