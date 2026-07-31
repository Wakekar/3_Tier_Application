# Yelp Camp Web Application

This web application allows users to add, view, access, and rate campgrounds by location. It is based on "The Web Developer Bootcamp" by Colt Steele, but includes several modifications and bug fixes. The application leverages a variety of technologies and packages, such as:

- **Node.js with Express**: Used for the web server.
- **Bootstrap**: For front-end design.
- **Mapbox**: Provides a fancy cluster map.
- **MongoDB Atlas**: Serves as the database.
- **Passport package with local strategy**: For authentication and authorization.
- **Cloudinary**: Used for cloud-based image storage.
- **Helmet**: Enhances application security.
- ...

## Setup Instructions

To get this application up and running, you'll need to set up accounts with Cloudinary, Mapbox, and MongoDB Atlas. Once these are set up, create a `.env` file in the same folder as `app.js`. This file should contain the following configurations:

```sh
CLOUDINARY_CLOUD_NAME=[Your Cloudinary Cloud Name]
CLOUDINARY_KEY=[Your Cloudinary Key]
CLOUDINARY_SECRET=[Your Cloudinary Secret]
MAPBOX_TOKEN=[Your Mapbox Token]
DB_URL=[Your MongoDB Atlas Connection URL]
SECRET=[Your Chosen Secret Key] # This can be any value you prefer
```

After configuring the .env file, you can start the project by running:
```sh
docker compose up
```
# 📸 Project Screenshots

This section demonstrates the complete workflow of the application, from development to production deployment on Amazon EKS using a complete DevOps CI/CD pipeline.

---

# 🖥️ Application Screenshots

## 🏠 1. Application Landing Page

<p align="center">
  <img src="./screenshots/01_Application_Landing_Page.png" width="100%">
</p>

---

## 🌐 2. Application Home Page

<p align="center">
  <img src="./screenshots/02_Application_2.png" width="100%">
</p>

---

## ⭐ 3. Application Review Page

<p align="center">
  <img src="./screenshots/03_Application_Review.png" width="100%">
</p>

---

## 👤 4. User Registration

<p align="center">
  <img src="./screenshots/07_User_registration.png" width="100%">
</p>

---

# ☁️ AWS Infrastructure

## 🖥️ 5. AWS EC2 Instances

<p align="center">
  <img src="./screenshots/04_Instances.png" width="100%">
</p>

---

## ☁️ 6. AWS CloudFormation Stack

<p align="center">
  <img src="./screenshots/05_Cloude_Formation.png" width="100%">
</p>

---

## ☸️ 7. Amazon EKS Cluster

<p align="center">
  <img src="./screenshots/20_EKS_Cluster.png" width="100%">
</p>

---

# 🔐 Application Configuration

## ☁️ 8. Cloudinary API Keys

<p align="center">
  <img src="./screenshots/06_cloudinary_keys.png" width="100%">
</p>

---

## 🗺️ 9. MapBox Token Configuration

<p align="center">
  <img src="./screenshots/09_MapBox_Token.png" width="100%">
</p>

---

# 🗄️ Database

## 🍃 10. MongoDB Database Entry

<p align="center">
  <img src="./screenshots/08_Database_Entry.png" width="100%">
</p>

---

## 🗄️ 11. MongoDB Atlas Cluster

<p align="center">
  <img src="./screenshots/15_MongoDB_Cluster.png" width="100%">
</p>

---

## 📈 12. MongoDB Metrics

<p align="center">
  <img src="./screenshots/16_MongoDB_Metrix.png" width="100%">
</p>

---

# 🚀 Jenkins CI/CD Pipeline

## ✅ 13. Jenkins Pipeline Success

<p align="center">
  <img src="./screenshots/10_Pipeline_success.png" width="100%">
</p>

---

## ☸️ 14. Pipeline Success (ClusterIP Deployment)

<p align="center">
  <img src="./screenshots/21_Pipeline_Success_ClusterIP.png" width="100%">
</p>

---

# 🔍 Security Scanning

## 🛡️ 15. Trivy Filesystem Scan Report

<p align="center">
  <img src="./screenshots/11_fs_report_Trivy.png" width="100%">
</p>

---

## 🐳 16. Trivy Docker Image Scan Report

<p align="center">
  <img src="./screenshots/12_image_report.png" width="100%">
</p>

---

# 📊 SonarQube Code Analysis

## 📈 17. SonarQube Dashboard

<p align="center">
  <img src="./screenshots/13_Sonarqube-Report.png" width="100%">
</p>

---

## 📑 18. SonarQube Code Quality Report

<p align="center">
  <img src="./screenshots/14_Code_Report.png" width="100%">
</p>

---

## 📊 19. SonarQube Analysis Dashboard

<p align="center">
  <img src="./screenshots/17_Sonarqube_2.png" width="100%">
</p>

---

# 📦 Source Code & Container Registry

## 🐙 20. GitHub Repository

<p align="center">
  <img src="./screenshots/18_Github.png" width="100%">
</p>

---

## 🐳 21. DockerHub Repository

<p align="center">
  <img src="./screenshots/19_DockerHub.png" width="100%">
</p>

---

# 🎯 Complete DevOps Workflow

```text
👨‍💻 Developer
        │
        ▼
🐙 GitHub Repository
        │
        ▼
⚙️ Jenkins CI/CD Pipeline
        │
        ├──────────────► 📊 SonarQube Code Analysis
        │
        ├──────────────► 🛡️ Trivy Filesystem Scan
        │
        ▼
🐳 Docker Image Build
        │
        ▼
🛡️ Trivy Docker Image Scan
        │
        ▼
📦 Push Docker Image to DockerHub
        │
        ▼
☸️ Amazon EKS Deployment
        │
        ▼
🌐 Application Successfully Running on Kubernetes
```
