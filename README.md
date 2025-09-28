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
cd Prolog_lab02

# Start SWI-Prolog
swipl
```

Load the system (adjust the filename if needed):

```prolog
?- [lab2].        % or: ?- ['lab2.pl'].
```

---

## 🚀 Quick Start

Start the interactive identification system:

```prolog
?- start.
```

**Example session:**

```text
=== ANIMAL IDENTIFICATION EXPERT SYSTEM ===
Does it have fur or hair? (yes/no): yes.
Does it make a characteristic sound? (yes/no): yes.
What sound does it make?
Options: [bark, meow, neigh]
Your answer: bark.
I think the animal is: dog
```

---

## 📖 Usage Guide

| Command                  | Description                                 |
|-------------------------|---------------------------------------------|
| `start.`                | Launch interactive identification           |
| `list_animals.`         | Show all known animals                      |
| `test_system.`          | Run the system’s comprehensive tests        |
| `show_properties(cat).` | Display the properties of a specific animal |

**Examples:**
```prolog
?- list_animals.
?- show_properties(cat).
?- is_mammal(dog).
?- can_fly(eagle).
?- can_swim(duck).
```

---

## 🏗️ System Architecture

### Knowledge Base (facts)

```prolog
has_fur(Animal).     % Mammals
lays_eggs(Animal).   % Birds, reptiles
flies(Animal).       % Flying animals
swims(Animal).       % Aquatic animals
```

### Inference Engine (flow)

```text
User Input → Questions → Pattern Matching → Classification → Result
```

---

## 🧪 Testing

Run the full test suite:

```prolog
?- test_system.
```

**Expected output (example):**
```text
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
```

### Individual test cases

| Test                    | Prolog Command             | Expected Result |
|-------------------------|----------------------------|-----------------|
| Mammal classification   | `?- is_mammal(dog).`       | `true.`         |
| Bird classification     | `?- is_bird(chicken).`     | `true.`         |
| Flying ability          | `?- can_fly(eagle).`       | `true.`         |
| Swimming ability        | `?- can_swim(duck).`       | `true.`         |
| Show properties         | `?- show_properties(cat).` | lists attributes |

---

## 🗂️ Suggested Repository Structure

```text
Prolog_lab02/
├─ lab2.pl                 % Main expert system (facts + rules + start/0)
├─ tests.pl                % Optional: queries used by test_system/0
└─ README.md               % This file
```

---

## 🛠️ Tips

- Group facts by category (mammals, birds, reptiles, aquatic).
- Add new animals by asserting their properties (e.g., `has_fur(cat).`, `meows(cat).`).
- If multiple animals match, refine the question flow inside `start/0`.

---

## 📜 License

MIT — free to use, modify, and distribute.
