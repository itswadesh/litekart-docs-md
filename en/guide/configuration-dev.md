---
title: Configuration
description: By default, Litekart is configured to cover most use cases. This default configuration can be overwritten by using the files inside config directory.
---

> By default, Litekart is configured to cover most use cases. This default configuration can be overwritten by using the files inside config directory.

## Client Settings

### Client Secrets (Must be changed)

Path: <em>.env</em>

```js
HTTP_ENDPOINT=http://localhost:7700
WS_ENDPOINT=ws://localhost:7700
GOOGLE_MAPS_API_KEY=AIzaSyCYDdBORAAuErqPZ8LomCSr-REST_OF_YOUR_GOOGLE_MAPS_API_KEY
ONESIGNAL_APP_ID=cb37a0dc-REST_OF_YOUR_ONESIGNAL_APP_ID
STRIPE_PUBLISHABLE_KEY=pk_test_REST_OF_YOUR_STRIPE_PUBLISHABLE_KEY
WEBSITE_NAME=Litekart
GOOGLE_ANALYTICS_ID=
```

### General Variables (Optional)

Path: <em>shared/config/index.js</em>

```js
export const typingTimeout = 200; // After this delay the search api will be fired
export const loadingTimeout = 500; // Loading indicator will be shown after this delay // used at Loading.vue of admin

export const { HTTP_ENDPOINT = "https://gapi.litekart.in" } = process.env;

export const { WS_ENDPOINT = "wss://gapi.litekart.in" } = process.env;

export const { GOOGLE_ANALYTICS_ID = "UA-49421899-13" } = process.env;

export const { STRIPE_PUBLISHABLE_KEY = "pk_test_" } = process.env;

export const { ONESIGNAL_APP_ID = "" } = process.env;

export const { GOOGLE_MAPS_API_KEY = "" } = process.env;

export const { WEBSITE_NAME = "Litekart" } = process.env;

export const HEAD = {
  titleTemplate: `%s - ${WEBSITE_NAME}`,
  htmlAttrs: { lang: "en" },
  meta: [
    { charset: "utf-8" },
    {
      name: "viewport",
      content: "width=device-width, initial-scale=1, user-scalable=no",
    },
    { "http-equiv": "x-ua-compatible", content: "ie=edge" },
  ],
  link: [
    { rel: "icon", type: "image/x-icon", href: "favicon.ico" },
    {
      rel: "stylesheet",
      href: "https://fonts.googleapis.com/css?family=Nunito&display=swap",
    },
  ],
};
```

## Server Configurations

### Server Secrets (Must be updated)

```js
MONGO_INITDB_ROOT_USERNAME=root
MONGO_INITDB_ROOT_PASSWORD=secret
MONGO_INITDB_DATABASE=litekart-gro

MONGO_USERNAME=admin
MONGO_PASSWORD=secret
MONGO_DATABASE=litekart-gro

SESSION_SECRET=ssh!secret!

REDIS_PASSWORD=secret

APP_PORT=7700
APP_ORIGIN=http://localhost:7777

FACEBOOK_APP_ID=
FACEBOOK_APP_SECRET=

GOOGLE_CLIENT_ID=
GOOGLE_CLIENT_SECRET=

OPENCAGE_KEY=
GOOGLE_MAPS_KEY=

STRIPE_SECRET_KEY=
RAZORPAY_KEY_ID=
RAZORPAY_KEY_SECRET=

SENDGRID_API_KEY=
FAST2SMS_KEY=
FAST2SMS_SENDER_ID=FSTSMS
TWILIO_ACCOUNT_SID=
TWILIO_AUTH_TOKEN=

SENTRY_DNS=
```

### User roles

```js
userRoles: ['user', 'vendor', 'delivery', 'manager', 'admin'], // This should be in ascending order of authority. e.g. In this case guest will not have access to any other role, where as admin will have the role of guest+user+vendor+delivery+manager+admin
```

### Store settings

```js
export const SHOP_NAME = "Litekart";

export const PAY_MESSAGE = "Payment for grocery @ " + SHOP_NAME;

export const ORDER_PREFIX = "L";

export const STATIC_PATH = "./../grocery-assets";

export const SEED_DATABASE = true; // It consumes huge memory and throws out of memory exception. Seeds database with some demo data when the database is empty.

export const UPLOAD_DIR = "/images/";

export const FROM_TWILIO_PHONE_NUMBER = "+15005550006";

export const FAST2SMS_TEMPLATE_ID = 1372;

// Store delivery time configuration
export const startT = { h: 8, m: 0 };
export const start = "10:00 pm";
export const endT = { h: 6, m: 0 };
export const end = "06:00 am";

export const closed = {
  from: { hour: 13, minute: 44 },
  to: { hour: 13, minute: 59 },
  message: "Sorry we are closed from 1:44 PM to 1:59 PM",
};
// prettier-ignore
export const userRoles = ['user', 'delivery', 'vendor', 'manager', 'admin'] // This should be in ascending order of authority. e.g. In this case guest will not have access to any other role, where as admin will have the role of guest+user+vendor+manager+admin

export const language = "en";
// prettier-ignore
export const worldCurrencies = ['AED', 'AFN', 'ALL', 'AMD', 'ANG', 'AOA', 'ARS', 'AUD', 'AWG', 'AZN', 'BAM', 'BBD', 'BDT', 'BGN', 'BHD', 'BIF', 'BMD', 'BND', 'BOB', 'BOV', 'BRL', 'BSD', 'BTN', 'BWP', 'BYN', 'BZD', 'CAD', 'CDF', 'CHE', 'CHF', 'CHW', 'CLF', 'CLP', 'CNY', 'COP', 'COU', 'CRC', 'CUC', 'CVE', 'CZK', 'DJF', 'DKK', 'DOP', 'DZD', 'EGP', 'ERN', 'ETB', 'EUR', 'FJD', 'FKP', 'GBP', 'GEL', 'GHS', 'GIP', 'GMD', 'GNF', 'GTQ', 'GYD', 'HKD', 'HNL', 'HRK', 'HTG', 'HUF', 'IDR', 'ILS', 'INR', 'IQD', 'IRR', 'ISK', 'JMD', 'JOD', 'JPY', 'KES', 'KGS', 'KHR', 'KMF', 'KPW', 'KRW', 'KWD', 'KYD', 'KZT', 'LAK', 'LBP', 'LKR', 'LRD', 'LSL', 'LYD', 'MAD', 'MDL', 'MGA', 'MKD', 'MMK', 'MNT', 'MOP', 'MRU', 'MUR', 'MVR', 'MWK', 'MXN', 'MXV', 'MYR', 'MZN', 'NAD', 'NGN', 'NIO', 'NOK', 'NZD', 'OMR', 'PAB', 'PEN', 'PGK', 'PHP', 'PKR', 'PLN', 'PYG', 'QAR', 'RON', 'RSD', 'RUB', 'RWF', 'SAR', 'SBD', 'SCR', 'SDG', 'SEK', 'SGD', 'SHP', 'SLL', 'SOS', 'SRD', 'SSP', 'STN', 'SVC', 'SYP', 'SZL', 'THB', 'TJS', 'TMT', 'TND', 'TOP', 'TRY', 'TTD', 'TWD', 'TZS', 'UAH', 'UGX', 'USD', 'USN', 'UYI', 'UYU', 'UZS', 'VEF', 'VND', 'VUV', 'WST', 'XAF', 'XCD', 'XDR', 'XOF', 'XPF', 'XSU', 'XUA', 'YER', 'ZAR', 'ZMW', 'ZWL']

export const sorts = [
  { name: "Relevance", val: null },
  { name: "Whats New", val: "-createdAt" },
  { name: "Price low to high", val: "price" },
  { name: "Price high to low", val: "-price" },
];
export const paymentStatuses = ["pending", "cancelled", "paid"];
export const orderStatuses = [
  {
    status: "Waiting for confirmation",
    title: "Order Placed Successfully",
    body: "Waiting for the vendor to confirm the order",
    icon: "/images/order/order.png",
    public: true,
    index: 1,
  },
  {
    status: "Packed",
    title: "Package is Ready!!",
    body: "Your order is ready for pickup",
    icon: "/images/order/package.png",
    public: true,
    index: 2,
  },
  {
    status: "Out for delivery",
    title: "Vroom Vroom!!",
    body: "Order has been picked up and on the way",
    icon: "/images/order/delivery-boy.png",
    public: true,
    index: 3,
  },
  {
    status: "Delivered",
    title: "Order Delivered",
    body: "The order has been delivered to you",
    icon: "/images/order/delivered.png",
    public: true,
    index: 4,
  },
  {
    status: "Payment Pending",
    title: "Payment Pending",
    body: "Payment for order is pending",
    icon: "/images/order/shopping-bag.png",
    public: false,
    index: 5,
  },
  {
    status: "NIS",
    title: "Not in stock",
    body: "Item is out of stock and could not delivered",
    icon: "/images/order/shopping-bag.png",
    public: false,
    index: 6,
  },
  {
    status: "Cancelled",
    title: "Order Cancelled",
    body: "Order cancelled by user",
    icon: "/images/order/shopping-bag.png",
    public: false,
    index: 7,
  },
];
// prettier-ignore
export const timesList = ['1 AM', '2 AM', '3 AM', '4 AM', '5 AM', '6 AM', '7 AM', '8 AM', '9 AM', '10 AM', '11 AM', '12 PM', '1 PM', '2 PM', '3 PM', '4 PM', '5 PM', '6 PM', '7 PM', '8 PM', '9 PM', '10 PM', '11 PM', '12 AM']
```

### Menu Items (Used at left menu of admin panel)

```js
[
  {
    icon: "store",
    title: "Catalogue",
    items: [
      {
        title: "Products",
        href: "/products",
        icon: "store",
        authenticate: "manager",
        color: "black",
        dashboard: true,
      },
      {
        title: "Categories",
        href: "/categories",
        icon: "store",
        authenticate: "manager",
        color: "black",
        dashboard: true,
      },
      {
        title: "Coupons",
        href: "/coupons",
        icon: "style",
        authenticate: "admin",
        color: "pink",
        dashboard: true,
      },
    ],
  },
  {
    icon: "local_shipping",
    title: "Transactions",
    items: [
      {
        title: "Orders",
        href: "/orders",
        icon: "store",
        authenticate: "manager",
        color: "black",
        dashboard: true,
      },
      {
        title: "Payments",
        href: "/payments",
        icon: "payment",
        authenticate: "admin",
        color: "red",
        dashboard: true,
      },
    ],
  },
  {
    icon: "email",
    title: "Email Templates",
    items: [
      {
        title: "Change Password",
        href: "/emails/user/change-password",
        icon: "store",
        authenticate: "manager",
        color: "black",
        dashboard: true,
      },
      {
        title: "Order Created",
        href: "/emails/order/created",
        icon: "stars",
        authenticate: "vendor",
        color: "blue",
        dashboard: true,
      },
      {
        title: "Order Updated",
        href: "/emails/order/updated",
        icon: "style",
        authenticate: "admin",
        color: "pink",
        dashboard: true,
      },
      {
        title: "Reset Password",
        href: "/emails/user/reset-password",
        icon: "style",
        authenticate: "admin",
        color: "pink",
        dashboard: true,
      },
      {
        title: "Reset",
        href: "/emails/user/reset",
        icon: "style",
        authenticate: "admin",
        color: "pink",
        dashboard: true,
      },
    ],
  },
  {
    icon: "settings",
    title: "Settings",
    items: [
      {
        title: "Store",
        href: "/settings/store",
        authenticate: "admin",
        icon: "settings",
      },
      {
        title: "Banners",
        href: "/banners",
        icon: "burst_mode",
        authenticate: "manager",
        color: "yellow",
        dashboard: true,
      },
      {
        title: "Image",
        href: "/settings/image",
        authenticate: "admin",
        icon: "settings",
      },
      {
        title: "SEO",
        href: "/settings/seo",
        authenticate: "admin",
        icon: "settings",
      },
      {
        title: "SMS / Email",
        href: "/settings/email",
        authenticate: "admin",
        icon: "settings",
      },
      {
        title: "Payments",
        href: "/settings/payments",
        authenticate: "admin",
        icon: "settings",
      },
      {
        title: "Pages",
        href: "/pages",
        icon: "style",
        authenticate: "admin",
        color: "pink",
        dashboard: true,
      },
      {
        title: "Delivery Locations",
        href: "/cities",
        icon: "style",
        authenticate: "admin",
        color: "pink",
        dashboard: true,
      },
      {
        title: "Export",
        href: "/export",
        icon: "burst_mode",
        authenticate: "manager",
        color: "yellow",
        dashboard: true,
      },
    ],
  },
];
```
