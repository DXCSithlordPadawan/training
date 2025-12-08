# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This repository contains an AI Training Documentation Project focused on creating a comprehensive training package for Artificial Intelligence tools including Claude Code, M365 Copilot, and related technologies. The project generates educational materials that comply with UK Government security standards.

## Project Goals

Create a complete self-study training program (37.5 hours/week) with:
- Detailed syllabus with hyperlinked resources and timings
- Curated list of free, verifiable resources (text and YouTube)
- Self-assessment questionnaires and quizzes
- Comprehensive documentation in multiple formats (MD, PDF, PPTX)
- Mermaid diagrams for architecture visualization
- YAML configuration examples

## Compliance Requirements

All deliverables must align with:
- **UK Gov Secure by Design** principles
- **NCSC Secure Design Principles**

## Required Deliverables

The project outputs the following files to `/localpath`:

1. **syllabus.md** - Detailed subject list with resource hyperlinks and timings
2. **resources.md** - Comprehensive list of all resources with URLs
3. **selfassessment.md** - Self-assessment questionnaire for post-training knowledge verification
4. **quiz.md** - Knowledge test with answers
5. **README.md** - Table of Contents, usage instructions, embedded diagrams, YAML examples
6. **aitrg_Guide.pdf** - Consolidated PDF with Executive Summary, Compliance Checklist, all docs, diagrams, YAML examples
7. **aitrg_Overview.pptx** - PowerPoint presentation for stakeholder distribution
8. **aitrg.zip** - Bundle containing all above assets

## Documentation Standards

- **Format**: All primary documents in Markdown (.md)
- **Diagrams**: Use Mermaid syntax for all architectural and process diagrams
- **Configuration**: YAML format with realistic example values
- **Resources**: Must be free (no payment or registration required) and verifiable
- **Content**: Include detailed server hardening steps where applicable

## Working Directory

All file operations should target: `localpath`

Permission is granted to write to this directory.

## Key Architectural Considerations

1. **Content Sourcing**: Resources must be both text-based and YouTube-based, ensuring diverse learning modalities
2. **Compliance Integration**: Security principles must be woven throughout the training content, not treated as separate modules
3. **Self-Assessment Design**: Questionnaires should validate practical understanding, not just theoretical knowledge
4. **Multi-Format Delivery**: Content must be adaptable across MD, PDF, and PPTX without loss of clarity
5. **Hyperlink Structure**: All syllabus entries must link directly to specific resources in resources.md for easy navigation

## Master Prompt Reference

The project requirements and action steps are defined in `aitrg_master_prompt.md`. Consult this file for complete project specifications and step-by-step generation instructions.
