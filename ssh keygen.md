  
 

##  

## **\#Create Users in Ubuntu and Set Up SSH Key-Based Access**


To check only "real" human users already exists

```bash
awk -F: '$3 >= 1000 && $3 < 65534 { print $1 }' /etc/passwd
```


Get super user rights
```bash 
sudo -i
```

Add a New User
```bash
sudo adduser mostafa
```

Set a password when prompted
```python
!$dnkjdnkasjsdk788&&^&*^
```

Set Name (`optional`)

```python
Golam Mostafa
```

adds the user mostafa to the sudo group
```bash
sudo usermod -aG sudo mostafa
```

switch to user mostafa, with that user's full login environment, using root privileges.
```bash
sudo su - mostafa
```


Create ".ssh" directory

```bash
mkdir -p ~/.ssh
```  


```bash
chmod 700 ~/.ssh
```  


Create and edit authorized_keys

```bash
vim ~/.ssh/authorized_keys
```  


copy past my public-keys (stating & production) 

```bash

ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABgQDBXTG7cFL9YnQKDUgbjdARpzbJRKQCXERn1AQbmNS0xARa65wPi8QJ9nHErak5lQu/0OaPSlTtVmPJkN+P6wWSl3QEzUCTVZIZ8gtrCRYNoKYXTzKQ1W+DecDQP0EIoqIRpIhe6ulPI1hCZe0bwTSSMyNnFePkS2BLJxbCjZgBmmsEZ+IBkDFvtSjYk+u3z9cDGFMAq84kMfjpvYGJ1Gz229Qf7NhMl//EBwYz42/BIxlCWVCKbYcDYxPPUaDI2LB1bybP9TLD+n96J0o/ARSGQDpT+rN+kMWIJUs4ryi9JN93kl64BB6vwiRtMiYP16/MDZzIvhBLBFXWvhDZZA7FMxG0d+5xfqeDHSJPC9i/BFyIKwKLvdkzCfSkTv/fZ12ZrS7Rp2GfHLfWYrXL88eM6gWDT6a9qqCSrBCrlekcedClh4Q71KaLcwqit/7R/QLlZZHYmFswmS/Rbz510mvU2o56IGe8+ihNXWtVIYj+XGAb5hl0VtWjsyn+vPUgdtk= mostafa@Golams-MacBook-Pro.local
```
   
Correct Permissions

```bash
chmod 600 ~/.ssh/authorized_keys
```


```bash
ssh -J mostafa@54.179.251.115 mostafa@10.10.8.159 
```



