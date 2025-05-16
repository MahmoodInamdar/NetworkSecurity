### Network Security Projects For Phising Data

📘 Project Overview: Phishing Detection via Network Security
This project is a machine learning-based network security solution designed to detect phishing attempts in network traffic. It provides a FastAPI-powered web application for real-time predictions and training, integrated with modern tools for scalable deployment and CI/CD automation.

🎯 Project Purpose
The application aims to identify phishing activities using network traffic data. It features:

A FastAPI web service for prediction and training

MongoDB integration for data persistence

Docker and AWS support for deployment

A modular architecture for maintainability and scalability

🧩 Core Application Files
File	Description
app.py	Main FastAPI web server handling API endpoints
main.py	Secondary core script, possibly for CLI or bootstrapping
push_data.py	Responsible for pushing data into the database
test_mongodb.py	Contains tests to validate MongoDB operations
setup.py	Project metadata and setup configuration

⚙️ Configuration & Setup
File	Purpose
requirements.txt	Lists all Python package dependencies
Dockerfile	Defines the Docker container setup
.gitignore	Specifies files and folders to exclude from Git
README.md	Provides project documentation and usage instructions

📂 Key Directories
Directory	Description
networksecurity/	Main package directory containing core ML pipeline
Network_Data/	Raw network traffic data
valid_data/	Cleaned and validated dataset
prediction_output/	Stores prediction results
final_model/	Contains the trained model and preprocessing pipeline
templates/	HTML templates for the web interface
data_schema/	Definitions of data structure and validation schemas
Artifacts/	Pipeline-generated artifacts
logs/	Application and pipeline logs
.github/	GitHub Actions for CI/CD workflows
__pycache__/	Python bytecode cache (auto-generated)

🚀 Application Functionality
✅ FastAPI Web Interface (app.py)
/train: Triggers the training pipeline

/predict: Accepts a CSV input for phishing prediction

HTML front-end interface for user interaction

🧠 Machine Learning Pipeline
Located in networksecurity/pipeline/training_pipeline.py

Trains and stores a custom NetworkModel with preprocessing

Outputs saved to final_model/ and prediction_output/

🗃️ Data Management
Raw data in Network_Data/

Processed data in valid_data/

Results and artifacts are logged and organized

🌐 Infrastructure & Deployment
Containerization: Docker support for local and cloud environments

Cloud Deployment: Compatible with AWS EC2, with ECR integration

CI/CD: GitHub Actions set up under .github/

Environment Configuration: Uses .env or similar for secrets and MongoDB connection

🛠️ Development Setup
Written in Python

All dependencies managed via requirements.txt

MongoDB for persistent storage

Template-based HTML UI via FastAPI and Jinja2

🧱 Project Architecture
Follows a modular design with clear separation of concerns:

Data Ingestion

Training Pipeline

Prediction Service

Web Interface

Logging & Monitoring

Deployment Automation




Setup github secrets:
AWS_ACCESS_KEY_ID=

AWS_SECRET_ACCESS_KEY=

AWS_REGION = us-east-1

AWS_ECR_LOGIN_URI = 788614365622.dkr.ecr.us-east-1.amazonaws.com/networkssecurity
ECR_REPOSITORY_NAME = networkssecurity


Docker Setup In EC2 commands to be Executed
#optinal

sudo apt-get update -y

sudo apt-get upgrade

#required

curl -fsSL https://get.docker.com -o get-docker.sh

sudo sh get-docker.sh

sudo usermod -aG docker ubuntu

newgrp docker