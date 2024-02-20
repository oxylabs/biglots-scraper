# Biglots Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Biglots Scraper](https://oxylabs.io/products/scraper-api/ecommerce/biglots?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Biglots website effortlessly. This brief guide showcases how Biglots Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Biglots results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Biglots page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.biglots.com/c/furniture/office-furniture/_/n-916368633?scm=furniture_jas23_viznav_inspo_office'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/biglots-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!doctype html>\n\t<!--[if (gt IE 9)|!(IE)]><!--><html class=\"no-js\" lang=\"en\"><!--<![endif]-->\n\t<head ... </html>",
      "created_at": "2024-02-20 12:15:54",
      "updated_at": "2024-02-20 12:15:57",
      "page": 1,
      "url": "https://www.biglots.com/c/furniture/office-furniture/_/n-916368633?scm=furniture_jas23_viznav_inspo_office",
      "job_id": "7165680462608747521",
      "status_code": 200
    }
  ]
}
```
With our Biglots Scraper, you can seamlessly harvest public data from any Biglots webpage. You can gather essential product specifics like price, customer testimonials, or descriptions to monitor the market and outshine your competition. If any queries arise, feel free to get in touch with our responsive support team via the live-chat feature or drop us an email at hello@oxylabs.io.