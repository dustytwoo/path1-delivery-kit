# Fulfill SOP — {{BRAND}} (dropship)

**Tier:** Launch pack ($497) deliverable — customize per client.  
**Owner after handoff:** Founder (or $97/mo light-ops nudges only — not full order-desk VA).  
**Rule zero:** Never place a supplier order before storefront payment clears.

---

## Supplier bind

| Role | URL / ID | Notes |
|------|----------|-------|
| Hero | {{SUPPLIER_URL}} (`{{SUPPLIER_ID}}`) | Default |
| Backup | {{BACKUP_SUPPLIER_URL}} (`{{BACKUP_SUPPLIER_ID}}`) | Use only if hero fails at cart |
| Store product | Shopify ID / handle: `{{HANDLE}}` | |
| Retail | {{RETAIL}} | |

Add a second table row set for SKU #2 when Launch pack includes two products.

---

## When a payment clears (card, Shop Pay, PayPal, etc.)

1. Capture from order admin: buyer name, email, **exact** shipping address, line items (SKU + qty), and any UTM / `utm_content` if present.
2. Open hero supplier listing → ship to buyer address (**exact match** — no “close enough”).
3. Prefer tracked shipping to the destination country; confirm cart ETA still matches storefront disclosure (default overseas: **15–30 days**).
4. Place order → save supplier order id.
5. When tracking appears, paste into customer notification (Shopify fulfillment / email reply).
6. Log one row in `fulfill-template.csv`: order id · date · AE (or supplier) link · SKU · qty · tracking · status.

---

## Daily / per-order checklist

- [ ] Payment status = paid / captured (not pending, not fraud-hold)  
- [ ] Address complete (street, city, region, postal, country, phone if required by supplier)  
- [ ] Correct SKU / variant mapped to supplier SKU  
- [ ] Qty matches paid line  
- [ ] Tracking sent to buyer  
- [ ] CSV row complete  

---

## Rules

1. **Never order before payment clears.**  
2. Storefront ETA = **ops-confirmed cart days only** — do not invent faster windows. Overseas default disclosure: **15–30 days · tracked**.  
3. No trademarked competitor names on invoices, notes, or customer email.  
4. If hero listing is OOS or cart blocks ship-to country → use backup; note it in CSV `notes`.  
5. Refunds / cancellations: follow [policy-stubs.md](./policy-stubs.md); update CSV `status`.  
6. Do not add paid DSers / Shopify apps that create new billing without founder approval.

---

## Escalation

| Situation | Action |
|-----------|--------|
| Supplier delay past disclosed window | Proactive buyer update + options per refund stub |
| Wrong item shipped | Open supplier dispute; offer remake or refund per policy |
| Fraud / chargeback | Pause fulfill; document; follow platform guidance |
| Address undeliverable | Contact buyer once; hold before re-ship |

---

## Handoff line for founder

> After checkout clears, place the supplier order to the exact address, paste tracking when live, and log the row. The sheet + this SOP are the whole fulfill path.
