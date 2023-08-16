# Streamlit App Deployment on AWS EC2

This repository contains instructions and resources to deploy a Streamlit app on an AWS EC2 instance.

## Prerequisites

- AWS Account
- Streamlit app code
- SSH Key Pair

## Steps to Deploy

1. Launch an EC2 instance on AWS using the Amazon Linux AMI.
2. Configure security groups to allow inbound traffic on SSH and the required app port.
3. Generate or use an existing SSH key pair to connect to the EC2 instance.
4. Update Ubuntu
    ```sh
    sudo apt update 
    ```
5. SSH into the EC2 instance:

    ```sh
    ssh -i /path/to/your-key.pem ec2-user@your-instance-ip
    ```

6. Install Python 3 and pip:

    ```sh
    sudo apt install python3 python3-pip
    ```

7. Install git & required apps

    ```sh
    sudo apt install git curl unzip tar make sudo vim wget -y
    ```

8. Install app dependencies:

    ```sh
    pip3 install -r requirements.txt
    ```

9. Run your Streamlit app:

    ```sh
    python3 -m streamlit run app.py
    ```
10. Permanent running
    
    ```sh
    nohup python3 -m streamlit run app.py
    ```

11. Access your Streamlit app in a web browser using your EC2 instance's public IP and the app port.

