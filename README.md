# Random Password Generator

A simple **Random Password Generator** built with **HTML, CSS, and JavaScript**. This tool creates a strong random password with uppercase, lowercase, numbers, and symbols.

## Features
- Generates a **12-character** secure password
- Includes **uppercase, lowercase, numbers, and special characters**
- Allows **one-click copying** of the generated password

## Demo
![Password Generator](generate.png)

## Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/addresskrish/Random-Password.git
   ```
2. Open `index.html` in your browser.

## Usage
1. Click the **Generate Password** button to create a secure password.
2. Click the **copy icon** to copy the password to the clipboard.

## Files Overview
- **index.html** → Structure of the password generator
- **app.css** → Styles the UI
- **app.js** → Handles password generation logic
- **copy.png & generate.png** → Icons for UI

## Code Explanation
```javascript
const passwordBox = document.getElementById('password');
const len = 12;
const uppercase = "ABCDEFGHIJKLMNOPQRSTUVWXYZ";
const lowercase = "abcdefghijklmnopqrstuvwxyz";
const numbers = "0123456789";
const symbols = "~`!@#$%^&*(){}[]+=-*/?'";
const allChars = uppercase + lowercase + numbers + symbols;

function createPassword() {
    let password = "";
    password += uppercase[Math.floor(Math.random() * uppercase.length)];
    password += lowercase[Math.floor(Math.random() * lowercase.length)];
    password += numbers[Math.floor(Math.random() * numbers.length)];
    password += symbols[Math.floor(Math.random() * symbols.length)];

    while(len > password.length) {
        password += allChars[Math.floor(Math.random() * allChars.length)]
    }
    passwordBox.value = password;
}

function copyPassword() {
    passwordBox.select();
    document.execCommand("copy");
}
```

## Author
**Krish**

Made with ❤️ by [Krish](https://github.com/addresskrish)

## License
This project is **open-source** and free to use.
