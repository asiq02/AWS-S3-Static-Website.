# AWS S3 Static Website Hosting

This repository provides step-by-step instructions for hosting a static website using Amazon S3 (Simple Storage Service).

## Steps to Host a Static Website on AWS S3

### Step 1: Create a Bucket
1. Open the Amazon S3 console.
2. Click **Create bucket** and configure the following:
   - **Bucket Name**: Provide a unique name for your bucket.
   - **Region**: Select the AWS Region closest to you.
   - **Object Ownership**: Choose **ACLs enabled** and **Bucket owner preferred**.
   - **Block Public Access**: Uncheck **Block all public access** to allow public access to your files.
   - **Bucket Versioning**: Enable versioning to keep track of file changes.
3. Click **Create bucket**.

### Step 2: Upload Website Content to Your Bucket
1. Navigate to your bucket in the Amazon S3 console.
2. Go to the **Objects** tab and click **Upload**.
3. Add your website files:
   - Click **Add files** to upload your `index.html`.
   - Click **Add folder** to upload additional website assets (like CSS, JS, images, etc.).
4. Click **Upload**.

### Step 3: Configure the Bucket for Static Website Hosting
1. Open your bucket and navigate to the **Properties** tab.
2. Scroll to the **Static website hosting** section and click **Edit**.
3. Configure the following settings:
   - **Static web hosting**: Enable.
   - **Hosting type**: Host a static website.
   - **Index document**: Enter `index.html`.
4. Click **Save changes**.
5. Copy the **Bucket website endpoint URL** provided.

### Step 4: Make Files Public
1. In your bucket, select the checkboxes for `index.html` and your website assets.
2. Click the **Actions** dropdown and select **Make public using ACL**.
3. Confirm by clicking **Make public**.

### View the Website
- Visit the **Bucket website endpoint URL** to view your hosted website.

---

## Notes
- Ensure you follow security best practices while managing permissions.
- If you need a custom domain, consider configuring Amazon Route 53 for domain management.

## License
This repository is licensed under the MIT License. Feel free to use and modify the instructions as needed.

Happy hosting!
