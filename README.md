# Lazada Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs’ [Lazada Scraper](https://oxylabs.io/products/scraper-api/ecommerce/lazada?utm_source=github&utm_medium=repositories&utm_campaign=product) (a part of Web Scraper API) is a data gathering solution allowing you to extract real-time information from an Lazada website effortlessly. This brief guide explains how an Lazada Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Lazada results by providing your own URLs to our service. We can return the HTML for any Lazada page you like.

#### Python code example

The example below illustrates how you can get HTML of Lazada page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.lazada.com.ph/'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/lazada-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html><head><script type=\"text/javascript\" async=\"\" src=\"//g.lazcdn.com/g/lzdmod/im/5 ... </html>",
      "created_at": "2023-12-18 10:29:11",
      "updated_at": "2023-12-18 10:29:44",
      "page": 1,
      "url": "https://www.lazada.com.ph/",
      "job_id": "7142460784642125825",
      "status_code": 200
    }
  ]
}
```
With our Lazada Scraper, you can seamlessly procure public data from any Lazada webpage. Gather important product information, such as brands, item availability, or shipping details, for understanding the market dynamics and outperforming your rivals. Should you have any queries, feel free to reach out to our support team through live chat or email us at hello@oxylabs.io.
