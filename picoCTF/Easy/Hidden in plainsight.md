# **Steganography**

1. We begin by downloading the file required. We use online exif tools to inspect the metadata of the file

2. In the file metadata, it have a "Comment" column that have random string of "c3RlZ2hpZGU6Y0VGNmVuZHZjbVE9". 

3. By using "CyberChef", paste the string into the input and add "From Base64" to the recipe section, or we can directly use the "Magic" operation to autodetect the possible decode. 

4. Decoding it reveals that it is "steghide:cEF6endvcmQ=". It gives a hint where the encoding process is using steghide.

5. By downloading steghide tools, we can extract the hidden message in the image.

6. Using the string obtained, "cEF6endvcmQ=", it will give error where it could not extract any data with that passphrase. 

5. Furthur decoding the "cEF6endvcmQ=" will reveal another plaintext of "pAzzword". By using it, it successfully extracted data to a file named "flag.txt", and the flag is contained in the file.
