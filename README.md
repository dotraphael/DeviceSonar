# DeviceSonar

DeviceSonar is an inventory management and monitoring platform for Windows environments. It collects hardware and software inventory data from endpoints, processes it centrally, and provides reporting and alerting capabilities.

## Architecture

- **DeviceSonar.Web** - Blazor Server web portal with REST API. Manages tenants, devices, inventory rules, reports, alerts, and software update tracking.
- **DeviceSonar.Agent** - Windows agent (WPF/console) installed on endpoints. Collects inventory data via WMI, registry, and PowerShell rules, then submits encrypted payloads to the server.
- **DeviceSonar.Sync** - CLI tool for generating software list and mapping databases from public repositories (winget, Chocolatey, SCUP catalogs, CVE records).

## Features and Limits

DeviceSonar needs no licence file or key and has no editions. Every installation and every tenant gets the full feature set: vulnerability scanning with CVE database sync, software list sync, global rule updates, CVE overrides, software mappings, device compliance posture scoring, the compliance and vulnerability dashboards, executive reports, the Reporting API, API Read Keys, and Power BI integration.

| Item | Value |
|------|-------|
| Database | MariaDB/MySQL or SQL Server, on every installation |
| Devices, tenants, inventory rules, super admins, alert rules | No product-wide cap. All items are available. You decide the limitations per tenant. |
| Data Retention | Configurable per tenant, no upper cap |
| Report / inventory data API date range | 90 days per request |
| Audit Log Retention | 365 days by default, up to 1825 days |

## Feedback and Support

- [Submit Feature Ideas](https://github.com/dotraphael/DeviceSonar) - vote on and suggest new features
- [Submit Issues](https://github.com/dotraphael/DeviceSonar) - report bugs or request assistance
- [Commercial Support](https://www.rflsystems.co.uk) - professional support for your DeviceSonar deployment

## Documentation

- [Server Installation](installation-server.md)
- [Agent Installation](installation-agent.md)
- [Administration Guide](administration.md)
- [Reporting Guide](reporting.md)
- [Sync Tool Guide](sync-tool.md)
- [Troubleshooting](troubleshooting.md)
- [Changelog](changelog.md)
