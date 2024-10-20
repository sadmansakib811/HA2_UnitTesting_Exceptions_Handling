# Energy Management Log Simulation

This project simulates energy generation and consumption for different energy sources over multiple days. It generates log files with random values representing energy produced by sources like wind turbines and solar panels, and energy consumed by systems such as lighting, heating, and the H-Bahn. The log files can be searched using both simple string search and regular expression search.

In **HA2**, we've enhanced the application by implementing 4 exception handling code as per the HA2 pdf and add 5 unit tests for each classes.


# Team Members:
1. **Sadman Sakib:** (Matriculation Number: 7213446),
2. **Farhana Binta Shaheed:** (Matriculation Number: 7216429),
3. **Md Azad Hossain:** (Matriculation Number: 7213230),
3. **Md Istiak Javed:** (Matriculation Number: 7221689),



# To see a video demonstration of the project, click here to watch the video.
 - Ha2 Explaination Team Video: https://www.youtube.com/watch?v=vcpvKBGdx7Q

## Contributors
- Sadman Sakib: In HA2 I have Implemented 4 Exception Handler in the Exception Handler class, And Created Test Suit for testing all the classes together and created 5+5 total 10 test cases for LogManagerTest.java and EnergySimulatorTest.java
- Farhana Binta Shaheed: I have Implemented 4 Exception Handler as per HA2 in the  FileReaderUtil search class and also add 5 Unit testing in FileReaderUtilTest.java class.
- Istiak Javed: Handled the 4 Eceptions in my simple string search class and add Unit Testing for SimpleStringSearchTest.java file.
- Azad Hossain: Add 5 Unit Testing in RegexSearchTest.java.
## Test Result Screenshots:
- Sadman Sakib Test Result Screenshot:
![sadman-energysimulatorTest](https://github.com/user-attachments/assets/98131ca4-0429-4a05-8b5f-509fa4863c35)
![sadman-logManagerTest (1)](https://github.com/user-attachments/assets/cbe05df3-4cc3-4070-b59a-2d8a718e88e2)


- Farhana Binta Shaheed test result Screenshot:
![farhana-FileReaderUtilTest](https://github.com/user-attachments/assets/b806c78f-ed32-4b4d-864e-4fbd3c4e604c)

- Md. Azad Hossain test result Screenshot:
![Azad Regex test](https://github.com/user-attachments/assets/c331379b-b950-4f33-acbb-e2bf26ffa459)

- Istiak Javed Test Result Screenshot:
![Istiyak simple search test](https://github.com/user-attachments/assets/5c0db6ac-a61a-44ce-abab-c993ce81842f)
## Project Structure

- **`Main.java`**: 
   - Manages the flow of the program.
  - Calls the log generation process, handles user input for searching the log files, and integrates exception handling demonstrations.
  - Prompts the user to select between simple string search or regular expression search to find specific terms in the log files.
  - Includes options for the user to delete or move log files after processing.

- **`ExceptionHandler.java`**:
  - Demonstrates various exception handling techniques:
    - Handling multiple exceptions.
    - Resource management using try-with-resources.
    - Exception chaining.
    - Re-throwing exceptions.
  - Processes log files and showcases how exceptions are handled in different scenarios.

- **`LogManager.java`**:
  - Responsible for generating 5 days of log files, with each log file containing:
    - Energy generation data from wind turbines and solar panels.
    - Energy consumption data for lighting, heating, and the H-Bahn.
    - The balance between total generated and consumed energy.
  - Implements exception handling for file operations, including re-throwing exceptions to the calling method.
  - The generated files are saved with the format: `FH_DORTMUND_energy_management_date_YYYY-MM-DD.log`.


- **`EnergySimulator.java`**:
    - Simulates random energy data for various sources and consumption points.
  - Methods like `simulateWindTurbine()` and `simulateLighting()` generate random values for energy generation and consumption.
  - Includes methods to simulate data exchange using both character and byte streams.
  - Implements exception handling for I/O operations, ensuring resources are properly managed.

- **`LogSearch.java`**:
  - Handles the search functionality for the generated log files.
  - Offers two types of searches:
    1. **Simple String Search**: Case-insensitive search for specific terms (like "Lighting" or "Heating") in the log files.
    2. **Regular Expression Search**: Allows searching using regular expressions (e.g., find all energy values using `\d+ kWh`).

- **`FileReaderUtil.java`**:
  - Reads and displays the content of log files.
  - Shows metadata of log files, such as creation date, last modified date, and file size.
  - Implements exception handling for file reading operations, including handling multiple exceptions and re-throwing them.
  - Utilizes try-with-resources for efficient resource management.
  - **`LogSearch.java`**:
  - Handles the search functionality for the generated log files.
  - Offers two types of searches:
    1. **Simple String Search**: Case-insensitive search for specific terms (like "Lighting" or "Heating") in the log files.
    2. **Regular Expression Search**: Allows searching using regular expressions (e.g., find all energy values using `\d+ kWh`).
  - Integrates exception handling when reading files and performing searches.

- **Test Classes**:
  - **`LogManagerTest.java`**:
    - Contains unit tests for the `LogManager` class, verifying file creation, content, and exception handling.
  - **`EnergySimulatorTest.java`**:
    - Contains unit tests for the `EnergySimulator` class, ensuring simulated values are within expected ranges.
  - **`FileReaderUtilTest.java`**:
    - Contains unit tests for the `FileReaderUtil` class, testing exception handling when reading files under various scenarios.

## Exception Handling Enhancements (HA2)

In this assignment, we've focused on implementing comprehensive exception handling throughout the application:

- **Handling Multiple Exceptions**: Specific catch blocks are used to handle different types of exceptions, providing detailed error messages.
- **Re-throwing Exceptions**: Exceptions are re-thrown to allow higher-level methods to handle them appropriately.
- **Resource Management**: Try-with-resources statements are used to ensure that all resources (like file readers and writers) are automatically closed after use, preventing resource leaks.
- **Exception Chaining**: When re-throwing exceptions, the original exception is passed along to preserve the stack trace and original cause.

These enhancements improve the robustness and reliability of the application, making it more resilient to unexpected conditions.

## How to Use the Program

1. **Run the Program**:
   - When the program starts, it generates 5 days of log files. These files contain random energy generation and consumption data.
   - Exception handling demonstrations are run, showcasing how the application handles various exceptions.

2. **Select a Log File**:
   - The program lists the available log files. You can choose a log file by entering the equipment name or date.

3. **View Metadata (Optional)**:
   - You have the option to view metadata of the selected log file, such as creation date, last modified date, and file size.

4. **Search the Log File**:
   - After selecting the log file, you can choose to search using:
     - **Simple String Search** (e.g., searching for "Heating").
     - **Regular Expression Search** (e.g., searching for `\d+ kWh` to find energy values).
   - The program will display matching lines from the log file.

5. **Delete or Move Log Files (Optional)**:
   - At the end of the program, you are given the option to delete or move log files:
     - **Delete a Log File**: Remove a specific log file from the directory.
     - **Move a Log File**: Move a log file to a different directory.

## Example Output

- Available log files:

- **FH_DORTMUND_energy_management_date_2024-10-07.log
- **FH_DORTMUND_energy_management_date_2024-10-06.log
- **FH_DORTMUND_energy_management_date_2024-10-05.log
- **FH_DORTMUND_energy_management_date_2024-10-04.log
- **FH_DORTMUND_energy_management_date_2024-10-03.log
- **Enter the number of the log file you want to open: 1
### After opening a log file output:
- Showing content of FH_DORTMUND_energy_management_date_2024-10-07.log: Energy Generation: Wind Turbine:  369 kWh Solar Panel: 95 kWh Total Generated: 464 kWh

- **Energy Consumption: Lighting: 157 kWh Heating: 122 kWh H-Bahn: 9 kWh Total Consumed: 288 kWh

- Energy Balance: 176 kWh

- Select the type of search:

- Simple String Search
- Regular Expression Search

- Enter your choice (1-2): 2

- Enter the search term or regular expression: \d+ kWh

- Match found: Wind Turbine: 369 kWh Match found: Solar Panel: 95 kWh Match found: Total Generated: 464 kWh Match found: Lighting: 157 kWh Match found: Heating: 122 kWh Match found: H-Bahn: 9 kWh Match found: Total Consumed: 288 kWh Match found: Energy Balance: 176 kWh

- Do you want to delete or move a log file?

- 1 Delete a log file
- 2 Move a log file
- Close the code
Exit Enter your choice (1-3): 1
Enter the name of the log file you want to delete: FH_DORTMUND_energy_management_date_2024-10-16.log Log file deleted: FH_DORTMUND_energy_management_date_2024-10-16.log



## How to Run

1. **Clone the repository**
  
2. **run the program or main file**





