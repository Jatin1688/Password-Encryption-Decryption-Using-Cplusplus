## Project Overview

This project is a simple C++ console application that demonstrates basic login and signup functionality using MySQL for data storage. The project includes password encryption and decryption to enhance security.

## Features

- **Signup and Login**: Users can create an account and log in using their credentials.
- **Password Encryption**: Passwords are encrypted before being stored in the database.
- **Password Decryption**: Encrypted passwords are decrypted for authentication during login.

## Prerequisites

- MySQL Server
- MySQL Connector/C++
- Windows Operating System
- C++ Compiler

## Installation

1. **Clone the Repository**:
    ```sh
    git clone https://github.com/your-username/your-repo-name.git
    ```

2. **Install MySQL Server**:
    - Download and install MySQL Server from the [official website](https://dev.mysql.com/downloads/mysql/).

3. **Install MySQL Connector/C++**:
    - Download and install MySQL Connector/C++ from the [official website](https://dev.mysql.com/downloads/connector/cpp/).

4. **Setup Database**:
    - Create a database named `mydb`.
    - Create a table `password` in the database using the following SQL command:
      ```sql
      CREATE TABLE password (
          Id VARCHAR(50) PRIMARY KEY,
          PW VARCHAR(255)
      );
      ```

5. **Update Database Credentials**:
    - Replace the placeholders `your password` in the source code with your actual MySQL password.

## Usage

1. **Compile the Program**:
    ```sh
    g++ -o login_app login_app.cpp -lmysqlcppconn
    ```

2. **Run the Program**:
    ```sh
    ./login_app
    ```

3. **Signup**:
    - Select the option to sign up and enter a user ID and password.
    - The password will be encrypted and stored in the MySQL database.

4. **Login**:
    - Select the option to log in and enter the user ID and password.
    - The program will decrypt the password and authenticate the user.

## Code Explanation

- **Login Class**: Handles user ID and password storage.
- **Encryption/Decryption Functions**: Encrypt and decrypt passwords using a simple shift cipher.
- **Database Functions**: Interact with the MySQL database to store and retrieve encrypted passwords.
