# AI Knowledge Representation Lab Practicals

<p align="center">

**A collection of Python implementations demonstrating fundamental Knowledge Representation techniques in Artificial Intelligence.**

</p>

## About the Project

This repository contains four practical implementations of fundamental Artificial Intelligence concepts, focusing on Knowledge Representation and Knowledge-Based Systems.

The project demonstrates how real-world information can be represented, structured, stored, retrieved, and processed using Python.

Each implementation focuses on a different knowledge representation approach and provides a simple interactive interface for demonstrating its functionality.

## Practicals Included

| No. | Practical | Description |
|:---:|---|---|
| 01 | University Knowledge Base | Stores and retrieves university-related information. |
| 02 | Medical Knowledge Representation | Matches user-provided symptoms with predefined medical knowledge. |
| 03 | Semantic Network Construction | Represents concepts and their relationships using a network structure. |
| 04 | Frame Representation | Organizes knowledge using frames, slots, and values. |

## Technology Stack

- **Language:** Python 3.x
- **Data Structures:** Dictionaries, Nested Dictionaries, Sets
- **Core Concepts:** Knowledge Representation, Rule-Based Matching, Graph Relationships, Frame-Based Representation
- **Dependencies:** Python Standard Library

No external packages are required.

## Project Structure

```text
AI-Knowledge-Representation/
│
├── university_knowledge_base.py
│
├── medical_knowledge_representation.py
│
├── semantic_network.py
│
├── frame_representation.py
│
├── README.md
│
└── LICENSE
```

*The LICENSE file should be added only after selecting an appropriate license.*

---

## 1. University Knowledge Base

### Overview
Implements a simple University Knowledge Base that maintains structured information about students, teachers, and academic courses.

### Key Features
- Stores student records with unique student IDs.
- Maintains teacher information and subject assignments.
- Stores available academic courses.
- Retrieves student details using student ID.
- Displays teacher and course information.
- Provides an interactive, menu-driven interface.

### Implementation
The knowledge base is implemented using nested Python dictionaries, where information is organized into categories and key-value pairs.

### Concepts Demonstrated
- Knowledge Base Representation
- Structured Knowledge Storage
- Nested Dictionaries
- Information Retrieval
- Functions and Control Flow

### Complexity Analysis

Let N represent the number of student records, T the number of teachers, and C the number of courses.

| Operation | Time Complexity |
|---|---|
| Student Search | O(1) average |
| Display Teachers | O(T) |
| Display Courses | O(C) |
| Storage | O(N + T + C) |

**Limitation:** The information is stored in memory and is not persistent. Data is lost when the program terminates.

---

## 2. Medical Knowledge Representation

### Overview
Implements a basic medical knowledge representation system that identifies possible medical conditions by matching user-provided symptoms against predefined symptom sets.

### Key Features
- Maintains predefined symptom information for multiple medical conditions.
- Accepts multiple symptoms from the user.
- Performs symptom matching using set operations.
- Calculates the number of matching symptoms.
- Ranks possible conditions based on matching symptom counts.
- Displays matching results.

### Implementation
Medical knowledge is represented using Python dictionaries and sets. Each medical condition is associated with a predefined set of symptoms.

The system uses set intersection to identify common symptoms between user input and stored medical knowledge.

### Concepts Demonstrated
- Medical Knowledge Representation
- Set Theory and Set Operations
- Knowledge-Based Matching
- Rule-Based Systems
- Sorting and Result Ranking

### Complexity Analysis

Let D represent the number of medical conditions, S the maximum number of symptoms per condition, and I the number of input symptoms.

| Operation | Time Complexity |
|---|---|
| Symptom Matching | O(D × (S + I)) average |
| Sorting Results | O(D log D) |
| Overall Time | O(D × (S + I) + D log D) |
| Space | O(D × S + I + D) |

**Limitation:** This is an educational demonstration, not a clinically validated diagnostic system. Symptom matching does not establish a medical diagnosis.

---

## 3. Semantic Network Construction

### Overview
Implements a Semantic Network to represent concepts and the relationships connecting them.

The network demonstrates how knowledge can be organized in the form of interconnected entities.

### Key Features
- Represents entities such as Student, Teacher, Course, and University.
- Establishes relationships between different entities.
- Displays the complete semantic network.
- Allows searching for relationships associated with a particular node.
- Uses a menu-driven interface.

### Example Representation

| Source Node | Relationship | Target Node |
|---|---|---|
| Student | is_a | Person |
| Student | studies | Course |
| Student | belongs_to | University |
| Teacher | teaches | Course |
| Teacher | works_at | University |
| Course | offered_by | University |

### Implementation
The semantic network is represented using nested Python dictionaries, functioning as an adjacency-list-like structure.

Each key represents a source concept, while its associated relationships identify connected concepts.

### Concepts Demonstrated
- Semantic Networks
- Graph-Based Knowledge Representation
- Nodes and Edges
- Directed Relationships
- Adjacency List Representation

### Complexity Analysis

Let V represent the number of nodes and E represent the number of relationships.

| Operation | Time Complexity |
|---|---|
| Display Network | O(V + E) |
| Search Node | O(1) average |
| Display Node Relationships | O(degree of node) |
| Storage | O(V + E) |

**Limitation:** The current implementation supports direct relationship retrieval. It does not implement graphical visualization, relationship traversal, or automatic inference.

---

## 4. Frame Representation

### Overview
Implements Frame-Based Knowledge Representation to organize information about entities using frames, slots, and corresponding values.

Frames provide a structured method of representing objects, concepts, and their attributes.

### Key Features
- Creates frames for Student, Teacher, and Course.
- Defines attributes using slots.
- Stores corresponding values for each slot.
- Displays all available frames.
- Supports searching and displaying individual frames.

### Example Frame

**Frame: Student**

| Slot | Value |
|---|---|
| Name | Rahul |
| Age | 21 |
| Course | MCA |
| Department | Computer Science |
| University | DAVV |

### Implementation
Frames are implemented using nested Python dictionaries.

Each frame represents an entity, while its internal key-value pairs represent slots and their associated values.

### Concepts Demonstrated
- Frame-Based Knowledge Representation
- Frames, Slots, and Values
- Nested Dictionaries
- Structured Object Representation
- Information Retrieval

### Complexity Analysis

Let F represent the number of frames, K the maximum number of slots per frame, and N the total number of slots.

| Operation | Time Complexity |
|---|---|
| Search Frame | O(1) average |
| Display One Frame | O(K) |
| Display All Frames | O(N) |
| Storage | O(F + N) |

**Limitation:** The current implementation uses static frames and does not support advanced features such as inheritance, default slot values, or procedural attachments.

---

## Getting Started

### Prerequisites

Make sure Python 3.x is installed on your system.

Verify the installation:

```bash
python --version
```

### Installation

Clone the repository:

```bash
git clone https://github.com/Divyansh-techi/AI-Knowledge-Representation.git
```

Navigate to the project directory:

```bash
cd AI-Knowledge-Representation
```

No additional dependency installation is necessary.

### Running the Programs

Execute each practical independently:

**1. University Knowledge Base**

```bash
python university_knowledge_base.py
```

**2. Medical Knowledge Representation**

```bash
python medical_knowledge_representation.py
```

**3. Semantic Network Construction**

```bash
python semantic_network.py
```

**4. Frame Representation**

```bash
python frame_representation.py
```

*Note: The filenames in the commands should match the actual filenames in the repository.*

---

## Learning Outcomes

After completing these practicals, the following concepts can be understood:

- Understanding Knowledge Representation in Artificial Intelligence.
- Designing and implementing a basic Knowledge Base.
- Representing domain-specific knowledge using Python.
- Applying set operations for knowledge matching.
- Understanding semantic relationships between entities.
- Implementing frame-based knowledge structures.
- Analyzing the time and space complexity of knowledge representation systems.

## Future Enhancements

Potential improvements for future development include:

- Integrating SQLite for persistent knowledge storage.
- Adding a graphical user interface using Tkinter.
- Implementing graphical semantic network visualization using NetworkX.
- Supporting frame inheritance and default values.
- Extending the medical knowledge base with validated domain knowledge and appropriate clinical oversight.

## Contributing

Contributions, suggestions, and improvements are welcome.

To contribute:

1. Fork the repository.
2. Create a new branch for your changes.
3. Implement and test your improvements.
4. Submit a Pull Request with a description of your changes.

## Author

**Divyansh Arekar**

GitHub: [@Divyansh-techi](https://github.com/Divyansh-techi)

## License

No license has been selected for this project yet. Add an appropriate open-source license if you intend to permit reuse, modification, and distribution.

---

<p align="center">

**Developed as part of Artificial Intelligence Laboratory Practicals.**

</p>