# BMAD Remote Sync Extension

## Overview

This is an experimental project extending [BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD) to address one of the current limitations of spec-driven development in collaborative environments.

## Problem Statement

Spec-driven design with BMAD works excellently when working alone, providing clear context and comprehensive development artifacts. However, in real-world collaborative scenarios with multiple team members, coordinating changes across distributed workspaces becomes complex. Team members working on different features need to stay synchronized with a central source of truth (like Jira, Linear, or other project management tools), leading to context loss and potential misalignment.

## Solution

This project aims to extend BMAD agents' capabilities by creating a custom agent and workflows that keep BMAD development artifacts in sync with remote project management tools using the **Model Context Protocol (MCP)** as the integration layer.


## Status

This is an **experimental and exploratory project** focused on discovery and proof-of-concept. It addresses one of the current limitations of spec-driven development by bridging the gap between isolated BMAD workflows and collaborative project management.

## Technology Stack

- [BMAD-METHOD](https://github.com/bmad-code-org/BMAD-METHOD) - Core framework
- Model Context Protocol (MCP) - Integration layer
- Custom BMAD agent and workflows - Synchronization logic

## Getting Started

To start using this extension, you need to configure your connection to your project management tool.

### Step 1: Add MCP Server for Your Project Management Tool

Configure the Model Context Protocol (MCP) server for your chosen project management tool. For Jira, use the official Atlassian MCP server:

- **Jira (Atlassian)**: [atlassian-mcp-server](https://github.com/atlassian/atlassian-mcp-server)
- Follow the setup instructions in the repository to connect your IDE/client to your Atlassian Cloud instance

For other project management tools (Linear, Asana, etc.), find or create an appropriate MCP server for that tool.

### Step 2: Configure Project Management Tool Information

Update the `docs/PM_TOOL.md` file with your specific project management tool configuration:

- Tool name and MCP server identifier
- Your name as the primary assignee
- Board URLs and project keys you work with
- Base URL and instance information

These configurations will be used by the BMAD development workflows to keep everything synchronized between your local workspace and the remote project management tool.

