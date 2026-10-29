# EWB Phishing URL Awareness Checker

## Overview
Phishing is a trick in which a fake link or message tries to make someone share information such as a password, OTP, or payment details. This beginner-friendly Python program reads URL text and flags selected warning signs. It never opens the link or sends information to the internet.

## Features
- Detects an `@` symbol in the URL
- Flags URLs longer than 100 characters
- Flags IPv4-style IP-address hostnames
- Flags hostnames with 5 or more dot-separated segments
- Flags punycode-style hostnames containing `xn--`
- Flags the HTTP scheme
- Allows multiple sample URLs in one run; type `q` to quit
- Handles malformed URL text without crashing for the workbook's malformed-input example
- Shows a “REVIEW CAREFULLY” summary when warning signs are found

## Requirements
- Python 3.10 or later
- No extra packages are required

## How to Run
Open a terminal in this project folder.

**Windows**
```bash
python phishing_checker.py
```
If `python` does not work on Windows, try:
```bash
py phishing_checker.py
```

**macOS / Linux**
```bash
python3 phishing_checker.py
```

Enter one of the safe sample strings from `tests/test_samples.md`. Type `q` to quit.

## Example Output
For the sample input `http://192.0.2.10/account`, the output includes:
```text
- Uses an IP address instead of a familiar domain.
- Uses HTTP. HTTPS alone does not prove trust.
REVIEW CAREFULLY: 2 warning sign(s) found.
```

## Testing
The five sample cases and a results table are in [`tests/test_samples.md`](tests/test_samples.md). Run each sample yourself and confirm that the actual output matches before marking it PASS.

## Screenshots
After you run the program and complete the tests, save your own screenshots with these exact names:
- `screenshots/sample_run.png`
- `screenshots/test_results.png`

They will appear here after you add the images to this repository:
![Sample run](screenshots/sample_run.png)
![Test results](screenshots/test_results.png)

## Improvements
1. **Repeat-use loop with quit command** — the program lets the user inspect several URL strings without restarting. Type `q`, `quit`, or `exit` to finish.
2. **Malformed-input handling** — catches a `ValueError` raised while parsing malformed URL text and prints a helpful message instead of crashing.
3. **Review summary** — prints the number of warning signs found when actual warning signs are present.

## Limitations
This is an educational awareness tool. It only reads URL text. It does not visit URLs, scan for malware, use reputation services, or prove that a URL is safe. “No listed warning signs found” does NOT mean a URL is safe. These checks can produce false positives and false negatives.

## Ethical Use
Use only the sample strings provided in the workbook or other harmless examples. Do not collect credentials, send phishing messages, open suspicious links to test them, or probe websites without permission.

## Author
Harsh Rawal  
EWB Cybersecurity Internship — Phishing URL Awareness Checker
