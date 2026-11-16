# Cybersecurity Homelab

A personal cybersecurity lab for building practical experience with virtualised infrastructure, vulnerable applications, security monitoring, and threat detection.

## Overview

This repository documents the setup and development of my cybersecurity homelab. The goal is to explore both offensive and defensive security in a controlled environment, including how activity on endpoints and web applications can be observed through security logs.

The lab is a work in progress. I'll add configuration notes, diagrams, and experiments as I complete them.

## Current environment

| Component | Purpose | Status |
| --- | --- | --- |
| Ubuntu Server + Docker + OWASP Juice Shop | Intentionally vulnerable web application for controlled testing | Deployed |
| Ubuntu Server + Wazuh | Centralised security monitoring | Deployed |
| Wazuh agent on the Juice Shop server | Collect endpoint security telemetry | Installed |
| Nginx | Reverse proxy and web access logs | Configuration in progress |
| Windows 11 virtual machine | Windows security testing and telemetry | VM set up; monitoring planned |

The lab uses virtual machines and a local test network. More detailed network architecture documentation will be added as the configuration develops.

## Homelab Topology - Written on [https://drawthenet.io/]
![Network Topology](architecture/network-topology.png)

## Tools and technologies

- **Virtualisation:** Hyper-V
- **Operating systems:** Ubuntu Server, Windows 11
- **Containers and applications:** Docker, OWASP Juice Shop
- **Monitoring:** Wazuh
- **Web infrastructure:** Nginx (in progress)
- **Planned telemetry:** Sysmon

## Planned work

- [ ] Document the network topology and virtual machine configuration.
- [ ] Complete the Nginx reverse proxy setup.
- [ ] Ingest and examine Nginx access logs in Wazuh.
- [ ] Generate controlled test activity against the lab application and examine resulting telemetry.
- [ ] Create and validate a Wazuh detection rule.
- [ ] Configure Windows event collection and Sysmon.
- [ ] Publish short reports covering security experiments, findings, and limitations.

## Documentation

This repository will gradually include:

- **Architecture:** a network diagram and descriptions of each system.
- **Setup:** reproducible instructions and sanitised configuration examples.
- **Experiments:** test objectives, procedures, observed events, detection results, and lessons learned.

## Scope and safety

All security testing described here is intended for systems I own or am explicitly authorised to test. Any published configuration files, logs, and screenshots will be reviewed to avoid exposing credentials, secrets, or sensitive network details.
