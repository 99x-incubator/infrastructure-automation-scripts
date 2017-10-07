# AWS
## 1. CloudFront Setup Template

This template will help you to easily host your website with your API. It will create a CloudFront distribution with S3 website bucket origin, API Gateway origin and Link with Route53 DNS record. SSL certificate will be appliled to the domain.

### How to use? 

1. Create a Hosted Zone 

[![image](https://user-images.githubusercontent.com/2338919/31308696-a4e2bdf6-ab98-11e7-90cd-3dc7b8bb4439.png)
](url)

2. Request a certificate for that domain and copy the certificate Arn

![image](https://user-images.githubusercontent.com/2338919/31308717-4ae1d21e-ab99-11e7-80cb-3a6dfd71dc0a.png)

3. Goto CloudFormation Service and create a new stack with CloudFrontSetup.yml

4. Fill in the required parameters and create the stack

![image](https://user-images.githubusercontent.com/2338919/31308798-8567de00-ab9a-11e7-9097-721cabb1af9e.png)

5. Once the template creation is successful (~15mins) goto S3 and find the S3 bucket with the given domain name. Upload your website code eg: AngularJS, ReactJS, etc...

### Outputs

1. S3 Butcket to upload website code
2. Link with API Gateway
3. Create CloudFront distribution with 1 & 2 Origins
4. Add SSL certificate to CloudFront distribution
5. Link Route53 domain to CloudFront

![image](https://user-images.githubusercontent.com/2338919/31308881-67d86944-ab9b-11e7-928b-b4053bb486e3.png)

Now you can visit your website! 

![image](https://user-images.githubusercontent.com/2338919/31308919-143a7ed4-ab9c-11e7-99ad-d6b4a2df94c9.png)



