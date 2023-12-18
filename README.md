# Adidas Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Adidas Scraper](https://oxylabs.io/products/scraper-api/ecommerce/adidas?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Adidas website effortlessly. This brief guide explains how an Adidas Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Adidas results by providing your own URLs to our service. We can return the HTML for any Adidas page you like.

#### Python code example

The example below illustrates how you can get HTML of Adidas page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.adidas.com/us/under_100-shoes'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/adidas-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\" class=\"theme-adidas\" prefix=\"og: http://ogp.me/ns# fb: http://ogp.me/ ... </html>",
      "created_at": "2023-12-18 10:26:29",
      "updated_at": "2023-12-18 10:26:32",
      "page": 1,
      "url": "https://www.adidas.com/us/under_100-shoes",
      "job_id": "7142460105970199553",
      "status_code": 200
    }
  ]
}
```
With our Adidas Scraper, you can conveniently pull public data from any Adidas web page. Gather the necessary product details, such as sports apparel pricing, customer feedback, or athletic footwear descriptions, to examine the marketplace and maintain a competitive edge. If you need help, reach out to our support team through live chat or send us an email at hello@oxylabs.io.