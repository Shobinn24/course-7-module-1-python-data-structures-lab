# Student Data Management System

A Python-based student records management system demonstrating efficient data structures and operations.

## About

Student Data Management System is a modular Python application that allows administrators to store, filter, and process student records efficiently. The application showcases Python's core data structures including lists, tuples, sets, and generators for handling student information.

## Features

- **Student Records Storage**: Manage student data using tuples and lists
- **Dynamic Filtering**: Filter students by major using list comprehensions
- **Formatted Display**: Clean, readable output for student information
- **Unique Attribute Tracking**: Extract unique majors using set operations
- **Memory-Efficient Processing**: Generator expressions for large datasets
- **Case-Insensitive Search**: Robust filtering regardless of input case
- **Comprehensive Testing**: Full test suite with pytest

## Technologies Used

- **Python 3.x** - Programming language
- **pytest** - Testing framework
- **pipenv** - Dependency management

## Installation

Clone the repository:
```sh
git clone <repo-url>
cd course-7-module-1-python-data-structures-lab
```

Install dependencies:
```sh
pipenv install
```

Enter the virtual environment:
```sh
pipenv shell
```

Install pytest (if not already installed):
```sh
pip install pytest
```

## Running Tests

Run the test suite:
```sh
pytest -x
```

## Project Structure
```
course-7-module-1-python-data-structures-lab/
├── student_data.py          # Student records storage
├── filter.py                # List comprehension filtering
├── data_processing.py       # Data formatting and display
├── set_operations.py        # Set comprehension operations
├── data_generator.py        # Generator expressions
├── tests/                   # Test suite
└── README.md
```

## Key Features Implementation

### Student Records Storage
Students are stored as tuples containing (ID, Name, Major) for data integrity:
```python
students = [
    (101, "Alice Johnson", "Computer Science"),
    (102, "Bob Smith", "Mathematics"),
    (103, "Charlie Davis", "Physics"),
]
```

### Filtering by Major
Case-insensitive filtering using list comprehensions:
```python
def filter_students_by_major(student_list, major):
    return [student for student in student_list if student[2].lower() == major.lower()]
```

### Data Display
Formatted output for clean presentation:
```python
# Output: "ID: 101 | Name: Alice Johnson | Major: Computer Science"
```

### Unique Major Extraction
Set comprehension for efficient unique value extraction:
```python
def unique_majors(student_list):
    return {student[2] for student in student_list}
```

### Memory-Efficient Processing
Generator expressions for lazy evaluation:
```python
def student_generator(student_list, major):
    return (student for student in student_list if student[2] == major)
```

## Core Python Concepts

This project demonstrates mastery of:

- **Lists & Tuples**: Structured data storage with immutability
- **List Comprehensions**: Efficient one-line filtering operations
- **Set Comprehensions**: Extracting unique values from sequences
- **Generator Expressions**: Memory-efficient lazy evaluation
- **f-strings**: Modern string formatting
- **Modular Design**: Separation of concerns across multiple files

## Learning Goals Achieved

✅ Store and manage student records using lists, tuples, and sets  
✅ Apply list comprehensions for efficient data filtering  
✅ Use generator expressions to process large datasets efficiently  
✅ Implement set operations for tracking unique attributes  
✅ Structure a Python application with modular techniques  

## Best Practices Applied

- Modular code organization across multiple files
- Case-insensitive filtering for robust user input handling
- Generator expressions for memory efficiency
- Set operations for O(1) lookup performance
- Comprehensive docstrings for all functions
- Full test coverage

## Development

### Available Commands

- `pipenv shell` - Activate virtual environment
- `pytest -x` - Run test suite (stop on first failure)
- `python -i student_data.py` - Interactive Python shell with student data

## Troubleshooting

**pytest: command not found**
```sh
pip install pytest
# or
pip3 install pytest
```

**ModuleNotFoundError**
```sh
pipenv install
pipenv shell
```

## Future Enhancements

- Add student course enrollment tracking
- Implement GPA calculations
- Add database persistence (SQLite)
- Create CLI interface for user interaction
- Add data validation and error handling
- Export student data to CSV/JSON

## Author

**Shobinn Clark**
- GitHub: [@shobinn24](https://github.com/shobinn24)
- Flatiron School - Full-Stack Software Engineering Program

## License

This project was created as part of the Flatiron School curriculum.

## Acknowledgments

- Flatiron School for project requirements and guidance
- Python community for excellent documentation