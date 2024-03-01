# HOSTING A STATIC WEBSITE WITH AMAZON S3


## Static websites have fixed content with no backend processing. They can contain HTML pages, images, style sheets, and all files that are needed to render a website. However, static websites do not use server-side scripting or a database. If you want your static webpages to provide interactivity and run programming logic, you can use JavaScript that runs in the user's web browser. 
You can easily host a static website on Amazon Simple Storage Service (Amazon S3) by uploading the content and making it publicly accessible. No servers are needed, and you can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere on the web. 

 

### SERVICES USED: 

- Amazon S3 Bucket 


## CREATE A BUCKET IN AMAZON S3 
 

- In the AWS Management Console, on the Services menu, choose S3. Choose Create bucket 
 
- An S3 bucket name is globally unique, and the namespace is shared by all AWS accounts. After you create a bucket, the name of that bucket cannot be used by another AWS account in any AWS Region unless you delete the bucket. 
 
- Public access to buckets is blocked by default. Because the files in your static website will need to be accessible through the internet, you must permit public access. 
 
- In the Object Ownership section, select ACLs enabled, then verify Bucket owner preferred is selected. 
 
- Clear Block all public access, then select the box that states I acknowledge that the current settings may result in this bucket and the objects within becoming public. Choose Create bucket. 
 
- Choose the name of your new bucket. Choose the Properties tab. Scroll to the Tags panel. Choose Edit then Add tag and enter: 
```
Key: Department 
Value: Marketing 
Choose Save changes to save the tag.
```
 
 
 
 
 
 
 
 ## CONFIGURE THE BUCKET FOR STATIC WEBSITE HOSITING
 

- In the Properties console scroll to the Static website hosting panel. 
- Choose Edit 
- Configure the following settings:
 ``` 
Static web hosting: Enable 
Hosting type: Host a static website 
Index document: index.html 
Note: You must enter this value, even though it is already displayed. Error document: error.html
```
- Choose Save changes. 
 
In the Static website hosting panel, choose the link under Bucket website endpoint. 
You will receive a 403 Forbidden message because the bucket permissions have not been configured yet. Keep this tab open in your web browser so that you can return to it later. 
Your bucket has now been configured to host a static website. 
 
 

## UPLOAD WEBSITE CONTENT TO YOUR BUCKET  
 

- Return to the Amazon S3 console and in the bucket, you created earlier, choose the Objects tab. 

- Choose Upload. Choose Add files. Locate all the files for your website that you want to upload.  
After selecting all the files you would like to upload, choose Upload. After all files are uploaded, select close. 

 

 

## ENABLE PUBLIC ACCESS TO THE BUCKET OBJECTS 

- All the objects (files) that you uploaded in your S3 Bucket are private by default. 

To make these objects accessible to the public: 

- Select all the uploaded objects. Go to the actions dropdown menu and choose Make public via ACL.  

- Choose Make public. Now your Static website is public. To access to URL for the website go to the Properties tab, and in the Static website hosting panel choose the Endpoint link and open in a new tab browser. 

 

 
