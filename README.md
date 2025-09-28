# 🐾 Animal Identification Expert System

A **Prolog-based expert system** that identifies animals through interactive questioning.

---

## 📦 Requirements

- [SWI-Prolog](https://www.swi-prolog.org/) (recommended)

---

## 📥 Installation

```bash
# Clone the repository
git clone https://github.com/BasantesAndres/Prolog_lab02
cd prolog-expert-system

# Start SWI-Prolog
swipl

# Load the system (adjust filename if needed)
?- lab2.pl
---

## 🚀 Quick Start

Start the interactive identification system:

```prolog
?- start.

=== ANIMAL IDENTIFICATION EXPERT SYSTEM ===
Does it have fur or hair? (yes/no): yes.
Does it make a characteristic sound? (yes/no): yes.
What sound does it make?
Options: [bark, meow, neigh]
Your answer: bark.
I think the animal is: dog


```markdown
## 📖 Usage Guide

| Command                 | Description                           |
|-------------------------|---------------------------------------|
| `start.`                | Launch interactive identification     |
| `list_animals.`         | Show all known animals                |
| `test_system.`          | Run comprehensive tests               |
| `show_properties(cat).` | Display properties of a specific animal |

Examples:

```prolog
?- list_animals.
?- show_properties(cat).
?- is_mammal(dog).
?- can_fly(eagle).
?- can_swim(duck).


```markdown
## 🏗️ System Architecture

### Knowledge Base Structure

Facts (properties) commonly used:

```prolog
has_fur(Animal).     % Mammals
lays_eggs(Animal).   % Birds, reptiles
flies(Animal).       % Flying animals
swims(Animal).       % Aquatic animals

User Input → Questions → Pattern Matching → Classification → Result


```markdown
## 🧪 Testing

Run all tests:

```prolog
?- test_system.
=== SYSTEM TESTS ===
Mammals:
- cat
- dog
- horse
- rabbit

Birds:
- chicken
- duck
- eagle
- ostrich
- penguin

Animals that fly:
- chicken
- eagle

