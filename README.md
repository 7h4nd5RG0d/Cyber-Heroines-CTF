# Cyber-Heroines-CTF

## Forensics  
### Barbara Liskov  
#### Input file: https://cyberheroines.ctfd.io/files/28d8d5f5890e833f41af9cd6b439ec73/BarbaraLiskov.pyc?token=eyJ1c2VyX2lkIjo3MTcsInRlYW1faWQiOm51bGwsImZpbGVfaWQiOjEwfQ.ZXE3aQ.jxGu_6PWMG8UPXTrjKX1s5arYhY  
 Approach: We are given a .pyc file for download, where pyc stands for python compiled file.  
So using linux we can just "cat" out the commnads in the .pyc file and get a base64 encoded string which when decoded gives us the flag.  

#### Flag: chctf{u_n3v3r_n33d_0pt1m4l_p3rf0rm4nc3,_u_n33d_g00d-3n0ugh_p3rf0rm4nc3}

### Margaret Hamilton
#### Input file: ![Apollo-Mystery](https://github.com/7h4nd5RG0d/Cyber-Heroines-CTF/assets/128285431/104e977e-22f6-4c88-b98f-ff8904a8cc9c)  
 Approach: Using binwalk we can see that files are hidden inside the image.  
 Using the command "binwalk -e -M <Input file>" we can extract the files where we get a png image that contains the flag.  

 Result:![margaret_flag](https://github.com/7h4nd5RG0d/Cyber-Heroines-CTF/assets/128285431/d8bcbf55-29df-4dd2-9bf0-11770f5da3d0)  

 #### Flag: chctf{i_wr1t3_code_by_h4nd}

 
