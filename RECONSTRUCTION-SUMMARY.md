# Documentation Reconstruction - Summary

## Objectif
Vider et reconstruire la documentation Mintlify pour inclure **uniquement les routes avec le filtre "api"** ainsi que le **login API (POST)**.

## Modifications Effectuées

### Fichiers Supprimés
- Tous les anciens fichiers MDX de documentation API
- `api-reference/admin.mdx`
- `api-reference/bundles.mdx`
- `api-reference/cart.mdx`
- `api-reference/gift.mdx`
- `api-reference/giveaways.mdx`
- `api-reference/support.mdx`
- Dossier `api-reference/endpoint/`
- Dossier `api-reference/user/` (ancienne structure)
- `quickstart.mdx`
- `development.mdx`
- `api-reference/openapi.json`

### Nouveaux Fichiers Créés

#### 1. Authentication
- **api-reference/authentication.mdx**
  - `POST /user/login` - API key authentication
  - JWT token structure and usage

#### 2. Items
- **api-reference/items.mdx**
  - `GET /item/details/{item}`
  - `GET /item/salesGraph/{item}`
  - `GET /item/listing/count/{item}`
  - `GET /item/listing/{item}`
  - `GET /item/buyorderList/{item}`
  - `GET /item/pricing/{item}`
  - `GET /item/pricing/bulk`
  - `GET /item/details/fromid/{backpackid}`
  - `GET /item/cs/details/fromid/{backpackid}`
  - `GET /item/getRaffleItems`

#### 3. Inventory
- **api-reference/inventory.mdx**
  - `GET /inventory/onSale`
  - `GET /inventory/onInventory`
  - `POST /inventory/withdraw`

#### 4. Trades
- **api-reference/trades.mdx**
  - `GET /trades/active`
  - `GET /trades/all`
  - `GET /trade/resend`

#### 5. Offers
- **api-reference/offers.mdx**
  - `GET /offers/received`
  - `GET /offers/my`
  - `POST /offers/create`
  - `POST /offers/accept`
  - `POST /offers/decline`
  - `POST /offers/remove`

#### 6. Buy Orders
- **api-reference/buyorders.mdx**
  - `POST /item/buyorder`
  - `POST /item/buyorder/update`
  - `POST /item/buyorder/remove`
  - `GET /user/buyorder/{item}`
  - `GET /user/getBuyorder`

#### 7. Deposit
- **api-reference/deposit.mdx**
  - `GET /deposit/{game}`
  - `GET /deposit/botList/{game}`
  - `GET /deposit/tradeStatus/{tradeid}`
  - `POST /deposit/setPriceForUpcomingTrade`

#### 8. User Account
- **api-reference/user-account.mdx**
  - `GET /user/disconnect`
  - `GET /user/disconnectSession/all`
  - `GET /user/disconnectSession/{id}`
  - `GET /user/infos`
  - `GET /user/balance`
  - `GET /user/ipList`
  - `GET /user/getContactMail`
  - `GET /user/notifications`

#### 9. User Settings
- **api-reference/user-settings.mdx**
  - `POST /user/setMailNotification`
  - `POST /user/setMailNotificationStatus`
  - `POST /user/setPrivacySetting`
  - `POST /user/setTradeUrl`
  - `POST /user/updateShortUrl`

#### 10. Two-Factor Authentication
- **api-reference/user-2fa.mdx**
  - `GET /user/2FA/create`
  - `POST /user/2FA/validate`
  - `POST /user/reset2FA/ask`
  - `POST /user/reset2FA/validate`

#### 11. Email Management
- **api-reference/user-email.mdx**
  - `POST /user/email/change/request`
  - `POST /user/email/change/validate`

#### 12. User History
- **api-reference/user-history.mdx**
  - `GET /user/getSalesInfos`
  - `GET /user/getSalesChartInfos`
  - `GET /user/getBalanceHistory`
  - `GET /user/getPurchaseHistory`
  - `GET /user/getSalesHistory`
  - `GET /user/getCashoutHistory`
  - `GET /user/getTransactionHistory`
  - `GET /user/getTransactionDetails`

#### 13. Cashout
- **api-reference/cashout.mdx**
  - `POST /cashout/process`

#### 14. Payment
- **api-reference/payment.mdx**
  - `POST /paiement/{provider}`

#### 15. Utilities
- **api-reference/utils.mdx**
  - `GET /utils/tradeurlCheck`

#### 16. Public Data
- **api-reference/public-data.mdx**
  - `GET /public/price`
  - `GET /infos/prices/buyorderAndLowestSales`
  - `GET /public/sales`

### Fichiers Mis à Jour

#### docs.json
- Restructuré la navigation pour refléter les nouvelles catégories
- Supprimé les références aux anciennes pages
- Ajouté les nouvelles pages organisées par catégorie

#### index.mdx
- Mis à jour la page d'accueil avec les nouvelles catégories
- Ajouté des informations sur l'authentification par API key
- Restructuré les cartes de navigation

#### api-reference/introduction.mdx
- Mis à jour pour refléter l'authentification par API key/JWT
- Supprimé les références à l'authentification Steam OpenID (non-API)
- Ajouté des informations sur les permissions API

## Structure Finale

```
api-reference/
├── introduction.mdx           # Vue d'ensemble de l'API
├── authentication.mdx         # Authentification par API key
├── items.mdx                  # Endpoints items
├── inventory.mdx              # Gestion d'inventaire
├── trades.mdx                 # Gestion des trades
├── offers.mdx                 # Système d'offres
├── buyorders.mdx              # Ordres d'achat
├── deposit.mdx                # Dépôts d'items
├── user-account.mdx           # Informations du compte
├── user-settings.mdx          # Paramètres utilisateur
├── user-2fa.mdx               # Authentification 2FA
├── user-email.mdx             # Gestion email
├── user-history.mdx           # Historique des transactions
├── cashout.mdx                # Retraits
├── payment.mdx                # Paiements
├── utils.mdx                  # Utilitaires
└── public-data.mdx            # Données publiques
```

## Routes Exclues (Non-API)

Les routes suivantes ont été **exclues** car elles n'ont PAS le filtre "api" :

- `GET /item/requestImage` - array() vide
- `GET /user/login` (Steam OpenID - non-API)
- `GET /user/isConnected` - array() vide
- `GET /utils/bots` - array() vide
- `GET /utils/infos` - array() vide
- Tous les endpoints de giveaways sans filtre "api"
- Tous les endpoints de support sans filtre "api"
- Tous les endpoints admin
- Tous les endpoints bundles
- Tous les endpoints cart
- Tous les endpoints gift
- Tous les endpoints server/cron
- Tous les endpoints webhook

## Routes Incluses (avec filtre "api")

✅ Toutes les routes listées dans les nouveaux fichiers MDX ont le filtre `array('api')` ou `array('connected','api')` dans index.php

✅ Le `POST /user/login` (loginAPI.php) a été inclus spécifiquement pour l'authentification API

## Nombre Total d'Endpoints Documentés

**~64 endpoints API** répartis sur 16 fichiers de documentation

## Notes

- La documentation se concentre uniquement sur les endpoints accessibles via API key
- L'authentification Steam OpenID a été remplacée par l'authentification API key/JWT
- Tous les exemples incluent des formats JSON et des cas d'erreur
- Les endpoints admin avec filtre "api" n'ont pas été inclus (réservés aux admins)

## Prochaines Étapes Suggérées

1. Vérifier que tous les endpoints documentés fonctionnent correctement
2. Tester l'authentification API key
3. Valider les exemples de requêtes/réponses
4. Déployer sur Mintlify
5. Mettre à jour les liens dans l'application principale

---

**Date de reconstruction:** 7 février 2026
**Fichiers créés:** 16 fichiers MDX + docs.json + index.mdx + API-README.md
**Fichiers supprimés:** ~30 fichiers MDX obsolètes
