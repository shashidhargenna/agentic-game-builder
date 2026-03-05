# Agentic Game Builder AI

## Overview

This project implements an **agentic AI system** that generates a playable browser game from a natural language idea.

The system is built using **n8n workflows** and follows three agent phases:

1. Requirements Clarification
2. Game Planning
3. Code Generation

The AI agent outputs a playable game using:

- index.html
- style.css
- game.js

# Architecture

User Input
↓
Webhook
↓
Clarification Agent
↓
Planning Agent
↓
Code Generator Agent
↓
Generated Game Files

# Tech Stack

- n8n (workflow orchestration)
- OpenAI API
- HTML / CSS / JavaScript
- Docker

# Project Structure
agentic-game-builder
│
├── Dockerfile
├── docker-compose.yml
│
├── game
│ ├── index.html
│ ├── style.css
│ └── game.js
│
└── workflows
└── game_builder_workflow.json

# Running the Project

### 1 Install Docker

https://www.docker.com/products/docker-desktop/

### 2 Start the system

docker compose up

### 3 Open n8n
http://localhost:5678

### 4 Import Workflow

Import:
workflows/game_builder_workflow.json

### 5 Send Game Idea

Example request:POST /webhook/game-idea

### Example Idea

Snake game where the snake grows by eating food.

# Output

The agent generates a playable browser game.

Open:
game/index.html

in your browser to play.

# Improvements (Future Work)

- Multi-game generation
- Asset generation using AI
- Dynamic difficulty systems
- Game templates library
