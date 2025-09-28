# 🐾 Animal Identification Expert System

Un **sistema experto en Prolog** que identifica animales mediante preguntas interactivas.

---

## 📦 Requisitos

- [SWI-Prolog](https://www.swi-prolog.org/) (recomendado)

---

## 📥 Instalación

```bash
# Clona el repositorio
git clone https://github.com/BasantesAndres/Prolog_lab02
cd Prolog_lab02

# Inicia SWI-Prolog
swipl
```

Carga el sistema (ajusta el nombre si corresponde):

```prolog
?- [lab2].        % o: ?- ['lab2.pl'].
```

---

## 🚀 Quick Start

Inicia la identificación interactiva:

```prolog
?- start.
```

**Ejemplo de sesión:**

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

| Comando                  | Descripción                                   |
|-------------------------|-----------------------------------------------|
| `start.`                | Inicia la identificación interactiva          |
| `list_animals.`         | Muestra todos los animales conocidos          |
| `test_system.`          | Ejecuta pruebas integrales del sistema        |
| `show_properties(cat).` | Muestra propiedades de un animal específico   |

**Ejemplos útiles:**
```prolog
?- list_animals.
?- show_properties(cat).
?- is_mammal(dog).
?- can_fly(eagle).
?- can_swim(duck).
```

---

## 🏗️ System Architecture

### Base de Conocimiento (hechos)

```prolog
has_fur(Animal).     % Mamíferos
lays_eggs(Animal).   % Aves, reptiles
flies(Animal).       % Animales voladores
swims(Animal).       % Animales acuáticos
```

### Motor de Inferencia (flujo)

```text
User Input → Questions → Pattern Matching → Classification → Result
```

---

## 🧪 Testing

Ejecuta la batería de pruebas:

```prolog
?- test_system.
```

**Salida esperada (ejemplo):**
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

### Casos de prueba individuales

| Prueba                   | Comando Prolog             | Resultado esperado |
|-------------------------|----------------------------|--------------------|
| Clasificación mamífero  | `?- is_mammal(dog).`       | `true.`            |
| Clasificación ave       | `?- is_bird(chicken).`     | `true.`            |
| Capacidad de volar      | `?- can_fly(eagle).`       | `true.`            |
| Capacidad de nadar      | `?- can_swim(duck).`       | `true.`            |
| Ver propiedades         | `?- show_properties(cat).` | lista de atributos |

---

## 🗂️ Estructura sugerida del repositorio

```text
Prolog_lab02/
├─ lab2.pl                 % Sistema experto (hechos + reglas + start/0)
├─ tests.pl                % Opcional: consultas usadas por test_system/0
└─ README.md               % Este archivo
```

---

## 🛠️ Tips

- Agrupa hechos por categoría (mamíferos, aves, reptiles, acuáticos).
- Añade animales declarando sus propiedades (ej.: `has_fur(cat).`, `meows(cat).`).
- Si varios animales coinc
