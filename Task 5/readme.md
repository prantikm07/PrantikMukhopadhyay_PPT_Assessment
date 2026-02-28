# Task 5: Static Website Hosting in S3

## Simple Definition

Static Website Hosting in Amazon S3 allows hosting HTML, CSS, and JavaScript files directly from an S3 bucket without using a server. It is a serverless and cost-effective way to publish websites.

## Objective

To learn how to configure Amazon S3 for static website hosting and make a website publicly accessible over the internet.

## Steps (GUI Method)

1. Go to AWS Console → S3.
2. Click **Create bucket**.
3. Enter a unique bucket name.
4. Select region (eu-north-1).
5. Disable "Block all public access".
6. Acknowledge warning and create bucket.

7. Open the bucket → Go to **Properties** tab.
8. Scroll to **Static website hosting**.
9. Click **Edit** → Enable.
10. Select:
    - Hosting type: Host a static website
    - Index document: index.html
11. Save changes.

12. Go to **Permissions** tab.
13. Add bucket policy to allow public read access:

{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Sid": "PublicReadGetObject",
      "Effect": "Allow",
      "Principal": "*",
      "Action": "s3:GetObject",
      "Resource": "arn:aws:s3:::YOUR_BUCKET_NAME/*"
    }
  ]
}

14. Replace YOUR_BUCKET_NAME with actual bucket name.
15. Save policy.

16. Go to **Objects** tab.
17. Click **Upload**.
18. Upload index.html (and other static files if any).
19. After upload, select file → Make sure public access is allowed.

20. Go back to **Properties** → Static website hosting.
21. Copy the **Bucket website endpoint URL**.
22. Paste URL in browser to verify website loads.

## Verification

- Bucket website endpoint loads successfully in browser.
- index.html file is accessible publicly.
- No Access Denied error appears.

Screenshots Submitted:

1. S3 bucket Properties page showing Static Website Hosting enabled and website endpoint.
2. Browser showing hosted website using S3 endpoint URL.

## Conclusion

Successfully hosted a static website using Amazon S3. This demonstrates serverless web hosting and understanding of S3 permissions and public access configuration.