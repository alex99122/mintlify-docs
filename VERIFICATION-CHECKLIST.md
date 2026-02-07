# API Endpoints Verification Checklist

## Authentication
- [x] POST /user/login (API Key authentication)

## Items (10 endpoints)
- [x] GET /item/details/{item}
- [x] GET /item/salesGraph/{item}
- [x] GET /item/listing/count/{item}
- [x] GET /item/listing/count/{item}/{userid}
- [x] GET /item/listing/{item}
- [x] GET /item/listing/{item}/{userid}
- [x] GET /item/buyorderList/{item}
- [x] GET /item/pricing/{item}
- [x] GET /item/pricing/bulk
- [x] GET /item/details/fromid/{backpackid}
- [x] GET /item/cs/details/fromid/{backpackid}
- [x] GET /item/getRaffleItems

## Inventory (3 endpoints)
- [x] GET /inventory/onSale
- [x] GET /inventory/onInventory
- [x] POST /inventory/withdraw

## Trades (3 endpoints)
- [x] GET /trades/active
- [x] GET /trades/all
- [x] GET /trade/resend

## Offers (6 endpoints)
- [x] GET /offers/received
- [x] GET /offers/my
- [x] POST /offers/create
- [x] POST /offers/accept
- [x] POST /offers/decline
- [x] POST /offers/remove

## Buy Orders (5 endpoints)
- [x] POST /item/buyorder
- [x] POST /item/buyorder/update
- [x] POST /item/buyorder/remove
- [x] GET /user/buyorder/{item}
- [x] GET /user/getBuyorder

## Deposit (4 endpoints)
- [x] GET /deposit/{game}
- [x] GET /deposit/botList/{game}
- [x] GET /deposit/tradeStatus/{tradeid}
- [x] POST /deposit/setPriceForUpcomingTrade

## User Account (8 endpoints)
- [x] GET /user/disconnect
- [x] GET /user/disconnectSession/all
- [x] GET /user/disconnectSession/{id}
- [x] GET /user/infos
- [x] GET /user/balance
- [x] GET /user/ipList
- [x] GET /user/getContactMail
- [x] GET /user/notifications

## User Settings (5 endpoints)
- [x] POST /user/setMailNotification
- [x] POST /user/setMailNotificationStatus
- [x] POST /user/setPrivacySetting
- [x] POST /user/setTradeUrl
- [x] POST /user/updateShortUrl

## Two-Factor Authentication (4 endpoints)
- [x] GET /user/2FA/create
- [x] POST /user/2FA/validate
- [x] POST /user/reset2FA/ask
- [x] POST /user/reset2FA/validate

## Email Management (2 endpoints)
- [x] POST /user/email/change/request
- [x] POST /user/email/change/validate

## User History (8 endpoints)
- [x] GET /user/getSalesInfos
- [x] GET /user/getSalesChartInfos
- [x] GET /user/getBalanceHistory
- [x] GET /user/getPurchaseHistory
- [x] GET /user/getSalesHistory
- [x] GET /user/getCashoutHistory
- [x] GET /user/getTransactionHistory
- [x] GET /user/getTransactionDetails

## Cashout (1 endpoint)
- [x] POST /cashout/process

## Payment (1 endpoint)
- [x] POST /paiement/{provider}

## Utilities (3 endpoints)
- [x] GET /utils/tradeurlCheck
- [x] GET /utils/bots
- [x] GET /utils/infos

## Public Data (3 endpoints)
- [x] GET /public/price
- [x] GET /infos/prices/buyorderAndLowestSales
- [x] GET /public/sales

---

## Total Endpoints Documented: 66+

## Mapping from index.php to Documentation Files

### index.php line 14-25 → items.mdx
- Line 14: GET /item/details/$item
- Line 16: GET /item/salesGraph/$item  
- Line 17-18: GET /item/listing/count/$item (with optional userid)
- Line 19-20: GET /item/listing/$item (with optional userid)
- Line 21: GET /item/getRaffleItems
- Line 23: GET /item/buyorderList/$item
- Line 24: GET /item/pricing/bulk
- Line 25: GET /item/pricing/$item

### index.php line 30-34 → inventory.mdx
- Line 30: GET /inventory/onSale
- Line 32: GET /inventory/onInventory
- Line 34: POST /inventory/withdraw

### index.php line 37-43 → trades.mdx
- Line 37-38: GET /trades/active (with optional userid for admin)
- Line 39-40: GET /trades/all (with optional userid for admin)
- Line 42: GET /trade/resend

### index.php line 45-52 → offers.mdx
- Line 45-46: GET /offers/received
- Line 47-48: GET /offers/my
- Line 49: POST /offers/create
- Line 50: POST /offers/decline
- Line 51: POST /offers/remove
- Line 52: POST /offers/accept

### index.php line 53-59 → items.mdx & buyorders.mdx
- Line 53: GET /item/details/fromid/$backpackid
- Line 54: GET /item/cs/details/fromid/$backpackid
- Line 56: POST /item/buyorder
- Line 57: POST /item/buyorder/update
- Line 58: POST /item/buyorder/remove
- Line 59: GET /user/buyorder/$item

### index.php line 80-84 → deposit.mdx
- Line 80: GET /deposit/$game
- Line 81: GET /deposit/botList/$game
- Line 83: GET /deposit/tradeStatus/$tradeid
- Line 84: POST /deposit/setPriceForUpcomingTrade

### index.php line 87 → authentication.mdx
- Line 87: POST /user/login (API key authentication)

### index.php line 89-136 → user-account.mdx, user-settings.mdx, user-2fa.mdx, user-email.mdx, user-history.mdx
- Line 89: GET /user/disconnect
- Line 90: GET /user/disconnectSession/all
- Line 91: GET /user/disconnectSession/$id
- Line 92-93: GET /user/infos
- Line 94-95: GET /user/balance
- Line 98: GET /user/2FA/create
- Line 99: POST /user/reset2FA/ask
- Line 100: POST /user/reset2FA/validate
- Line 101-102: GET /user/getSalesInfos
- Line 103-104: GET /user/getSalesChartInfos
- Line 105-106: GET /user/getBalanceHistory
- Line 107-108: GET /user/getPurchaseHistory
- Line 109-110: GET /user/getSalesHistory
- Line 111-112: GET /user/getCashoutHistory
- Line 113-114: GET /user/getTransactionHistory
- Line 115-116: GET /user/getTransactionDetails
- Line 117-118: GET /user/getBuyorder
- Line 119: POST /user/2FA/validate
- Line 120: POST /user/setMailNotification
- Line 121: POST /user/setMailNotificationStatus
- Line 122: POST /user/setPrivacySetting
- Line 123: POST /user/setTradeUrl
- Line 124: POST /user/updateShortUrl
- Line 130: POST /user/email/change/request
- Line 131: POST /user/email/change/validate
- Line 132-133: GET /user/ipList
- Line 134-135: GET /user/getContactMail
- Line 136: GET /user/notifications

### index.php line 159 → utils.mdx
- Line 159: GET /utils/tradeurlCheck

### index.php line 169 → cashout.mdx
- Line 169: POST /cashout/process

### index.php line 173 → payment.mdx
- Line 173: POST /paiement/$provider

### index.php line 193, 195, 198 → public-data.mdx
- Line 193: GET /public/sales
- Line 195: GET /public/price
- Line 198: GET /infos/prices/buyorderAndLowestSales

---

## Excluded Endpoints (No 'api' filter)

The following endpoints from index.php were **intentionally excluded** because they do NOT have the 'api' filter:

- Line 15: GET /item/requestImage/$item (no filter)
- Line 27-28: GET /bundles/all, GET /bundles/add (no filter)
- Line 35: POST /inventory/randomHat (connected only)
- Line 61-73: Support endpoints (connected only)
- Line 75-78: Admin endpoints (admin only)
- Line 86: GET /user/login (Steam OpenID, not API)
- Line 88: GET /user/isConnected (no filter)
- Line 96-97: CSV token generation (connected only)
- Line 125-129: Payment alerts, affiliates, email validation (no api filter or no filter)
- Line 138-151: Giveaways endpoints (no api filter or connected only)
- Line 154: GET /csrf/token (connected only)
- Line 156-163: Utils endpoints without api filter
- Line 166: POST /cart/bulk/add (connected only)
- Line 170-171: Cashout link/unlink (connected only)
- Line 175: POST /gift/claim (connected, recaptcha)
- Line 178-191: Server, cron, webhook endpoints (server filter)

## Verification Status

✅ All API endpoints with 'api' filter are documented
✅ POST /user/login for API key authentication is documented
✅ Navigation structure matches the new documentation
✅ All files are properly formatted in MDX
✅ Examples and error responses included for all endpoints

---

**Last Updated:** February 7, 2026
**Total API Endpoints:** 66+
**Documentation Files:** 17 MDX files
