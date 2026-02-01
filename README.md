# CardTrader API Skills

AI agent skills for working with the CardTrader REST API. Provides comprehensive guidance for marketplace operations, inventory management, order fulfillment, and wishlist management.

## Installation

Install this skill using the GitHub Copilot Skills CLI:

```bash
npx skills add Eomm/cardtrader-api-skills
```

This will add the CardTrader API skill to your local skills directory, making it available to your AI agent.

## What's Included

### `cardtrader-api`

A complete skill for interacting with CardTrader's trading card marketplace API.

**Capabilities:**
- **Marketplace Operations**: Search products, manage cart, purchase, create wishlists
- **Inventory Management**: List, create, update, and delete products (single and batch operations)
- **Order Management**: List orders, update status, ship orders, handle cancellations
- **Reference Data**: Access games, categories, expansions, blueprints, and properties
- **CSV Import/Export**: Bulk inventory operations via CSV files
- **CardTrader Zero**: Special handling for CardTrader Zero orders and inventory

**Response Examples**: Includes JSON response examples in `examples/` for common endpoints:
- `expansions.json` - Expansion/set listings
- `blueprints.json` - Card blueprint details with editable properties
- `wishlist.json` - Wishlist structure with items
- `marketplace-products.json` - Product search results

## Usage

Once installed, the skill automatically activates when you:
- Mention CardTrader API operations
- Ask about trading card marketplace integration
- Need to manage inventory or orders
- Want to search for cards or manage wishlists

**Example prompts:**
- "Search for Magic cards in the Core Set 2019 expansion"
- "How do I create a product listing for a Near Mint card?"
- "Show me how to process CardTrader Zero orders"
- "Bulk update my inventory prices using the API"

## API Configuration

To use the CardTrader API, you'll need:

1. **API Token**: Obtain from your [CardTrader profile settings](https://www.cardtrader.com/en/docs/api/full/reference)
2. **Base URL**: `https://api.cardtrader.com/api/v2`
3. **Authentication**: Bearer token in request headers

```bash
Authorization: Bearer [YOUR_AUTH_TOKEN]
```

## Rate Limits

- General endpoints: 200 requests per 10 seconds
- Marketplace products: 10 requests per second
- Job status checks: 1 request per second

## Documentation

The full API documentation is available at [CardTrader API Docs](https://www.cardtrader.com/en/docs/api/full/reference).

## License

MIT