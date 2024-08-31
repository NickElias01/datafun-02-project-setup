# datafun-02-project-setup
Elias Analytics - Reusable Module for Data Analytics Projects


## Overview:
nickelias_project_setup is a Python module designed to streamline the creation of project folder structures for data analytics projects. 
This module offers a set of reusable functions that can automatically generate folders based on specified criteria, such as ranges, lists, prefixes, or time intervals. It ensures consistency and efficiency in setting up project directories, which is crucial for organizing data and related files in a structured manner.


## Features
1. Create Folders by Year Range: Automatically generate folders for a specified range of years.
2. Create Folders from a List of Names: Generate folders based on a list of names, with optional transformations such as converting to lowercase or removing spaces.
3. Create Prefixed Folders: Create folders with a specified prefix combined with a list of names.
4. Create Folders Periodically: Generate a series of folders at fixed intervals for a specified duration.
5. Provide options to force lowercase and remove spaces in folder creation


## Installation:

To use the Elias Analytics module, ensure you have Python installed on your machine. 
Clone this repository or copy the nickelias_project_setup.py file to your project directory.


## Example Usage
The main() function in the module demonstrates how to use the various folder creation functions:

```python
import nickelias_project_setup

def main():
    # Create folders for a range of years
    result = nickelias_project_setup.create_folders_for_range(start_year=2020, end_year=2025)
    print(result)

    # Create folders from a list of names
    folder_names = ['folder a', 'folder b', 'folder c']
    nickelias_project_setup.create_folders_from_list(folder_names, to_lowercase=True, remove_spaces=True)

    # Create folders using a prefix
    folder_names = ['csv', 'excel', 'json', 'xml']
    prefix = 'data-'
    nickelias_project_setup.create_prefixed_folders(folder_names, prefix)

    # Create folders periodically over a duration
    duration_secs = 5  # duration in seconds
    nickelias_project_setup.create_folders_periodically(duration_secs)

    # Create folders for geographic regions with transformations
    regions = ["North America", "South America", "Europe", "Asia", "Africa", "Oceania", "Middle East"]
    nickelias_project_setup.create_folders_from_list(regions, to_lowercase=True, remove_spaces=True)

if __name__ == '__main__':
    main()
```
    
## Function Descriptions:

### 1. **create_folders_for_range(start_year: int, end_year: int) -> str**

  *Generates folders for a range of years. Returns a message indicating the number of folders created.

### 2. **create_folders_from_list(folder_list: list, to_lowercase: bool = False, remove_spaces: bool = False) -> str**

  *Creates folders based on a list of names, with optional transformations (lowercase, remove spaces). Returns a message indicating the folders created.

### 3. **create_prefixed_folders(folder_list: list, prefix: str) -> str**

  *Generates folders by applying a prefix to each name in a list. Returns a message indicating the prefixed folders created.

### 4. **create_folders_periodically(duration_secs: int) -> None**

  *Creates folders at 1-second intervals for a specified duration. Outputs the total number of folders created.

## Error Handling

The module includes error handling to manage common issues such as:

-Invalid year ranges
-Permission errors
-OS-related errors during folder creation

Contributing
Contributions are welcome! Please feel free to submit a pull request or open an issue for any bug fixes or enhancements.
