AWS Static Website Hosting On Amazon S3 Bucket With CloudFront 
This Terraform script automates the deployment of a static website on AWS, utilizing various AWS services. Below is an overview of the key components configured by this script:

AWS Provider Configuration:
Configures the AWS provider for the desired region (us-east-1 in this case).
Route 53 Hosted Zone:
Creates a Route 53 hosted zone for your domain (mystaticwebsiteproject.com).
ACM Certificate:
Requests an ACM (AWS Certificate Manager) certificate for your domain and its subdomains, utilizing DNS validation.
S3 Bucket:
Creates an S3 bucket with a specific name (s3bucket.mystaticwebsiteproject.com) to store and serve static website content.
CloudFront Distribution:
Sets up a CloudFront distribution with the S3 bucket as the origin, enhancing content delivery and providing a secure and scalable frontend.
Route 53 Record Sets:
Configures DNS records in Route 53 for your domain:
An A record pointing to the CloudFront distribution.
NS and SOA records for authoritative nameservers.
A CNAME record for ACM certificate validation.
A CNAME record for routing to the S3 bucket.
