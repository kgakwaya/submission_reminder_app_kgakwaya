# Submission Reminder App

This **Submission Reminder App** is a Bash-based application designed to help students keep track of their pending assignment submissions. The app reads assignment data from a CSV file and displays reminders for students who have not yet submitted their work.

## Directory Structure
When you run the environment setup script (`create_environment.sh`), it creates the following structure:

- `app/reminder.sh`: Sources the required files and checks the submissions file.
- `assets/submissions.txt`: Contains student records in CSV format with three columns: Student, Assignment, and Submission Status.
- `config/config.env`: Holds configuration variables such as the assignment name and the number of days remaining.
- `modules/functions.sh`: Contains helper functions used by the app (including the `check_submissions` function).
- `startup.sh`: The main script that starts the application.

## How the App Works
### Setup:
Run the `create_environment.sh` script to create the directory structure and necessary files automatically.

### Configuration:
The `config/config.env` file stores general settings. For example:
```sh
# config.env - Configuration file for submission reminder app
ASSIGNMENT="Shell Navigation"
DAYS_REMAINING=2
```
These variables determine which assignment to check and how many days are left until submission is due.

### Submissions Data:
The `assets/submissions.txt` file holds the submission records in the following format:
```csv
Student,Assignment,Submission Status
Desire,Shell Navigation,not submitted
Kevine,Shell Navigation,submitted
Davina,Shell Navigation,not submitted
Elie,Shell Navigation,not submitted
Franky,Shell Navigation,submitted
Kagaba,Shell Navigation,not submitted
Idrissa,Shell Navigation,submitted
yvanna,Shell Navigation,not submitted
Jullian,Shell Navigation,submitted
```
Each row represents a student’s submission status for a specific assignment.

## How to Run the App
### Set Up the Environment:
Run the `create_environment.sh` script:
```sh
./create_environment.sh
```
Enter your name when prompted. This will create the `submission_reminder_<yourName>` directory with all necessary files.

### Start the Application:
Navigate into the created directory:
```sh
cd submission_reminder_<yourName>
```
Run the application:
```sh
./startup.sh
```
This script will process the submission records and display reminders for students who have not submitted their assignments.

## Requirements
- **Bash Shell** (version 4.0 or later preferred)
- **Standard Unix Utilities** like `cat`, `xargs`, and `tail`

## License
This project is open-source and available under the MIT License.

Feel free to modify this README and the app scripts as needed to better suit your requirements. Enjoy using the **Submission Reminder App**!


