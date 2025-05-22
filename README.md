# Cybersecurity-OSINT-Incident-Response
Brand Impersonation Investigation & Takedown (OSINT + Incident Response)
This project was part of a cybersecurity internship, where I was tasked with investigating a phishing website impersonating a legitimate brand and executing a full takedown and protection strategy using only open-source and legally safe tools.

🔍 Step-by-Step Breakdown
1️⃣ Initial Recon: Domain Info & Hosting Intelligence
Objective: Understand who owns the phishing domain, when it was created, and where it is hosted.
Tools Used:
whois.whois, ViewDNS, ICANN Lookup → For WHOIS data
SecurityTrails, Google Dig, DNSDumpster → DNS enumeration
Findings:
Identified the registrar (WebNIC) and hosting provider (Cloudflare)
Discovered no email setup (no MX records) — confirming phishing intent
DNS points to suspicious IPs with Cloudflare protection

2️⃣ Infrastructure & Technology Stack Mapping
Objective: Reveal how the phishing site was built and if it shares infrastructure with other scams.
Tools Used:
Shodan, Censys → For port scanning and IP mapping
BuiltWith, Wappalyzer → For tech stack identification
crt.sh, Censys certificates → For SSL certificate transparency logs
Findings:
Site built on WordPress using WPBakery and RankMath SEO
Shared hosting with other known scam sites
Open ports (2083, 2086, 8443) identified, potentially reused across scam domains
Over 20 SSL certs issued, indicating reuse of infrastructure
3️⃣ Risk & Impact Assessment
Objective: Quantify the risks to customers, the brand, and its partners.
Method:
Developed a Risk Matrix assessing Likelihood × Impact
Considered legal, reputational, and financial risks
Key Risks Identified:
Threat	------------------------->  Likelihood---Impact	----Severity
Customerphishing-------------->	      High---	High---- Critical
Brand trust degradation	-------->Medium---High----High
Legal/trademark violation	------>High	---Medium----	High
Financial fraud	------->Medium---Medium	----Medium

4️⃣ Takedown Action Plan
Objective: Legally and efficiently report the phishing site for takedown.
Steps Taken:
Identified abuse contacts for registrar and CDN
Submitted abuse email to WebNIC
Submitted takedown report to Cloudflare Abuse Portal
Attached evidence: WHOIS logs, screenshots, Shodan/IP scans
Escalation plan: ICANN, APWG, and DMCA takedown if unresponsive
Tools Used:
Email + Evidence attachments (PDF + images)
Cloudflare: abuse.cloudflare.com
DMCA Templates and ICANN escalation references

5️⃣ Stakeholder Communication Plan
Objective: Prepare messaging for internal and external audiences.
Deliverables:
Internal Alert for security/legal/comms teams
Press Holding Statement in case of media inquiries
Customer-facing reassurance (optional)
Tone: Calm, clear, and transparent

6️⃣ Future-Proofing & Brand Protection Strategy
Objective: Build processes to detect and respond faster in future impersonation cases.
Recommendations Made:
Monitoring Tools:
crt.sh, Censys, SecurityTrails → Domain & cert alerts
VirusTotal, URLScan, CheckPhish → Automated threat intelligence feeds
Internal Readiness:

SOPs for impersonation reporting
Tabletop simulations with cross-team drills
Trademark registration in key markets
Ready-to-send abuse/DMCA templates

🧠 Skills Gained
OSINT investigation
Digital forensics (read-only, passive recon)
Risk analysis & incident response planning
Legal coordination (abuse, DMCA)
Cybersecurity communication strategy

🔒 Note: All evidence was collected via non-intrusive, publicly accessible tools. No private systems were accessed or disrupted. The phishing domain has been redacted for safety.

