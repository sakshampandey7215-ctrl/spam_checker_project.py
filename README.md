Local Spam / Scam Message Checker
A simple, offline Python tool that analyzes text messages (SMS, WhatsApp, email, etc.) and gives a risk score based on common scam indicators.

No internet connection required. No external libraries. Just pure Python.

Features
Risk Score (0–100) with clear status:

HIGH RISK (≥ 75) → Likely scam

MEDIUM RISK (40–74) → Be careful

LOW RISK (< 40) → Looks relatively safe

Detects multiple categories of scam signals:

Urgent / pressure language

Money-related requests

Fake authority (bank, police, Amazon, etc.)

Requests for personal info (OTP, password, Aadhaar, PAN, etc.)

Suspicious links and call-to-action phrases

Supports multi-line paste

Counts each category only once (no score inflation)

Works completely offline

Requirements
Python 3.6 or higher

No third-party packages needed (only uses the built-in re module)

How to Run
Download or clone this repository.

Open a terminal in the project folder.

Run the script:

python spam_checker.py
Paste the message you want to check.

Press Enter twice (empty line) to analyze.

Optionally check more messages.

Example Output
==================================================
  Local Spam / Scam Message Checker
==================================================
Paste the message below.
Press Enter twice (empty line) when finished.

URGENT: Your bank account will be blocked within 24 hours.
Send OTP and account details immediately.
Click here: http://bit.ly/fakebank

==================================================
Risk Score : 100/100
Status     : HIGH RISK  →  LIKELY SCAM
Reasons    : Asking personal info, Fake authority, Money related, Suspicious links / calls to action, Urgent language
==================================================
How the Scoring Works
Category

Risk Points

Urgent language

25

Money related

30

Fake authority

25

Asking personal info

30

Suspicious links / call to action

20

The final score is capped at 100.

Project Structure
spam-scam-checker/
├── spam_checker.py     # Main script
└── README.md           # This file
Disclaimer
This tool is for educational and personal awareness purposes only.
It uses simple pattern matching and cannot guarantee 100% accuracy.
Always use your own judgment and never share OTPs, passwords, or bank details with unknown sources.

License
This project is open source and available under the MIT License.

Contributing
Feel free to open issues or submit pull requests if you want to:

Add more scam patterns

Improve the scoring logic

Add a simple GUI

Support other languages

Stay safe online!

