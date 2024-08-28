## Project: Encrypter-Decrypter

### Overview
This project is a simple Text Encryption and Decryption tool built using Python's `Tkinter` library. The application provides a graphical user interface (GUI) that allows users to encrypt and decrypt text messages using Base64 encoding. The user must enter a secret key to perform these actions, ensuring that only authorized individuals can view the original or encrypted messages.

### Features
- **Text Encryption**: Converts a user inputted text message into an encrypted format using Base64 encoding.
- **Text Decryption**: Converts an encrypted message back to its original form, provided the correct secret key is entered.
- **Password Protection**: Ensures that encryption and decryption can only be performed with the correct password.
- **Reset Functionality**: Allows users to clear the text input and reset the secret key.

### Requirements
- Python 3.x
- Tkinter (Python's standard GUI library, typically included with Python)

### How It Works
1. **Main Screen**:
   - The application starts with a main screen where the user can enter the text they want to encrypt or decrypt.
   - The user is prompted to enter a secret key, which is required for both encryption and decryption.

2. **Encryption**:
   - When the user enters text and the correct secret key (default: `6969`), the text is converted into a Base64 encoded string.
   - The encoded text is displayed in a new window labeled "ENCRYPT".

3. **Decryption**:
   - Similarly, if the user enters an encoded text and the correct secret key, the application decodes the message and displays the original text in a new window labeled "DECRYPT".

4. **Reset**:
   - The user can clear the current text and reset the secret key entry by clicking the "RESET" button.

### Code Explanation

#### Import Statements
```python
from tkinter import *
from tkinter import messagebox
import base64
import os
```
- **Tkinter**: Used for creating the GUI.
- **messagebox**: Used for displaying pop-up messages.
- **base64**: Used for encoding and decoding the text.
- **os**: Not used in the provided code, but typically used for file or OS operations.

#### Main Functions

- **decrypt()**:
  - Decodes a Base64 encoded message if the correct password is provided.
  - Displays the decoded message in a new window.

- **encrypt()**:
  - Encodes a plain text message into Base64 format if the correct password is provided.
  - Displays the encoded message in a new window.

- **main_screen()**:
  - Sets up the main GUI window where users can input text, enter the secret key, and access encryption and decryption functionalities.
  - Also includes a reset button to clear inputs.

### Usage

1. **Running the Application**:
   - Ensure Python is installed on your system.
   - Run the Python script. The main window will appear.

2. **Encrypting Text**:
   - Enter the text you want to encrypt in the first text box.
   - Enter the secret key (default: `6969`).
   - Click the "ENCRYPT" button to see the encoded message.

3. **Decrypting Text**:
   - Enter the Base64 encoded text in the first text box.
   - Enter the secret key (default: `6969`).
   - Click the "DECRYPT" button to see the original message.

4. **Resetting**:
   - To clear the text and reset the key, click the "RESET" button.

### Customization
- **Change Password**: 
  - Modify the `password` variable in the `encrypt()` and `decrypt()` functions to change the secret key from `1234` to any desired value.

- **GUI Design**:
  - The `Tkinter` library offers flexibility in modifying the layout, colors, fonts, and sizes used in the GUI.

### Notes
- **Security**: This tool is not intended for high-security encryption. Base64 encoding is a reversible process and should not be used for secure data encryption.
- **Password Protection**: The password is hardcoded for simplicity but can be modified to use a more secure method of authentication.

### Conclusion
This project is a basic implementation of text encryption and decryption using Python and Tkinter. It provides a foundational understanding of how encoding and decoding work, as well as how to create a simple GUI application.
