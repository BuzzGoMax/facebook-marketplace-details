[Facebook Marketplace Details](https://apify.com/data-slayer/facebook-marketplace-details?fpr=data)

Extract comprehensive Facebook Marketplace listing data without authentication or cookies. This scraper retrieves detailed product information, pricing, seller details, location data, and vehicle specifications directly from listing IDs — perfect for dropshippers who need fast, reliable access to marketplace inventory without the hassle of managing login credentials.

## Key Features

🔒 **Cookieless / No Login Required** - Access Facebook Marketplace listing data without authentication, cookies, or account credentials. Run scrapes at scale without worrying about session management or account restrictions.

📈 **Scalable Architecture** - Built to handle high-volume data extraction efficiently. Process multiple listing IDs in parallel to gather competitive intelligence and inventory data across entire marketplaces.

✅ **Rich Listing Data** - Capture complete listing details including title, description, pricing (formatted price and currency), condition, location (coordinates and postal codes), creation time, availability status, delivery options, and comprehensive vehicle specifications (make, model, odometer, transmission, fuel type, horsepower, exterior/interior colors).

⚡ **Fast & Reliable** - Optimized extraction engine delivers consistent results with minimal latency. Get the data you need to make sourcing decisions quickly and confidently.

📊 **Export-Ready Formats** - Download your extracted data in JSON, CSV, or Excel formats for immediate integration with inventory management systems, pricing tools, or analytics platforms.

## Use Cases

**Dropshippers & Resellers**: Identify underpriced inventory opportunities in local markets by extracting listing prices, conditions, and seller locations. Build a database of potential products to source, compare pricing across regions, and discover trending items with minimal upfront investment.

**Market Research Analysts**: Track pricing trends, inventory availability, and product conditions across Facebook Marketplace categories. Analyze vehicle specifications, seller types, and geographic distribution to understand market dynamics and competitive positioning.

**Lead Generation Specialists**: Extract seller contact opportunities and messaging availability from active listings. Build targeted outreach lists based on product categories, locations, and listing characteristics to connect buyers with sellers or offer value-added services.

## Inputs

| Field | Type | Description |
| --- | --- | --- |
| listingId | String | The unique Facebook Marketplace listing ID to fetch details for. Found in the listing URL (e.g., `1547618196594748` from `facebook.com/marketplace/item/1547618196594748/`) |

## Outputs

**Formats**: JSON, CSV, Excel

**Key Fields Extracted**:

- `id` - Unique listing identifier
- `marketplace_listing_title` - Product title
- `custom_title` - Seller's custom title
- `formatted_price` - Display price with currency symbol
- `listing_price` - Structured price object (amount, currency, offset)
- `condition` - Item condition (USED, NEW, etc.)
- `redacted_description` - Full product description
- `location_text` - Human-readable location
- `location` - Geographic coordinates (latitude, longitude) and postal code
- `creation_time` - Unix timestamp of listing creation
- `is_live` - Listing active status
- `is_sold` - Sale completion status
- `is_pending` - Transaction pending status
- `delivery_types` - Available delivery methods (IN_PERSON, SHIPPING)
- `messaging_enabled` - Whether buyer can message seller
- `vehicle_make_display_name` - Vehicle manufacturer (for vehicle listings)
- `vehicle_model_display_name` - Vehicle model
- `vehicle_odometer_data` - Mileage with unit (kilometers/miles)
- `vehicle_transmission_type` - Transmission type (AUTOMATIC, MANUAL)
- `vehicle_fuel_type` - Fuel type (PETROL, DIESEL, ELECTRIC)
- `vehicle_exterior_color` - Exterior color
- `vehicle_seller_type` - Seller classification (PRIVATE_SELLER, DEALER)
- `vehicle_specifications` - Detailed specs including horsepower, engine size, gas mileage
- `share_uri` - Direct link to listing

## How to Use

**Step 1**: Enter the target listing ID in the `listingId` input field. You can find this ID in the Facebook Marketplace listing URL (the numeric string after `/item/`).

**Step 2**: Click "Start" to run the scraper. The actor will fetch comprehensive listing details directly from Facebook's servers.

**Step 3**: Once complete, download your data in JSON, CSV, or Excel format from the dataset tab. Import directly into your inventory management system or analysis tools.

## Sample Output

```
{
  "id": "1547618196594748",
  "marketplace_listing_title": "2013 MINI Cooper",
  "custom_title": "2013 MINI cooper",
  "formatted_price": {
    "text": "AU$11,990"
  },
  "listing_price": {
    "amount": "11990.00",
    "currency": "AUD"
  },
  "condition": "USED",
  "redacted_description": {
    "text": "2013 R56 JCW, 192,000km on the clock, timing chain done 15000km ago..."
  },
  "location_text": {
    "text": "Clyde, VIC"
  },
  "location": {
    "latitude": -38.125305175781,
    "longitude": 145.36560058594,
    "reverse_geocode_detailed": {
      "country_alpha_two": "AU",
      "postal_code_trimmed": "3978"
    }
  },
  "creation_time": 1759872299,
  "is_live": true,
  "is_sold": false,
  "is_pending": true,
  "delivery_types": ["IN_PERSON"],
  "messaging_enabled": true,
  "vehicle_make_display_name": "MINI",
  "vehicle_model_display_name": "Cooper",
  "vehicle_odometer_data": {
    "unit": "KILOMETERS",
    "value": 192000
  },
  "vehicle_transmission_type": "AUTOMATIC",
  "vehicle_fuel_type": "PETROL",
  "vehicle_exterior_color": "black",
  "vehicle_seller_type": "PRIVATE_SELLER",
  "share_uri": "https://www.facebook.com/marketplace/item/1547618196594748/"
}
```

## 🧩 Other Facebook Actors by Data Slayer

| Actor | What it does | Link |
| --- | --- | --- |
| Facebook Page Details Scraper | Get full page profiles — followers, contact info, ratings | [Try it](https://apify.com/data-slayer/facebook-page-details) |
| Facebook Posts Scraper | Extract posts from any Facebook page | [Try it](https://apify.com/data-slayer/facebook-page-posts) |
| Facebook Group Posts Scraper | Extract posts from any public Facebook group | [Try it](https://apify.com/data-slayer/facebook-group-posts) |
| Facebook Reviews Scraper | Extract customer reviews from any Facebook page | [Try it](https://apify.com/data-slayer/facebook-page-reviews) |
| Facebook Page Search Scraper | Search and discover Facebook pages by keyword | [Try it](https://apify.com/data-slayer/facebook-search-pages) |
| Facebook People Search Scraper | Search and find Facebook profiles by keyword | [Try it](https://apify.com/data-slayer/facebook-search-people) |
| Facebook Events Scraper | Discover Facebook events by keyword search | [Try it](https://apify.com/data-slayer/facebook-search-events) |

## 💬 Feedback and Support

We actively maintain this actor and ship improvements based on user feedback. If you run into any issues or have ideas for new features:

- Create an issue on the Actor's **Issues tab** in Apify Console
- Rate the actor if it helped you — it helps others find it too
We typically respond within 24 hours.