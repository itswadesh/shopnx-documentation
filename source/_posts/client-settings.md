---
title: Client Settings
date: 2017-07-24 06:40:12
---
### Path: 
<em>client/app/settings.ts</em>
### Enable / Disable demo mode
<p>Restricts users from saving data if enabled</p>
``` bash
  static demo: boolean = false;
  ```  
### List of order status for Order Management
``` bash
  static orderStatus: string[] = ['Payment Pending', 'Order Placed', 'Paid', 'Order Accepted', 'Order Executed', 'Shipped', 'Delivered', 'Not in Stock', 'Cancellation Requested', 'Cancelled'];
  ```  

### Enabled Payment Methods for ecommerce
``` bash
  static paymentMethods: any = ['PayPal', 'COD'];
  ```  
### Regional Settings
``` bash
  static country: any = { name: 'India', code: 'IN' };
    static currency: any = {
        symbol: 'Rs', //Required only for sort icons at homepage
        code: 'INR', // Shop currency
        paypal: 'USD',// Paypal currency code *** Please choose from https://developer.paypal.com/docs/classic/api/currency_codes/
        exchange_rate: '0.015' // Paypal currency code(USD) / Shop currency (INR) ***  exchange_rate should not be 0 else it will generate divided by 0 error
    };
  ```  
  <br/>
  <br/>
  <br/>
### Menu for Dashboad and Header
``` bash
  static menu: any[] = [
        { name: 'Products', url: '/admin/product', icon: 'store', authenticate: 'admin', color: 'black', dashboard: true },
        { name: 'My Orders', url: '/admin/my-orders', icon: 'watch_later', authenticate: 'user', color: 'grey', dashboard: true },
        { name: 'Manage Orders', url: '/admin/manage-orders', icon: 'history', authenticate: 'manager', color: 'orange', dashboard: true },
        { name: 'Address', url: '/admin/address', icon: 'location_city', authenticate: 'user', color: 'yellow', dashboard: true },
        { name: 'Reviews', url: '/admin/reviews', icon: 'stars', authenticate: 'manager', color: 'blue', dashboard: true },
        { name: 'My Reviews', url: '/admin/my-reviews', icon: 'star_rate', authenticate: 'user', color: 'green', dashboard: true },
        { name: 'My Wishlist', url: '/admin/wishlist', icon: 'favorite', authenticate: 'user', color: 'purple', dashboard: true },
        { name: 'Media Library', url: '/admin/media-library', icon: 'perm_media', authenticate: 'manager', color: 'teal', dashboard: true },
        { name: 'Brands', url: '/admin/brands', icon: 'wb_auto', authenticate: 'manager', color: 'purple', dashboard: true },
        { name: 'Categories', url: '/admin/categories', icon: 'view_comfy', authenticate: 'manager', color: 'light-blue', dashboard: true },
        { name: 'Features', url: '/admin/features', icon: 'check_circle', authenticate: 'manager', color: 'brown', dashboard: true },
        { name: 'Coupons', url: '/admin/coupons', icon: 'style', authenticate: 'admin', color: 'pink', dashboard: true },
        { name: 'Shippings', url: '/admin/shippings', icon: 'local_shipping', authenticate: 'admin', color: 'red', dashboard: true },
        { name: 'Users', url: '/admin/users', icon: 'face', img: 'auth.png', authenticate: 'admin', color: 'lime', dashboard: true },
        { name: 'Media Library', url: '/admin/media-library', authenticate: 'user', icon: 'perm_media' },
        { name: 'Profile', url: '/account/edit-profile', authenticate: 'user', icon: 'face' },
        { name: 'Change Password', url: '/account/change-password', authenticate: 'user', icon: 'lock' },
        { name: 'Logout', url: '/account/logout', authenticate: 'user', icon: 'vpn_key' },
    ];
  ```  
  <br/>
  <br/>
  <br/>
  <br/>
  <br/>
  <br/>
  <br/>
  <br/>