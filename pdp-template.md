# PDP template — {{PRODUCT_TITLE}}

**Brand:** {{BRAND}}  
**SKU code:** {{SKU_CODE}}  
**Retail:** {{RETAIL}}  
**Supplier URL:** {{SUPPLIER_URL}} (`{{SUPPLIER_ID}}`)  
**Store handle:** `{{HANDLE}}`  
**Status:** Draft → Soft QA → Live  

Fill every `{{…}}`. Do **not** use Nestora (or any other client’s brand) as the product name.

---

## Shopify / Pages title

```
{{PRODUCT_TITLE}}
```

*(Clear benefit + object. Avoid trademarked competitor names.)*

---

## SEO

**Meta title:** {{PRODUCT_TITLE short}} | {{BRAND}}  
**Meta description:** {{1–2 sentence benefit}}. Honest tracked shipping — typically {{SHIP_ETA}} from overseas when dropship.  
**Handle:** `{{HANDLE}}`

---

## Under-price ship line (required)

Default overseas dropship (confirm against live supplier cart before publish):

```
Typically ships in 15–30 days · tracked from overseas
```

If supplier is domestic / faster, replace with **ops-confirmed** window only.  
**Never** invent “ships tomorrow,” “Prime speed,” or “free US shipping” until cart/ops confirms.

Alternate short forms:

- `Ships tracked · typically 15–30 days (overseas)`
- `Tracked delivery · see shipping policy for ETA`

---

## Bullets (4–6)

Write customer-facing bullets. Always include one **honest shipping** bullet.

1. **{{Benefit 1}}** — …
2. **{{Benefit 2}}** — …
3. **{{Benefit 3}}** — …
4. **Honest shipping** — fulfilled via overseas dropship (unless domestic confirmed); tracked delivery typically **15–30 days**. Not Amazon Prime — we say so up front.
5. *(Optional)* **{{Fit / size / material note}}** — …
6. *(Optional)* **{{Care / use note}}** — …

---

## Description body (outline)

Paste into Shopify `body_html` or Pages product section.

1. **Hook (1 line):** problem → outcome in plain language.  
2. **What it is (1–2 short paragraphs):** what the buyer gets; how to use; who it’s for.  
3. **Why {{BRAND}} (bullets above).**  
4. **Shipping note (required):**

```
Shipping note: Orders are fulfilled via dropship from overseas unless otherwise stated. You’ll receive tracking after we place your order. Please allow typically 15–30 days for delivery. Not Prime-speed shipping.
```

5. **Disclaimers:** no medical / FDA / “guaranteed results” language unless the client’s counsel has approved specific claims. No fake affiliations with trademark brands.

---

## FAQ stubs (storefront accordion or page)

**How long does shipping take?**  
Typically **15–30 days** for overseas dropship (tracked). Domestic/faster suppliers use the window confirmed at order time. See Shipping policy.

**When do I get tracking?**  
After payment clears and we place the supplier order, we email/post tracking as soon as the carrier provides it.

**What’s your return / refund policy?**  
See Returns policy. Brief version: [link]. We keep policies honest about overseas return friction.

**Is this Prime / next-day?**  
No. We disclose overseas ETAs up front so there are no surprises.

**Who do I contact?**  
{{BRAND}} support: {{SUPPORT_EMAIL_OR_FORM}}

---

## Variants (if any)

| Option name | Values | Maps to supplier SKU |
|-------------|--------|----------------------|
| e.g. Size | S / M / L | … |

---

## Claims hard-no (checklist before publish)

- [ ] No trademark competitor names in title/body  
- [ ] No medical / FDA / disease / “cures anxiety” style claims  
- [ ] No “free shipping” unless ops-confirmed  
- [ ] No hard **7–15 day** promise unless supplier cart proves it  
- [ ] Honest **15–30** (or confirmed window) present on PDP + meta  
- [ ] No Nestora (or other brands) left in copy  

---

## Creative / UTM note

Bio or caption link example (see [utm-sheet.md](./utm-sheet.md)):

```
{{STORE_URL}}/products/{{HANDLE}}?utm_source={{SOURCE}}&utm_medium={{MEDIUM}}&utm_campaign={{CAMPAIGN}}&utm_content={{BRAND}}_{{ANGLE}}_{{SKU_CODE}}_{{CREATIVE}}
```
