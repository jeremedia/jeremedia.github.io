---
layout: post
title: "Literate Technology at Work: A Real Example"
date: 2025-07-14
categories: technology
---

## Literate Technology at Work: A Real Example

*Computing that works through conversation, turning plain language into executable action.*

This migration case study is more than just a technical success story—it is a living example of *Literate Technology* in action.

**Literate Technology** reimagines computers as literate collaborators—tools that understand, respond to, and act upon natural language. With a coding assistant like Claude Code, users don’t need to know the syntax of Bash, the intricacies of DNS APIs, or the arcane details of VirtualMin configuration. Instead, they describe their goals in ordinary language. The assistant—imbued with the power of literate computing—translates these goals into concrete, executable actions.

In this example, the engineer never wrote a shell script or touched a config file; the assistant generated each command and configuration step and, with the engineer’s explicit approval, invoked them directly in the engineer’s shell using the provided credentials—allowing the engineer to focus entirely on describing needs, intentions, and constraints in plain English. The coding assistant handled:

- Provisioning new cloud servers
- Securely connecting remote networks
- Rewriting DNS records at scale
- Debugging and automating a complex migration

Every step was completed under *plain-English supervision*, with the assistant reporting back in understandable terms, adapting to new instructions, and clarifying only when necessary.

**This is the promise of Literate Technology:**
Computing, at every level of complexity—from launching droplets to tuning firewalls—can now be accessed, controlled, and orchestrated by *anyone* who can communicate with language. The mysteries of the “arcane” command line, API, and infrastructure are unmasked and democratized. Technical power is no longer reserved for those fluent in code, but is extended to every literate user.

Here, a coding assistant becomes, quite literally, the *literate interface* to the world of system administration—making every advanced potential of the computer accessible, usable, and trustworthy.

---

## Case Study: Coding Assistant-Driven Migration with Engineer Supervision

### Background

A senior engineer needed to migrate a multi-domain VirtualMin Ubuntu machine serving 67 sites from a robust, static-IP fiber environment to a cable internet connection with dynamic addressing, achieving the cutover with under five minutes of cumulative downtime across all sites. The engineer’s priority was to retain the home-based VirtualMin stack for control and cost efficiency, but the new network context demanded a radical change in exposure, routing, and automation.

With only SSH and cloud provider credentials in hand, the engineer turned to a coding assistant—Claude Code—not for documentation or code snippets, but for *hands-on execution* based on plain-English direction.

### A Division of Roles

- **Engineer:** Provided access credentials and high‑level English instructions to set up Tailscale on the droplet, configure Caddy as a reverse proxy, update Google DNS records, and validate via the VirtualMin API over SSH.
- **Coding Assistant:** Took those instructions, ran all commands, created configurations, handled errors, and reported results back, asking for confirmation or new direction only when needed.

### Step-by-Step Narrative

#### 1. Engineer’s English-Language Plan

*High‑level goals and constraints stated in plain English.*

With the high‑level goal clarified, the assistant asked only a handful of follow‑up questions—such as which specific domains and which cloud region—before proceeding.

#### 2. Assistant Executes the Plan

*Assistant translates the plan into concrete actions—provision, connect, configure.*

**A. Provisioning and Service Installation**

Upon receiving SSH credentials, Claude Code:

- Created the Digital Ocean droplet as directed.
- Installed and authenticated Tailscale using the provided auth key.
- Installed Caddy and configured it for multi-domain reverse proxying to the home server’s Tailscale IP.

**B. DNS Automation**

With access to the Google Cloud DNS API or credentials, the assistant:

- Queried for all relevant A records.
- Updated each domain’s A record to the droplet’s IP, handling propagation and verifying DNS status.

**C. Validation with VirtualMin API**

Following the engineer’s plain-English instructions, Claude Code:

- Used SSH to access the home VirtualMin server.
- Ran `virtualmin list-domains` and `virtualmin check-config`, reporting back in the agreed format (JSON or plain text) to the engineer.

#### 3. Troubleshooting and Adjustment

*Iterative fixes applied as real‑world issues surface.*

When issues arose—such as two domains returning 502 errors—the engineer simply stated the problem (“Two domains are returning 502s. Here are the logs and the curl output.”). Claude Code:

- Inspected Caddy’s logs and upstream configurations.
- Ran connectivity tests between the droplet and the home server over Tailscale.
- Diagnosed a firewall rule as the root cause, fixed it, and re-tested access.
- Reported the successful fix back to the engineer.

#### 4. Flow of Control

At all times, the engineer remained in charge of intent, policy, and final approval.\
The assistant never acted without direction, and never assumed context not given in plain English. The engineer did *not* write code or run commands—only provided permissions and operational goals.

### Key Benefits for Engineers

- **Eliminate context-switching:** Translate business or operational goals directly into action—no need to touch Bash, Python, or Caddyfile syntax.
- **Automate every step:** Handle cloud provisioning, DNS cutover, and health checks with only English instructions and credential setup.
- **Deliver instant troubleshooting:** Investigate, resolve, and verify issues described in plain language, keeping the engineer firmly in their natural-language comfort zone.
- **Ensure accountability:** Report progress, request confirmations, and surface logs for full transparency and auditability.

### Key Benefits for Everyone

- **Speak plainly:** Use everyday language to accomplish complex tasks—no command-line skills required.
- **Gain instant expertise:** Tap into a vast reservoir of technical knowledge without years of training.
- **Stay in control:** Define goals and constraints in plain language while the assistant handles execution under your direction.
- **Save time and reduce stress:** Offload tedious configuration and troubleshooting to the assistant and focus on higher‑level decisions.
- **Expand possibilities:** Access powerful computing capabilities that were previously out of reach for non‑specialists.

### Conclusion

This migration was not a demonstration of AI as a search engine or an “autocomplete on steroids”—it was a live proof that coding assistants, when granted access and supervised by a human, can carry out complex technical operations with reliability and speed. The human engineer set the vision and policy; the assistant handled every command-line and configuration detail, closing the loop between intent and outcome.

For engineering teams, the message is clear: *You don’t have to hand over control—just give direction. The assistant will do the rest, and tell you exactly what happened.*

---

## About This Narrative

This case study was not imagined or based on theoretical capabilities. Instead, the narrative was **directly derived from actual session logs** generated during a real infrastructure migration using Claude Code as the coding assistant.

#### How the Narrative Was Built

- **Session logs** (in JSONL format) captured every exchange:
  - The engineer’s English-language instructions, context, and decisions
  - The coding assistant’s responses, clarifications, execution steps, and status reports
- **All technical actions** described—provisioning servers, configuring services, updating DNS, troubleshooting, and validation—were recorded as real requests and outputs in the assistant’s log.
- **Representative excerpts** from these logs were distilled into “scripted scenes” that reflect the true sequence and flavor of the migration, with no technical steps invented or dramatized.
- **Control and agency** in the story reflect what actually occurred:
  - The human set intent and policy in English
  - The assistant did the command-line and configuration work
  - The assistant reported status and awaited further human direction before taking additional action

#### Why This Matters

By grounding the narrative in actual logs:

- The story becomes a reliable demonstration of what current coding assistants can achieve with real engineer guidance.
- It provides **verifiable evidence** of how such collaborations unfold: the division of labor, the pace of troubleshooting, and the technical literacy of the assistant.

These logs show that natural language alone can now orchestrate complex systems. That’s Literate Technology in practice.



