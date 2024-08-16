# AWS-cloud-menu-project
Various AWS usage and services
Here's a more detailed project description based on the provided content:

---

# AWS Automation with Python CGI Scripts

## Project Overview

The **AWS Automation with Python CGI Scripts** project is designed to simplify and automate various tasks on Amazon Web Services (AWS) using Python scripts executed as CGI (Common Gateway Interface) programs. This project is ideal for developers, system administrators, or anyone looking to automate repetitive AWS tasks using a simple web interface.

### Key Features

This project includes a set of Python CGI scripts that allow users to perform the following AWS operations effortlessly:

- **EC2 Instance Management**:
  - **Launch Standard EC2 Instances**: Quickly spin up new EC2 instances using predefined configurations.
  - **Launch RHEL GUI EC2 Instances**: Deploy EC2 instances with Red Hat Enterprise Linux (RHEL) and a graphical user interface (GUI) for easy remote access.

- **CloudWatch Logs Access**:
  - **Retrieve CloudWatch Logs**: Access and view logs from CloudWatch to monitor and debug applications running on AWS.

- **Audio Transcription**:
  - **Convert Audio to Text**: Utilize AWS Transcribe to convert audio files stored in S3 into text, enabling easy analysis and processing of spoken content.

- **MongoDB Integration**:
  - **Connect to MongoDB Databases**: Establish and verify connections to MongoDB databases, making it easier to work with your data stored in the cloud.

- **S3 File Management**:
  - **Upload Files to S3**: Seamlessly upload files to Amazon S3, providing a simple way to store and manage data in the cloud.

- **Lambda, S3, and SES Integration**:
  - **Automated Email Sending**: Automatically send emails using AWS Lambda, S3, and SES by retrieving email addresses from an S3 file.

### Prerequisites

To get started with this project, ensure you have the following:

- **Python 3**: The scripts are written in Python 3, so make sure it is installed on your system.
- **AWS Account**: You need an active AWS account with the necessary permissions to execute the operations.
- **Required Python Packages**:
  - **Boto3**: The AWS SDK for Python, which can be installed using:
    ```bash
    pip install boto3
    ```
  - **PyMongo**: The MongoDB driver for Python, which can be installed using:
    ```bash
    pip install pymongo
    ```
  - **dotenv**: For managing environment variables, which can be installed using:
    ```bash
    pip install python-dotenv
    ```

### Setting Up the Project

1. **Environment Variables**:
   - Create a `.env` file in the project directory to securely store your AWS credentials and MongoDB connection details. Add the following lines to your `.env` file:

     ```plaintext
     # AWS credentials
     AWS_ACCESS_KEY_ID=your_aws_access_key_id
     AWS_SECRET_ACCESS_KEY=your_aws_secret_access_key
     AWS_DEFAULT_REGION=your_aws_default_region

     # MongoDB credentials
     MONGO_DB_USERNAME=your_mongodb_username
     MONGO_DB_PASSWORD=your_mongodb_password
     MONGO_ATLAS_CONNECTION_STRING=your_mongo_atlas_connection_string
     ```

2. **Running the Scripts**:
   - Place the Python scripts in a CGI-enabled directory on your web server. When accessed via a web browser, these scripts will execute the corresponding AWS operations based on user input.

### Supported Operations

The following operations are supported by the scripts:

- **launch_ec2_instance**: Launches a basic EC2 instance.
- **launch_rhel_gui_instance**: Launches an EC2 instance with RHEL GUI.
- **access_cloud_logs**: Retrieves logs from AWS CloudWatch.
- **audio_to_text_event**: Transcribes an audio file from S3 to text using AWS Transcribe.
- **connect_python_to_mongodb**: Connects to a MongoDB database.
- **upload_to_s3**: Uploads a file to an S3 bucket.
- **integrate_lambda_s3_ses**: Downloads email IDs from an S3 file and sends test emails using AWS SES.

### Conclusion

This project is a powerful tool for automating AWS tasks through Python scripts executed as CGI programs. It offers a convenient way to manage AWS resources, handle data in S3 and MongoDB, and integrate with other AWS services such as Lambda and SES, all from a web interface.

Whether you're managing a small set of cloud resources or need a scalable solution for automation, this project provides the building blocks to streamline your AWS operations.
