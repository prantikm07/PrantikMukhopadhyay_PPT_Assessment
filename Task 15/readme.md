# Task 15: CloudFront Distribution for S3 Static Website

## Simple Definition

CloudFront is a Content Delivery Network (CDN) that delivers website content globally with low latency by caching content at edge locations.

## Objective

To configure CloudFront distribution for an S3 static website to improve performance and global availability.

## Architecture Overview

User  
↓  
CloudFront Distribution  
↓  
S3 Static Website Bucket

## Steps

### Step 1: Prepare S3 Static Website

1. Go to S3.
2. Enable Static Website Hosting.
3. Upload index.html file.
4. Ensure bucket policy allows public read access.

### Step 2: Create CloudFront Distribution

1. Go to CloudFront → Create Distribution.
2. Origin domain:
   - Select S3 bucket.
3. Set viewer protocol policy:
   - Redirect HTTP to HTTPS.
4. Default cache behavior: Keep default.
5. Create distribution.

### Step 3: Wait for Deployment

1. Wait until status changes to Deployed.
2. Copy CloudFront domain name.

### Step 4: Test Website

1. Open CloudFront URL in browser.
2. Confirm website loads successfully.

## Verification

* CloudFront distribution status = Deployed.
* Website accessible using CloudFront URL.
* Faster content delivery.

## Conclusion

Successfully configured CloudFront distribution for S3 static website, demonstrating CDN usage and global content delivery optimization.