# Test Results

Python version used: [fill in after running `python --version` or `py --version`]
Operating system: Windows (edit if different)
Date tested: [enter the date you actually tested]

Run each input in `phishing_checker.py` and compare your output. These are the expected observations from the workbook; mark PASS/FAIL honestly after testing.

| # | Input | Expected result | Actual result | Pass/Fail |
|---|---|---|---|---|
| 1 | `https://www.example.com/login` | No listed warning signs; not a safety guarantee | [fill after running] | [fill] |
| 2 | `http://192.0.2.10/account` | IP-address hostname + HTTP | [fill after running] | [fill] |
| 3 | `http://example.com@sample.invalid/login` | @ symbol + HTTP | [fill after running] | [fill] |
| 4 | `https://a.b.c.d.e.example.invalid/path` | Many hostname segments | [fill after running] | [fill] |
| 5 | `https://xn--example.invalid/` | Punycode-style hostname | [fill after running] | [fill] |

## Additional improvement checks
- [ ] Enter `http://[bad` and confirm the program displays a helpful invalid-format message rather than crashing.
- [ ] Enter two sample URLs in one session, then type `q` and confirm the program exits.

## Notes
[Write 2–3 sentences in your own words about what you learned and what surprised you.]
