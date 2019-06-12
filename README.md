# post-demo

## Step 1
Build a JSON proxy for SOAP endoint. This can be done by deploying the attached proxy or creating a new proxy with SOAP backend.

## Step 2
Invoke and test the JSON endpoint.
This is a GET call with required information passed in query parameters e.g.
```
https://{{org}}-{{env}}.apigee.net/foreignexchange/v1/productfxrates_v1?InterfaceName=getFx&InterfaceVersion=1.0&MessageType=Request&BusinessReferenceID=testgetFx001&SourceSystemID=Gateway&Timestamp=2019-05-31T00:00:00Z&OrganisationName=Access Prepaid Travel AOL
```

## Step 3
Create a secure endpoint. This will use API Key Verification.
This will require creation of API Products, Apps and Developers. Secure endpoint is `https://{{org}}-{{env}}.apigee.net/foreignexchange/v1/productfxrates_v2`

## Step 4
Create another secure endpoint. This will require a bearer token for authentcation.
Authentcation is oAuth password grant type.
User Store will OKTA. OKTA usernames are
- one.test@gmail.com
- two.test@gmail.com
- three.test@gmail.com
- four.test@gmail.com
- five.test@gmail.com

## Step 5
Invoke the token endpoint
```
https://{{org}}-{{env}}.apigee.net/oauth/token
```
get the token and invoke token secure endpoint `https://{{org}}-{{env}}.apigee.net/foreignexchange/v1/productfxrates_v3`

## Step 6
Create the dev portal and deploy the API proxy onto the dev portal
https://demo-au06-post.apigee.io
Try Out API from dev portal

## Step 7
Check Analtics information
