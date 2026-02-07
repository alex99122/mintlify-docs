# Mannco.store API Documentation

This documentation covers the **API-only endpoints** of the Mannco.store platform.

## What's Included

This documentation includes **only** the endpoints that:
1. Have the `api` filter in the routing configuration
2. The `POST /user/login` endpoint for API key authentication

## Authentication

All API endpoints require authentication using an **API key**:

1. Obtain your API key from your Mannco.store account settings
2. Call `POST /user/login` with your API key to receive a JWT token
3. Use the JWT token for all subsequent API requests

## API Categories

- **Authentication** - API key login and JWT token management
- **Items** - Browse items, prices, listings, and buy orders
- **Inventory** - Manage your inventory on the platform
- **Trades** - View and manage Steam trades
- **Offers** - Create and manage trade offers between users
- **Buy Orders** - Create and manage buy orders for items
- **Deposit** - Deposit items from Steam to the platform
- **User Account** - Account information, balance, sessions
- **User Settings** - Manage account settings and preferences
- **Two-Factor Authentication** - Set up and manage 2FA
- **Email Management** - Change and validate email addresses
- **User History** - View transaction and activity history
- **Cashout** - Withdraw balance to payment providers
- **Payment** - Add balance to your account
- **Utilities** - Helper endpoints for validation and information
- **Public Data** - Access public pricing and market data

## Documentation Structure

```
mintlify-docs/
├── api-reference/
│   ├── introduction.mdx          # API overview and basics
│   ├── authentication.mdx         # API key authentication
│   ├── items.mdx                  # Item endpoints
│   ├── inventory.mdx              # Inventory management
│   ├── trades.mdx                 # Trade management
│   ├── offers.mdx                 # Offer system
│   ├── buyorders.mdx              # Buy order system
│   ├── deposit.mdx                # Item deposits
│   ├── user-account.mdx           # User account info
│   ├── user-settings.mdx          # User settings
│   ├── user-2fa.mdx               # Two-factor authentication
│   ├── user-email.mdx             # Email management
│   ├── user-history.mdx           # Transaction history
│   ├── cashout.mdx                # Balance withdrawal
│   ├── payment.mdx                # Payment deposits
│   ├── utils.mdx                  # Utility endpoints
│   └── public-data.mdx            # Public market data
├── docs.json                      # Mintlify navigation config
└── index.mdx                      # Documentation homepage

```

## Development

To view the documentation locally:

```bash
# Install Mintlify CLI
npm i -g mintlify

# Navigate to the docs directory
cd mintlify-docs

# Start the dev server
mintlify dev
```

The documentation will be available at `http://localhost:3000`.

## Deployment

This documentation is designed to be deployed with [Mintlify](https://mintlify.com/).

## Support

- **Website:** [mannco.store](https://mannco.store)
- **Discord:** Join our Discord community
- **Support Tickets:** Available through the website

## License

See LICENSE file for details.
