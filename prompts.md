# 📚 Security as a Prompt

## 🧑‍💼 Access Control & Identity
- **Admin Access Review**: Revoke AWS users with admin rights not in DevOps
- **Inactive Okta Users**: Disable users who haven't logged in for 90+ days
- **GitHub Team Audit**: Flag GitHub teams with production access not covered by policy
- **Customer Data Role Review**: Collect roles with access to sensitive data and request reapproval
- **MFA Enforcement**: Verify MFA is enabled for all GitHub and Okta admin accounts
- **Least Privilege Validation**: Validate least privilege in production systems
- **Geo Check**: Compare login geolocation with allowed countries
- **Dependabot Audit**: Identify GitHub repos without Dependabot and calculate compliance percentage

## 🛡️ Vulnerability Management
- **Prod Scan**: Run Nuclei scan on https://prod.app.com for high and critical vulnerabilities
- **Infra Recon**: Perform subdomain enumeration and port scan on staging.project.io
- **DAST Auth**: Run authenticated DAST scan on the customer portal login flow
- **SSH Exposure**: Scan AWS EC2 for open SSH ports
- **S3 Audit**: Check for public S3 buckets with sensitive data
- **Firewall Scan**: Scan GCP firewall rules for misconfigurations

## 🚨 Incident Response
- **Critical CrowdStrike**: Isolate host on critical CrowdStrike alert
- **SIEM Enrichment**: Enrich SIEM alerts with asset and user context
- **SentinelOne Triage**: Auto-triage SentinelOne alerts and escalate confirmed incidents
- **Ransomware Lockdown**: Lock infected user accounts in Okta on ransomware detection
- **Breach Timeline**: Collect logs from affected services and build a breach timeline
- **Foreign Login Monitor**: Analyze login attempts from foreign countries for anomalies

## 📋 Compliance & Audit
- **SOC2 AC-2 Check**: Verify SOC2 control status in Vanta
- **Access Log Evidence**: Collect Okta access logs for audit
- **Patch SLA Check**: Confirm systems are patched within 7 days of CVE release
- **License Check**: Scan GitHub repos for open source license violations
- **Vendor Compliance Check**: Check vendor attestations
- **EOL Enforcement**: Detect and remove end-of-life software in production

## 🖥️ Asset Management
- **Unused IAM Roles**: Identify AWS IAM roles unused for 60+ days
- **S3 Security Config**: Ensure all S3 buckets have encryption and logging enabled
- **Cloud Cleanup**: Detect unused cloud assets
- **Secrets Detection**: Scan latest GitHub commits for secrets or misconfigured IaC
- **Docker Security**: Scan Dockerfiles for vulnerabilities and misconfigurations
- **Dependency Guard**: Block pull requests with unscanned third-party dependencies

## 📡 Monitoring & Alerting
- **Weekly Event Digest**: Compile security event summary
- **Failed Logins Report**: Generate a report of failed access attempts
- **Vuln Summary**: Summarize high-severity vulnerabilities across recent scans
- **Cert Expiry Check**: Identify expiring TLS certificates
- **Jira Vuln Dashboard**: Generate dashboard with open vulnerabilities grouped by team
- **Software Deviation**: Detect deviations from approved software list on corporate devices

## 🎓 Training & Awareness
- **Phishing Sim**: Send simulated phishing training to all employees
- **Training Tracker**: Track completion of mandatory security training
- **Secret Paste Alert**: Detect internal secrets in public forums
- **Password Age Alert**: Identify users with passwords older than 90 days
- **Password Reuse Detection**: Detect reuse of passwords across applications
- **New Hire Security Onboarding**: Trigger security training for new hires

## 🤝 Vendor Management
- **Vendor Risk Feed**: Monitor third-party vendors for recent security incidents
- **Vendor Access Scope**: Validate that vendor accounts follow least privilege
- **Data Vendor Review**: Review vendors storing customer data
- **Attestation Check**: Verify vendor security attestations
- **Vendor Endpoint Drift**: Detect changes in vendor endpoints
- **Vendor Logs Review**: Analyze vendor access logs

## 🔐 Data Protection
- **PII Scanner**: Scan Google Drive for sensitive personal data
- **Outbound Email Scan**: Monitor outbound email for unencrypted attachments
- **RDS Encryption**: Identify RDS databases missing encryption at rest
- **File Share Monitor**: Detect publicly shared files from internal systems
- **Data Upload Watch**: Detect customer data uploaded to non-approved platforms
- **Sensitive Access Audit**: Track access to protected data repositories

## 💻 Endpoint Security
- **USB Detection**: Detect USB devices used on critical endpoints
- **Antivirus Status**: Verify antivirus is active and up to date
- **Software Audit**: Detect installation of unauthorized software
- **MDM Policy Bypass**: Detect mobile devices bypassing MDM policies
- **Patch Compliance**: Verify current security patches on all endpoints
- **EDR Alerts**: Monitor for suspicious endpoint behavior using EDR tools