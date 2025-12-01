# Plant Database Application 

> **Final Project Submission**
>
> **Course:** Mobile Device Application Development
>

A comprehensive mobile application developed with **Flutter** for managing botanical information and land-use data. This project demonstrates the implementation of a **local relational database (SQLite)**, hybrid image management, and MVC architecture.

##  Project Overview

This application serves as a digital botanical library. It solves the problem of organizing complex relationships between plant species and their specific utilities (e.g., which part of a plant is used for medicine vs. construction).

The app features a **pre-populated database** for offline access and supports dynamic data entry, allowing users to contribute new plant species and images.

##  Key Features

* **Robust Data Persistence:** Utilizes **SQLite** (`sqflite`) for efficient, offline local storage.
* **Relational Data Modeling:** Manages complex Many-to-One relationships between:
    * Plants (Taxonomy)
    * Components (Root, Leaf, Stem)
    * Usage Types (Food, Medicine, Insecticide)
* **Hybrid Image System:**
    * **Assets:** Optimized local loading for default dataset (e.g., Mango, Neem).
    * **Dynamic Handling:** Supports user-generated content and external image sources.
* **Interactive UI:** Designed with Material Design 3 principles for a clean user experience.

##  Tech Stack

* **Framework:** Flutter (Dart)
* **Database:** SQLite (via `sqflite` package)
* **Architecture:** MVC (Model-View-Controller) pattern
* **Tools:** Android Studio / VS Code, Git

##  Database Schema

The application implements a relational schema to ensure data integrity:

| Table Name | Description |
| :--- | :--- |
| `plants` | Stores core biological info (ID, Scientific Name, Family, Image Path). |
| `plantComponents` | Lookup table for plant parts (e.g., Leaf, Root, Fruit). |
| `landUseTypes` | Lookup table for usage categories (e.g., Medicine, Construction). |
| `landUses` | **Junction Table** linking a specific Plant + Component to a Usage Type. |

##  Getting Started

Follow these steps to run the project locally.

### Prerequisites
* Flutter SDK (Latest Stable)
* Android Emulator or Physical Device

### Installation

1.  **Clone the repository**
    ```bash
    git clone [https://github.com/yourusername/plant-database-app.git](https://github.com/yourusername/plant-database-app.git)
    ```

2.  **Navigate to the project directory**
    ```bash
    cd plant-database-app
    ```

3.  **Install dependencies**
    ```bash
    flutter pub get
    ```

4.  **Setup Assets**
    * Ensure image files (e.g., `mango.jpg`, `neem.jpg`) are placed in `assets/images/`.

5.  **Run the App**
    ```bash
    flutter run
    ```
    *Note: The `DatabaseHelper` class will automatically initialize the database and seed initial data upon the first launch.*

##  Screenshots

| Plant List | Plant Detail | Land Use Info |
| :---: | :---: | :---: |
| ![List Screen](path/to/screenshot1.png) | ![Detail Screen](path/to/screenshot2.png) | ![Usage Screen](path/to/screenshot3.png) |

---

---
*This project is part of the Mobile Device Application Development course curriculum.*
