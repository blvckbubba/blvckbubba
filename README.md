### Hi there 👋

<!--
**blvckbubba/blvckbubba** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...

- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
My name is Akinrelere Ayodamope
<p> I just finished working on a task on hosting a static webpage on a private s3 bucket and accessing it through cloudfront </p>
Creating a Bucket on Amazon S3
Here is a step-by-step guide.

<p>Prerequisite: ensure you have a AWS account and the files for your static website</p><img width="1920" alt="Screenshot 2024-05-11 at 09 15 05" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/0ef765e5-3529-42d0-a955-29cb18405465">


<p>STEP ONE:Creating a Bucket on Amazon S3</p>
a) After logging into your AWS Console, under Services > All Services, search for “S3” and click on it to go to the S3 dashboard.
<img width="1920" alt="Screenshot 2024-05-11 at 08 10 07" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/90b8289e-84f9-44f8-ac94-8ff9f89345c3">

b) On the S3 Dashboard, click on the Create Bucket button to create a new storage bucket to store your static website files.<img width="1920" alt="Screenshot 2024-05-11 at 08 10 35" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/4b5367dd-18dd-48c0-8b32-491945704515">
c) Enter a bucket name, untick the checkbox for Block all public access, and make sure to check the I acknowledge… <img width="1920" alt="Screenshot 2024-05-11 at 08 11 54" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/0ed922da-58b2-4da5-aa62-f3c0f1740b09">
d) Leave all other settings intact & click on the Create bucket button at the bottom of the page.<img width="1920" alt="Screenshot 2024-05-11 at 08 12 18" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/5dd0c6d6-020a-4733-8339-e717a8ca18cb">

<p>Step 2 - Upload Website files to S3 Bucket </p>
a) After creating a new bucket, click on the bucket name to view the bucket details.<img width="1920" alt="Screenshot 2024-05-11 at 08 17 16" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/97bb3f90-f825-4eca-ac8b-e23c2422d7b4">
b) When you create a new bucket it will be always empty. Click on the Upload button to upload some files.
<img width="1920" alt="Screenshot 2024-05-11 at 08 17 24" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/49519145-3c3a-43db-90b7-ddb85e288bfb">
c) On the File Upload page, click on the Add files to add a file from your computer, or Add folder to add multiple files from a folder.<img width="1920" alt="Screenshot 2024-05-11 at 08 19 44" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/0e6fc155-1ffd-42ef-afc4-705c95c03734">
d) Leave all other settings intact, scroll to the bottom of the page and click on the Upload button to start the uploading of the files you have added above.<img width="1920" alt="Screenshot 2024-05-11 at 08 20 14" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/e4d2748d-b3d0-4d18-9b23-964bfc0150c3">
e) Depending on your network connection and the number of files, you will have to wait while the files are being uploaded to the S3 Bucket.<img width="1920" alt="Screenshot 2024-05-11 at 08 20 20" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/e9d29d49-0f69-4021-8684-ebf157cabadd">
<p>Step 3 - Enabling Static Website Hosting on S3 Bucket</p>
a) On the Bucket overview page, click on the Properties tab and scroll down.<img width="1920" alt="Screenshot 2024-05-11 at 08 24 42" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/42847b08-5201-4292-9b18-8c89369c1e7b">
b) Look for Static website hosting section and click on the Edit button.

c) Select Enable option for Static website hosting setting and you will be presented with more options as the following screenshot.<img width="1920" alt="Screenshot 2024-05-11 at 08 25 02" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/a497f72e-4b5a-45a5-ba38-98a5e5d21338">
Hosting type: Select Host a static website and save changes.
<p>Step 4 - Add a Bucket Policy</p>
a) On the Bucket overview page, click on the Permissions tab, scroll down and look for Bucket policy section.<img width="1920" alt="Screenshot 2024-05-11 at 08 34 57" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/c1cd0d0b-3242-4aff-baa2-bd9e7ac23237">
b) On the Bucket policy section, click on the Edit button.

c) To grant public read access for your website on this bucket, copy the following bucket policy, and paste it in the Bucket policy editor below.<img width="1920" alt="Screenshot 2024-05-11 at 08 38 05" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/68d63dbb-9f74-4742-b8ff-8f1a6081c8ab">
e) You should now be able to access your website via the Amazon S3 Endpoint on the internet via thr URL in the properties tab.<img width="1920" alt="Screenshot 2024-05-11 at 08 41 01" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/7dd19175-6097-4f7d-96cc-72f72ff2a326">
<p>Step 5 - Creating a CloudFront Distribution</p>
a) From the top navigation under Services > All Services, search for “CloudFront” and click on it.<img width="1920" alt="Screenshot 2024-05-11 at 08 59 49" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/a3d9529c-03e8-4f59-8d31-b9a12593eb1f">
b) On the CloudFront Distributions page, click on the Create distribution button.
On the Create distribution page > under Origin section > for Origin domain > enter the Amazon S3 static website endpoint from earlier.<img width="1920" alt="Screenshot 2024-05-11 at 09 04 19" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/afe2a697-4171-41c7-9e23-26d1947c9377">

c) Enter “index.html” for Default root object. This file name must match with the index document file name entered previously on S3.<img width="1920" alt="Screenshot 2024-05-11 at 09 05 01" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/4fa4dc21-b604-4925-a47b-179abe4bbd3c">
d) Leave other settings intact. Scroll to the bottom and click on the Create distribution button.CloudFront will now distribute all your files to edge locations around the world. This process will take some time to complete.<img width="1920" alt="Screenshot 2024-05-11 at 09 05 35" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/43b15051-14ac-4957-be2c-945b5752cb4b">
e) Once Status has updated to Enabled, the distribution is ready to be accessed.
f) The URL for the distribution can be found under the Domain name column. For example: [d2liqy50s69x6u.cloudfront.net] Hopefully, you will see your static website by accessing this URL on your web browser.
<img width="1920" alt="Screenshot 2024-05-11 at 09 11 38" src="https://github.com/blvckbubba/blvckbubba/assets/145864600/97403b0c-2f7d-41a3-bc01-9d158aabb7dc">

