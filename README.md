# Security Audit & Risk Assessment

## Overview
This project conducts a **Security Audit & Risk Assessment** on an organization to evaluate its security posture, identify vulnerabilities, and recommend mitigation strategies. The assessment follows industry best practices, aligning with frameworks such as **NIST CSF, ISO 27001, and CIS Controls**.

## Objectives
- Identify security risks and vulnerabilities.
- Perform an automated security audit using scripts.
- Map findings to industry compliance frameworks.
- Provide a risk assessment matrix with mitigation plans.
- Deliver an executive summary and presentation.

## Deliverables
- **Security Audit Report** (`/docs/security_audit_report.pdf`)
- **Risk Assessment Matrix** (`/docs/risk_matrix.xlsx`)
- **Security Audit Scripts** (`/scripts/`)
- **Compliance Checklist** (`/compliance/compliance_checklist.pdf`)
- **Presentation Deck** (`/presentation/security_audit_presentation.pptx`)

## Tools & Technologies
- **Nmap** (Network scanning)
- **Nessus/OpenVAS** (Vulnerability scanning)
- **Python & PowerShell** (Audit scripting)
- **Excel/CSV** (Risk Matrix)
- **Markdown & LaTeX** (Documentation)

## Project Structure
```
├── docs/
│   ├── security_audit_report.pdf
│   ├── risk_matrix.xlsx
│
├── scripts/
│   ├── security_audit.py
│   ├── windows_audit.ps1
│
├── compliance/
│   ├── compliance_checklist.pdf
│
├── presentation/
│   ├── security_audit_presentation.pptx
│
├── README.md
```

## Security Audit Process
1. **Define Scope**: Identify assets and security domains.
2. **Information Gathering**: Collect system logs, network topology, and access controls.
3. **Vulnerability Assessment**: Use automated scanners to detect weaknesses.
4. **Risk Analysis**: Assign likelihood and impact scores.
5. **Compliance Mapping**: Align findings with industry frameworks.
6. **Risk Mitigation Plan**: Recommend security controls and best practices.
7. **Presentation & Report**: Summarize key findings and solutions.

## Sample Security Audit Script (Python)
```python
import os
import subprocess

def check_open_ports():
    print("Scanning open ports...")
    output = subprocess.run(['nmap', '-p-', '127.0.0.1'], capture_output=True, text=True)
    print(output.stdout)

def check_users():
    print("Checking user accounts...")
    output = subprocess.run(['cut', '-d:', '-f1', '/etc/passwd'], capture_output=True, text=True)
    print(output.stdout)

if __name__ == "__main__":
    check_open_ports()
    check_users()
```

## How to Use
1. **Clone this repository**
   ```bash
   git clone https://github.com/JustinRLew/Security-Audit-Risk-Assessment.git
   ```
2. **Run the security audit script**
   ```bash
   python scripts/security_audit.py
   ```
3. **Review the generated report** in `/docs/`
4. **Present findings** using `/presentation/security_audit_presentation.pptx`

## Next Steps
- Integrate **SIEM log analysis**.
- Add **cloud security audits (AWS IAM, S3 misconfigurations)**.
- Include **incident response playbooks**.

## License
This project is licensed under the MIT License.
