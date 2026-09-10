# Introduction to Amazon CloudFront

## 📌 Project Overview

This project demonstrates how to use **Amazon CloudFront** with **Amazon S3** to deliver image content through a global Content Delivery Network (CDN).

The project was completed as an AWS hands-on lab and covers the process of creating an S3 bucket, uploading images, configuring a CloudFront distribution, and testing image delivery through the CloudFront domain.

---

## 🎯 Objectives

* Create an Amazon S3 bucket.
* Upload image files to Amazon S3.
* Configure Amazon CloudFront with Amazon S3 as the origin.
* Block direct public access to the S3 bucket.
* Serve images through CloudFront.
* Create and test an HTML page using the CloudFront domain.

---

## 🏗️ Architecture

```text
User / Browser
      │
      ▼
Amazon CloudFront
      │
      ▼
Amazon S3 Bucket
      │
      ▼
Image Objects
```

CloudFront retrieves the image objects from the S3 origin and delivers them through its global network of edge locations.

---

## 🛠️ AWS Services Used

| Service                | Purpose                  |
| ---------------------- | ------------------------ |
| Amazon S3              | Store image objects      |
| Amazon CloudFront      | Deliver content globally |
| AWS Management Console | Configure AWS resources  |

---

## 🚀 Implementation

### 1. Create an S3 Bucket

An Amazon S3 bucket was created to store the image files.

The bucket was configured with public access blocked.

![Create Bucket](./screenshots/01-Create%20Bucket.png)

---

### 2. Upload Images to the Bucket

Image files were uploaded to the S3 bucket.

![Upload Images](./screenshots/02-Upload%20images%20in%20bucket.png)

---

### 3. Test Direct S3 Access

Direct access to the image was tested using the S3 object URL.

The request returned an **AccessDenied** error because public access to the bucket was blocked.

![Access Denied](./screenshots/03-%20Access%20denied%20for%20image.png)

---

### 4. Create a CloudFront Distribution

A CloudFront distribution was created with the S3 bucket configured as the origin.

![Create Distribution](./screenshots/04-%20Create%20distribution.png)

---

### 5. CloudFront Distribution Created

The CloudFront distribution was successfully created and deployed.

![Distribution Created](./screenshots/05-Distribution%20created.png)

---

### 6. Create the HTML Test Page

A simple HTML test page was created using **Notepad**.

The page uses the CloudFront distribution domain to display the images.

![CloudFront Notepad HTML](./screenshots/06-%20Cloudfront-Notepad-html.png)

The HTML file used for testing is available here:

**[myimages.html](./myimages.html)**

---

### 7. Open the First Image via CloudFront

The first image was successfully displayed through the CloudFront distribution.

![First Image via CloudFront](./screenshots/07-Open%20first%20image%20via-cloudfront.png)

---

### 8. Open the Second Image via CloudFront

The second image was successfully displayed through the CloudFront distribution.

![Second Image via CloudFront](./screenshots/08-Open%20second%20image%20via-cloudfront.png)

---

## 🌐 CloudFront Distribution

**CloudFront Domain:**

`ddp5f4bgy9gp7.cloudfront.net`

The CloudFront distribution provides access to the S3 content through CloudFront rather than direct public access to the S3 bucket.

---

## ✅ Results

The CloudFront distribution was successfully created and tested.

The project demonstrated that:

* Amazon S3 can be used as a CloudFront origin.
* Direct public access to the S3 bucket can remain blocked.
* CloudFront can retrieve objects from the S3 origin.
* Images can be served through a CloudFront domain.
* CloudFront edge locations can be used to deliver content efficiently.

---

## 📚 What I Learned

Through this hands-on project, I gained practical experience with:

* Creating and configuring an Amazon S3 bucket.
* Uploading and managing S3 objects.
* Understanding S3 public access blocking.
* Creating an Amazon CloudFront distribution.
* Configuring Amazon S3 as a CloudFront origin.
* Using a CloudFront domain to serve web content.
* Creating and testing an HTML page.
* Understanding the role of CloudFront edge locations and caching.

---

## 🏁 Conclusion

This hands-on project provided practical experience with **Amazon S3 and Amazon CloudFront**, demonstrating how CloudFront can be used as a content delivery layer in front of an S3 origin to efficiently deliver image content to users.
