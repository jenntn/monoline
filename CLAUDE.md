# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

MONOLINE is a personal Kanban board app for tracking projects. It supports multiple boards (e.g., wedding planning, home improvement) with drag-and-drop cards organized into columns/lanes.

## Architecture

Single-file app: everything lives in `index.html` — HTML, CSS, and JavaScript inline. No build tools, no dependencies, no framework. Data is persisted in `localStorage`.

### Data Model

- **Boards** — top-level containers; user can create multiple independent boards
- **Columns** — vertical lanes within a board (e.g., To Do, In Progress, Done); user-defined per board
- **Cards** — items within a column, each containing:
  - Title
  - Free-form notes (rich text)
  - Sub-tasks (checklist with checkboxes)
  - Gmail link (optional URL to an email thread)
  - Tags (colored labels for categorization)

### Design System

Minimal black-and-white wireframe aesthetic — like a low-fidelity designer mockup. Monochrome palette with color used sparingly and only for functional purposes: tag badges and warning/status highlights. The look should feel skeletal, structural, and intentionally unfinished.

## Development

Open `index.html` directly in a browser. No server required. Refresh to see changes.

## Conventions

- All code stays in the single `index.html` file
- No external dependencies or CDNs unless absolutely necessary (e.g., a drag-and-drop library)
- Use vanilla JS — no frameworks
- Mobile-friendly: must work well on phone screens
- localStorage for all persistence
