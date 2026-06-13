# Cybersecurity Homelab Overview

## Purpose

This homelab is a practical cybersecurity learning environment built to develop hands-on skills in system administration, networking, blue-team monitoring, log analysis, vulnerability management, and incident response.

The lab is designed around realistic constraints: using available hardware, open-source tools where practical, and a phased learning approach. The aim is not to build a perfect enterprise environment, but to create a useful, repeatable, and well-documented lab for developing cybersecurity skills.

## Learning Goals

The main goals of this homelab are to practise:

- Virtualisation with Proxmox
- Windows and Linux administration
- Network troubleshooting
- SSH and remote administration
- Centralised logging
- SIEM deployment and monitoring
- Vulnerability scanning
- Incident response workflows
- Security documentation
- GRC-aligned technical evidence gathering

## Current Hardware

| Device | Role | Notes |
|---|---|---|
| Proxmox Host | Virtualisation server | Runs the main cybersecurity lab VMs |
| HP ProBook 450 G6 | Windows admin workstation | Windows 11 Pro, used for administration and testing |
| HP ProBook 11 G2 | Future lab device | Available for future use |
| HP 250 G8 | Non-lab device | Repurposed for work-from-home use |

## Current Admin Workstation

| Item | Details |
|---|---|
| Hostname | cli-w11pro-01 |
| Operating System | Windows 11 Pro |
| CPU | Intel i7 8th Gen |
| RAM | 16 GB |
| Storage | 256 GB SSD |
| Local Admin Account | wst-admin |
| IP Address | 192.168.1.123 |
| Tools Installed | Wireshark, Nmap, administration tools |

## Current Virtual Machines

| VM Name | Role | Status |
|---|---|---|
| srv-ubuntu-01 | Ubuntu server | Built and configured |
| cli-ubuntu-01 | Ubuntu client | Built and configured |
| Future Wazuh VM | SIEM / security monitoring | Built and configured |
| Future test targets | Vulnerability and detection practice | Planned |

## Current Skills Practised

So far, this lab has involved:

- Installing and managing virtual machines in Proxmox
- Building Ubuntu server and client systems
- Configuring a Windows 11 Pro administration workstation
- Testing SSH connectivity between Linux systems
- Troubleshooting SSH configuration issues
- Using snapshots for rollback and recovery
- Preparing for centralised logging
- Documenting technical decisions and issues
- Deploying Wazuh manager and monitoring agents

## Current Lab Phase

The current focus is Wazuh deployment and monitoring.

The next major milestone is to collect logs from lab systems into a central security monitoring platform and begin building detection and investigation workflows before moving on to Vulnerability scanning.

## Planned Lab Roadmap

| Phase | Topic | Status |
|---|---|---|
| Phase 1 | Proxmox setup | Complete |
| Phase 2 | Ubuntu server and client setup | Complete |
| Phase 3 | Windows admin workstation setup | Complete |
| Phase 4 | SSH and remote administration | Complete |
| Phase 5 | Centralised logging | Complete |
| Phase 6 | Wazuh SIEM deployment | Complete |
| Phase 7 | Wazuh SSH detection validation | Complete |
| Phase 8 | Vulnerability scanning | Planned |
| Phase 9 | Incident response exercises | Planned |
| Phase 10 | Reporting and GRC-style documentation | Planned |

## Documentation Standard

Each major lab phase should include:

- Objective
- Environment
- Tools used
- Steps performed
- Commands used
- Explanation of important commands
- Issues encountered
- Troubleshooting process
- Final outcome
- Screenshots or sanitized evidence
- Reflection

## Security and Privacy Notice

This repository is public and contains only sanitized documentation.

The following information should not be committed:

- Passwords
- Private keys
- API tokens
- Real credentials
- Public IP addresses
- Personal data
- Sensitive screenshots
- Router or ISP details
- Unredacted configuration files

## Reflection

This homelab is intended to show practical learning, not just completed tasks. Troubleshooting, failed attempts, configuration mistakes, and rollback decisions are documented because they show real operational thinking and technical growth.
