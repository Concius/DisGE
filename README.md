# DisGE

# DisGE: Dynamic Interactive Structure Grammatical Evolution

A novel two-stage Grammatical Evolution framework for generating dynamic dialogue in interactive entertainment systems.

## Overview

DisGE addresses the critical challenge of maintaining engaging NPC dialogue throughout extended gameplay sessions. Traditional dialogue systems rely on static, pre-written content that quickly becomes repetitive. DisGE separates dialogue architecture evolution from semantic content generation, enabling contextually appropriate and personality-consistent conversations.

## Key Features

- **Two-Stage Evolution**: Separate optimization of dialogue structure and semantic content
- **Context-Aware**: Integrates game state, relationships, weather, and character personalities
- **Real-Time Performance**: ~24s generation time suitable for interactive applications
- **Perfect Structural Diversity**: Generates unique dialogue patterns across scenarios
- **Modular Architecture**: Ready for integration with Large Language Models

## System Architecture

### Stage 1: Structure Evolution
- Evolves dialogue flow patterns and conversational architectures
- Generates variable-length sequences (2-6 elements)
- Adapts complexity based on relationship levels and context

### Stage 2: Content Evolution
- Populates structures with semantically appropriate content blocks
- Operates at conceptual rather than linguistic levels
- Maintains character personality consistency

## Quick Start

```python
from disge import DisGESystem

# Initialize system
disge = DisGESystem()

# Define game context
context = {
    'activity': 'fishing',
    'time': 'morning',
    'weather': 'sunny',
    'relationship_level': 5
}

# Define character
character = {
    'name': 'Fisher Bob',
    'chattiness': 0.6,
    'formality': 0.4,
    'style': 'friendly'
}

# Generate dialogue
dialogue = disge.generate_dialogue(context, character)
print(dialogue)
