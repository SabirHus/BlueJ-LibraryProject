**Library Management System**
A Java-based ecosystem model that is a library simulation centered on high-fidelity data management, hierarchical inheritance, and modular design. The system allows storage, retrieval and reservation of different types of media on a centralized engine of management.

**Technical Architecture**
The system employs a huge object-oriented hierarchy to manage a variety of library assets:

**Basic Management Engine (Library.java)**
Data Structures: O(1) time complexity method using HashMap and HashSet in accessing items and users.
ID Generation: Provides collision resistant User ID algorithm and automatic numbering on the Reservation sequences.
Persistence: Has a dynamic flag based file reader which can read a single file with mixed types of records (Books, CDs, Users).

**Inheritance Model**
The project is structured in a rigid hierarchy in order to reduce the amount of code duplication:
LibraryItem (Abstract): This is the parent class which describes the important features of all assets, including Title, Item Code, Cost, Times b borrowed and Loan status.

**Intermediary Classes:**
PrintedItem: Manages pagination and publisher information of hard copy.
AudioVisual: Controls duration of playing of digital media.
Leaf Classes: Book, CD, DVD and Periodical formats Granular implementations.

**Key Features**
Advanced Reservation Logic: It has a Diary and libraryReservation system that has automatic date verification and conflicts checking.
Date Utility: This is a custom DateUtil class that offers high-quality date-to-string and date-to-string conversions, lease-year calculations and days-between logic.
Polymorphic Reporting: It is a method overriding (e.g., printDetails()) a hierarchy-wide method to enable context-sensitive data display in system audits.
Data Persistence: Supports Users and Reservations Data by reading both and writing to formatted.txt files.

**Getting Started**
Environment: Click on the project file to open the project in BlueJ.
Initialization: Click the Library class right-click to make a new instance of the Library.
Loading Data: with the readData() method. A file dialog will be shown; choose one of the given data files (e.g., items all.txt).

**Operations:**
Print Inventory: To see everything loaded and users type printAll()
Make Reservation: Call makeLibraryReservation: You need to input User ID, item code and date.
View Schedule: To view reservations made during a given period, call printDiaryEntries.

**Project Structure**
Data Files: Has sample texts of Book records, CD records, DVD records, and User records as .txt files.
Source Code: The source code of the Java engine of the core engine and asset types.
BlueJ Package: BlueJ environment and class dependencies configuration.
