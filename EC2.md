# Create Public Instance act as bastion host
![image](https://github.com/user-attachments/assets/ce38219f-7c16-4795-9afc-7db6e7f9cb53)
Create the private instance and create key pair to access the instance from it
![image](https://github.com/user-attachments/assets/b78adea0-9b2c-4d65-8fb3-b3748217af28)
![image](https://github.com/user-attachments/assets/0f0a9d7b-95d0-4763-b526-effcc73c16ac)
# Connect to the private instance from the bastion host instance
- First Create .pem file and write the content of key file on it
- ![image](https://github.com/user-attachments/assets/892a2c8c-014c-4f7a-87da-e12b4e6c840c)
- Chmod the key file access
- ![image](https://github.com/user-attachments/assets/cdcfcbf0-cfb1-4204-b27c-f856fa1db95b)
# Now Connect to the private instance
- using ssh -i "example.pem" ec2-user@ private ip address
- ![image](https://github.com/user-attachments/assets/e0175054-ef49-4ab4-9431-43a770c11c2a)


