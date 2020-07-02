# Customizations

You get the fully working web app with Customer Application, Delivery Application, Admin, and Restaurant Dashboard with the Regular License. All the features mentioned in the Item's description will be available.
The only thing that is not shipped with the Regular License is the Editable Vue Source Code. i.e., You only get the production-ready compiled JavaScript code for the front-end (Vue - Customer, Vendor and Delivery Application). But you will get fully editable back-end codebase (NodeJS - Admin and Restaurant Dashboard).

With the Regular License; you will be able to edit the logos, favicons, splash-screens, store name, store currency, listing pageSize, Minimum order value, shipping charges etc. easily from the Admin Dashboard. But you won't be able to modify the layout or add your custom functions to the Customer or the Delivery Application.

## Change Store Name

```js
export const SHOP_NAME = 'Litekart'
```

## Change message during payment collection

```js
export const PAY_MESSAGE = 'Payment for grocery @ ' + SHOP_NAME
```

## Change Order Prefix

```js
export const ORDER_PREFIX = 'L'
```

## The path where all static files will be stored

```js
export const STATIC_PATH = './../grocery-assets'
```

## Whether to populate the database with some sample data for a fresh installation

```js
export const SEED_DATABASE = true // It consumes huge memory and throws out of memory exception. Seeds database with some demo data when the database is empty.
```

## The directory where all images will be stored

```js
export const UPLOAD_DIR = '/images/'
```

## Twillion phone number for sending SMS

```js
export const FROM_TWILIO_PHONE_NUMBER = '+15005550006'
```

## Defines when the store will be closed for order acceptance

```js
// Store delivery time configuration
export const startT = { h: 8, m: 0 }
export const start = '10:00 pm'
export const endT = { h: 6, m: 0 }
export const end = '06:00 am'
export const closed = {
  from: { hour: 13, minute: 44 },
  to: { hour: 13, minute: 59 },
  message: 'Sorry we are closed from 1:44 PM to 1:59 PM'
}
```

## User roles in ascending order of authority

```js
// prettier-ignore
export const userRoles = ['user', 'delivery', 'vendor', 'manager', 'admin'] // This should be in ascending order of authority. e.g. In this case guest will not have access to any other role, where as admin will have the role of guest+user+vendor+manager+admin
```

## Sort orders for listing page

```js
export const sorts = [
  { name: 'Relevance', val: null },
  { name: 'Whats New', val: '-createdAt' },
  { name: 'Price low to high', val: 'price' },
  { name: 'Price high to low', val: '-price' }
]
```

## Different payment statuses available for admin

```js
export const paymentStatuses = ['pending', 'cancelled', 'paid']
```

## Order status with image and description. Also used for push notifications

```js
export const orderStatuses = [
  {
    status: 'Waiting for confirmation',
    title: 'Order Placed Successfully',
    body: 'Waiting for the vendor to confirm the order',
    icon: '/images/order/order.png',
    public: true,
    index: 1
  },
  {
    status: 'Packed',
    title: 'Package is Ready!!',
    body: 'Your order is ready for pickup',
    icon: '/images/order/package.png',
    public: true,
    index: 2
  },
  {
    status: 'Out for delivery',
    title: 'Vroom Vroom!!',
    body: 'Order has been picked up and on the way',
    icon: '/images/order/delivery-boy.png',
    public: true,
    index: 3
  },
  {
    status: 'Delivered',
    title: 'Order Delivered',
    body: 'The order has been delivered to you',
    icon: '/images/order/delivered.png',
    public: true,
    index: 4
  },
  {
    status: 'Payment Pending',
    title: 'Payment Pending',
    body: 'Payment for order is pending',
    icon: '/images/order/shopping-bag.png',
    public: false,
    index: 5
  },
  {
    status: 'NIS',
    title: 'Not in stock',
    body: 'Item is out of stock and could not delivered',
    icon: '/images/order/shopping-bag.png',
    public: false,
    index: 6
  },
  {
    status: 'Cancelled',
    title: 'Order Cancelled',
    body: 'Order cancelled by user',
    icon: '/images/order/shopping-bag.png',
    public: false,
    index: 7
  }
]
```
