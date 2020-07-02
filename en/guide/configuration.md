---
title: Configuration
description: By default, Litekart is configured to cover most use cases. This default configuration can be overwritten by using the files inside config directory.
---

> By default, Litekart is configured to cover most use cases. This default configuration can be overwritten by using the files inside config directory.

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

### General store settings

```js
export const language = 'en'
// prettier-ignore
export const worldCurrencies = ['AED', 'AFN', 'ALL', 'AMD', 'ANG', 'AOA', 'ARS', 'AUD', 'AWG', 'AZN', 'BAM', 'BBD', 'BDT', 'BGN', 'BHD', 'BIF', 'BMD', 'BND', 'BOB', 'BOV', 'BRL', 'BSD', 'BTN', 'BWP', 'BYN', 'BZD', 'CAD', 'CDF', 'CHE', 'CHF', 'CHW', 'CLF', 'CLP', 'CNY', 'COP', 'COU', 'CRC', 'CUC', 'CVE', 'CZK', 'DJF', 'DKK', 'DOP', 'DZD', 'EGP', 'ERN', 'ETB', 'EUR', 'FJD', 'FKP', 'GBP', 'GEL', 'GHS', 'GIP', 'GMD', 'GNF', 'GTQ', 'GYD', 'HKD', 'HNL', 'HRK', 'HTG', 'HUF', 'IDR', 'ILS', 'INR', 'IQD', 'IRR', 'ISK', 'JMD', 'JOD', 'JPY', 'KES', 'KGS', 'KHR', 'KMF', 'KPW', 'KRW', 'KWD', 'KYD', 'KZT', 'LAK', 'LBP', 'LKR', 'LRD', 'LSL', 'LYD', 'MAD', 'MDL', 'MGA', 'MKD', 'MMK', 'MNT', 'MOP', 'MRU', 'MUR', 'MVR', 'MWK', 'MXN', 'MXV', 'MYR', 'MZN', 'NAD', 'NGN', 'NIO', 'NOK', 'NZD', 'OMR', 'PAB', 'PEN', 'PGK', 'PHP', 'PKR', 'PLN', 'PYG', 'QAR', 'RON', 'RSD', 'RUB', 'RWF', 'SAR', 'SBD', 'SCR', 'SDG', 'SEK', 'SGD', 'SHP', 'SLL', 'SOS', 'SRD', 'SSP', 'STN', 'SVC', 'SYP', 'SZL', 'THB', 'TJS', 'TMT', 'TND', 'TOP', 'TRY', 'TTD', 'TWD', 'TZS', 'UAH', 'UGX', 'USD', 'USN', 'UYI', 'UYU', 'UZS', 'VEF', 'VND', 'VUV', 'WST', 'XAF', 'XCD', 'XDR', 'XOF', 'XPF', 'XSU', 'XUA', 'YER', 'ZAR', 'ZMW', 'ZWL']

// prettier-ignore
export const timesList = ['1 AM', '2 AM', '3 AM', '4 AM', '5 AM', '6 AM', '7 AM', '8 AM', '9 AM', '10 AM', '11 AM', '12 PM', '1 PM', '2 PM', '3 PM', '4 PM', '5 PM', '6 PM', '7 PM', '8 PM', '9 PM', '10 PM', '11 PM', '12 AM']
```

### Menu Items (Used at left menu of admin panel)

```js
;[
  {
    icon: 'store',
    title: 'Catalogue',
    items: [
      {
        title: 'Products',
        href: '/products',
        icon: 'store',
        authenticate: 'manager',
        color: 'black',
        dashboard: true
      },
      {
        title: 'Categories',
        href: '/categories',
        icon: 'store',
        authenticate: 'manager',
        color: 'black',
        dashboard: true
      },
      {
        title: 'Coupons',
        href: '/coupons',
        icon: 'style',
        authenticate: 'admin',
        color: 'pink',
        dashboard: true
      }
    ]
  },
  {
    icon: 'local_shipping',
    title: 'Transactions',
    items: [
      {
        title: 'Orders',
        href: '/orders',
        icon: 'store',
        authenticate: 'manager',
        color: 'black',
        dashboard: true
      },
      {
        title: 'Payments',
        href: '/payments',
        icon: 'payment',
        authenticate: 'admin',
        color: 'red',
        dashboard: true
      }
    ]
  },
  {
    icon: 'email',
    title: 'Email Templates',
    items: [
      {
        title: 'Change Password',
        href: '/emails/user/change-password',
        icon: 'store',
        authenticate: 'manager',
        color: 'black',
        dashboard: true
      },
      {
        title: 'Order Created',
        href: '/emails/order/created',
        icon: 'stars',
        authenticate: 'vendor',
        color: 'blue',
        dashboard: true
      },
      {
        title: 'Order Updated',
        href: '/emails/order/updated',
        icon: 'style',
        authenticate: 'admin',
        color: 'pink',
        dashboard: true
      },
      {
        title: 'Reset Password',
        href: '/emails/user/reset-password',
        icon: 'style',
        authenticate: 'admin',
        color: 'pink',
        dashboard: true
      },
      {
        title: 'Reset',
        href: '/emails/user/reset',
        icon: 'style',
        authenticate: 'admin',
        color: 'pink',
        dashboard: true
      }
    ]
  },
  {
    icon: 'settings',
    title: 'Settings',
    items: [
      {
        title: 'Store',
        href: '/settings/store',
        authenticate: 'admin',
        icon: 'settings'
      },
      {
        title: 'Banners',
        href: '/banners',
        icon: 'burst_mode',
        authenticate: 'manager',
        color: 'yellow',
        dashboard: true
      },
      {
        title: 'Image',
        href: '/settings/image',
        authenticate: 'admin',
        icon: 'settings'
      },
      {
        title: 'SEO',
        href: '/settings/seo',
        authenticate: 'admin',
        icon: 'settings'
      },
      {
        title: 'SMS / Email',
        href: '/settings/email',
        authenticate: 'admin',
        icon: 'settings'
      },
      {
        title: 'Payments',
        href: '/settings/payments',
        authenticate: 'admin',
        icon: 'settings'
      },
      {
        title: 'Pages',
        href: '/pages',
        icon: 'style',
        authenticate: 'admin',
        color: 'pink',
        dashboard: true
      },
      {
        title: 'Delivery Locations',
        href: '/cities',
        icon: 'style',
        authenticate: 'admin',
        color: 'pink',
        dashboard: true
      },
      {
        title: 'Export',
        href: '/export',
        icon: 'burst_mode',
        authenticate: 'manager',
        color: 'yellow',
        dashboard: true
      }
    ]
  }
]
```
