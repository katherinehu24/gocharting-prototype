# gocharting-prototype

GoCharting website + checkout redesign prototypes. All single self-contained HTML files — open in any modern browser, no build step.

## Live prototypes

- **[Features / Homepage](https://katherinehu24.github.io/gocharting-prototype/)** — `index.html`
- **[Pricing page](https://katherinehu24.github.io/gocharting-prototype/pricing.html)** — `pricing.html`
- **[Trial activation flow](https://katherinehu24.github.io/gocharting-prototype/trial.html)** — `trial.html` *(redesigned in-app 4-step trial flow)*

## Trial activation flow — what it shows

Redesigned 4-step in-app trial activation, compressing the current 5-step production flow while preserving all CME compliance and fraud-prevention requirements:

1. **Plan** — choose CME Premium ($35/mo) or CME Group Bundle ($40/mo), optional Crypto/Forex add-on. Live price updates in side panel.
2. **Verify** — consolidated identity + Non-professional subscriber acknowledgment on a single screen (collapses the current 2-step compliance modal).
3. **Confirm** — phone verification with SMS OTP. Real countdown, auto-advance, paste-to-fill.
4. **Trade** — trial-active state with computed trial timeline (Day 7 reminder → Day 8 charge → Day 22 refund window).

### Notable features

- Persistent left-rail order summary with live price updates as plan/variant changes
- Country selector in top nav (US / India / Rest of World) with friendly "coming soon" panel for non-US
- Subscriber Addendum modal (click the link on Step 2)
- Real form validation, inline check marks, ZIP validation, US states dropdown
- OTP error state — append `#demo` to URL, then enter `000000` on the OTP screen to see it
- Mobile-responsive with compact summary bar below 1024px

### Production notes

- Emoji flags in the country selector should be replaced with SVG flag components
- Loading states currently simulate ~700ms — wire to real API endpoints
- "Manage subscription" link is a placeholder
- See `#demo` URL hash for prototype-only affordances (demo restart link, OTP test code hint)

## Local development

```bash
git clone https://github.com/katherinehu24/gocharting-prototype.git
cd gocharting-prototype
open trial.html  # or index.html, pricing.html
```
