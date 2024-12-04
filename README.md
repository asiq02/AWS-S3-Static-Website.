# AWS-S3-Static-Website.
Using the AWS S3 (Simple storage service) hosting a Static Website.

Step 1 : Creating bucket
Create an bucket in Amazon S3
Open Amazon S3.
Create a storage space for your website files.
Select the AWS Region closest to you. You can find this at the top right corner of your AWS Management console, right next to your name!
Choose Create bucket.
For Object Ownership, choose ACLs enabled.
Choose Bucket owner preferred.
For Block Public Access settings for this bucket, clear the check box for Block all public access.
For Bucket Versioning, choose Enable.
Choose Create bucket.

Step 2 : Upload Website Content to Your bucket
For Bucket Versioning, choose Enable.
Choose Create bucket.
Return to the Amazon S3 console with your bucket page open.
Choose the Objects tab.
Choose Upload.
Choose Add files.
Choose index.html.
Choose Add folder and the following files in after index.html.
Choose Upload.

Step 3 : Configure a static website on Amazon S3
Make sure you're back in your bucket's page. 
If you're not sure, choose Buckets on the left hand side navigation bar, and then choose the bucket you created for this project. 
Choose the Properties tab.
Scroll all the way down to the Static website hosting panel..
Choose Edit.
Configure the following settings:  
               Static web hosting: Choose Enable.
               Hosting type: Choose Host a static website.
               Index document: Enter index.html
Choose Save changes. 
In the Static website hosting panel, click on the URL under Bucket website endpoint.

Step 4 : Make objects in your S3 bucket public
Select the checkboxes next to your index.html file and the folder of website assets.
In the Actions dropdown, choose Make public using ACL.
Choose Make public.
Once the green banner pops up, choose Close.

                                               *VIEW THE WEBSITE*

