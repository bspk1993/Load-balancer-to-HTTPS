# Load-balancer-to-HTTPS

HTTP to HTTPS

req SSL certificate(free in AWS)

Req a public certificate

Your domain.com / www.yourdomain.com (recommended but optional)

Choose DNS validation

Click Request

Validate Domain ownership ACM will give CNAME record 

go to DNS provider
--> IF using Amazon Route 53 --> add record there
---> if using Godaddy --> add record there

After adding CNAME wait for 5-15 min

ELB--> ALB (which is needed) --> Click Listeners --> Add listerners --Choose protocol :HTTPS port 443 --> Choose your SSL certificate (from ACM) --->Select target group (same as HTTP) ---> save 

Redirect HTTP to HTTPS ---> Edit Rules ---> Change actions to port 443 redirect to HTTPS status code :301
