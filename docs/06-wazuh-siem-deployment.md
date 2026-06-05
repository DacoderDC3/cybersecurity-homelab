# Wazuh SIEM Deployment

## Objective

Deploy Wazuh as the central security monitoring platform for the cybersecurity homelab and connect lab systems using Wazuh agents.

The goal of this phase was to establish basic endpoint visibility across the lab and prepare the environment for log analysis, alert review, vulnerability detection, and incident response practice.

## Environment

| System | Role | Status |
|---|---|---|
| Wazuh Manager | Central SIEM / security monitoring server | Deployed |
| srv-ubuntu-01 | Ubuntu server agent | Connected |
| cli-ubuntu-01 | Ubuntu client agent | Connected |
| Additional VM servers | Lab monitored endpoints | Connected |
| Windows Admin Workstation | Administration and testing | Used for access and validation |

## Tools Used

- Proxmox VE
- Ubuntu Server
- Wazuh Manager
- Wazuh Agents
- Wazuh Dashboard
- SSH
- Web browser
- Linux CLI

## Skills Practised

- SIEM deployment
- Endpoint agent installation
- Linux service validation
- Log collection
- Security monitoring
- Agent registration
- Troubleshooting connectivity
- Dashboard validation
- Evidence-based documentation

## Deployment Summary

Wazuh Manager was deployed as the central monitoring system for the homelab. Wazuh agents were installed across the VM servers and successfully connected to the manager.

This provides a foundation for future blue-team work, including:

- endpoint monitoring
- security alert review
- vulnerability visibility
- file integrity monitoring
- log analysis
- incident response exercises

## Verification Steps

The deployment was verified by checking:

- Wazuh Manager service status
- Wazuh Agent service status
- agent registration
- dashboard visibility
- communication between agents and manager
- alerts appearing in the Wazuh interface


## Evidence

> Screenshots to add later:

### Evidence	File
- Wazuh dashboard overview	screenshots/wazuh-dashboard-overview-redacted.png
- Connected agents list	screenshots/wazuh-agents-connected-redacted.png
- Wazuh Manager service status	screenshots/wazuh-manager-status-redacted.png
- Wazuh Agent service status	screenshots/wazuh-agent-status-redacted.png

## Issues encountered and resolved:

- Unsupported OS: I initially installed Wazuh on Ubuntu 26.04 which was unsupported, fortunately I had created baseline snapshot which I could rollback to and troubleshoot further.
-- Resolution: destroyed the VM, rebuilt using Ubuntu 24.04 LTS and re-installed Wazuh
- Not enough disk space: Wazuh did not install successfully becasue the VM wasn't allowing it to use the unused Free Disk space.
-- Resolution: A quick command expand the root filesystem did the trick sudo bash lvextend -r -l +100%FREE /dev/mapper...

## Security and Privacy Notes

The following information has been removed or redacted from public documentation:

- passwords
- enrollment keys
- authentication tokens
- private keys
- public IP addresses
- sensitive screenshots
- unnecessary personal information

> Reflection

Deploying Wazuh created the first proper security monitoring layer in the homelab. This phase moved the lab from basic system administration into blue-team operations by allowing multiple endpoints to report security events into a central platform.

This deployment will support future exercises in vulnerability management, incident response, alert triage, detection tuning, and security reporting.

## Useful Commands
Check services status

```bash
sudo systemctl status wazuh-manager
sudo systemctl status wazuh-agent

List connected agents from the manager
(Command meaning:
> ~/var/ossec/bin/agent_control: Wazuh’s agent management utility.
> -l: lists registered agents and their connection status.)

```bash
sudo /var/ossec/bin/agent_control -l
