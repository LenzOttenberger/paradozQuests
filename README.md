# Paradoz Quests

Story quests for **Minecraft Paper** servers using **BetonQuest 3.0**.

This repository contains the quest system for the **Paradoz** project. Every quest is written as a separate package to keep the project scalable and easy to maintain.

## Features

- 📖 Story-driven quests
- 💬 Branching NPC dialogues
- 🧩 Modular package structure
- 👥 Citizens NPC integration
- ⚡ Designed for BetonQuest 3.0
- 📈 Easy to extend with new quests and NPCs

---

## Requirements

- Paper
- BetonQuest 3.0 (development build)
- Citizens

Additional plugins may be required depending on future quests.

---

## Project Structure

```
packages/
│
├── edwin/
│   ├── actions.yml
│   ├── conditions.yml
│   ├── conversation.yml
│   ├── objectives.yml
│   └── package.yml
│
├── lia/
├── mirabel/
├── roy/
└── tom/
```

Each NPC has its own package.

A package usually contains:

| File | Description |
|------|-------------|
| actions.yml | Quest actions |
| conditions.yml | Dialogue and quest conditions |
| conversation.yml | NPC conversations |
| objectives.yml | Objectives and stages |
| package.yml | Package registration |

---

## Design Philosophy

The project follows a modular architecture.

- Every NPC manages only its own dialogue.
- Quest progress is controlled through objectives and stages.
- NPC packages remain independent from each other.
- Adding new content should not require editing old conversations whenever possible.

This makes the project easy to expand as the storyline grows.

---

## Current Quests

| ID | Name | Status |
|----|------|--------|
| q001 | Welcome to Aeris | ✅ Complete |

More quests are currently in development.

---

## Adding a New Quest

1. Create or choose an NPC package.
2. Add new dialogue to `conversation.yml`.
3. Register actions and conditions.
4. Create quest objectives.
5. Connect the quest with previous progression if necessary.

The repository is organized so that new quests can be added without restructuring existing ones.

---

## Naming Convention

Quest IDs:

```
q001
q002
q003
...
```

NPC packages:

```
edwin
lia
mirabel
roy
tom
```

Actions and conditions follow the quest ID:

```
start_q001
finish_q001
q001_stage
```

This keeps every quest self-contained and avoids naming conflicts.

---

## Future Plans

- Main storyline
- Side quests
- NPC schedules
- Cutscenes
- Timed quests
- Reputation system
- Hidden dialogue branches
- World events

---

## License

This repository is intended for the Paradoz project.

Feel free to use it as inspiration for your own BetonQuest projects.
