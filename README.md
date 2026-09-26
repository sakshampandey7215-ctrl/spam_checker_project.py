🚨 Local Spam / Scam Message Checker

A simple Python-based spam and scam message checker that analyzes text messages for common warning signs such as urgent language, money requests, fake authority claims, requests for personal information, and suspicious links.

The project uses regular expressions (re) to detect suspicious patterns and calculates a risk score from 0–100.

⚠️ Note: This is an educational project and should not be considered a guaranteed scam detector. A message marked as "Low Risk" may still be unsafe.

✨ Features

🔍 Detects common spam/scam patterns

📊 Generates a risk score from 0 to 100

🚨 Classifies messages as:

HIGH RISK — 75+

MEDIUM RISK — 40–74

LOW RISK — below 40

💰 Detects money-related requests

🔐 Detects requests for sensitive information such as OTP, PIN, CVV, PAN, etc.

🏦 Detects messages pretending to come from authorities or companies

🔗 Detects suspicious URLs and shortened links

⚡ Uses Python's built-in re module

🖥️ Runs directly in the terminal

🧠 How It Works

The checker looks for suspicious patterns in five categories:

Category	Examples	Risk Points
🚨 Urgent Language	urgent, immediately, last chance	65
💰 Money Related	send money, transfer, crypto, wallet	80
🏦 Fake Authority	bank, police, income tax, amazon	70
🔐 Personal Information	OTP, password, PIN, CVV, PAN	90
🔗 Suspicious Links	http://, https://, bit.ly, tinyurl	60

Each category is counted only once, even if multiple patterns from the same category appear.

The final score is capped at 100.

Example

A message such as:

URGENT! Your bank account will be blocked within 24 hours.
Send your OTP immediately using the link https://example.com


could trigger several categories:

Urgent Language

Money/Account-related warning

Fake Authority

Personal Information

Suspicious Link

The program then calculates a risk score and displays the detected reasons.

🛠️ Technologies Used

Python 3

Regular Expressions (re)

Terminal / Command Line

No external Python libraries are required.

📋 Requirements

Make sure Python 3 is installed on your computer.

Check your Python version:

python --version


or:

python3 --version

🚀 Installation
1. Clone the repository
git clone https://github.com/YOUR-USERNAME/spam-checker.git

2. Move into the project directory
cd spam-checker

3. Run the program
python spam_checker.py

💻 Usage

After starting the program, paste your message into the terminal.

You can enter multiple lines.

Press Enter twice when you have finished entering the message.

Example:

===== Local Spam / Scam Message Checker ====
Paste the message below (press Enter twice to check ):

URGENT! Your account will be blocked.
Please verify your OTP immediately.
https://example.com


Example output:

=============================================
Risk Score : 100/100
Status : HIGH RISK (LIKELY SCAM/SCAM)
REASON  : Urgent language, Fake Authority, Asking personal info, Suspicious links
=============================================

📁 Project Structure
spam-checker/
│
├── spam_checker.py
└── README.md

🎯 Risk Levels
🔴 High Risk — 75 to 100

The message contains multiple or highly suspicious indicators.

Recommended action: Do not click links, send money, or share personal information. Verify the message through an official source.

🟠 Medium Risk — 40 to 74

The message contains some suspicious characteristics.

Recommended action: Be cautious and verify the sender and request before taking action.

🟢 Low Risk — 0 to 39

No strong spam signals were detected.

Important: This does not guarantee that the message is safe.

⚙️ Customization

You can add or modify detection patterns in the checkpoints dictionary.

For example:

"Suspicious Links": {
    "patterns": [
        r"http[s]?://",
        r"bit\.ly",
        r"tinyurl"
    ],
    "risk points": 60
}


You can add additional scam keywords or categories depending on your requirements.

🔮 Future Improvements

Some possible improvements for future versions:

 Add a graphical user interface (GUI)

 Add email/SMS input support

 Improve pattern matching

 Detect suspicious phone numbers

 Add whitelist/blacklist functionality

 Generate a detailed report

 Save scan history

 Add machine-learning based detection

 Improve detection of phishing URLs

 Add multilingual scam detection

 Create a web version of the checker

⚠️ Limitations

This project uses rule-based pattern matching, so it has some limitations:

It may produce false positives.

It may miss cleverly written scams.

Keywords alone cannot determine whether a message is genuinely fraudulent.

The risk score is a heuristic, not a probability of fraud.

Legitimate messages may contain words such as "urgent" or "OTP."

Therefore, users should independently verify suspicious messages.

🔒 Safety Tips

Regardless of the score:

Never share your OTP, PIN, CVV, or password with someone who asks for it.

Don't click suspicious links.

Verify unexpected payment requests independently.

Contact banks or companies using their official websites or phone numbers.

Be cautious of messages creating artificial urgency.

👨‍💻 Author

Your Name

If you found this project useful, consider giving the repository a ⭐ on GitHub!

📄 License

This project is available for educational and personal use. You can add a license such as the MIT License if you want others to freely use and modify the project.
