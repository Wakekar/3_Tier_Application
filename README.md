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

# 📸 Project Screenshots

## 🏠 Application Landing Page

<p align="center">
  <img src="./Screenshots/01_Application_Landing_Page.png" alt="Application Landing Page" width="100%">
</p>

---

## 🌐 Application Home Page

<p align="center">
  <img src="./Screenshots/02_Application_2.png" alt="Application Home Page" width="100%">
</p>

---

## ⭐ Application Review Page

<p align="center">
  <img src="./Screenshots/03_Application_Review.png" alt="Application Review Page" width="100%">
</p>

---

## 🖥️ AWS EC2 Instances

<p align="center">
  <img src="./Screenshots/04_Instances.png" alt="AWS EC2 Instances" width="100%">
</p>

---

## ☁️ AWS CloudFormation

<p align="center">
  <img src="./Screenshots/05_Cloude_Formation.png" alt="CloudFormation" width="100%">
</p>

---

## ☁️ Cloudinary Configuration

<p align="center">
  <img src="./Screenshots/06_cloudinary_keys.png" alt="Cloudinary" width="100%">
</p>

---

## 👤 User Registration

<p align="center">
  <img src="./Screenshots/07_User_registration.png" alt="User Registration" width="100%">
</p>

---

## 🍃 MongoDB Database Entry

<p align="center">
  <img src="./Screenshots/08_Database_Entry.png" alt="Database Entry" width="100%">
</p>

---

## 🗺️ MapBox Token

<p align="center">
  <img src="./Screenshots/09_MapBox_Token.png" alt="MapBox Token" width="100%">
</p>

---

## 🚀 Jenkins Pipeline Success

<p align="center">
  <img src="./Screenshots/10_Pipeline_success.png" alt="Pipeline Success" width="100%">
</p>

---

## 🛡️ Trivy Filesystem Scan

<p align="center">
  <img src="./Screenshots/11_fs_report_Trivy.png" alt="Filesystem Scan" width="100%">
</p>

---

## 🐳 Trivy Image Scan

<p align="center">
  <img src="./Screenshots/12_image_report.png" alt="Image Scan" width="100%">
</p>

---

## 📊 SonarQube Dashboard

<p align="center">
  <img src="./Screenshots/13_Sonarqube-Report.png" alt="SonarQube Dashboard" width="100%">
</p>

---

## 📈 SonarQube Code Report

<p align="center">
  <img src="./Screenshots/14_Code_Report.png" alt="Code Report" width="100%">
</p>

---

## 🗄️ MongoDB Atlas Cluster

<p align="center">
  <img src="./Screenshots/15_MongoDB_Cluster.png" alt="MongoDB Cluster" width="100%">
</p>

---

## 📉 MongoDB Metrics

<p align="center">
  <img src="./Screenshots/16_MongoDB_Metrix.png" alt="MongoDB Metrics" width="100%">
</p>

---

## 📊 SonarQube Analysis

<p align="center">
  <img src="./Screenshots/17_Sonarqube_2.png" alt="SonarQube Analysis" width="100%">
</p>

---

## 🐙 GitHub Repository

<p align="center">
  <img src="./Screenshots/18_Github.png" alt="GitHub" width="100%">
</p>

---

## 🐳 DockerHub Repository

<p align="center">
  <img src="./Screenshots/19_DockerHub.png" alt="DockerHub" width="100%">
</p>

---

## ☸️ Amazon EKS Cluster

<p align="center">
  <img src="./Screenshots/20_EKS_Cluster.png" alt="Amazon EKS Cluster" width="100%">
</p>

---

## ✅ Kubernetes Deployment Success

<p align="center">
  <img src="./Screenshots/21_Pipeline_Success_ClusterIP.png" alt="Pipeline Success ClusterIP" width="100%">
</p>
