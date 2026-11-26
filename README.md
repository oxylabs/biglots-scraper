# Biglots Scraper API

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.io/pages/gitoxy?utm_source=github&utm_medium=referral&utm_content=biglots-scraper&utm_campaign=banner&groupid=877)

<p align="left">
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%9A%80_Get_Started-FF6B35?style=for-the-badge" alt="Get started"></a>
  <a href="https://developers.oxylabs.io/products/web-api"><img src="https://img.shields.io/badge/%F0%9F%93%9A_Documentation-4A90E2?style=for-the-badge" alt="Documentation"></a>
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%93%8A_Dashboard-2EA44F?style=for-the-badge" alt="Dashboard"></a>
  <a href="https://discord.gg/Pds3gBmKMH"><img src="https://img.shields.io/badge/%F0%9F%92%AC_Discord-5865F2?style=for-the-badge" alt="Discord"></a>
  <a href="https://www.youtube.com/@oxylabs"><img src="https://img.shields.io/badge/%E2%96%B6%EF%B8%8F_YouTube-FF0000?style=for-the-badge" alt="YouTube"></a>
</p>

Oxylabs' [Biglots Scraper](https://oxylabs.io/products/scraper-api/ecommerce/biglots?utm_source=github&utm_medium=referral&utm_content=biglots-scraper&groupid=877) is a data gathering solution allowing you to extract real-time information from an Biglots website effortlessly. This brief guide showcases how Biglots Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Biglots results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Biglots page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
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
      "created_at": "2025-02-20 12:15:54",
      "updated_at": "2025-02-20 12:15:57",
      "page": 1,
      "url": "https://www.biglots.com/c/furniture/office-furniture/_/n-916368633?scm=furniture_jas23_viznav_inspo_office",
      "job_id": "7165680462608747521",
      "status_code": 200
    }
  ]
}
```
With our Biglots Scraper, you can seamlessly harvest public data from any Biglots webpage. You can gather essential product specifics like price, customer testimonials, or descriptions to monitor the market and outshine your competition. If any queries arise, feel free to get in touch with our responsive support team via the live-chat feature or drop us an email at support@oxylabs.io.

