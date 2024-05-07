# Dynamic Mockups API
<a href="https://dynamicmockups.com/?utm_source=github&utm_medium=readme&utm_campaign=mockup-generator-api" target="_blank">Dynamic Mockups</a> helps you auto-generate Mockups at Scale from Photoshop Templates via <a href="https://dynamicmockups.com/mockup-generator-api?utm_source=github&utm_medium=readme&utm_campaign=mockup-generator-api" target="_blank">API</a>

## Introduction

Dynamic Mockups API is a powerful tool for businesses that need to automate the creation of product mockups. It enables users to programmatically generate mockups from Photoshop files using smart objects, and offers a variety of features to customize these mockups according to specific needs.

## Key Features

- **Automation of Mockups**: Automatically replace smart objects in your Photoshop templates with new designs.
- **Bulk Processing**: Generate multiple mockups at once to save time and effort.
- **Customization**: Use features like transform perspectives (skew, distort, rotate) and blending modes to enhance your mockups.
- **Integration**: Easily integrate with popular eCommerce platforms like Etsy, Shopify, WooCommerce or custom App via API.

https://github.com/dynamicmockups/mockup-generator-api/assets/169197692/7ce68b15-d3ec-44aa-94ec-68060a4c5afe

## Getting Started

### Prerequisites

Before you begin, make sure you have:
- A valid Dynamic Mockups API key. You can get one for Free [here](https://docs.dynamicmockups.com/docs/how-to-get-api-key/).
- Photoshop files prepared with smart objects. Use this [example](https://app-dynamicmockups-production.s3.eu-central-1.amazonaws.com/public/DynamicMockupsPhotoshopTemplateExample.psd) as a referrence or use one of the mockups from our [Public Library](https://app.dynamicmockups.com/mockup-library).

### Configuration

Configure the API with your credentials:
```javascript
var headers = new Headers();
headers.append("X-API-KEY", "API_KEY");
headers.append("Accept", "application/json");

var requestOptions = {
  method: "POST",
  headers: headers,
};
```

### Usage

Here's a simple example of how to create a mockup:
```javascript
// Create a t-shirt mockup with Dynamic Mockups logo
await fetch('https://app.dynamicmockups.com/api/v1/renders', {
  method: "POSt",
  headers: {
    'content-type': 'application/json',
    'x-api-key': '38a429a1-659e:abad-9817fdf6d87e'
  },
  body: JSON.stringify({
    "mockup_uuid": "6308f2f7-80eb-42ab-a109-08a33e6dcc2d",
    "smart_objects": [{
      "uuid": "22ec3dec-4df8-4643-8c68-01b72fa506f5",
      "asset": {
        "url": "https://dynamicmockups.com/logo.png",
        "color": "#ffd667"
      }
    }]
  })
}).then((response) => response.json())
```

## Community
Join our <a href="https://join.slack.com/t/dynamicmockups/shared_invite/zt-2165e7s2a-sEo2vTTs22fL2tUZdNFUXg" target="_blank">Slack Community</a> where you can chat with other developers using the API, get help with the implementation or request additional features.

## Support
For support, you can reach out to our customer service team at support@dynamicmockups.com or visit our documentation page at <a href="https://docs.dynamicmockups.com/docs/intro/" target="_blank">Dynamic Mockups Documentation</a>.
