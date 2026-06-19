# ForgeMesh Secure Connectivity Platform

**Status:** Sanitized public summary
**Format:** Public-safe product and validation overview
**Role:** Solo-developed secure connectivity platform
**Timeline:** 2026-present
**Current status:** Active MVP validation and product development

## One-Sentence Summary

ForgeMesh is a self-hosted secure connectivity platform designed to simplify remote access, device connectivity, and operational visibility across distributed environments while keeping control-plane ownership, network data, and security policy under customer control.

## Quick Read

- Built as a standalone self-hosted connectivity product, independent from mandatory SaaS infrastructure.
- Designed for remote employees, distributed infrastructure, cloud resources, branch locations, industrial systems, and edge devices.
- Uses a customer-owned control plane for identity, enrollment, approval, authorized configuration, audit events, and operational visibility.
- Prioritizes validation, diagnostics, controlled rollout, and repeatable testing before expanding networking scope.
- Current validation has proven Windows install, join, approval, connect, reboot recovery, upgrade recovery, peer reachability, and endpoint-discovery stability in controlled lab conditions.
- Direct internet connectivity, NAT traversal, LTE/CGNAT behavior, relay fallback, router nodes, and broader policy models remain explicit roadmap milestones rather than completed claims.

## Overview

ForgeMesh originated from operational requirements around remote support, industrial monitoring systems, distributed infrastructure, customer-owned environments, and geographically distributed devices. In those contexts, secure access and visibility were as important as connectivity itself. Traditional VPN deployments, router-level changes, port forwarding, static IP assumptions, and third-party networking services can create friction for support and operations teams.

The product direction is to provide a secure connectivity layer that organizations can host and control themselves. ForgeMesh aims to reduce the operational burden of connecting people, systems, and infrastructure without requiring customers to surrender ownership of their control plane, topology data, audit records, or security policies.

See: [ForgeMesh connectivity flow](../assets/diagrams/forgemesh-connectivity-flow.md)

## Problem

Distributed environments often include remote employees, servers, cloud resources, branch locations, industrial systems, RTUs, and edge devices. Providing secure connectivity between those systems can require VPN appliances, manual firewall rules, port forwarding, static IP dependencies, and vendor-operated networking services.

Those approaches can increase support overhead, reduce visibility, make troubleshooting harder, and create uncomfortable ownership boundaries around network data and operational access.

## Solution

ForgeMesh provides a self-hosted connectivity layer built around customer-controlled infrastructure. The platform focuses on secure device connectivity, device enrollment, identity and authorization, endpoint discovery, authorized configuration, operational diagnostics, controlled rollout, and validation-driven network behavior.

The intent is not to replace every networking product. The goal is to provide a practical, owner-controlled connectivity platform for teams that need stronger visibility, clearer auditability, and less dependence on router changes or externally operated control planes.

## Architecture Principles

| Principle | Meaning |
| --- | --- |
| Customer-owned infrastructure | The organization owns the control plane, database, network data, policies, logs, and deployment environment. |
| Security by design | Device approval, hashed tokens, controlled authorization, secure communication paths, and audit events are core behaviors rather than later additions. |
| Validation-driven development | Connectivity behavior is tested through repeatable validation flows before being treated as production-ready capability. |
| Connectivity first | The platform is measured by whether it reduces friction connecting people, systems, and infrastructure. |
| Operational safety | Ordinary mesh clients should not take ownership of DNS resolution, default routes, gateways, or endpoint-security behavior unless explicitly authorized. |

## Operational Safety

ForgeMesh is designed to minimize disruption to existing environments. Ordinary mesh clients should not take ownership of DNS resolution, default routes, gateways, or endpoint-security behavior unless that behavior is explicitly authorized.

Secure access should improve supportability without silently changing how the customer's existing environment resolves names, routes traffic, or enforces endpoint security.

## Current Product Shape

ForgeMesh is structured as a standalone product family with these surfaces:

| Surface | Purpose |
| --- | --- |
| Control plane | Self-hosted API service for owner bootstrap, users, invites, device enrollment, approval, authorized configuration, audit events, licensing, and client release workflows. |
| Desktop client | Endpoint client and service lifecycle for Windows-first validation, with Linux/macOS direction as part of the product surface. |
| Device and service lifecycle | Join, approval, connection, status, diagnostics, service start/stop, reboot recovery, and upgrade recovery flows. |
| Endpoint discovery | Diagnostic visibility into local and observed endpoint candidates without causing unstable configuration churn. |
| Reach and relay direction | Customer-owned internet-reachable roles for future endpoint discovery, NAT traversal assistance, and encrypted relay fallback. |
| Router and edge direction | Future support for gateway, RTU, industrial, and site-level connectivity through approved routing roles. |

## Validation Work

The current validation approach separates proven behavior from roadmap behavior.

Validated in controlled Windows lab conditions:

- Install from a packaged Windows client artifact.
- Join through a one-time invite.
- Admin approval and mesh IP assignment.
- Service-owned connection lifecycle after approval.
- Peer reachability between approved Windows clients.
- Reboot recovery.
- Upgrade recovery while preserving local identity and state.
- Endpoint-discovery visibility without unnecessary configuration churn.
- DNS and default-route safety for ordinary mesh clients.

Not yet claimed as complete:

- Direct internet connectivity across unrelated networks.
- NAT traversal or UDP hole punching.
- LTE, CGNAT, hotel Wi-Fi, or restrictive corporate NAT behavior.
- Relay fallback.
- Long-duration uptime validation.
- Router nodes, NAT gateway behavior, exit nodes, DNS provider behavior, or full policy enforcement.

## Responsibilities

- Product architecture and boundary definition.
- Rust control-plane and client/service development.
- Self-hosted SQLite-backed control-plane design.
- Device enrollment, approval, authorized configuration, and audit-event workflow design.
- Windows client packaging, installation, service lifecycle, diagnostics, and validation planning.
- Endpoint-discovery and connectivity-observability planning.
- Documentation, runbooks, validation records, and technical risk boundaries.
- AI-assisted engineering workflow with human-owned architecture, validation, and release decisions.

## Technologies

| Area | Technologies / Practices |
| --- | --- |
| Core implementation | Rust |
| Desktop/client surface | Tauri direction, Windows service lifecycle, packaged client artifacts |
| Data layer | SQLite, schema migrations, local state persistence |
| APIs | HTTPS/HTTP API design, owner/admin workflows, device-token workflows |
| Connectivity | Secure transport lifecycle, endpoint discovery, future customer-owned reach and relay roles |
| Validation | Windows lifecycle validation, peer reachability checks, diagnostics export, smoke scripts, runbooks |

## Business Value

ForgeMesh is designed to help organizations:

- Reduce remote-access and device-connectivity complexity.
- Maintain ownership of networking infrastructure, policies, and operational data.
- Improve visibility into device state, connectivity status, and endpoint behavior.
- Support distributed users, infrastructure, and industrial environments more safely.
- Reduce reliance on router-level changes, static network assumptions, and vendor-operated control planes.
- Make connectivity issues easier to reproduce, diagnose, and validate before rollout.

## Why It Matters

Secure connectivity is not just a networking problem. It is also an operations, support, auditability, and ownership problem. ForgeMesh reflects the same engineering philosophy used elsewhere in this portfolio: make the environment reproducible, keep authority explicit, validate behavior before expanding scope, and document boundaries honestly.

## Public-Safe Boundary

This page does not include proprietary source code, private endpoints, credentials, customer data, internal deployment details, license files, screenshots, or sensitive network information.