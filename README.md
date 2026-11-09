<hr>

<div align="center">

![Hexnode MDM Skill Banner](banner.png)

<h1 align="center">Hexnode MDM Skill</h1>

</div>

<pre align="center">Expert knowledge base and automation toolkit for Hexnode Mobile Device Management (UEM)</pre>

![Platform](https://img.shields.io/badge/Platform-macOS%20%7C%20iOS%20%7C%20Android%20%7C%20Windows-blue)
![API Coverage](https://img.shields.io/badge/API%20Parameters-512-green)
![License](https://img.shields.io/badge/license-MIT-blue)

---

## Overview

The **Hexnode MDM Skill** is a comprehensive knowledge base and automation toolkit for working with Hexnode's Mobile Device Management (UEM) platform. It provides complete API documentation, automation scripts, troubleshooting guides, and best practices for managing devices across macOS, iOS, Android, and Windows platforms.

This skill enables AI agents and developers to:
- Create and manage MDM policies programmatically via API
- Automate device enrollment and configuration workflows
- Execute remote actions and scripts on managed devices
- Troubleshoot common MDM issues with proven solutions
- Implement device renaming, security policies, and app deployment

## Features

### 📚 Complete API Documentation
- **104 endpoints** fully documented with examples
  - Actions: 37 endpoints (Scan, Lock, Wipe, Install Apps, etc.)
  - Policies: 9 endpoints (Create, Edit, Delete, Associate)
  - Devices/Users/Groups: 18 endpoints
  - Applications: 12 endpoints (Apps, Groups, Catalogs)
  - Automations, Reports, Content: 28 endpoints
- **512 policy parameters** across all platforms
  - macOS: 115 parameters
  - iOS: 224 parameters
  - Android: 99 parameters
  - Windows: 74 parameters
- Every parameter and endpoint documented with:
  - HTTP method and URL
  - Request/response examples
  - Parameter types and descriptions
  - Curl examples
- Platform-specific policy configuration examples
- Authentication and error code reference

### 🚀 Automation Scripts
- **Device renaming scripts** for macOS (COMPANY naming convention)
- **Policy creation templates** (Firewall, Windows Defender, FileVault, etc.)
- **Bash and PowerShell** examples for cross-platform support
- Ready-to-deploy scripts for Hexnode's Automated Tasks

### 🛠️ Troubleshooting Knowledge Base
- 13+ common scenarios with proven solutions
- Script execution issues (Pending forever, permission errors)
- API integration debugging
- Enrollment and compliance problem resolution

### 📋 Policy Templates
- **50+ policy categories for macOS** (Firewall, FileVault, VPN, WiFi, etc.)
- **40+ policy categories for Windows** (Defender, BitLocker, Firewall)
- iOS and Android policy configurations
- Testing and production naming conventions

### 🔧 Workflows & Best Practices
- 5-day testing workflow for new policies
- Script development and deployment guidelines
- API rate limiting and error handling
- Security best practices for MDM operations

## Contents

* [Quick Start](#quick-start)
* [API Reference](#api-reference)
* [Scripts & Examples](#scripts--examples)
* [Troubleshooting](#troubleshooting)
* [Contributing](#contributing)
* [License](#license)
* [Support](#support)

---

## Quick Start

### Requirements

- Hexnode MDM/UEM account with API access enabled
- API Key from Hexnode Admin portal
- (Optional) Python 3.7+ for automation scripts
- (Optional) Bash/PowerShell for script execution

### Installation

**For AI Agents (Claude, Codex, etc.):**

```bash
# Install skill in agents directory
cp -r hexnode-mdm ~/.agents/skills/

# Or for Codex
cp -r hexnode-mdm ~/.codex/skills/
```

**For Manual Use:**

```bash
# Clone the repository
git clone https://github.com/santiagoagustinfernandez/hexnode-mdm-skill.git

# Navigate to the directory
cd hexnode-mdm-skill

# Set up environment variables
export HEXNODE_API_KEY="your-api-key-here"
export HEXNODE_BASE_URL="https://your-portal.hexnodemdm.com"
```

### Setup Instructions

1. **Enable API Access in Hexnode:**
   - Login to your Hexnode portal
   - Navigate to: **Admin → API**
   - Enable API Access
   - Copy your API Key

2. **Configure Environment Variables:**
   ```bash
   export HEXNODE_API_KEY="your-api-key-here"
   export HEXNODE_BASE_URL="https://your-portal.hexnodemdm.com"
   ```

3. **Verify API Connection:**
   ```bash
   curl -H "Authorization: $HEXNODE_API_KEY" \
        "$HEXNODE_BASE_URL/api/v1/devices/" | head -20
   ```

### Usage Examples

#### Example 1: Query API for Devices

```bash
curl -H "Authorization: $HEXNODE_API_KEY" \
     "$HEXNODE_BASE_URL/api/v1/devices/?platform=mac&per_page=10"
```

#### Example 2: Create a macOS Firewall Policy

```bash
curl -X POST \
  -H "Authorization: $HEXNODE_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "[PROD] Firewall Enabled - macOS",
    "macos": {
      "firewall": {
        "Enable_Firewall": true,
        "firewall_enabled": "allow_incoming_connections",
        "Enable_StealthMode": true
      }
    }
  }' \
  "$HEXNODE_BASE_URL/api/v1/policy/"
```

#### Example 3: Ask AI Agent a Question

Once the skill is installed, ask your AI agent:

```
"How do I configure FileVault via Hexnode API?"
"What parameters are available for iOS VPN policies?"
"Troubleshoot: my script shows 'Pending' status forever"
"Create a Windows Defender policy for production"
```

The agent will use the skill's knowledge base to provide accurate, context-aware answers.

---

## API Reference

Complete API documentation available in:

- **[HEXNODE_API_COMPLETE.md](HEXNODE_API_COMPLETE.md)** - All 104 endpoints with examples
  - Scraped from official Hexnode documentation
  - Includes HTTP methods, parameters, curl examples
  - Organized by category (Actions, Policies, Devices, etc.)
- **[API_REFERENCE.md](API_REFERENCE.md)** - 512 policy parameters reference
  - Platform-specific configurations (macOS, iOS, Android, Windows)
  - Parameter types, descriptions, and default values
- **[SKILL.md](SKILL.md)** - Complete skill documentation with workflows

### Key Endpoints

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/v1/devices/` | GET | List devices (supports pagination & filtering) |
| `/api/v1/devices/{id}/` | GET | Get device details |
| `/api/v1/policy/` | GET/POST | List or create policies |
| `/api/v1/policy/{id}/` | GET/PUT/DELETE | Manage specific policy |
| `/api/v1/actions/associate_policy/` | POST | Associate policy to devices/groups |
| `/api/v1/device-groups/` | GET/POST | Manage device groups |

### Authentication

All API requests require an API Key in the `Authorization` header:

```bash
Authorization: YOUR_API_KEY_HERE
```

---

## Scripts & Examples

### Device Renaming (macOS)

Automatically rename Macs on enrollment with format: `COMPANY-{COUNTRY}{OS}-{SERIAL}`

**Location:** `scripts/macos/klr_rename_hexnode.sh`

**Features:**
- Extracts serial number from system
- Determines country from network location
- Updates both hostname and Hexnode display name
- Designed for Hexnode Automated Tasks

**Usage:**
```bash
# In Hexnode Console:
# Manage → Automated Tasks → Scripts
# Upload klr_rename_hexnode.sh
# Run as Administrator
# Trigger: On Enrollment
```

### Okta Integration (macOS)

Deploy Okta Verify and Browser Plugin to macOS devices for SSO and MFA/ZTA.

**Location:** `scripts/macos/okta_*.sh`

**Available Scripts:**
- `okta_verify_install.sh` - Install Okta Verify for MFA/ZTA (3.6 KB)
- `okta_browser_plugin_install.sh` - Install Browser Plugin for SSO (2.7 KB)
- `OKTA_SCRIPTS_README.md` - Complete implementation guide (4.1 KB)

**Implementation Method:**

**Option 1: App Management (Recommended)**
```
1. Hexnode UI → Policies → Create/Edit Policy
2. macOS → App Management → Required Apps
3. Add "Okta Verify" from enterprise catalog
4. macOS → App Configurations → Configure ZTA integration
5. Policy Targets → Assign to "All macOS Devices" group
6. Save
```

**Option 2: Custom Scripts**
```bash
# In Hexnode Console:
# Manage → Automated Tasks → Scripts
# Upload okta_verify_install.sh
# Run as Administrator
# Trigger: On Enrollment
# Target: macOS devices
```

**Features:**
- ✅ Automatic installation on enrollment
- ✅ CrowdStrike ZTA integration support
- ✅ Detailed logging (`/var/log/hexnode_okta_*.log`)
- ✅ Version detection and updates
- ✅ Dynamic group assignment

**Documentation:**
- See `docs/OKTA_HEXNODE_IMPLEMENTATION_GUIDE.md` for step-by-step guide
- See `docs/REPORTE_PARA_PABLO.md` for technical details
- See `scripts/macos/OKTA_SCRIPTS_README.md` for script documentation

### Policy Creation Scripts

**Bash Scripts:**
- `create_firewall_policies.sh` - macOS and Windows Firewall policies
- `create_macos_testing_policy.py` - Multi-platform policy creator

**PowerShell Scripts:**
- Windows-specific configurations (see SKILL.md)

---

## Troubleshooting

### Common Issues

**1. Script shows "Pending" forever**

**Cause:** Script missing executable permissions or contains syntax errors

**Solution:**
```bash
# Test locally first
sudo bash /path/to/script.sh

# Check for errors
bash -n /path/to/script.sh  # Syntax check

# Ensure shebang is correct
head -1 /path/to/script.sh  # Should be #!/bin/bash or #!/bin/zsh
```

**2. API returns 401 Unauthorized**

**Cause:** Invalid or missing API Key

**Solution:**
- Verify API is enabled in Admin → API
- Check API Key is correct
- Ensure no extra spaces in Authorization header

**3. Policy not applying to devices**

**Cause:** Policy not assigned to device groups

**Solution:**
```bash
# Associate policy to group
curl -X POST \
  -H "Authorization: $API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
    "policies": [POLICY_ID],
    "targets": {"devicegroup_id_list": [GROUP_ID]}
  }' \
  "$BASE_URL/api/v1/actions/associate_policy/"
```

**For complete troubleshooting guide, see SKILL.md section "Troubleshooting Scripts"**

---

## Project Structure

```
hexnode-mdm-skill/
├── README.md                          # This file
├── SKILL.md                           # Complete skill documentation (4500+ lines)
├── HEXNODE_API_COMPLETE.md            # All 104 endpoints with examples (96 KB)
├── API_REFERENCE.md                   # 512 policy parameters reference
├── hexnode_api_complete_docs.json     # Scraped API data (JSON format)
├── banner.png                         # GitHub repository banner (21:9)
├── .gitignore                         # Git ignore patterns
├── docs/                              # Implementation guides
│   ├── OKTA_HEXNODE_IMPLEMENTATION_GUIDE.md
│   ├── REPORTE_PARA_PABLO.md
│   ├── RESUMEN_EJECUTIVO_PABLO.md
│   └── GUIA_IMPLEMENTACION_OKTA_SCRIPTS.md
├── scripts/                           # Automation scripts
│   ├── macos/
│   │   ├── klr_rename_hexnode.sh      # macOS renaming script
│   │   ├── okta_verify_install.sh     # Okta Verify installation
│   │   ├── okta_browser_plugin_install.sh
│   │   └── OKTA_SCRIPTS_README.md     # Okta scripts documentation
│   └── windows/                       # Windows scripts (TBD)
└── examples/                          # Usage examples
    └── policy_templates/              # Policy JSON templates
```

---

## Contributing

Contributions are welcome! To contribute:

1. **Fork** this repository
2. **Create a feature branch:** `git checkout -b feature/my-new-feature`
3. **Make your changes** and test thoroughly
4. **Commit:** `git commit -am 'Add new feature'`
5. **Push:** `git push origin feature/my-new-feature`
6. **Create a Pull Request**

### Contribution Guidelines

- Ensure no API keys or secrets are committed
- Test scripts on local Hexnode instance before submitting
- Update documentation for new features
- Follow existing code style and naming conventions
- Add examples for new API parameters

**Working on your first pull request?** See: [How to Contribute to an Open Source Project on GitHub](https://kcd.im/pull-request)

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Support

**Maintainer:** [@santiagoagustinfernandez](https://github.com/santiagoagustinfernandez)

**Questions or Issues?**
- Open an issue on [GitHub Issues](https://github.com/santiagoagustinfernandez/hexnode-mdm-skill/issues)
- Email: santiagoagustinfernandez@gmail.com

**Hexnode Official Resources:**
- [Hexnode Documentation](https://www.hexnode.com/mobile-device-management/help/)
- [Hexnode API Docs](https://www.hexnode.com/mobile-device-management/developers/)
- [Hexnode Support](https://www.hexnode.com/mobile-device-management/contact-sales/)

---

<div align="center">

**Made with ❤️ for the MDM automation community**

</div>
