# ✅ Conformité de la Documentation API

## Objectif
Documenter **UNIQUEMENT** les routes avec le filtre `'api'` dans `index.php`, avec une seule exception : `POST /user/login` pour l'authentification API.

## Validation Complète

### ✅ Règle Principale Respectée
Tous les endpoints documentés ont le filtre `'api'` dans leur déclaration dans `index.php`, SAUF l'exception explicite du login.

### ✅ Exception Documentée
- **POST /user/login** (ligne 87) - `array()` - Exception pour authentification API key

### ✅ Endpoints avec Filtre 'api' (64 au total)

| Endpoint | Ligne | Filtres | Fichier Doc |
|----------|-------|---------|-------------|
| GET /item/details/{item} | 14 | array('api') | items.mdx |
| GET /item/salesGraph/{item} | 16 | array('connected','api') | items.mdx |
| GET /item/listing/count/{item} | 17-18 | array('api') | items.mdx |
| GET /item/listing/{item} | 19-20 | array('api') | items.mdx |
| GET /item/getRaffleItems | 21 | array('connected','api') | items.mdx |
| GET /item/buyorderList/{item} | 23 | array('api') | items.mdx |
| GET /item/pricing/bulk | 24 | array('connected','api') | items.mdx |
| GET /item/pricing/{item} | 25 | array('connected','api') | items.mdx |
| GET /inventory/onSale | 30 | array('connected','api') | inventory.mdx |
| GET /inventory/onInventory | 32 | array('connected','api') | inventory.mdx |
| POST /inventory/withdraw | 34 | array('connected','api') | inventory.mdx |
| GET /trades/active | 37 | array('connected','api') | trades.mdx |
| GET /trades/all | 39 | array('connected','api') | trades.mdx |
| GET /trade/resend | 42 | array('connected','api') | trades.mdx |
| GET /offers/received | 45 | array('connected','api') | offers.mdx |
| GET /offers/my | 47 | array('connected','api') | offers.mdx |
| POST /offers/create | 49 | array('connected','api') | offers.mdx |
| POST /offers/decline | 50 | array('connected','api') | offers.mdx |
| POST /offers/remove | 51 | array('connected','api') | offers.mdx |
| POST /offers/accept | 52 | array('connected','api') | offers.mdx |
| GET /item/details/fromid/{backpackid} | 53 | array('api') | items.mdx |
| GET /item/cs/details/fromid/{backpackid} | 54 | array('api') | items.mdx |
| POST /item/buyorder | 56 | array('connected','api') | buyorders.mdx |
| POST /item/buyorder/update | 57 | array('connected','api') | buyorders.mdx |
| POST /item/buyorder/remove | 58 | array('connected','api') | buyorders.mdx |
| GET /user/buyorder/{item} | 59 | array('connected','api') | buyorders.mdx |
| GET /deposit/{game} | 80 | array('connected','api') | deposit.mdx |
| GET /deposit/botList/{game} | 81 | array('api') | deposit.mdx |
| GET /deposit/tradeStatus/{tradeid} | 83 | array('connected','api') | deposit.mdx |
| POST /deposit/setPriceForUpcomingTrade | 84 | array('connected','api') | deposit.mdx |
| GET /user/disconnect | 89 | array('connected','api') | user-account.mdx |
| GET /user/disconnectSession/all | 90 | array('connected','api') | user-account.mdx |
| GET /user/disconnectSession/{id} | 91 | array('connected','api') | user-account.mdx |
| GET /user/infos | 92 | array('connected','api') | user-account.mdx |
| GET /user/balance | 94 | array('connected','api') | user-account.mdx |
| GET /user/2FA/create | 98 | array('connected','api') | user-2fa.mdx |
| POST /user/reset2FA/ask | 99 | array('connected','api') | user-2fa.mdx |
| POST /user/reset2FA/validate | 100 | array('connected','api') | user-2fa.mdx |
| GET /user/getSalesInfos | 101 | array('connected','api') | user-history.mdx |
| GET /user/getSalesChartInfos | 103 | array('connected','api') | user-history.mdx |
| GET /user/getBalanceHistory | 105 | array('connected','api') | user-history.mdx |
| GET /user/getPurchaseHistory | 107 | array('connected','api') | user-history.mdx |
| GET /user/getSalesHistory | 109 | array('connected','api') | user-history.mdx |
| GET /user/getCashoutHistory | 111 | array('connected','api') | user-history.mdx |
| GET /user/getTransactionHistory | 113 | array('connected','api') | user-history.mdx |
| GET /user/getTransactionDetails | 115 | array('connected','api') | user-history.mdx |
| GET /user/getBuyorder | 117 | array('connected','api') | buyorders.mdx |
| POST /user/2FA/validate | 119 | array('connected','api') | user-2fa.mdx |
| POST /user/setMailNotification | 120 | array('connected','api') | user-settings.mdx |
| POST /user/setMailNotificationStatus | 121 | array('connected','api') | user-settings.mdx |
| POST /user/setPrivacySetting | 122 | array('connected','api') | user-settings.mdx |
| POST /user/setTradeUrl | 123 | array('connected','api') | user-settings.mdx |
| POST /user/updateShortUrl | 124 | array('connected','api') | user-settings.mdx |
| POST /user/email/change/request | 130 | array('connected','2fa','api') | user-email.mdx |
| POST /user/email/change/validate | 131 | array('connected','2fa','api') | user-email.mdx |
| GET /user/ipList | 132 | array('connected','api') | user-account.mdx |
| GET /user/getContactMail | 134 | array('connected','api') | user-account.mdx |
| GET /user/notifications | 136 | array('connected','api') | user-account.mdx |
| GET /utils/tradeurlCheck | 159 | array('connected','api') | utils.mdx |
| POST /cashout/process | 169 | array('connected','api') | cashout.mdx |
| POST /paiement/{provider} | 173 | array('connected','api') | payment.mdx |
| GET /public/sales | 193 | array('api') | public-data.mdx |
| GET /public/price | 195 | array('api') | public-data.mdx |
| GET /infos/prices/buyorderAndLowestSales | 198 | array('api') | public-data.mdx |

**Total: 63 endpoints avec filtre 'api' + 1 exception (login) = 64 endpoints**

---

## ❌ Endpoints EXCLUS (Correctement)

Ces endpoints n'ont PAS été documentés car ils n'ont PAS le filtre `'api'` :

### Endpoints avec array() vide
- Ligne 15: `GET /item/requestImage` - array()
- Ligne 27: `GET /bundles/all` - array()
- Ligne 28: `GET /bundles/add` - array()
- Ligne 86: `GET /user/login` (Steam OpenID) - array()
- Ligne 88: `GET /user/isConnected` - array()
- Ligne 127: `POST /user/setAffiliates` - array()
- Ligne 128: `POST /user/email/validation/request` - array()
- Ligne 129: `POST /user/email/validation/validate` - array()
- Ligne 138-142: Giveaways publics - array()
- Ligne 156: `POST /utils/seon` - array()
- Ligne 160: `GET /utils/bots` - array() ✅ **CORRIGÉ**
- Ligne 161: `GET /utils/infos` - array() ✅ **CORRIGÉ**
- Ligne 163: `POST /utils/sms` - array()
- Ligne 187: `GET /cron/getLateInventory` - array()
- Ligne 189: `GET /webhook/payoneer` - array()
- Ligne 190: `POST /webhook/tipalti` - array()
- Ligne 191: `POST /webhook/payment/{provider}` - array()

### Endpoints avec array('connected') uniquement
- Ligne 35: `POST /inventory/randomHat`
- Ligne 61-73: Support endpoints
- Ligne 96-97: `GET /user/generateCSVToken`
- Ligne 125: `POST /user/closePaymentAlert`
- Ligne 126: `POST /user/closePaymentReviews`
- Ligne 141-151: Giveaways connectés
- Ligne 154: `GET /csrf/token`
- Ligne 157: `POST /utils/replaceItems`
- Ligne 158: `POST /utils/inspect/ingame`
- Ligne 166: `POST /cart/bulk/add`
- Ligne 170: `POST /cashout/link`
- Ligne 171: `POST /cashout/unlink`

### Endpoints admin/server uniquement
- Ligne 31, 33, 38, 40, 43, 46, 48, 63, 71-78, 82, 93, 95, 97, 102, 104, 106, 108, 110, 112, 114, 116, 118, 133, 135: Variantes admin
- Ligne 75-78: Admin endpoints
- Ligne 178-188: Server/cron endpoints

### Endpoints avec autres filtres
- Ligne 175: `POST /gift/claim` - array('connected', 'recaptcha')
- Ligne 197: `GET /infos/admin` - array('noDB')

---

## 📊 Statistiques Finales

| Catégorie | Nombre |
|-----------|--------|
| Endpoints avec filtre 'api' | 63 |
| Exceptions (login API) | 1 |
| **Total documenté** | **64** |
| Endpoints exclus (sans 'api') | ~136 |
| **Total dans index.php** | **~200** |

---

## ✅ Conformité Validée

- [x] Tous les endpoints avec `'api'` dans les filtres sont documentés
- [x] Aucun endpoint SANS `'api'` n'est documenté (sauf l'exception login)
- [x] L'exception `POST /user/login` est clairement identifiée
- [x] Les corrections ont été appliquées (suppression de /utils/bots et /utils/infos)
- [x] La documentation est cohérente avec les règles établies
- [x] Tous les fichiers MDX sont à jour
- [x] La navigation dans docs.json correspond aux fichiers créés

---

## 🎯 Conclusion

La documentation Mintlify respecte strictement la règle :

> **"Prend juste les call avec le filtre api (enlève ceux qui n'ont pas de filtre) à l'exception du login"**

✅ **Conformité: 100%**

---

**Date de validation:** 7 février 2026  
**Validé par:** AI Assistant  
**Version:** 1.0
