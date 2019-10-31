# Tokopedia Bug Bounty Rules
Keep user informations safe and secure are our top priority and a core company value at Tokopedia. we are pleased with contribution from external security researchers and look forward to awarding them for their invaluable contribution to the security of all Tokopedia users.
## Responsible Disclosure Policy
If you comply with the policies below when reporting a security issue to Tokopedia, we will not initiate a lawsuit or law enforcement investigation against you in response to your report. We ask that:
- You give us reasonable time to investigate and mitigate an issue that you report before making any information about the report public or sharing such information with others.
- You do not interact with an individual account (which includes modifying or accessing data from the account) if the account owner has not consented to such actions.
- You make a good faith effort to avoid privacy violations and disruptions to others, including (but not limited to) unauthorised access to or destruction of data, and interruption or degradation of our services.
- You do not exploit a security issue that you discover for any reason. (This includes demonstrating additional risk, such as attempted compromise of sensitive company data or probing for additional issues.)
- You do not intentionally violate any other applicable laws or regulations, including (but not limited to) laws and regulations prohibiting the unauthorised access to data.
- For the purposes of this policy, you are not authorised to access user data or company data, including (but not limited to) personally identifiable information and data relating to an identified or identifiable natural person.
## Bug bounty program terms
We recognise and reward security researchers who help us to keep people safe by reporting vulnerabilities in our services. Monetary bounties for such reports are entirely at Tokopedia's discretion, based on risk, impact and other factors. To potentially qualify for a bounty, you first need to meet the following requirements:
- Adhere to our responsible disclosure policy (see above).
- Report a security bug: identify a vulnerability in our services or infrastructure which creates a security or privacy risk. (Note that Tokopedia ultimately determines the risk of an issue, and that many software bugs are not security issues.)
- Your report must describe a problem involving one of the products or services listed below (See "Bug Bounty Program").
- We specifically exclude certain types of potential security issues; these are listed below (See "Bug Bounty Program").
- Submit your report via our "Report a security vulnerability" form (one issue per report) and respond to the report with any updates. Please do not contact employees directly or through other channels about a report.
- If you inadvertently cause a privacy violation or disruption (such as accessing account data, service configurations or other confidential information) while investigating an issue, you must disclose this in your report.
- Use test accounts when investigating issues. If you cannot reproduce an issue with a test account, you can use a real account (except for automated testing). Do not interact with other accounts without consent.
In turn, we will follow these guidelines when evaluating reports under our bug bounty programme:
- We investigate and respond to all valid reports. Due to the volume of reports that we receive, however, we prioritise evaluations based on risk and other factors, and it may take some time before you receive a reply.
- We determine bounty amounts based on a variety of factors, including (but not limited to) impact, ease of exploitation and quality of the report. 
- We aim to pay similar amounts for similar issues, but bounty amounts and qualifying issues may change over time. Past rewards do not necessarily guarantee similar results in the future.
- In the event of duplicate reports, we award a bounty to the first person to submit an issue. (Tokopedia determines duplicates and may not share details on the other reports.) A given bounty is only paid to one individual.
- We reserve the right to publish reports (and accompanying updates).
## In Scope
+ In Scope Properties
```
- *.tokopedia.com
- *.tokopedia.net
- payment.tokopedia.id
- tokocash.com
- iOS Application
- Android Application
- Android Seller Application
```
+ In Scope Vulnerability
```
- SQL Injection
- Cross-site Scripting (XSS)
- Significant Authentication Bypass
- Access Control Issues (Insecure Direct Object Reference issues, etc)
- Cross-site Request Forgery in Critical Action
- Information disclosure of Sensitive Information
- Server-Side Request Forgery (SSRF)
- Server-side Remote Code Execution (RCE)
- XML External Entity Attacks (XXE)
- Exposed Administrative Panels that don't require login credentials
- Directory Traversal Issues
- Local File Disclosure (LFD)
- Server Side Template Injection (SSTI)
```
## Out of Scope
+ Out of Scope Properties
```
- 3rd Party Apps (Microsite, Wordpress, CMS, Blog, Even Inside tokopedia.com/* ,etc. )
- 3rd Party Plugins
```
+ Out of Scope Vulnerability
```
- Self-XSS (we require evidence on how the XSS can be used to attack another Tokopedia user).
- We will accept reports of XSS on Out of Scope Properties but will not reward for them.
- XSS issues that affect only outdated browsers.
- Reports that state that software is out of date/vulnerable without a proof of concept.
- Password, email and account policies, such as email id verification, reset link expiration, password complexity.
- Missing security headers which do not lead directly to a vulnerability.
- Missing best practices (we require evidence of a security vulnerability).
- Host header injections unless you can show how they can lead to stealing user data.
- Reports of spam (i.e., any report involving ability to send emails & SMS without rate limits).
- Stack traces that disclose information.
- Open Redirect
- CSV injection.
- Clickjacking
- Highly speculative reports about theoretical damage. Be concrete.
- Vulnerabilities as reported by automated tools without additional analysis as to how they're an issue.
- Reports of insecure SSL/TLS ciphers (unless you have a working proof of concept, and not just a report from a scanner).
- Reports from automated web vulnerability scanners (Acunetix, Vega, etc.) that have not been validated.
- Social Engineering (Phishing,Fraud, etc.).
- Denial of Service Attacks.
- Reflected File Download (RFD).
- window.opener (tabnabbing), related issues.
- Physical or social engineering attempts (this includes phishing attacks against Tokopedia employees).
- Content injection issues.
- Most Brute Forcing issues
- Cross-site Request Forgery (CSRF) with minimal security implications (Logout CSRF, etc.)
- Missing autocomplete attributes.
- Phishing risk via unicode/punycode or RTLO issues.
- Being able to upload files with wrong extension in chooser.
- Missing cookie flags on non-security-sensitive cookies.
- Issues that require physical access to a victim’s computer.
- Missing security headers that do not present an immediate security vulnerability.
- Missing HTTP security headers, specifically, Example : Strict-Transport-Security, X-Frame-Options, X-XSS-Protection, X-Content-Type-Options, Content-Security-Policy, X-Content-Security-Policy, X-WebKit-CSP, Content-Security-Policy-Report-Only
- Fraud issues (please see the below section elaborating on this).
- SSL/TLS scan reports (this means output from sites such as SSL Labs).
- Banner grabbing issues (figuring out what web server we use, etc.).
- Open ports without an accompanying proof-of-concept demonstrating vulnerability.
- Recently disclosed 0day vulnerabilities. We need time to patch our systems, please give us 1 month before reporting these types of issues.
- Entering the Tokopedia offices, throwing crisps everywhere, unleashing a bunch of hungry racoons, and hijacking an abandoned terminal on an unlocked workstation while staff are distracted..
```

## Reporting Guidlines
- Please send the details of the report through this link : **https://bounty.tokopedia.net**

## Bug Severity Terms
- Info (No Reward & No Certificate)
- Low (Certificate Only)
- Medium (Certificate & Rewards)
- High (Certificate & Rewards)
- Critical (Certificate & Rewards)

**Note : We will proceed the reward as soon as possible after completely verification, keep in mind that it can take up to 90 days to receive the reward.**

## Frequently asked questions
**Q: What if I found a vulnerability, but I don't know how to exploit it?**

A: We expect that vulnerability reports sent to us have a valid attack scenario to qualify for a reward, and we consider it as a critical step when doing vulnerability research. Reward amounts are decided based on the maximum impact of the vulnerability, and the panel is willing to reconsider a reward amount, based on new information (such as a chain of bugs, or a revised attack scenario).

**Q: Who determines whether my report is eligible for a reward?**

A: The reward panel consists of the members of the Tokopedia Security Team.

**Q: When will reward be paid?**

A: You will be paid after the vulnerabilty has been fixed by our engineer. So give us reasonable time to fix it.

**Q: What happens if I disclose the bug publicly before you had a chance to fix it?**

A: Please read our **Responsible Disclosure Policy**. In essence, our pledge to you is to respond promptly and fix bugs in a sensible timeframe - and in exchange, we ask for a reasonable advance notice. Reports that go against this principle will usually not qualify, and we cancel the reward. And if it contains sensitive information, it doesn't close the possibility to litigate by applicable laws. 
