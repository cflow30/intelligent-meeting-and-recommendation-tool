# intelligent-meeting-and-recommendation-tool
This project uses AWS services to streamline meeting audio management. It features transcription with Amazon Transcribe, summarization with Amazon Comprehend, and secure storage via Amazon S3. The user-friendly interface allows querying and recommendations, with AWS Lambda automating processes for efficiency and scalability
# AWS-Based Transcription and Query Application

## Overview

This project is an AWS-based application that allows users to upload audio files for transcription and query documents. The application leverages various AWS services such as Lambda, S3, API Gateway, Bedrock, DynamoDB, and OpenSearch.

## Architecture Diagram

![Architecture Diagram](Architeture.drawio.png)

## Project Deliverables

- **Code**: Full code for the Streamlit application and Lambda functions.
- **Architecture Diagram**: Provided in the `Architeture.drawio.png` file.
- **Developer Guide**: Instructions for setting up and deploying the application.
- **User Guide**: Instructions for end-users to interact with the application.

## Developer Guide

### Prerequisites

- An AWS account with appropriate permissions.
- Basic knowledge of AWS services and the AWS Management Console.
- Python installed on your local machine.

### Step-by-Step Instructions

#### Step 1: Setting Up S3 Buckets

1. **Log in to the AWS Management Console.**
2. **Navigate to S3**:
   - Create two buckets, one for audio files (`maudiofiles`) and another for output results (`awsengagements`).

#### Step 2: Setting Up Lambda Functions

1. **Navigate to Lambda**:
   - Create three Lambda functions:
     1. `StartTranscriptionJob`
     2. `CheckJobStatus`
     3. `ProcessTranscriptionJob`
   - Configure these functions to handle respective tasks as defined in the architecture.

#### Step 3: Setting Up API Gateway

1. **Navigate to API Gateway**:
   - Create a new REST API.
   - Set up endpoints to trigger the Lambda functions for:
     - Starting transcription.
     - Checking job status.
     - Processing transcription.

#### Step 4: Setting Up Bedrock and OpenSearch

1. **Navigate to Bedrock**:
   - Set up Bedrock for querying the knowledge base.
   - Sync the knowledge base with OpenSearch using Titan Embedding.

#### Step 5: Setting Up DynamoDB

1. **Navigate to DynamoDB**:
   - Create a table to store chat history.

#### Step 6: Deploying the Streamlit Application

1. **Set up a local Python environment**.
2. **Install necessary libraries**:
   ```sh
   pip install streamlit boto3 requests
