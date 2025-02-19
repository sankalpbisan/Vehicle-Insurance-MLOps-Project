# Vehicle Insurance MLOps Project

This repository contains the implementation of an end-to-end MLOps pipeline for a vehicle insurance project. The goal of this project is to predict vehicle insurance claims using machine learning models, integrated with MLOps practices such as modular coding, continuous integration, and continuous deployment.

---

## 🧑‍💻 Table of Contents

- [Project Overview](#-project-overview)
- [Features](#-features)
- [Technologies Used](#-technologies-used)
- [Setup & Installation](#-setup-&-installation)
- [How It Works](#-how-it-works)
- [Model Development](#-model-development)
- [Deployment](#-deployment)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🚀 Project Overview

The **Vehicle Insurance MLOps Project** aims to build and deploy machine learning models that can predict which customer is likely to buy insurance for vehicles. The project follows best practices for model development, deployment, and monitoring in a real-world MLOps environment.

---

## 🌟 Features

- **Predictive Model**: Uses machine learning to predict the likelihood of a vehicle insurance claim.
- **MLOps Pipeline**: Fully automated pipeline for continuous model training, testing, and deployment.
- **Model Monitoring**: Tools for tracking model performance and drift.
- **Data Processing**: Efficient ETL (Extract, Transform, Load) pipeline to handle raw data.
- **Automated Deployment**: Deploy models automatically using CI/CD tools.

---

## 🛠️ Technologies Used

- **Programming Languages**: Python, Shell Scripting
- **Machine Learning Framework**: Scikit-learn
- **MLOps Tools**: MLflow, Docker, GitHub Actions
- **Cloud Platform**: AWS (S3 Bucket, ECR)
- **Database/Storage**: MongoDB
- **Version Control**: Git, GitHub

---

## ⚙️ Setup & Installation

Follow these steps to set up the project locally:

### 1. Clone the repository:

```bash
git clone https://github.com/sankalpbisan/Vehicle-Insurance-MLOps-Project.git
```

### 2. Install dependencies:

```bash
cd Vehicle-Insurance-MLOps-Project
pip install -r requirements.txt
```

### 3. Set access/environment variables:

Ensure you have all the required environment variables set. You can use a `.env` file or set them directly.

If you want to run the training-pipeline, then you'll have to add you own access_id and access_key from MongoDB Atlas along with AWS credentials for pushing model onto AWS and using its services like Elastic Container Registry (ECR) and EC2.

You can either set these variables from environment variables service in windows or directly provide them in constants file as:
```
AWS_ACCESS_KEY_ID=your_access_key
AWS_SECRET_ACCESS_KEY=your_secret_key
REGION_NAME = "your_selected_region"
```
and
```
DATABASE_NAME = "your_database_name"
COLLECTION_NAME = "your_collection_name"
MONGODB_URL_KEY = "your_connection_url"
```

### 4. Run the project:

To start the project locally:

```bash
python app.py
```

### 5. Dockerize the application:

If you wish to run it in a containerized environment:

```bash
docker build -t vehicle-insurance .
docker run -p 5000:5000 vehicle-insurance
```
I have directly pushed the 'model.pkl' file to S3 bucket in AWS and predictions are done using pickle file from this bucket only.

---

## 🧠 How It Works

1. **Data Ingestion**: Collect data from MongoDB database Cluster.
2. **Data Validation**: Received Data is validated to check whether  data is proper as excepcted or not.
3. **Data Preprocessing**: Clean, normalize, and transform the data into a format suitable for model training.
4. **Model Development**: Train multiple machine learning models, tune hyperparameters, and select the best model.
5. **Model Evaluation**: Evaluate models using appropriate metrics (accuracy, precision, recall, etc.).
6. **Deployment**: Deploy the model to a production environment (here, AWS) using CI/CD pipelines.

---

## 🤖 Model Development

This project uses a combination of classical machine learning techniques to predict 'buying insurance?' The models are evaluated and tuned to achieve the best performance based on validation data.

### Key Steps:
1. Data preprocessing (handling missing values, feature engineering, scaling).
2. Model training using Scikit-learn.
3. Hyperparameter tuning and model selection.

For more details on how the models are developed and trained, check the `notebooks` and `src` directories.

---

## 🚢 Deployment

The model is deployed in a production-like environment using Docker and Kubernetes. CI/CD pipelines ensure that changes are automatically tested, validated, and deployed.

### Steps:
1. **Dockerize the Model**: Containerize the model using Docker.
2. **CI/CD Integration**: Configure GitHub Actions : CI/CD pipelines for automated testing and deployment.

---

## 🤝 Contributing

Contributions are welcome! 

If you have any suggestions feel free to reach out.

## 📜 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 📬 Contact

For any questions or inquiries, feel free to reach out:

- **Email**: sankalpbisan07@gmail.com
- **LinkedIn**: [My LinkedIn Profile](https://in.linkedin.com/in/sankalpbisan)

---

*I have removed all instances from AWS and MongoBD for security concerns, and from AWS, because of the cost factor.*

---

Also check out my various projects:
1. **Design-and-Development-of-Real-Time-Sign-Language-to-Speech-Conversion-System** - [Click Here to visit this repo](https://github.com/sankalpbisan/Design-and-Development-of-Real-Time-Sign-Language-to-Speech-Conversion-System.git)
2. **Student Performance Indicator** - [Click Here to visit this repo](https://github.com/sankalpbisan/MLOps_practice_project_students_performance_indicator.git)
3. **Patients Hospital Charges Predictor** - [Click Here to visit this repo](https://github.com/sankalpbisan/MLOps_Practice_Project-Patients-Hospital-Charges-Predictor.git)

---

Thank you for visiting the Vehicle Insurance MLOps Project repository. Feel free to explore the code, raise issues, or contribute to the project!



