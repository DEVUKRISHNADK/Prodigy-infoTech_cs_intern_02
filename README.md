
---

# Image Encryption and Decryption using XOR and Pixel Shuffling

This project provides a simple yet effective method to encrypt and decrypt images using XOR operations, addition, and pixel shuffling techniques. This method demonstrates basic cryptographic principles applied to image data.

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
  - [Example](#example)
- [Functions Overview](#functions-overview)
- [File Structure](#file-structure)
- [Contributing](#contributing)
- [License](#license)

## Introduction

The script encrypts an image by applying an XOR operation with a key, adding another key, and then shuffling the pixels. The decryption process reverses these steps. This method offers a simple way to obscure images but should not be relied upon for high-security applications.

## Features

- **Encryption:** Encrypts an image using a combination of XOR, addition, and pixel shuffling.
- **Decryption:** Decrypts the encrypted image by reversing the encryption process.
- **Simple and Fast:** Easy-to-understand code with basic cryptographic operations.
- **Customizable Keys:** Users can input their own encryption keys for added security.

## Prerequisites

Before running the script, ensure you have the following installed:

- Python 3.x
- The following Python libraries:
  - `Pillow`: For image processing.
  - `NumPy`: For numerical operations and array manipulation.

You can install the required libraries using pip:

```bash
pip install pillow numpy
```

## Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/your-username/image-encryption.git
   ```

2. Navigate to the project directory:

   ```bash
   cd image-encryption
   ```

3. Ensure that your Python environment has the necessary libraries installed.

## Usage

1. Place the image you want to encrypt in the project directory or provide the full path to the image.

2. Run the script:

   ```bash
   python image_encryption.py
   ```

3. Follow the on-screen prompts:

   - **Input the path to the image**: Specify the path to the image you wish to encrypt.
   - **Input the path to save the encrypted image**: Specify where you want to save the encrypted image.
   - **Input the path to save the decrypted image**: Specify where you want to save the decrypted image.
   - **Input the encryption keys**: Provide two integer keys that will be used in the encryption process.

### Example:

```bash
Enter the path to the input image: example.jpg
Enter the path to save the encrypted image: encrypted_example.jpg
Enter the path to save the decrypted image: decrypted_example.jpg
Enter the first encryption key (integer): 123
Enter the second encryption key (integer): 45
```

After running the script, the encrypted image will be saved to `encrypted_example.jpg`, and the decrypted image will be saved to `decrypted_example.jpg`.

## Functions Overview

- **load_image(image_path):** 
  - **Description:** Loads an image from the specified path and converts it into a NumPy array.
  - **Returns:** A NumPy array of the image, the image mode, and the image size.
  
- **save_image(image_array, mode, size, output_path):** 
  - **Description:** Saves a NumPy array as an image file.
  - **Arguments:** 
    - `image_array`: The NumPy array of the image.
    - `mode`: The mode of the image (e.g., 'RGB').
    - `size`: The size of the image (width, height).
    - `output_path`: The path where the image will be saved.

- **encrypt_image(image_array, key1, key2):** 
  - **Description:** Encrypts an image using XOR with `key1`, adds `key2`, and shuffles the pixels.
  - **Arguments:** 
    - `image_array`: The NumPy array of the image to be encrypted.
    - `key1`: The first encryption key.
    - `key2`: The second encryption key.
  - **Returns:** The encrypted image as a NumPy array.

- **decrypt_image(encrypted_image_array, key1, key2):** 
  - **Description:** Decrypts an image by reversing the encryption process.
  - **Arguments:** 
    - `encrypted_image_array`: The NumPy array of the encrypted image.
    - `key1`: The first decryption key (same as the encryption key).
    - `key2`: The second decryption key (same as the encryption key).
  - **Returns:** The decrypted image as a NumPy array.

## File Structure

```bash
.
├── image_encryption.py   # Main script for image encryption and decryption
├── example.jpg           # Example image (optional)
└── README.md             # This README file
```

---

### Notes:
- Replace `"https://github.com/your-username/image-encryption.git"` with your actual GitHub repository URL.
- You can expand the "Usage" section by providing examples with actual images if needed.
- You might include a troubleshooting section in the future if users encounter issues.
