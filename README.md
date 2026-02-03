An ecosystem simulation of a library with high fidelity, with a hierarchical and modular emphasis on data management. The system will enable storage, retrieval and booking of various types of media using a centralized management engine.

Technical Architecture
The system employs an extensive hierarchy of classes to handle different data types:

Core Management Engine (`Library.java):** Implements the use of unique IDs through the use of a random generator; uses `HashMap` and `HashSet` to access items and users in O(1) time.
Audacious Inheritance Model: This model is based on the principle that, within an object-oriented hierarchy, every object possesses an inheritance chain.<|human|>Hierarchical Inheritance Model: The concept behind this model is that in an object-oriented hierarchy each object has an inheritance chain.
* Library Item (Abstract):** Positioning of key attributes to all assets (Title, Code, Cost).
* PrintedItem and AudioVisual: Physical and digital media intermediary classes.
* `Book`: Granular data handling of specific media formats, supplied as leaf classes.
|human|>* `CD, DVD, Periodical`: Granular data handling of specific media formats offered as leaf classes.

Design Features
* Advanced Data Persistence:
TMpl. We use Scanner to read formatted text files and PrintWriter to write secure state.
* Reservation Logic: Has an advanced LibraryReservation system and automated sequence numbering and date verification.
* Polymorphic Reporting:** Employs method overriding throughout the class hierarchy to give it context sensitive data visualization when performing audits on the system.

Key Engineering Challenges
* Unique Identifier Integrity: Developed a collision-resistant User ID production algorithm based on a set to maintain used prefixes.
* Flexible Data Ingestion: Dynamic Flag-based file reader was designed to accept mixed-type data records (Book, CD, User) into a single source file.
