# Library Management System

A high-fidelity Java simulation of a library ecosystem, centered on hierarchical inheritance, modular design, and robust data management. This system provides a centralized engine for the storage, retrieval, and reservation of diverse media types.

---

## Technical Architecture

The system utilizes an extensive object-oriented hierarchy to manage a variety of library assets with efficiency and scalability.

### Core Management Engine (`Library.java`)
* **Efficient Data Structures**: Leverages `HashMap` and `HashSet` to achieve **O(1) time complexity** for accessing items and users.
* **Intelligent ID Generation**: Implements a collision-resistant algorithm for unique User IDs and automated sequence numbering for reservations.
* **Flexible Persistence**: Features a dynamic, flag-based file reader capable of ingesting mixed-type records (Books, CDs, DVDs, and Users) from a single source file.

### Inheritance Model
The project follows a rigid class hierarchy designed to eliminate code duplication and enforce data integrity:

* **LibraryItem (Abstract)**: The foundational parent class defining essential attributes for all assets: Title, Item Code, Cost, Times Borrowed, and Loan Status.
* **Intermediary Classes**:
    * `PrintedItem`: Manages pagination and publisher data for physical media.
    * `AudioVisual`: Controls playing time duration for digital media.
* **Leaf Classes**: Granular, format-specific implementations including `Book`, `CD`, `DVD`, and `Periodical`.

---

## Key Features

* **Advanced Reservation Logic**: Integrated `Diary` and `LibraryReservation` systems featuring automatic date verification and conflict checking to prevent double-booking.
* **Robust Date Utility**: A custom `DateUtil` class providing high-quality string-to-date conversions, leap-year calculations, and "days-between" logic.
* **Polymorphic Reporting**: Utilizes method overriding (e.g., `printDetails()`) across the entire hierarchy to provide context-sensitive data visualization during system audits.
* **Data Persistence**: Full support for reading and writing User and Reservation data to formatted `.txt` files for long-term storage.

---

## Getting Started

### Prerequisites
* **BlueJ IDE**: This project is optimized for the BlueJ environment.

### Initialization
1.  **Open Project**: Open the project folder in BlueJ.
2.  **Instantiate**: Right-click the `Library` class and select the constructor to create a new instance.
3.  **Load Data**: Call the `readData()` method. When the file dialog appears, select a data file (e.g., `items_all.txt`).

---

## Operations

| Action | Method to Call | Description |
| :--- | :--- | :--- |
| **Print Inventory** | `printAll()` | Displays all loaded items and registered users. |
| **Make Reservation**| `makeLibraryReservation()` | Parameters: `UserID`, `ItemCode`, `StartDate`, and `NoOfDays`. |
| **View Schedule** | `printDiaryEntries()` | Displays all reservations active during a specified date range. |

---

## Project Structure

* **Data Files**: Sample `.txt` files containing formatted records for Books, CDs, DVDs, Periodicals, and Users.
* **Source Code**: Java files for the core engine, utility classes, and the complete asset inheritance tree.
* **BlueJ Package**: Configuration files defining class dependencies and the visual editor layout.
