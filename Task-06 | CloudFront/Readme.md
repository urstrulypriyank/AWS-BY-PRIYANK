# CloudFront (Similar to cloudFlare)
CloudFront is a CDN (Content delivery network) service provided by aws.
The goal of the service to improve the read response time 
Performace improvement is done by the help of serving data from edge locations
- The content is cached at edge location 

The edge location contain cache if hit serverd else served from the origin location

- Ideal for serving site frontend's static

***For Dynamic content cross region replication is a good way ***

## Origin of data can be in 
- ALB, EC2 ,S3 static site, Any Http backend
