<div align="center">
  
# [Regular-Expressions.](https://github.com/BrenoFariasdaSilva/Regular-Expressions) <img src="https://github.com/BrenoFariasdaSilva/Regular-Expressions/blob/main/.assets/Bash.svg"  width="3%" height="3%">

</div>

<div align="center">
  
---

Welcome to my collection of commonly used regular expressions! This repository is a handy resource for developers and anyone dealing with text pattern matching. Regular expressions (regex) are powerful tools for string manipulation and validation.
This repository contains a collection of regular expressions I have found useful. I hope you find them useful too!

---

</div>

<div align="center">

![GitHub Code Size in Bytes Badge](https://img.shields.io/github/languages/code-size/BrenoFariasdaSilva/Regular-Expressions)
![GitHub Last Commit Badge](https://img.shields.io/github/last-commit/BrenoFariasdaSilva/Regular-Expressions)
![GitHub License Badge](https://img.shields.io/github/license/BrenoFariasdaSilva/Regular-Expressions)
![Wakatime Badge](https://wakatime.com/badge/github/BrenoFariasdaSilva/Regular-Expressions.svg)

</div>

<div align="center">
  
![RepoBeats Statistics](https://repobeats.axiom.co/api/embed/682d293532f9df756a1a65514d8043fa551b454e.svg "Repobeats analytics image")

</div>

## Table of Contents
- [Regular-Expressions. ](#regular-expressions-)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Setup](#setup)
    - [Clone the repository](#clone-the-repository)
  - [Contents](#contents)
    - [1. Email Address](#1-email-address)
    - [2. URL (HTTP/HTTPS)](#2-url-httphttps)
    - [3. Date (DD/MM/YYYY) Format](#3-date-ddmmyyyy-format)
    - [4. Username](#4-username)
    - [5. Password Strength](#5-password-strength)
    - [6. CPF (Brazil)](#6-cpf-brazil)
    - [7. Zip Code (Brazil)](#7-zip-code-brazil)
    - [8. Phone Number (Brazil)](#8-phone-number-brazil)
    - [9. SQL Injection](#9-sql-injection)
    - [10. IPv4 Address](#10-ipv4-address)
    - [11. IPv6 Address](#11-ipv6-address)
    - [12. Comments with Double Spaces](#12-comments-with-double-spaces)
  - [Contributing](#contributing)
  - [License](#license)
    - [Creative Commons Zero v1.0 Universal](#creative-commons-zero-v10-universal)

## Introduction

The primary purpose of this repository is to provide a curated list of regular expressions that I frequently use in various projects. Whether you are validating user inputs, searching for specific patterns in text, or parsing data, these regex patterns can be a valuable addition to your toolkit.

## Setup

### Clone the repository

1. Clone the repository with the following command:

```bash
git clone https://github.com/BrenoFariasdaSilva/Regular-Expressions.git
cd Regular-Expressions
```

## Contents

### 1. Email Address

A regex for validating email addresses, checking for the basic structure of an email, including '@' and domain extensions.

  ```regex
  ^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
  ```

### 2. URL (HTTP/HTTPS)

Validate URLs with this regex, checking for the basic structure, including the protocol, domain name, and optional path.

  ```regex
  ^(http|https):\/\/[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}(\/[a-zA-Z0-9%_.-]+\/?)*$
  ```

### 3. Date (DD/MM/YYYY) Format

This regex validates dates in the format DD/MM/YYYY, checking for leap years and the correct number of days in each month.

  ```regex
  ^(0[1-9]|[12][0-9]|3[01])\/(0[1-9]|1[0-2])\/(19|20)\d{2}$
  ```

### 4. Username

This regex validates usernames with the following criteria:

- Minimum 3 characters.
- Maximum 16 characters.
- Only letters, numbers, underscores and hyphens.

  ```regex
  ^[a-zA-Z0-9_-]{3,16}$
  ```

### 5. Password Strength

This regex validates passwords with the following criteria:

- Minimum 8 characters.
- At least one uppercase letter.
- One lowercase letter.
- One number.
- One special character.

  ```regex
  ^(?=.*[a-z])(?=.*[A-Z])(?=.*\d)(?=.*[@$!%*?&])[A-Za-z\d@$!%*?&]{8,}$
  ```

### 6. CPF (Brazil)

This regex validates Brazilian CPFs, checking for the correct number of digits and the correct check digits.

  ```regex
  ^\d{3}\.\d{3}\.\d{3}-\d{2}$
  ```

### 7. Zip Code (Brazil)

This regex validates Brazilian zip codes, checking for the correct number of digits.

  ```regex
  ^\d{5}-\d{3}$
  ```

### 8. Phone Number (Brazil)

This regex validates Brazilian phone numbers, checking for the correct number of digits and the correct area code.

  ```regex
  ^\(\d{2}\) \d{4,5}-\d{4}$
  ```

### 9. SQL Injection

This regex helps identify SQL injection attempts, checking for the most common SQL injection keywords.

  ```regex
  (\b(?:SELECT|INSERT|UPDATE|DELETE|DROP|CREATE|ALTER)\b|\b(?:UNION|JOIN|WHERE|FROM)\b|\b(?:AND|OR|NOT)\b)
  ```

### 10. IPv4 Address

This regex validates IPv4 addresses, checking for the correct number of octets and the correct range of numbers in each octet.

  ```regex
  ^(?:[0-9]{1,3}\.){3}[0-9]{1,3}$
  ```

### 11. IPv6 Address

This regex validates IPv6 addresses, checking for the correct number of hextets and the correct range of numbers and letters in each hextet.

  ```regex
  ^(?:[0-9a-fA-F]{1,4}:){7}[0-9a-fA-F]{1,4}$
  ```

### 12. Comments with Double Spaces

This regex helps identify comments in a file with double spaces after the comment character, ensuring proper formatting.

  ```regex
  \S[ ]{2}#
  ```

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**. If you have suggestions for improving the code, your insights will be highly welcome.
In order to contribute to this project, please follow the guidelines below or read the [CONTRIBUTING.md](CONTRIBUTING.md) file for more details on how to contribute to this project, as it contains information about the commit standards and the entire pull request process.
Please follow these guidelines to make your contributions smooth and effective:

1. **Set Up Your Environment**: Ensure you've followed the setup instructions in the [Setup](#setup) section to prepare your development environment.

2. **Make Your Changes**:
   - **Create a Branch**: `git checkout -b feature/YourFeatureName`
   - **Implement Your Changes**: Make sure to test your changes thoroughly.
   - **Commit Your Changes**: Use clear commit messages, for example:
     - For new features: `git commit -m "FEAT: Add some AmazingFeature"`
     - For bug fixes: `git commit -m "FIX: Resolve Issue #123"`
     - For documentation: `git commit -m "DOCS: Update README with new instructions"`
     - For refactorings: `git commit -m "REFACTOR: Enhance component for better aspect"`
     - For snapshots: `git commit -m "SNAPSHOT: Temporary commit to save the current state for later reference"`
   - See more about crafting commit messages in the [CONTRIBUTING.md](CONTRIBUTING.md) file.

3. **Submit Your Contribution**:
   - **Push Your Changes**: `git push origin feature/YourFeatureName`
   - **Open a Pull Request (PR)**: Navigate to the repository on GitHub and open a PR with a detailed description of your changes.

4. **Stay Engaged**: Respond to any feedback from the project maintainers and make necessary adjustments to your PR.

5. **Celebrate**: Once your PR is merged, celebrate your contribution to the project!

## License

### Creative Commons Zero v1.0 Universal

This project is licensed under the [Creative Commons Zero v1.0 Universal](LICENSE), which means you are free to use, modify, and distribute the code. See the [LICENSE](LICENSE) file for more details.
