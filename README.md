# Ip_Checker_Gui

## Introduction

The **AbuseIPDB Checker** is a Python application with a graphical user interface (GUI) created using the `tkinter` library. This application allows users to check the abuse report for a given IP address using the AbuseIPDB API. It fetches information about the specified IP address and displays the results in a readable JSON format.

## Table of Contents

1. [Getting Started](#getting-started)
   - [Prerequisites](#prerequisites)
   - [Installation](#installation)
2. [Usage](#usage)
   - [Input](#input)
   - [Output](#output)
   - [Example](#example)
3. [Development](#development)
   - [Project Structure](#project-structure)
   - [Dependencies](#dependencies)
   - [Building the Application](#building-the-application)
4. [Contributing](#contributing)
   - [Reporting Issues](#reporting-issues)
   - [Pull Requests](#pull-requests)

## 1. Getting Started

### Prerequisites

Before using the AbuseIPDB Checker, ensure that you have the following prerequisites installed on your computer:

- Python: Python 3.x is recommended. You can download it from [python.org](https://www.python.org/downloads/).

### Installation

1. Clone the repository or download the source code.

   ```bash
   git clone https://github.com/yourusername/abuseipdb-checker.git
   ```

2. Change to the project directory.

   ```bash
   cd abuseipdb-checker
   ```

3. Install the required Python libraries using pip.

   ```bash
   pip install requests
   ```

## 2. Usage

### Input

- **IP Address**: Enter the IP address you want to check for abuse. This is the main input required for the application.

### Output

- **Abuse Report**: After clicking the "Check AbuseIPDB" button, the application will make an API request to AbuseIPDB. The abuse report for the specified IP address will be displayed in the text widget in a formatted JSON format.

### Example

Here's how to use the AbuseIPDB Checker:

1. Launch the application by running the Python script (`abuseipdb_checker.py`).

   ```bash
   python abuseipdb_checker.py
   ```

2. Enter the IP address you want to check in the input field.

3. Click the "Check AbuseIPDB" button.

4. The abuse report for the specified IP address will be displayed in the text widget.

## 3. Development

If you want to contribute to the development of the AbuseIPDB Checker application, you can follow these guidelines:

### Project Structure

The project directory is organized as follows:

- `abuseipdb_checker.py`: The main Python script that creates the GUI and handles API requests.
- `README.md`: Documentation for the application.
- `LICENSE`: License information for the application.

### Dependencies

The AbuseIPDB Checker has the following dependencies:

- `requests`: Used for making HTTP requests to the AbuseIPDB API.

### Building the Application

To make changes or extend the application, you can modify the `abuseipdb_checker.py` script. After making changes, you can test the application locally by running it with Python.

## 4. Contributing

### Reporting Issues

If you encounter any issues with the AbuseIPDB Checker, please report them on the [GitHub Issues page](https://github.com/yourusername/abuseipdb-checker/issues).

### Pull Requests

We welcome contributions! If you'd like to contribute to the project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them with descriptive messages.
4. Push your branch to your fork on GitHub.
5. Create a pull request to the main repository's `main` branch.

