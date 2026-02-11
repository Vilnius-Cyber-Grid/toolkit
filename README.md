# SOC Automation Toolkit

A curated collection of automation tools, scripts, and workflows for Security Operations Center (SOC) teams. This repository is designed for **cybersecurity knowledge sharing** and practical implementation.

> ⚠️ **Public Repository Notice**: This repo is public. Do not commit sensitive data, credentials, API keys, or organization-specific configurations. See [Security Considerations](#security-considerations) for details.

---

## 📁 Repository Structure

```
toolkit/
├── docs/                    # Documentation, recipes, playbooks
├── m365/                    # Microsoft 365 automations
├── n8n/
│   ├── credentials/         # Credential templates (examples only)
│   └── workflows/           # n8n workflow JSON files
└── scripts/
    └── windows/             # PowerShell scripts for Windows
```

---

## 🔄 n8n Workflows

**Location:** `/n8n/workflows/`, `/n8n/credentials/`

Automated workflows for SOC operations using [n8n](https://n8n.io/).

### Features
- **Import/Export ready** - JSON workflow files for easy deployment
- **IOC Processing** - Automated indicator of compromise handling
- **Alert Enrichment** - Contextual data gathering for security alerts
- **Case Management** - Ticket creation and tracking automation

### Usage
1. Import workflow JSON into your n8n instance
2. Configure credentials using templates from `/n8n/credentials/`
3. Adjust node parameters to match your environment
4. Test in a sandbox before production deployment

### Best Practices
- Use environment variables for sensitive values
- Implement error handling nodes in all workflows
- Add logging nodes for audit trails
- Test with sample data before connecting to production systems

---

## 🪟 Windows/PowerShell Scripts

**Location:** `/scripts/windows/`

PowerShell scripts for Windows security operations.

### Categories
| Category | Description |
|----------|-------------|
| **Audit** | System configuration and compliance checks |
| **Hardening** | Security baseline implementation scripts |
| **Incident Response** | Forensic collection and triage tools |
| **Log Collection** | Event log gathering and forwarding |

### Features
- ✅ Clear parameters with documentation
- ✅ Safe execution with `-WhatIf` support where applicable
- ✅ Usage examples in script headers
- ✅ Error handling and logging

### Execution
```powershell
# Example: Run with verbose output
.\Script-Name.ps1 -Parameter "Value" -Verbose

# Example: Preview changes without executing
.\Script-Name.ps1 -WhatIf
```

---

## ☁️ M365 Automations

**Location:** `/m365/`

Microsoft 365 security automation templates.

### Integration Points
- **Power Automate** - Low-code automation flows
- **Microsoft Graph API** - Programmatic access to M365 data
- **Microsoft Defender** - Security alert and incident handling

### Common Patterns

| Pattern | Description |
|---------|-------------|
| Alert → Teams | Security alert notifications to Teams channels |
| Alert → Email | Email notifications for critical events |
| Alert → Ticket | Automatic ticket creation in ITSM systems |
| Defender → SIEM | Event forwarding to SIEM platforms |

### Security Notes
- Request **minimal permissions** necessary for each automation
- Use managed identities where possible
- Review and audit app registrations regularly
- Document all API permissions in automation descriptions

---

## 📚 Documentation

**Location:** `/docs/`

### Contents
- **Recipes** - Step-by-step guides for specific tasks
- **Playbooks** - Incident response procedures
- **Demo Scenarios** - Sample use cases for training

### Quick Start Guide

**Get running in 10 minutes:**

1. **Clone the repository**
   ```bash
   git clone <repo-url>
   cd toolkit
   ```

2. **Choose your tool**
   - n8n workflows → Import JSON to n8n instance
   - PowerShell scripts → Copy to target system
   - M365 automations → Import to Power Automate

3. **Configure credentials**
   - Copy example files and fill in your values
   - Never commit actual credentials

4. **Test in sandbox**
   - Always test before production deployment

---

## 🔒 Security Considerations

### What NOT to include in this repository
- ❌ API keys and secrets
- ❌ Passwords or credentials
- ❌ Organization-specific IP addresses or hostnames
- ❌ Internal URLs or endpoints
- ❌ Customer or employee data
- ❌ Proprietary detection logic

### What to include
- ✅ Template configurations with placeholder values
- ✅ Generic example workflows
- ✅ Documented scripts with sanitized examples
- ✅ Best practices and patterns

---

## 🤝 Contributing

We welcome contributions! Please follow these guidelines:

1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/your-feature`)
3. **Test** your changes thoroughly
4. **Document** any new scripts or workflows
5. **Submit** a pull request

### Contribution Standards
- Include usage examples in script headers
- Add error handling and logging
- Sanitize all examples (no real data)
- Follow existing naming conventions

---

## 📋 Issue Templates

Use our issue templates for:
- 🐛 Bug reports
- ✨ Feature requests
- 📚 Documentation improvements
- 🔧 Script/workflow requests

---

## 📜 License

This project is shared for educational and community purposes. See [LICENSE](LICENSE) for details.

---

## 📬 Contact

For questions or suggestions, please open an issue or start a discussion.

---

**Disclaimer**: These tools are provided as-is for educational purposes. Always review and test scripts before running them in production environments. The maintainers are not responsible for any damage caused by improper use.
