# NTest SBOM Scanner

**Status:** Private/proprietary source code not included  
**Format:** Public-safe summary

## Overview

The SBOM Scanner is an internal desktop utility for software inventory and vulnerability visibility. It was built to simplify SBOM scanning, vulnerability review, and report export for support, QA, secure development lifecycle, and compliance operations.

Two related implementations exist in the private project history:

- JavaFX/Maven desktop application
- Modern Tauri/Rust/TypeScript desktop application

## Problem

SBOM and vulnerability review workflows can be difficult for non-specialists when they rely on manual command-line usage. Support and QA teams need repeatable outputs that can be reviewed, archived, and shared internally.

## Solution

The tool wraps SBOM scanning workflows in a desktop interface:

- Select SBOM input files.
- Run vulnerability scans through established tools.
- Export readable reports.
- Create consistent summaries for internal review.
- Detect or help manage required scanner dependencies.

## Technologies

| Area | Technologies |
| --- | --- |
| Original desktop app | JavaFX, Maven |
| Modern desktop app | Tauri, Rust, TypeScript |
| SBOM generation/scanning workflows | Syft, Grype |
| Reports | HTML, JSON, Excel-style outputs |
| Platforms | Windows, Linux, macOS concepts |

## Business and Compliance Impact

- Improved software inventory visibility.
- Helped automate vulnerability reporting workflows.
- Supported secure development lifecycle practices.
- Made scanner outputs easier to consume by support, QA, and compliance stakeholders.

## Public-Safe Boundary

This page does not publish proprietary source code, internal package lists, vulnerability findings, customer references, or confidential software inventory.
