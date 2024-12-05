# AWS S3 Static Website Hosting

This guide provides step-by-step instructions for hosting a static website using Amazon S3.

## Steps to Host Your Static Website

### 1. Create an S3 Bucket
1. Open the Amazon S3 console.
2. Click **Create bucket** and configure the following:
   - **Bucket Name**: Enter a unique name for your bucket.
   - **Region**: Select the AWS Region closest to you.
   - **Object Ownership**: Choose **ACLs enabled** and **Bucket owner preferred**.
   - **Block Public Access**: Uncheck **Block all public access** to allow public access to files.
   - **Bucket Versioning**: Enable versioning to track changes to your files.
3. Click **Create bucket**.

### 2. Upload Website Content
1. Open your bucket in the Amazon S3 console.
2. Go to the **Objects** tab and click **Upload**.
3. Add your website files:
   - Use **Add files** to upload `index.html`.
   - Use **Add folder** to upload additional assets (e.g., CSS, JavaScript, images).
4. Click **Upload**.

### 3. Enable Static Website Hosting
1. In your bucket, go to the **Properties** tab.
2. Scroll to **Static website hosting** and click **Edit**.
3. Configure the following:
   - **Static web hosting**: Enable.
   - **Hosting type**: Select **Host a static website**.
   - **Index document**: Enter `index.html`.
4. Click **Save changes**.
5. Copy the **Bucket website endpoint URL** provided.

### View the Website
- Visit the **Bucket website endpoint URL** to view your hosted website.

### 4. Add a Bucket Policy for Public Access
1. Go to the **Permissions** tab in your bucket.
2. Scroll to **Bucket policy** and click **Edit**.
3. Add the following policy to allow public read access:
   ```json
   {
       "Version": "2012-10-17",
       "Statement": [
           {
               "Sid": "PublicReadGetObject",
               "Effect": "Allow",
               "Principal": "*",
               "Action": "s3:GetObject",
               "Resource": "arn:aws:s3:::your-bucket-name/*"
           }
       ]
   }

