# Ebay Scraper

[![Oxylabs promo code](https://github.com/oxylabs/ebay-scraper/blob/main/19-Ebay-scraper.png)](https://oxylabs.io/pages/gitoxy?utm_source=877&utm_medium=affiliate&groupid=877&utm_content=ebay-scraper-github&transaction_id=102f49063ab94276ae8f116d224b67)

<p align="left">
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%9A%80_Get_Started-FF6B35?style=for-the-badge" alt="Get started"></a>
  <a href="https://developers.oxylabs.io/products/web-api"><img src="https://img.shields.io/badge/%F0%9F%93%9A_Documentation-4A90E2?style=for-the-badge" alt="Documentation"></a>
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%93%8A_Dashboard-2EA44F?style=for-the-badge" alt="Dashboard"></a>
  <a href="https://discord.gg/Pds3gBmKMH"><img src="https://img.shields.io/badge/%F0%9F%92%AC_Discord-5865F2?style=for-the-badge" alt="Discord"></a>
  <a href="https://www.youtube.com/@oxylabs"><img src="https://img.shields.io/badge/%E2%96%B6%EF%B8%8F_YouTube-FF0000?style=for-the-badge" alt="YouTube"></a>
</p>

[eBay Scraper](https://oxy.yt/Qapz) is a sophisticated solution designed to gather data from eBay website in real time and without a hassle. This quick guide will detail the process of scraping eBay using Oxylabs' Scraper API.

### How it works

You can get eBay results by providing your own URLs to our service. We can return the HTML, parsed JSON, or Markdown output of any eBay page you like.

#### Python code example

The example below illustrates how you can get an eBay product page result in HTML format.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.ebay.com/itm/293608130360',
    'geo_location': 'United States',
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

Find code examples for other programming languages [**here**](https://github.com/oxylabs/ebay-scraper/tree/main/code%20examples)

#### Output example

```json
{
    "results": [
        {
            "content":"<!doctype html>\n<html lang=\"en\">\n<head>
            ...
            </script></body>\n</html>\n",
            "created_at": "2022-11-17 14:53:52",
            "updated_at": "2022-11-17 14:53:54",
            "page": 1,
            "url": "https://www.ebay.com/itm/293608130360",
            "job_id": "6999021798385787905",
            "status_code": 200
        }
    ]
}
```

With Oxylabs’ eBay Scraper, publicly available data extraction will feel effortless. From product information to customer reviews – you’ll have all the data you need. If you have further queries, you can contact us via live chat or [email](mailto:support@oxylabs.io), and we’ll sort out your concerns in no time.

Also, check this tutorial on [pypi](https://pypi.org/project/Ebay-scraper-api/)
