# customer-portal

**Status:** Runnable scaffold (ERPNext password login)  
**Kind:** Next.js  
**Backend:** `customer_portal`  
**Package:** `@zatgo/customer-portal`  
**Stack:** [FRONTEND_STACK](../../Docs/Foundation/FRONTEND_STACK.md)

## Auth

Sign in with ERPNext / Frappe **site URL + email/password**. Login runs on the Next.js server (`/api/erpnext/*`) via `@zatgo/erpnext` and stores an encrypted httpOnly cookie.

Set `ERPNEXT_SESSION_SECRET` in production (required). For local dev, copy `.env.example` to `.env.local` and either set a secret or `ALLOW_INSECURE_DEV_SECRETS=1`. Use **Continue offline** to browse without a site.

## Run

```bash
pnpm install
pnpm --filter @zatgo/customer-portal dev
# → http://localhost:3002
```

Optional:

```bash
NEXT_PUBLIC_FRAPPE_BASE_URL=http://127.0.0.1:8082 \
ALLOW_INSECURE_DEV_SECRETS=1 \
pnpm --filter @zatgo/customer-portal dev
```
