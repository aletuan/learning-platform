# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a **Learning Video Platform** project in the planning and documentation phase. The project is a comprehensive video-based educational platform that combines video streaming, AI-powered features, interactive learning tools, and community engagement.

**Current Status**: Documentation and product design phase - no implementation code exists yet.

## Architecture & Structure

### Current Repository Structure
```
learning-platform/
├── docs/                           # Comprehensive project documentation
│   ├── analysis/                   # Product analysis and market research
│   ├── prds/                       # Product Requirements Documents
│   ├── roadmap/                    # Development roadmap and prioritization
│   └── setup/                      # Configuration and setup documentation
├── .mcp.json                       # MCP server configuration
└── CLAUDE.md                       # This file
```

### Planned Platform Architecture
Based on the PRDs, the system will include:

- **Core Video Streaming Infrastructure** (M1): HTML5 player with adaptive bitrate streaming, multi-quality support, cross-device compatibility
- **AI-Powered Transcription System** (M2): Real-time synchronized subtitle generation, searchable transcripts, technical vocabulary optimization
- **User Management System** (M3): Authentication, profiles, GDPR/CCPA compliance, cross-device session sync
- **Content Management System** (M4): Hierarchical course structure, upload pipeline, search/filtering, approval workflow
- **AI-Generated Quiz System** (S1): Automated assessment generation, multiple question types, adaptive difficulty
- **Community Discussion Platform** (S2): Video-specific threads, Q&A system, user reputation, moderation tools

## MCP Integration

The project is configured with Model Context Protocol (MCP) servers for AI-powered automation:

### Available MCP Servers
- **Playwright MCP**: Browser automation, testing, web scraping, screenshot generation
- **Figma MCP**: Design workflow integration, asset retrieval, design system management

### Configuration
MCP servers are configured in `.mcp.json`. Figma integration requires `FIGMA_ACCESS_TOKEN` environment variable.

## Development Timeline & Phases

### Phase 1 - Foundation (Q1 2026)
- Core streaming infrastructure
- AI transcription system  
- User authentication & profiles

### Phase 2 - Enhancement (Q2 2026)
- Content management system
- AI-generated quizzes
- Community discussion features

### Phase 3 - Scale (Q3 2026)
- Mobile optimization
- Progress tracking & analytics
- Advanced content discovery

### Phase 4 - Differentiation (Q4 2026-Q2 2027)
- Gamification & badges
- Advanced AI features
- Creator tools

## Key Documentation Files

- `docs/prds/PRD-Summary-Index.md`: Master index of all product requirements
- `docs/analysis/Learning_Platform_Product_Analysis.md`: Comprehensive market analysis and competitive positioning
- `docs/roadmap/Product_Roadmap_MoSCoW.md`: Feature prioritization and development timeline
- `docs/setup/MCP_SETUP.md`: MCP server configuration and usage guide

## Target Market & Technical Focus

- **Primary Audience**: Students, professionals, educators, lifelong learners
- **Content Focus**: Technical and professional development (React, programming, etc.)
- **Key Differentiators**: AI integration, community-centric design, unified learning experience
- **Competition**: Positioned against Coursera, Udemy, Skillshare with superior AI features and community tools

## Project Guidelines

Since this is a documentation-phase project:
- Focus on planning, architecture, and requirement refinement
- No build/test/lint commands exist yet - implementation hasn't started
- Use MCP tools for research, competitive analysis, and design workflows
- Maintain comprehensive documentation as implementation approaches
- Follow PRD specifications when implementation begins