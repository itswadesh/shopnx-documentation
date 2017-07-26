---
title: Server Settings
date: 2017-07-23 06:40:12
---
<p>Path: <em>server/config.ts</em></p>
### Website Settings
``` bash
smsEnabled = true;
emailEnabled = true;
  ```  
### Review Settings
``` bash
reviewSettings = {
  enabled: true, // Enables review for products
  moderate: false // If enabled, the review will be visible to public after admin approval
};
  ``` 
### Product Settings
``` bash
  product = { moderate: false };
  ``` 
### User Roles
``` bash
  userRoles = ['user', 'manager', 'admin']; // This should be in ascending order of authority. e.g. In this case guest will not have access to any other role, where as admin will have the role of guest+user+vendor+manager+admin
  ``` 
### Forgot Password Email Settings
``` bash
forgotPasswordEmail = (body) => { // Expects email id and password reset token
  return {
    from: 'passwordreset@codenx.com',
    to: body.email,
    subject: 'ShopNx Password Reset Request',
    text: 'You are receiving this because you (or someone else) have requested the reset of the password for your account.\n\n' +
    'Please click on the following link, or paste this into your browser to complete the process:\n\n' +
    process.env.DOMAIN + '/account/reset-password/' + body.token + '\n\n' +
    'If you did not request this, please ignore this email and your password will remain unchanged.\n'
  }
}
  ``` 
### Reset Password Email Settings
``` bash
resetPasswordEmail = (body) => { // Expects email id and name
  return {
    from: 'passwordreset@codenx.com',
    to: body.email,
    subject: 'ShopNx Password Changed',
    text: 'Hello,\n\n' +
    'This is a confirmation that the password for your account ' + body.to + ' has just been changed.\n'
  };
}
  ``` 
### Order Placed Email Settings
``` bash
orderPlacedEmail = (body) => { // Expects email id, orderNo, ...
  return {
    from: 'CodeNx <admin@codenx.com>',
    to: body.to,
    subject: 'Order Placed Successfully',
    text: 'Order No: ' + body.orderNo
    + '\n Status: ' + body.status
    + '\n\n Payment Method: ' + body.payment_method
    + '\n\n Payment ID: ' + body.id
    + '\n Amount: ' + body.amount.currency + ' ' + Math.round(body.amount.total * 100 / body.amount.exchange_rate) / 100
    + '\n\n Name: ' + body.address.recipient_name
    + '\n Address: ' + body.address.line1
    + '\n City: ' + body.address.city
    + '\n Zip: ' + body.address.postal_code
  };
}
  ``` 
### Order Updated Email Settings
``` bash
orderUpdatedEmail = (body) => {
  return {
    from: 'CodeNx <admin@codenx.com>',
    to: body.to,
    subject: 'Your Order Status Updated',
    text: 'Order No: ' + body.orderNo
    + '\n Status: ' + body.status
    + '\n\n Payment Method: ' + body.payment_method
    + '\n\n Payment ID: ' + body.id
    + '\n Amount: ' + body.amount.currency + ' ' + Math.round(body.amount.total * 100 / body.amount.exchange_rate) / 100
    + '\n\n \n Name: ' + body.address.recipient_name
    + '\n Address: ' + body.address.line1
    + '\n City: ' + body.address.city
    + '\n State: ' + body.address.state
    + '\n Zip: ' + body.address.postal_code
  };
}
  ``` 