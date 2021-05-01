#  About

## What is Cryptography?
**Cryptography** is a technique of securing information by encrypting and decrypting data.
The user can send or receive data across insecure networks using the cryptography.
## What is Encryption?
The Process of converting plain text to cipher text is called encryption.
The **Cipher Text** is a non-readable format of text data or encrypted text.

## What is Decryption?
**Decryption** is just opposite of encryption or the process of converting cipher text to plain text is called decryption.
## Why Cryptography is important?
For Security.

## What is Key?
A Key is basically, a random string that the cryptography algorithm uses to perform encryption & decryption.
# Required Module
To continue following this tutorial we need a Python library **"Cryptography"** command

    pip install cryptography

# Get Started

## Creating a Key 
The first step of cryptography is to create a key. As we already know the key is required for encryption decryption process.

    from cryptography.fernet import fernet

    def generate_key();
	    key=Fernet.generate_key()
	    with open('mykey.key','wb') as mykey;
		    mykey.write(key)
	    print("key is generated successfully")

The length of key is 40-50 random characters so it is impossible to remember the key value that's why we can have to save our key value.

## Load the Key

    def load_key();
	    with open('mykey.key','rb') as mykey;
	    key= mykey.read()
	    return key.

## Encrypting a file

    from cryptography.fernet import fernet
    def encrypt_file(filename);
	    #First load the key.
	    key=load_key()
	    f=Fernet(key)
	    with open (filename,'rb') as original_file;
		    original= original_file.read()
	    enc_file="enc"+str(filename)
	    encrypted=F.encrypt(original) with open (enc_file,'wb') as 	encryptedfile
	    encryptedfile.write(encrypted)
	    print("file is encrypted & save"+encryptedfile)

**Let’s understand the code :**  
⦁ We initialize the Fernet object as store is as a local variable f.  
⦁ Next, we read our original data (filename) into original.  
⦁ Then we encrypt the data using the Fernet object and store it as encrypted.  
⦁ And finally, we write it into a new file.

## Decrypting a File

    from cryptography.fernet import Fernet  
    def decript_file(filename):  
        # First load the key..  
        key = load_key()  
        f = Fernet(key)  
        with open(filename, 'rb') as encrypted_file:  
            encrypted = encrypted_file.read()  
        dec_file = "dec" + str(filename)  
        decrypted = f.decrypt(encrypted)  
        with open(dec_file, 'wb') as decrypted_file:  
            decrypted_file.write(decrypted)  
        print("File is decripted and save as " + dec_file)

**Let’s understand the code :**  
⦁ We initialize the Fernet object as store is as a local variable f  
⦁ Next, we read our encrypted data into encrypted  
⦁ Then we decrypt the data using the Fernet object and store it as decrypted  
⦁ And finally, we write it into a new file.

-----------------------
Thanks for visiting my GitHub Profile and please make sure to follow me.
