# URL Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs’ [URL Scraper](https://oxylabs.io/products/scraper-api/web/url-scraper?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an URL website effortlessly. This brief guide explains how a URL Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get URL results by providing your own URLs to our service. We can return the HTML for any URL page you like.

#### Python code example

The example below illustrates how you can get HTML of [oxylabs.io/blog](https://oxylabs.io/blog) page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://oxylabs.io/blog'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/url-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\" /><meta name=\"viewport\" content=\"width=de ... </html>",
      "created_at": "2023-12-18 11:36:46",
      "updated_at": "2023-12-18 11:36:48",
      "page": 1,
      "url": "https://oxylabs.io/blog",
      "job_id": "7142477791164971009",
      "status_code": 200
    }
  ]
}
```
With our URL Scraper, you can seamlessly extract public data from any URL web page. Gather the specific data points you need, such as stock indices, trade volumes, or economic reports, to conduct your financial analysis and stay up-to-date on market trends. If you run into any issues or need assistance, don't hesitate to reach out to our support team through live chat or email us at support@finscraper.io.
