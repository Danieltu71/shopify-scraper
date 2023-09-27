# Shopify Scraper

[<u>Shopify
Scraper</u>](https://oxylabs.io/products/scraper-api/ecommerce/shopify-scraper)
is a scraping tool for simplified public Shopify data acquisition on a
large scale. Follow this quick tutorial to see the scraping process of
Shopify using Oxylabs’ [<u>Scraper
API</u>](https://oxylabs.io/products/scraper-api).

## How it works

To extract public Shopify data, simply send a request to our API with
the URLs you want to scrape, and you will receive the HTML of any
Shopify page.

### Python code example

This code sample makes a request to our API and retrieves the HTML of
the Shopify homepage:

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.shopify.com/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('USERNAME', 'PASSWORD'),  # Your credentials go here
    json=payload,
)

# Instead of response with job status and results URL, this will return the
# JSON response with results.
pprint(response.json())
```

Visit the
[<u>documentation</u>](https://developers.oxylabs.io/scraper-apis/e-commerce-scraper-api/all-domains)
for more details about the payload parameters.

### Output sample

```json
{
  "results": [
    {
      "content": "<!doctype html>\n<html lang=\"en\">\n<head>
      ...
      </script></body>\n</html>\n",
      "created_at": "2023-06-12 14:57:02",
      "updated_at": "2023-06-12 14:57:03",
      "page": 1,
      "url": "https://www.shopify.com/",
      "job_id": "7074036885059813377",
      "status_code": 200
    }
  ]
}
```

Oxylabs’ Shopify Scraper API eases the scraping process and allows you
to collect public information from any website built on the Spotify
platform. You can extract details like prices, products, descriptions,
availability, reviews, images, and much more. If you need assistance or
have any questions, feel free to contact us via [<u>live
chat</u>](https://oxylabs.io/) or
[<u>email</u>](mailto:support@oxylabs.io).
