# 📱 Address Book Management System in C

A **menu-driven Address Book Management System** developed using **C programming**. This project allows users to efficiently manage contact information such as names, phone numbers, and email addresses.

The application supports **creating, searching, editing, deleting, and listing contacts**, with contact data stored permanently in a CSV file. When the program starts, previously saved contacts are automatically loaded from the file.

## 🚀 Features

* ➕ **Create Contact**

  * Add a new contact with name, phone number, and email.
  * Validates contact information before storing it.
  * Prevents duplicate phone numbers and email addresses.

* 🔍 **Search Contact**

  * Search contacts by:

    * Name
    * Phone number
    * Email address
  * Supports partial matching using string functions.

* ✏️ **Edit Contact**

  * Update an existing contact's:

    * Name
    * Phone number
    * Email address
  * Performs validation while updating phone numbers and emails.

* 🗑️ **Delete Contact**

  * Delete a selected contact.
  * Automatically shifts the remaining contacts to maintain the array structure.

* 📋 **List All Contacts**

  * Displays all contacts in a formatted table.
  * Contacts are sorted alphabetically by name using **Bubble Sort**.

* 💾 **File Handling**

  * Saves contacts into a `contact.csv` file.
  * Automatically loads saved contacts when the application starts.
  * Provides persistent data storage between program executions.

* ✅ **Input Validation**

  * Validates names, phone numbers, and email addresses.
  * Phone numbers must contain exactly 10 digits.
  * Prevents duplicate contact information.

## 🛠️ Technologies Used

* **Programming Language:** C
* **Concepts:**

  * Structures
  * Arrays
  * Pointers
  * Functions
  * String handling
  * File handling
  * Searching
  * Sorting
  * Input validation
* **File Format:** CSV
* **Compiler:** GCC

## 📂 Project Structure

```text
AddressBook/
│
├── main.c              # Main program and menu
├── contact.c           # Contact management functions
├── contact.h           # Contact structures and function declarations
├── file.c              # File read/write operations
├── file.h              # File handling function declarations
├── contact.csv         # Stored contact information
└── README.md           # Project documentation
```

## ⚙️ How the Program Works

When the application starts, it initializes the Address Book and loads previously stored contacts from `contact.csv`.

The user is then presented with a menu:

```text
----------------------- Address Book Menu -----------------------

1. Create contact
2. Search contact
3. Edit contact
4. Delete contact
5. List all contacts
6. Save and Exit
7. Exit
```

The selected operation is executed through the corresponding function.

### Data Flow

```text
Program Start
      ↓
Initialize Address Book
      ↓
Load contacts from contact.csv
      ↓
Display Menu
      ↓
User selects operation
      ↓
Create / Search / Edit / Delete / List
      ↓
Update Address Book
      ↓
Save contacts to CSV
      ↓
Exit
```

## 💾 Data Storage

Contact information is stored in `contact.csv` using the following format:

```text
Name,Phone,Email
```

Example:

```text
Kiran,9876543211,kiran@gmail.com
Virat,1818181818,virat@g.com
```

The program loads this data when it starts and writes updated data back to the CSV file.

## 🔤 Sorting

The **List Contacts** operation uses **Bubble Sort** to arrange contacts alphabetically based on their names.

```text
Before Sorting:
Virat
Kiran
Abhi

After Sorting:
Abhi
Kiran
Virat
```

## 🔐 Validation

The project includes basic validation mechanisms:

### Name Validation

* Cannot be empty.
* Allows alphabetic characters, spaces, and dots.

### Phone Validation

* Must contain exactly 10 digits.
* Only numeric characters are accepted.
* Duplicate phone numbers are rejected.

### Email Validation

* Must start with a lowercase alphabet.
* Must contain `@`.
* Must contain `.com`.
* Duplicate email addresses are rejected.

## ▶️ Compilation and Execution

### 1. Clone the Repository

```bash
git clone <your-repository-url>
cd AddressBook
```

### 2. Compile

```bash
gcc main.c contact.c file.c -o addressbook
```

### 3. Run

Linux/macOS:

```bash
./addressbook
```

Windows:

```bash
addressbook.exe
```

## 📚 C Concepts Demonstrated

This project helped implement and understand several important C programming concepts:

* Structures and nested structures
* Arrays of structures
* Pointers and pointer-to-structure
* Function declaration and definition
* Passing structures using pointers
* String manipulation
* `strcmp()`, `strcpy()`, `strlen()`, `strstr()`
* Character validation using `ctype.h`
* File handling using `FILE *`
* `fopen()`, `fscanf()`, `fprintf()`, `fclose()`
* Searching techniques
* Bubble Sort
* Menu-driven programming
* CRUD operations
* Input validation




