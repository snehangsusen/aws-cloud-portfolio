# Cloud Static Website Hosting using AWS

## Project Description

This project demonstrates how to host a static website using cloud
services on Amazon Web Services (AWS). The website is deployed using
Amazon S3 and can optionally use CloudFront CDN for faster global
delivery.

This project is useful for beginners who want to learn basic cloud
deployment and static website hosting.

------------------------------------------------------------------------

## Architecture

User ↓ CloudFront CDN ↓ Amazon S3 (Static Website Hosting)

------------------------------------------------------------------------

## AWS Services Used

-   Amazon S3 -- Static website hosting
-   Amazon CloudFront -- Content Delivery Network (optional)
-   GitHub -- Version control and project repository

------------------------------------------------------------------------

## Project Structure

aws-static-website │ ├── index.html └── README.md

------------------------------------------------------------------------

## Steps to Deploy

### 1. Create S3 Bucket

1.  Login to AWS Console
2.  Open Amazon S3
3.  Click **Create Bucket**
4.  Give a unique bucket name
5.  Disable **Block all public access**

Example bucket name:

snehangsu-cloud-project

------------------------------------------------------------------------

### 2. Upload Website File

Upload:

index.html

------------------------------------------------------------------------

### 3. Enable Static Website Hosting

Go to:

Bucket → Properties → Static Website Hosting

Enable it and set:

Index document: index.html

------------------------------------------------------------------------

### 4. Add Bucket Policy

Add the following policy to allow public access.

{ "Version":"2012-10-17", "Statement":\[ { "Effect":"Allow",
"Principal":"*", "Action":"s3:GetObject",
"Resource":"arn:aws:s3:::YOUR_BUCKET_NAME/*" }\] }

Replace YOUR_BUCKET_NAME with your actual bucket name.

------------------------------------------------------------------------

### 5. Access the Website

After enabling static website hosting, AWS will generate a website URL.

Example:

http://your-bucket-name.s3-website-us-east-1.amazonaws.com

Open this URL in your browser to view the website.

------------------------------------------------------------------------

## Learning Outcomes

-   Understanding cloud storage
-   Deploying static websites on AWS
-   Configuring bucket policies
-   Basic cloud architecture

------------------------------------------------------------------------

## Author

Snehangsu Sen\
B.Tech -- Information Technology\
Dr. B. C. Roy Engineering College, Durgapur
