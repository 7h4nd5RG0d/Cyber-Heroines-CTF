# Cyber-Heroines-CTF

## Forensics  
### Barbara Liskov(100)  
#### Input file: https://cyberheroines.ctfd.io/files/28d8d5f5890e833f41af9cd6b439ec73/BarbaraLiskov.pyc?token=eyJ1c2VyX2lkIjo3MTcsInRlYW1faWQiOm51bGwsImZpbGVfaWQiOjEwfQ.ZXE3aQ.jxGu_6PWMG8UPXTrjKX1s5arYhY  
 Approach: We are given a .pyc file for download, where pyc stands for python compiled file.  
So using linux we can just "cat" out the commnads in the .pyc file and get a base64 encoded string which when decoded gives us the flag.  

#### Flag: chctf{u_n3v3r_n33d_0pt1m4l_p3rf0rm4nc3,_u_n33d_g00d-3n0ugh_p3rf0rm4nc3}

### Margaret Hamilton(100)
#### Input file: ![Apollo-Mystery](https://github.com/7h4nd5RG0d/Cyber-Heroines-CTF/assets/128285431/104e977e-22f6-4c88-b98f-ff8904a8cc9c)  
 Approach: Using binwalk we can see that files are hidden inside the image.  
 Using the command "binwalk -e -M <Input file>" we can extract the files where we get a png image that contains the flag.  

 Result:![margaret_flag](https://github.com/7h4nd5RG0d/Cyber-Heroines-CTF/assets/128285431/d8bcbf55-29df-4dd2-9bf0-11770f5da3d0)  

 #### Flag: chctf{i_wr1t3_code_by_h4nd}

### Elizabeth Feinler(200)
#### Input file: https://cyberheroines.ctfd.io/files/34b02e792b5194a6b5755d6c0c8dc1cf/NoName.pcap?token=eyJ1c2VyX2lkIjo3MTcsInRlYW1faWQiOm51bGwsImZpbGVfaWQiOjEyfQ.ZXK_OA.evR-nOtq98SBSvHJS6YkeCvcOYA

Approach: Opening the pcap file in wireshark and following the UDP stream we see that every entry is prefixed with a number which is suspicious.  
".............143.google.WiCys.com..................150.fit.WiCys.edu..................143.fit.WiCys.edu..................164.netflix.WiCys.in..................146.google.WiCys.com..................173.fit.WiCys.edu..................143.fit.WiCys.edu..................162.US.WiCys.gov..................63.google.WiCys.com......	...........141.google.WiCys.com......
...........164.netflix.WiCys.in..................60.google.WiCys.com..................162.fit.WiCys.edu......
...........137.US.WiCys.gov..................60.netflix.WiCys.in..................146.US.WiCys.gov..................137.google.WiCys.com..................144.netflix.WiCys.in..................60.fit.WiCys.edu..................155.netflix.WiCys.in..................141.google.WiCys.com..................151.netflix.WiCys.in..................156.US.WiCys.gov..................137.US.WiCys.gov..................156.fit.WiCys.edu..................64.google.WiCys.com..................155.US.WiCys.gov..................63.netflix.WiCys.in..................137.netflix.WiCys.in..................163.fit.WiCys.edu..................171.google.WiCys.com..................163.US.WiCys.gov...... ...........164.US.WiCys.gov......!...........63.fit.WiCys.edu......"...........155.fit.WiCys.edu......#...........175.fit.WiCys.edu....."  
So copying the data in VSCode and using "Ctrl+Shift+L" to select and delete the unnecessary parts we get "143 150 143 164 146 173 143 162 63 141 164 60 162 137 60 146 137 144 60 155 141 151 156 137 156 64 155 63 137 163 171 163 164 63 155 175" which when put into cyberchef gives us the flag under octal decoding.

#### Flag: chctf{cr3at0r_0f_d0main_n4m3_syst3m}

### Stephanie Wehner(300)
#### Input file: https://drive.google.com/file/d/1wFihQD4zdespZx1Bjw5fV_zANoNrJg9k/view?usp=drive_link
Approach: 


 
