# Selenium Automation Tests

This repository contains Selenium WebDriver automation scripts for interacting with a sample web application. The tests cover three main functionalities:

1. **FillForm** - Automates user registration.
2. **Table** - Extracts product information from a web table and saves it to a CSV file.
3. **Dropdown** - Selects options from a dropdown and records manufacturer details.

## Prerequisites

Ensure you have the following installed:
- .NET (for running NUnit tests)
- Chrome browser
- Chrome WebDriver
- NUnit and Selenium WebDriver NuGet packages

## Setup

1. Clone this repository:
   ```sh
   git clone https://github.com/your-username/your-repo.git
   cd your-repo
   ```
2. Restore dependencies:
   ```sh
   dotnet restore
   ```
3. Ensure `chromedriver.exe` is available in your system PATH or in the project directory.

## Test Descriptions

### 1. FillForm
Automates the user registration process on `http://practice.bpbonline.com/`.

- Navigates to the registration page.
- Fills in user details with randomly generated email.
- Submits the form and verifies successful account creation.
- Logs out after registration.

Run test:
```sh
   dotnet test --filter Test_RegisterUser
```

### 2. Table
Extracts product information from a web table and stores it in `productinformation.csv`.

- Finds and reads the product listing table.
- Extracts product names and prices.
- Saves data in CSV format.

Run test:
```sh
   dotnet test --filter TestExtractProductInformation
```

### 3. Dropdown
Interacts with a dropdown menu to retrieve manufacturer details.

- Selects each manufacturer from the dropdown.
- Checks if products are available.
- Saves the information in `manufacturer.txt`.

Run test:
```sh
   dotnet test --filter TestSelectFromDropDown
```

## Running All Tests
Execute all tests using:
```sh
   dotnet test
```

## Cleanup
After running tests, ChromeDriver instances should close automatically. If necessary, manually close any remaining browser windows.

---

This repository provides an automated approach to form filling, table extraction, and dropdown selection using Selenium WebDriver.
