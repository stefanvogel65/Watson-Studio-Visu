# Create Web Page in Object Storage

The following steps can be followed in order to serve a static Web page through placing a file / files in Cloud Object Storage on IBM Cloud.

## Step 1: Create a COS Service

Login to IBM Cloud and create a Cloud Object Storage (COS) service, if not done already.

## Step 2: Create a COS bucket and upload a file

1.  In the resource list under "Storage" select the Cloud Object Storage service you created above.
1.  In the Buckets section, click Create bucket to create a new bucket.
1.  Under "Predefined Buckets" select "Quickly get started"
2.  Enter a meaningful name for the bucket and click Next
3.  Upload an index.html file. You might want to take this one: [index.html](index.html)
4.  Skip the "Test your bucket" step and click "View bucket configuration"

## Step 3: Publish the content

In order to allow public access to the files in the bucket, set the appropriate access policy.

In the Access policies section of your bucket, choose the Public access tab, set the Role for this bucket to Object Reader and click Create access policy.

<img src="https://user-images.githubusercontent.com/35991100/114985546-37e3f700-9e93-11eb-814c-1d69f4abce04.png" alt="drawing" width="75%"/>

Confirm to enable the public access policy.

Note that now all objects in the bucket are publically accessible.

# Step 4: View the content in a browser

In the list of object in the bucket, select the index.html to show its details. In the details Overview tab copy the public URL for the object.

<img src="https://user-images.githubusercontent.com/35991100/114986522-62827f80-9e94-11eb-8d8d-a5155d34a4ce.png" alt="drawing" width="75%"/>


You can share this URL and access the file's content in any browser.

## Outlook

You might want to update index.html and add additional files to enhance your public Web site.


