# Introduction to Amazon CloudFront

## 📌 Project Overview

This project demonstrates how to use **Amazon CloudFront** with **Amazon S3** to securely and efficiently deliver image content through a global content delivery network (CDN).

The project was completed as an AWS hands-on lab and covers the process of creating an S3 bucket, uploading images, configuring a CloudFront distribution, and testing image delivery through the CloudFront domain.

---

## 🎯 Objectives

* Create an Amazon S3 bucket and upload image files.
* Configure Amazon CloudFront with Amazon S3 as the origin.
* Block direct public access to the S3 bucket.
* Use CloudFront to serve image content.
* Create an HTML page that displays images through CloudFront.
* Test the CloudFront distribution.

---

## 🏗️ Architecture

```text id="x2q9vm"
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

CloudFront retrieves the images from the S3 origin and delivers them through its global network of edge locations.

---

## 🛠️ AWS Services Used

| Service                    | Purpose                     |
| -------------------------- | --------------------------- |
| **Amazon S3**              | Store image objects         |
| **Amazon CloudFront**      | Distribute content globally |
| **AWS Management Console** | Configure AWS resources     |

---

## 🚀 Implementation

### 1. Create an S3 Bucket

An Amazon S3 bucket was created to store the image files.

The bucket was configured with:

* ACLs disabled
* Block all public access enabled
* Default S3 settings

![Create Bucket](./screenshots/01-Create%20Bucket.png)

---

### 2. Upload Images to the S3 Bucket

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

After the distribution was successfully deployed, the CloudFront domain name was used to access the content.

![Distribution Created](./screenshots/05-Distribution%20created.png)

---

### 6. Create the HTML Test Page

A simple HTML page was created using **Notepad**.

The page uses the CloudFront domain name to display the images.

![CloudFront Notepad HTML](./screenshots/06-%20Cloudfront-Notepad-html.png)

The HTML test page is available in this repository:

[`myimages.html`](./myimages.html)

---

### 7. Open the First Image via CloudFront

The first image was successfully displayed through the CloudFront distribution.

![First Image via CloudFront](./screenshots/07-Open%20first%20image%20via-cloudfront.png)

---

### 8. Open the Second Image via CloudFront

The second image was also successfully delivered through CloudFront.

![Second Image via CloudFront](./screenshots/08-Open%20second%20image%20via-cloudfront.png)

---

## 🌐 CloudFront Distribution

**CloudFront Domain:**

`ddp5f4bgy9gp7.cloudfront.net`

The CloudFront distribution provides access to the S3 content through CloudFront instead of direct public access to the S3 bucket.

---

## ✅ Results

The CloudFront distribution was successfully created and tested.

The project demonstrated that:

* Amazon S3 can be used as a CloudFront origin.
* Direct public access to the S3 bucket can remain blocked.
* CloudFront can retrieve objects from the S3 origin.
* Images can be served through a CloudFront domain.
* CloudFront uses edge locations to deliver content efficiently.

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
* Understanding the basic role of CloudFront edge locations and caching.

---

## 🏁 Conclusion

This hands-on project provided practical experience with **Amazon S3 and Amazon CloudFront**, demonstrating how CloudFront can be used as a content delivery layer in front of an S3 origin to efficiently deliver image content to users.
