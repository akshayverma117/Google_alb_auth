# Google_alb_auth
- Create a load balancer for redirection
- Create a target group and add required instances
- In AWS Cognito create a new User Pools
- Add email as required attribute
- Create a new app client
- add post authentication trigger as a lambda function for verifying certain domains
```sh
def lambda_handler(event, context):
    allowedDomains = ["ABC.com"]
    userDomain event['request']['userAttributes']['email'].split("@")[-1]
    #print userDomain
    if userDomain in allowedDomains:
        return event
    raise Exception("Domain not allowed")
```
- In identity provider as google
- add google app id
- app secret
- authorize scope
- profile email openid
- Create a new domain name
- checkbox google profile, email, openid
- made updates in the google auth 
