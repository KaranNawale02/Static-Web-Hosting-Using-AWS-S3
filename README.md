# Static-Web-Hosting-Using-AWS-S3
Static Web hosting using amazon web services S3 bucket. 

## Step 1 : Creating a S3 ucket

### To create a bucket
#### 1. Sign in to the AWS Management Console and open the Amazon S3 console at
#### 2. Choose Create bucket.
#### 3. Enter the Bucket name (for example, example.com).
#### 4. Choose the Region where you want to create the bucket.
      Choose a Region that is geographically close to you to minimize latency and costs,
      or to address regulatory requirements. The Region that you choose
      determines your Amazon S3 website endpoint. For more information, see Website endpoints.
#### 5. To accept the default settings and create the bucket, choose Create.


![log_ing](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/ca7c55f7-9f75-4b6e-9ce6-ce81fa515fb6)


![bucket created](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/2a92cf08-cc9b-48d7-aa5c-85ca64cb494f)


![create bucket 01](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/dae038bb-cb78-4619-a401-d2eb8d8f8c87)


![create bucket 02](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/8a9712b4-f808-4182-8104-6c4b76cc8a89)


![create bucket 03](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/72a5dbdf-2042-4ecd-89ad-0d75b741dae6)


![create bucket 04](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/1e01e9fe-2911-44a9-8f81-63e456d6161b)


![create bucket 05](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/86053baf-c5e0-4752-b735-80037cb25330)


![bucket created](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/e4bc737e-9352-4e31-bbe2-a1573a374609)

## Step 2: Enable static website hosting

### To enable static website hosting
#### 1. In the Buckets list, choose the name of the bucket that you want to enable static website hosting for.

   ![choose bucket](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/1aead793-132f-4c43-9739-22b3599b5378)
   

#### 3. Choose Properties.

   ![choose properties](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/bbd31f50-cab9-4176-9c2e-3691af165761)
   

#### 3.Under Static website hosting, choose Edit.

   ![select staic web hosting](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/88d46aca-2b0d-412f-882d-033a8020ae76)
   

#### 4. Choose Use this bucket to host a website.
#### 5. Under Static website hosting, choose Enable.

![enable hosting](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/1eeea03c-ca39-4a17-8ab8-9b32e814132e)


#### 7. In Index document, enter the file name of the index document, typically index.html.
   The index document name is case sensitive and must exactly match the file name of the HTML index document that you plan to upload to your S3 bucket. When you configure a bucket for website hosting, you     must specify an index document. Amazon S3 returns this index document when requests are made to the root domain or any of the subfolders
   
#### 8. (Optional) To provide your own custom error document for 4XX class errors, in Error document, enter the custom error document file name.
   The error document name is case sensitive and must exactly match the file name of the HTML error document that you plan to upload to your S3 bucket. If you don't specify a custom error document and an 
   error occurs, Amazon S3 returns a default HTML error document.
   
#### 9. (Optional) If you want to specify advanced redirection rules, in Redirection rules, enter JSON to describe the rules.
   For example, you can conditionally route requests according to specific object key names or prefixes in the request.
   
   ![option](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/8de93fdb-536c-49b5-b6c5-ff279db7e5ab)
   
   
#### 10. Choose Save changes.
   Amazon S3 enables static website hosting for your bucket. At the bottom of the page, under Static website hosting, you see the website endpoint for your bucket.

   ![select staic web hosting](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/ec5ba712-a2e2-4882-9619-84e45f69290a)
   

#### 12. Now scorll down and Under Static website hosting, note the Endpoint.
The Endpoint is the Amazon S3 website endpoint for your bucket. After you finish configuring your bucket as a static website, you can use this endpoint to test your website.

![note endpoints](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/e0ed4a6e-2dfe-42ba-beec-622074309057)


## Step 3: Edit Block Public Access settings
By default, Amazon S3 blocks public access to your account and buckets. If you want to use a bucket to host a static website, you can use these steps to edit your block public access settings.
#### 1. Choose the name of the bucket that you have configured as a static website.
#### 2. Choose Permissions.

![choose permission](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/580589ef-9287-41ca-9d9e-68b4b170cb7d)

#### 3. Under Block public access (bucket settings), choose Edit.

![permission edit](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/506ca5f5-1481-4bff-8f7d-9c250904df80)

#### 4. Clear Block all public access, and choose Save changes.

![permisson diselectt and save chanhes](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/8473170f-3322-4ea0-9b19-704da0a12ec2)


## Step 4: Add a bucket policy that makes your bucket content publicly available
#### 1. Under Buckets, choose the name of your bucket.
#### 2. Choose Permissions.
#### 3. Under Bucket Policy, choose Edit.

![bucket policy](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/472be58d-13de-4e12-a340-2de8b45d68b6)


#### 4. To grant public read access for your website, copy the following bucket policy, and paste it in the Bucket policy editor.
                        {
    "Version": "2012-10-17",
    "Statement": [
        {
            "Sid": "PublicReadGetObject",
            "Effect": "Allow",
            "Principal": "*",
            "Action": [
                "s3:GetObject"
            ],
            "Resource": [
                "arn:aws:s3:::Bucket-Name/*"
            ]
        }
    ]}


#### 5. Update the Resource to your bucket name.
In the preceding example bucket policy, Bucket-Name is a placeholder for the bucket name. To use this bucket policy with your own bucket, you must update this name to match your bucket name.


#### 6. Choose Save changes.
A message appears indicating that the bucket policy has been successfully added.
If you see an error that says Policy has invalid resource, confirm that the bucket name in the bucket policy matches your bucket name.
If you get an error message and cannot save the bucket policy, check your account and bucket Block Public Access settings to confirm that you allow public access to the bucket.


## Step 5: Configure an index document
When you enable static website hosting for your bucket, you enter the name of the index document (for example, index.html). After you enable static website hosting for the bucket, you upload an HTML file with this index document name to your bucket.

#### 1. Create an index.html file.
If you don't have html, css code then you can use my code also.

#### 2. Save the index file locally.

#### 3 In the Buckets list, choose the name of the bucket that you want to use to host a static website.

![choose bucket](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/1aead793-132f-4c43-9739-22b3599b5378)

#### 4. Enable static website hosting for your bucket, and enter the exact name of your index document (for example, index.html). 


#### 5. To upload the index document to your bucket, do one of the following:
a) Drag and drop the index file into the console bucket listing.
b) Choose Upload, and follow the prompts to choose and upload the index file.


#### 6. (Optional) Upload other website content to your bucket.

## Step 6: Test your website endpoint
At the bottom of the page, under Static website hosting, choose your Bucket website endpoint.

![final output 01](https://github.com/KaranNawale02/Static-Web-Hosting-Using-AWS-S3/assets/124289243/ca18fea1-3d3b-4855-9a5b-a7170b2710a1)


   

