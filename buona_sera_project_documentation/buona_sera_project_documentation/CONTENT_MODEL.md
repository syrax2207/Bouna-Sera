# Content Model & Verification Register

## 1. Content principles

All business-specific content must be accurate, current and approved. The website concept must not turn research assumptions into facts.

Use these statuses:
- `VERIFIED`: checked against a current authoritative source or directly confirmed by the business.
- `NEEDS_CONFIRMATION`: found in research/listings but not confirmed.
- `CONCEPT_COPY`: proposed creative text, not an official business statement.
- `PLACEHOLDER`: intentionally empty or temporary; must not appear on a public launch.

## 2. Business profile fields

| Field | Current value | Status | Required action |
|---|---|---|---|
| Business name | Buona Sera Cafe | NEEDS_CONFIRMATION | Confirm official spelling |
| Address | HA 05, near Sanskar Public School, Block A, Sector 104, Hajipur, Noida, UP 201304 | NEEDS_CONFIRMATION | Confirm with owner/current official listing |
| Phone | +91 98717 56513 | NEEDS_CONFIRMATION | Call/check current official source and owner approval |
| WhatsApp | Not confirmed | PLACEHOLDER | Ask whether this number accepts WhatsApp enquiries |
| Opening hours | Previously reported 10:30 AM–11:30 PM | NEEDS_CONFIRMATION | Verify all days and holiday exceptions |
| Website | No verified official URL established in prior research | NEEDS_CONFIRMATION | Search current listing/social bio and ask owner |
| Social profile | Not confirmed | PLACEHOLDER | Verify official account |
| Menu | Partial customer/listing references only | NEEDS_CONFIRMATION | Obtain current owner-approved menu |
| Prices | Prior estimate only; no verified item prices | PLACEHOLDER | Obtain current prices |
| Reservations | Not confirmed | PLACEHOLDER | Ask whether table enquiries/bookings are accepted |
| Delivery/takeaway | Not confirmed | PLACEHOLDER | Verify before mentioning |

## 3. Menu data shape

Use structured records, for example:

```ts
type MenuItem = {
  id: string;
  name: string;
  description?: string;
  price?: number;
  currency?: "INR";
  category: string;
  image?: string;
  dietaryLabels?: string[];
  availability?: "available" | "seasonal" | "unknown";
  verificationStatus: "verified" | "needs-confirmation" | "concept-copy";
  source?: string;
  lastVerified?: string;
};
```

Only display fields that have been verified and approved. Do not infer allergens or dietary suitability.

## 4. Story copy

Do not invent:
- Founding year or origin story.
- Owner/founder identity.
- Family recipes or heritage.
- Ingredient sourcing claims.
- Chef credentials.
- Sustainability claims.
- Awards or press mentions.

Until confirmed, use neutral concept copy focused on the visitor experience rather than unverifiable history.

## 5. Reviews and social proof

Do not create fake testimonials. Do not copy full third-party reviews. Do not display rating stars, review totals or review quotes without current verification, appropriate attribution and permission/terms review.

## 6. Verification log template

| Claim / field | Source | Checked date | Confirmed by | Status | Notes |
|---|---|---|---|---|---|
| Example: opening hours | Owner / official source | YYYY-MM-DD | Name/role | VERIFIED | Record exceptions |

Update this table before content is treated as launch-ready.
