# Image Decoding Instructions

This repository contains a text file (```HW1.txt```) which is a Base64 encoded representation of an image. To view the original image, you need to decode this text file back into a PNG file.

Choose the method below that matches your operating system.

## 1. Windows

Use built-in ```certuril``` tool

- Open Command Prompt (cmd.exe) in the folder where the file is located.
- Run the following command:
	```certutil -decode "HW1.txt" "restored_image.png"```

This will create a new file named restored_image.png in the same directory.

## 2. Linux

You can use the standard base64 utility found in most terminals.

- Open your Terminal in the folder where the file is located.
- Run the following command:
	base64 -d -i HW1.txt > restored_image.png

**Note:** The input file might contain header/footer lines from Windows certutil.
The -d flag decodes, and -i ignores non-alphabet characters (like newlines/headers).

This will decode the text content and save it as restored_image.png.