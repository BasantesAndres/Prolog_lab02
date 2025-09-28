`# 🐾 Animal Identification Expert System
A Prolog-based expert system that identifies animals through interactive questioning.
📥 Installation
Clone from Repository
bash# Clone the repository
git clone https://github.com/yourusername/prolog-expert-system.git
cd prolog-expert-system

# Start SWI-Prolog
swipl

# Load the system
?- [animal_expert].
🚀 Quick Start
Start the interactive identification system:
prolog?- start.
Follow the prompts and answer with yes or no:
=== ANIMAL IDENTIFICATION EXPERT SYSTEM ===
Does it have fur or hair? (yes/no): yes.
Does it make a characteristic sound? (yes/no): yes.
What sound does it make?
Options: [bark, meow, neigh]
Your answer: bark.
I think the animal is: dog
📖 Usage Guide
CommandDescriptionstart.Launch interactive identificationlist_animals.Show all known animalstest_system.Run comprehensive testsshow_properties(cat).Display animal properties
🏗️ System Architecture
Knowledge Base Structure
Facts (Properties)
├── has_fur(Animal)         # Mammals
├── lays_eggs(Animal)       # Birds, reptiles
├── flies(Animal)           # Flying animals
└── swims(Animal)           # Aquatic animals
Inference Engine Flow
User Input → Questions → Pattern Matching → Classification → Result
🧪 Testing
Run All Tests
prolog?- test_system.
Expected Output
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
Individual Test Cases
TestCommandExpected ResultMammal classification?- is_mammal(dog).true.Bird classification?- is_bird(chicken).true.Flying ability?- can_fly(eagle).true.Swimming ability?- can_swim(duck).true.Properties display?- show_properties(cat).List of cat properties
