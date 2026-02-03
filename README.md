# Library Management System

A Java simulated library ecosystem, based on extensive hierarchical inheritance, modular design, and robust data management. This system offers a centralised processor of storing, retrieval, and reservation of various types of media.

## Technical Architecture

It is an object-oriented hierarchy-based system to efficiently and scalably manage various library assets.

Management engine core (Library.java) is an engine core that manages the system's lifecycle within the platform.<|human|>Core Management Engine (Library.java) This is the engine core managing the lifecycle of the system in the platform.
* **Efficient Data Structures**: Takes advantage of using hashmap and hashset data structures to ensure that access to items and users are done in time complexity of O(1).
* **Intelligent ID Generation**: Uses collision resistant algorithm in unique User IDs and automated sequence numbering in reservations.
* **Flexible Persistence**: It has a dynamic flag-based file reader that is able to consume balanced types of records (Books, CDs, DVDs and Users) in one file.

### Inheritance Model
The project has a strict class hierarchy that is meant to ensure that there is no duplication of codes and also to enforce data integrity:

* LibraryItem (Abstract): This is the parent class containing the basic attributes of all assets including Title, Item Code, Cost, Times borrained, and Loan Status.
* **Intermediary Classes**:
    * `PrintedItem`: Pagination and publisher data of physical media are handled here.
    * `AudioVisual`: regulates the time played in digital media.
* Leaf Classes: Granular format-specific implementations; such as Book, CD, DVD, Periodical.

## Key Features

* Advanced Reservation Logic A complete and unified system, combining a Diary and a LibraryReservation system with automatic date verification and conflict resolution to eliminate: double-booking.
* Strong Date Utility: A date utility, a custom class, DateUtil, which offers a good-quality string-to-date conversion, leap-year and days-between algorithms.
* Polymorphic Reporting - Takes advantage of method overriding (e.g. printDetails) throughout the whole hierarchy to give context sensitive data visualisation when auditing the system.
* Data Persistence: The ability to read and write User and Reservation data to formatted User and Reservation data in the form of an `.txt file to store over the long term.

## Getting Started

### Prerequisites
**BlueJ IDE: This project is BlueJ environment optimised.

### Initialisation
1.  OpenJ: Open the project in BlueJ.
2.  The fifth step is instantiation, which involves the right-clicking of the Library class and then choosing the constructor to make a new instance.
3.  Load Data: invoke the readData() method. When it opens the file dialog, one is to choose a data file (e.g., items all.txt).

## Operations

|Action| Method to Call| Description|
| :--- | :--- | :--- |
| **Print Inventory** | printAll() | Shows all loaded objects and users registered.
| make Library reservation make library reservation() This method takes the following parameters: UserID, item code, start date and number of days.
| `printDiaryEntries()` | `printDiaryEntries()` Shows all the reservations that are active over the period of a chosen time.

## Project Structure

* **Data Files: Template Book, CD, DVD, Periodical and User sample data in formatted.txt files.
* **Simple Code): Java code to the basic engine, utility classes as well as the entire asset inheritance tree.
* **BlueJ Package: Files that specify the dependencies of classes and the layout of the visual editor.
