# 🌐 Hosting a Static Website Using Amazon S3

This project demonstrates how to host a static website using **Amazon S3**. It is a simple and cost-effective way to deploy websites using AWS cloud services.

## 📌 Project Overview

In this project, we configure an S3 bucket to host a static website by uploading HTML, CSS, and JavaScript files and enabling public access.

## 🚀 Features

* Static website hosting using Amazon S3
* Public access configuration
* Easy deployment process
* Scalable and reliable hosting

## 🛠️ Technologies Used

* Amazon S3 (AWS)
* HTML5
* CSS3
* JavaScript

## 📂 Project Structure

```
project-folder/
│── index.html
│── error.html (optional)
│── styles.css
│── script.js
│── assets/
```

## ⚙️ Setup Instructions

### 1️⃣ Create an S3 Bucket

* Go to AWS Management Console
* Navigate to S3 service
* Click **Create Bucket**
* Provide a unique bucket name
* Disable "Block all public access" (for hosting)

### 2️⃣ Upload Website Files

* Open your bucket
* Click **Upload**
* Add your website files (HTML, CSS, JS)

### 3️⃣ Enable Static Website Hosting

* Go to **Properties** tab
* Scroll to **Static Website Hosting**
* Enable it
* Set:

  * Index document: `index.html`
  * Error document: `error.html` (optional)

### 4️⃣ Set Bucket Policy

Add the following policy to allow public access:

```json
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR-BUCKET-NAME/*"
    }
  ]
}
```

### 5️⃣ Access Your Website

* Copy the **S3 website endpoint URL**
* Open it in your browser

🎉 Your static website is now live!


## 💡 Benefits of Using Amazon S3

* Highly scalable
* Low cost
* High availability
* Easy integration with other AWS services

## ⚠️ Notes

* Ensure correct permissions are set for public access
* Bucket name must be globally unique
* Use proper file paths in your HTML


