# UTM sheet — {{BRAND}}

**Purpose:** Consistent link tags for bio, organic posts, and *future* ads (ads are **out of scope** unless Dylan greenlights separately).  
**Pattern source:** Scrubbed from Nestora muscle-memory (`{brand}_{angle}_{sku}_{creative}`) — client-facing links use **{{BRAND}}**, never Nestora.

---

## Canonical pattern

Prefer full UTM set when the platform allows long URLs:

```
{{STORE_URL}}/products/{{HANDLE}}?utm_source={{SOURCE}}&utm_medium={{MEDIUM}}&utm_campaign={{CAMPAIGN}}&utm_content={{BRAND_SLUG}}_{{ANGLE}}_{{SKU_CODE}}_{{CREATIVE_ID}}
```

| Param | What to put | Examples |
|-------|-------------|----------|
| `utm_source` | Platform | `tiktok`, `instagram`, `youtube`, `bio`, `email` |
| `utm_medium` | Channel type | `organic`, `social`, `cpc` (only if paid later) |
| `utm_campaign` | Push / week | `launch`, `week1`, `restock` |
| `utm_content` | Creative id | `{{BRAND_SLUG}}_invisible-mess_roller_org-01` |

**Brand slug:** lowercase, hyphenated (`acme-pets`).  
**Angle:** short hyphenated hook (`invisible-mess`, `doorway-mud`).  
**SKU code:** stable internal code (`roller`, `lick-mat`).  
**Creative id:** `org-01` … `org-07` for organic week packs; `ad-01` only if paid exists.

### Short form (bio length limits)

When only one query param fits, pack identity into `utm_content`:

```
{{STORE_URL}}/products/{{HANDLE}}?utm_content={{BRAND_SLUG}}_{{ANGLE}}_{{SKU_CODE}}_{{CREATIVE_ID}}
```

---

## Example rows (replace with client values)

| Creative | Channel | Full URL |
|----------|---------|----------|
| org-01 | TikTok organic | `{{STORE_URL}}/products/{{HANDLE}}?utm_source=tiktok&utm_medium=organic&utm_campaign=week1&utm_content={{BRAND_SLUG}}_{{ANGLE}}_{{SKU_CODE}}_org-01` |
| org-02 | Instagram Reels | `{{STORE_URL}}/products/{{HANDLE}}?utm_source=instagram&utm_medium=organic&utm_campaign=week1&utm_content={{BRAND_SLUG}}_{{ANGLE}}_{{SKU_CODE}}_org-02` |
| bio | Profile link | `{{STORE_URL}}/products/{{HANDLE}}?utm_source=bio&utm_medium=social&utm_campaign=evergreen&utm_content={{BRAND_SLUG}}_{{ANGLE}}_{{SKU_CODE}}_bio` |

---

## Logging

When an order arrives with UTM present, copy `utm_content` into `fulfill-template.csv` column `utm_creative_id`. That is how organic creative attribution stays tied to fulfill without a paid ads stack.

---

## Rules

1. One creative id per distinct post / cut — don’t reuse `org-01` for a different video.  
2. Never put Nestora (or another client’s slug) in a new client’s UTMs.  
3. Do not promise that UTMs alone equal a tracking “pixel stack.” Meta/TikTok pixels are separate and out of default scope.  
4. No paid `utm_medium=cpc` rows unless paid spend is explicitly approved.
