# API Endpoints Verification Checklist

## Authentication
- [x] POST /user/login (API Key authentication) - EXCEPTION (ligne 87: array())

## Items (10 endpoints)
- [x] GET /item/details/{item} - ligne 14: array('api')
- [x] GET /item/salesGraph/{item} - ligne 16: array('connected','api')
- [x] GET /item/listing/count/{item} - ligne 17: array('api')
- [x] GET /item/listing/count/{item}/{userid} - ligne 18: array('api')
- [x] GET /item/listing/{item} - ligne 19: array('api')
- [x] GET /item/listing/{item}/{userid} - ligne 20: array('api')
- [x] GET /item/buyorderList/{item} - ligne 23: array('api')
- [x] GET /item/pricing/{item} - ligne 25: array('connected','api')
- [x] GET /item/pricing/bulk - ligne 24: array('connected','api')
- [x] GET /item/details/fromid/{backpackid} - ligne 53: array('api')
- [x] GET /item/cs/details/fromid/{backpackid} - ligne 54: array('api')
- [x] GET /item/getRaffleItems - ligne 21: array('connected','api')

## Inventory (3 endpoints)
- [x] GET /inventory/onSale - ligne 30: array('connected','api')
- [x] GET /inventory/onInventory - ligne 32: array('connected','api')
- [x] POST /inventory/withdraw - ligne 34: array('connected','api')

## Trades (3 endpoints)
- [x] GET /trades/active - ligne 37: array('connected','api')
- [x] GET /trades/all - ligne 39: array('connected','api')
- [x] GET /trade/resend - ligne 42: array('connected','api')

## Offers (6 endpoints)
- [x] GET /offers/received - ligne 45: array('connected','api')
- [x] GET /offers/my - ligne 47: array('connected','api')
- [x] POST /offers/create - ligne 49: array('connected','api')
- [x] POST /offers/accept - ligne 52: array('connected','api')
- [x] POST /offers/decline - ligne 50: array('connected','api')
- [x] POST /offers/remove - ligne 51: array('connected','api')

## Buy Orders (5 endpoints)
- [x] POST /item/buyorder - ligne 56: array('connected','api')
- [x] POST /item/buyorder/update - ligne 57: array('connected','api')
- [x] POST /item/buyorder/remove - ligne 58: array('connected','api')
- [x] GET /user/buyorder/{item} - ligne 59: array('connected','api')
- [x] GET /user/getBuyorder - ligne 117: array('connected','api')

## Deposit (4 endpoints)
- [x] GET /deposit/{game} - ligne 80: array('connected','api')
- [x] GET /deposit/botList/{game} - ligne 81: array('api')
- [x] GET /deposit/tradeStatus/{tradeid} - ligne 83: array('connected','api')
- [x] POST /deposit/setPriceForUpcomingTrade - ligne 84: array('connected','api')

## User Account (8 endpoints)
- [x] GET /user/disconnect - ligne 89: array('connected','api')
- [x] GET /user/disconnectSession/all - ligne 90: array('connected','api')
- [x] GET /user/disconnectSession/{id} - ligne 91: array('connected','api')
- [x] GET /user/infos - ligne 92: array('connected','api')
- [x] GET /user/balance - ligne 94: array('connected','api')
- [x] GET /user/ipList - ligne 132: array('connected','api')
- [x] GET /user/getContactMail - ligne 134: array('connected','api')
- [x] GET /user/notifications - ligne 136: array('connected','api')

## User Settings (5 endpoints)
- [x] POST /user/setMailNotification - ligne 120: array('connected','api')
- [x] POST /user/setMailNotificationStatus - ligne 121: array('connected','api')
- [x] POST /user/setPrivacySetting - ligne 122: array('connected','api')
- [x] POST /user/setTradeUrl - ligne 123: array('connected','api')
- [x] POST /user/updateShortUrl - ligne 124: array('connected','api')

## Two-Factor Authentication (4 endpoints)
- [x] GET /user/2FA/create - ligne 98: array('connected','api')
- [x] POST /user/2FA/validate - ligne 119: array('connected','api')
- [x] POST /user/reset2FA/ask - ligne 99: array('connected','api')
- [x] POST /user/reset2FA/validate - ligne 100: array('connected','api')

## Email Management (2 endpoints)
- [x] POST /user/email/change/request - ligne 130: array('connected','2fa','api')
- [x] POST /user/email/change/validate - ligne 131: array('connected','2fa','api')

## User History (8 endpoints)
- [x] GET /user/getSalesInfos - ligne 101: array('connected','api')
- [x] GET /user/getSalesChartInfos - ligne 103: array('connected','api')
- [x] GET /user/getBalanceHistory - ligne 105: array('connected','api')
- [x] GET /user/getPurchaseHistory - ligne 107: array('connected','api')
- [x] GET /user/getSalesHistory - ligne 109: array('connected','api')
- [x] GET /user/getCashoutHistory - ligne 111: array('connected','api')
- [x] GET /user/getTransactionHistory - ligne 113: array('connected','api')
- [x] GET /user/getTransactionDetails - ligne 115: array('connected','api')

## Cashout (1 endpoint)
- [x] POST /cashout/process - ligne 169: array('connected','api')

## Payment (1 endpoint)
- [x] POST /paiement/{provider} - ligne 173: array('connected','api')

## Utilities (1 endpoint SEULEMENT)
- [x] GET /utils/tradeurlCheck - ligne 159: array('connected','api')

## Public Data (3 endpoints)
- [x] GET /public/price - ligne 195: array('api')
- [x] GET /infos/prices/buyorderAndLowestSales - ligne 198: array('api')
- [x] GET /public/sales - ligne 193: array('api')

---

## Total Endpoints Documented: 64

## CORRECTIF APPLIQUÉ

### Endpoints SUPPRIMÉS (n'ont PAS le filtre 'api'):
- ❌ GET /utils/bots - ligne 160: array() - **PAS de filtre 'api'**
- ❌ GET /utils/infos - ligne 161: array() - **PAS de filtre 'api'**

### Règle Appliquée

**SEULEMENT les routes avec le filtre 'api' sont incluses**, avec UNE SEULE exception :
- ✅ POST /user/login (ligne 87) - Exception explicite pour l'authentification API

Toutes les autres routes sans le filtre 'api' sont **EXCLUES**, même si elles semblent utiles.

---

## Routes Exclues (exemples de routes SANS filtre 'api')

- ligne 15: GET /item/requestImage - array() ❌
- ligne 27-28: GET /bundles/* - array() ❌
- ligne 35: POST /inventory/randomHat - array('connected') ❌
- ligne 61-73: /messages/*, /support/* - array('connected') ❌
- ligne 75-78: /admin/* - array('connected', 'admin') ❌
- ligne 86: GET /user/login - array() (Steam OpenID) ❌
- ligne 88: GET /user/isConnected - array() ❌
- ligne 96-97: /user/generateCSVToken - array('connected') ❌
- ligne 125-126: /user/closePayment* - array('connected') ❌
- ligne 127-129: /user/setAffiliates, email/validation/* - array() ❌
- ligne 138-151: /giveaways/* - array() ou array('connected') ❌
- ligne 154: /csrf/token - array('connected') ❌
- ligne 156-158: /utils/seon, replaceItems, inspect - array() ou array('connected') ❌
- ligne 160-161: /utils/bots, /utils/infos - array() ❌
- ligne 163: /utils/sms - array() ❌
- ligne 166: /cart/bulk/add - array('connected') ❌
- ligne 170-171: /cashout/link, unlink - array('connected') ❌
- ligne 175: /gift/claim - array('connected', 'recaptcha') ❌
- ligne 178-191: /server/*, /cron/*, /webhook/* - array('server') ou array() ❌
- ligne 197: /infos/admin - array('noDB') ❌

---

## Verification Status

✅ Tous les endpoints avec le filtre 'api' sont documentés  
✅ POST /user/login (exception) est documenté  
✅ Aucun endpoint SANS filtre 'api' n'est inclus (sauf l'exception login)  
✅ Navigation docs.json mise à jour  
✅ Fichiers MDX propres et formatés  

---

**Last Updated:** February 7, 2026  
**Total API Endpoints:** 64 (63 avec 'api' + 1 exception login)  
**Documentation Files:** 17 MDX files
