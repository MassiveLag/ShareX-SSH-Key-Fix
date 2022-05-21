#There are different ways to fix the issue that you get by sharex if you want to use sftp support.

If you get the error "Invalid private key file."
that means most likely you are using .ppk file or a wrong key that sharex does not support.

How to fix?

Fix 1: 

#OpenSSH
Sharex only takes OpenSSH keys, if you need to convert your putty key:
-Open PuttyGen
-Click Load
-Load your private key
-Go to Conversions->Export OpenSSH and export your private key and use it in sharex

Do you now get the error "Key 'OPENSSH' is not supported." 
This means that this is not supported. The keys that in the most situations aren't working are ECDSA, Ed25519 and SSH-1 (RSA)

#How to create a new key that works with shareX

Step 1, download puttygen at https://www.puttygen.com/download-putty

Step 2, Open PuttyGen

Step 3, You see on the top 5 different key types. As i mentioned only 2 of them will be the best key to use for ShareX. So select RSA or DSA (Recommended RSA)

Step 4, Click "Generate" now it generates a key for you, this can take a few seconds. 

Step 5, When key is generated click "Save public key" & "Save private key"

Step 6, When you have saved private and public key. go with your mouse to "Conversions" and click "Export OpenSSH key"

Step 7, Now your OpenSSH key should be saved at the directory where you saved it. Now you can start adding the OpenSSH key to your ShareX sftp key directory

NOTICES: Make sure you are using the correct bind adres, port and user.
