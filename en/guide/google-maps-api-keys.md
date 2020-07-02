# Google Maps API Keys

## Setup

- Goto https://console.cloud.google.com and login with your Google Account or create an account.
- Create a Project on Google Cloud Console.
- Enable the following API's on your project:

```Geocoding API
Maps Javascript API
Places API
Maps Elevation API
Maps Static API
GeoLocation API
```

- You will have to setup the Google Billing account as well.
- From the Left menu, goto API & Services > Credentials and click on `Create Credentials`
- Create a Key named HTTP Key and under the website restrictions tab add your website URL like the following

<div class="Alert Alert--nuxt-green">
If your website is my-domain.com add these:
https://my-domain.com/* and https://www.my-domain.com/*
</div>

- Create another key named IP Key and under the IP Addresses section paste your website/server IP address.

<div class="Alert Alert--nuxt-green">
Goto https://www.ipvoid.com/find-website-ip and find your website's IP address
</div>

## Very Important

<div class="Alert Alert--nuxt-green">
Sometimes you will be shown a error message like:
Geocoding failed because `This IP, site or mobile application is not authorized to use this API Key. Request received from IP address *.*.*.* with empty referer.
The *.*.*.* is your server's IP address which need to be set on the IP Restricted key. Go back to the Google Cloud Console and set this IP Address provided on the error.
</div>

- Save all the changes and navigate to the api folder and inside .env file insert both keys

<div class="Alert Alert--nuxt-green">
Google API's takes 5-10 minutes to reflect the changes on your website.
</div>

## Important Links

- https://console.cloud.google.com
- https://cloud.google.com/maps-platform
- https://www.ipvoid.com/find-website-ip
