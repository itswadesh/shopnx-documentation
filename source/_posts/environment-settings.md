---
title: Environment Settings
---
  Rename <em>.env.sample</em> to <em>.env</em> and change according to your generated credentials
  Generate the following APIs and input the credentials into .env file present at the root of the project

### Email Client
 [Sendgrid](http://www.sendgrid.com/)

### Payment Gateway 
 [Paypal Developer](http://developer.paypal.com/)

### Login through Facebook 
 [Facebook Developer](http://developer.facebook.com/)

### Google Auth Login 
 [Google Developer Console](http://developer.facebook.com/)

### Use twitter account to login to ShopNx 
 [Twitter Developer](https://dev.twitter.com/)
      

``` bash
MONGODB_URI=mongodb://localhost:27017/shopnx-dev
DOMAIN=http://localhost:4200
SESSION_SECRET=shopnx-secret
PAYPAL_MODE=sandbox
PAYPAL_CLIENT_ID=YOUR_PAYPAL_CLIENT_ID
PAYPAL_CLIENT_SECRET=YOUR_PAYPAL_CLIENT_SECRET
STRIPE_APIKEY=sk_test_REST_OF_YOUR_KEY
SENDGRID_APIKEY=YOUR_SENDGRID_API_KEY
FACEBOOK_ID=YOUR_FACEBOOK_ID
FACEBOOK_SECRET=YOUR_FACEBOOK_SECRET
TWITTER_ID=YOUR_TWITTER_ID
TWITTER_SECRET=YOUR_TWITTER_SECRET
GOOGLE_ID=YOUR_GOOGLE_ID
GOOGLE_SECRET=YOUR_GOOGLE_SECRET
GOOGLE_MAPS_API=YOUR_GOOGLE_MAPS_API
  ``` 