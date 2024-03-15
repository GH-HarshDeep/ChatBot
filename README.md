
# CUSTOM CHATBOT

A custom chatbot application that integrates with openai and allows users to login/signup through firebase and is deployed on an EC2 server further allowing to upload files to the server that is processed to save in a S3 bucket.


## Installation on local machine

Clone the project in your local machine

```bash
  git clone "github_project_link"
```
Install all requirements.
```bash
  python3 -m pip install -r requirements
```
Replace the code with your OPENAPI key and also the firebase authentication attributes.

If any error regarding version conflict run this command.
```bash
  python3 -m pip install --ignore-installed streamlit
```
Run the app.
```bash
  python3 -m streamlit run login.py
```

## Uploading to EC2 server.

1. Create an EC2 server and allow connection from anywhere on port 8501

2. Connect to EC2 server.

3. Get root access.

```bash
  sudo su
```

4. Update the packages.

```bash
  yum update
```

5. Install git.

```bash
  yum install git
```

6. Clone the project on the EC2 server.

```bash
  git clone "github_project_link"
```

7. Install pip

```bash
  yum install python3-pip
```

8. Install all requirements.

```bash
  python3 -m pip install -r requirements.txt
```

9. If any error regarding version conflict run this command.

```bash
  python3 -m pip install --ignore-installed streamlit
```

9. Replace the code with your OPENAPI key and also the firebase authentication attributes.

10. Create IAM Role with full access to S3.

11. Attach this IAM role to the EC2 server.

12. Create S3 bucket and write bucket policy such that only the above IAM role can access that bucket.

13. Insert the S3 bucket id to the code.

14. Run the app.

```bash
  python3 -m streamlit run login.py
```
