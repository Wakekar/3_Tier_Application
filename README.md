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

This section showcases the complete workflow of the project, from application deployment to CI/CD pipeline execution, security scanning, cloud infrastructure, and Kubernetes deployment.

---

## 🖥️ Application Screenshots

### 🏠 1. Application Landing Page

![Application Landing Page](01_Application_Landing_Page.png)

---

### 🌐 2. Application Home Page

![Application Home Page](02_Application_2.png)

---

### ⭐ 3. Application Review Page

![Application Review Page](03_Application_Review.png)

---

### 👤 4. User Registration

![User Registration](07_User_registration.png)

---

## ☁️ AWS Infrastructure

### 🖥️ 5. AWS EC2 Instances

![AWS EC2 Instances](04_Instances.png)

---

### ☁️ 6. AWS CloudFormation Stack

![AWS CloudFormation](05_Cloude_Formation.png)

---

### ☸️ 7. Amazon EKS Cluster

![Amazon EKS Cluster](20_EKS_Cluster.png)

---

## 🔐 Application Configuration

### ☁️ 8. Cloudinary API Keys

![Cloudinary API Keys](06_cloudinary_keys.png)

---

### 🗺️ 9. MapBox Token Configuration

![MapBox Token](09_MapBox_Token.png)

---

## 🗄️ Database

### 🍃 10. MongoDB Database Entry

![MongoDB Database Entry](08_Database_Entry.png)

---

### 🗄️ 11. MongoDB Atlas Cluster

![MongoDB Atlas Cluster](15_MongoDB_Cluster.png)

---

### 📈 12. MongoDB Metrics

![MongoDB Metrics](16_MongoDB_Metrix.png)

---

## 🚀 Jenkins CI/CD Pipeline

### ✅ 13. Jenkins Pipeline Success

![Jenkins Pipeline Success](10_Pipeline_success.png)

---

### ☸️ 14. Jenkins Pipeline Success (ClusterIP Deployment)

![Pipeline Success ClusterIP](21_Pipeline_Success_ClusterIP.png)

---

## 🔍 Security Scanning

### 🛡️ 15. Trivy Filesystem Scan Report

![Trivy Filesystem Scan](11_fs_report_Trivy.png)

---

### 🐳 16. Trivy Docker Image Scan Report

![Trivy Image Scan](12_image_report.png)

---

## 📊 SonarQube Code Analysis

### 📈 17. SonarQube Dashboard

![SonarQube Dashboard](13_Sonarqube-Report.png)

---

### 📑 18. SonarQube Code Quality Report

![SonarQube Code Report](14_Code_Report.png)

---

### 📊 19. SonarQube Analysis Dashboard

![SonarQube Analysis Dashboard](17_Sonarqube_2.png)

---

## 📦 Source Code & Container Registry

### 🐙 20. GitHub Repository

![GitHub Repository](18_Github.png)

---

### 🐳 21. DockerHub Repository

![DockerHub Repository](19_DockerHub.png)

---

# 🎯 Project Workflow Summary

✔️ Application Development

⬇️

✔️ Source Code Hosted on GitHub

⬇️

✔️ Jenkins CI/CD Pipeline

⬇️

✔️ SonarQube Static Code Analysis

⬇️

✔️ Trivy Filesystem Security Scan

⬇️

✔️ Docker Image Build

⬇️

✔️ Trivy Docker Image Scan

⬇️

✔️ DockerHub Image Push

⬇️

✔️ Amazon EKS Deployment

⬇️

✔️ Application Successfully Running on Kubernetes

---
