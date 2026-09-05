# IFMS Landing Page -- context for future work

A single static HTML page (`index.html`, plain HTML/Tailwind via CDN or inline classes -- no build
step, no framework) that links out to the three public-facing portals in the IFMS prototype suite:
Employee Portal, Pensioner Portal, Vendor Portal.

**Deliberately does not link to `admin_portal`** -- that's an internal back-office tool, not a
public self-service portal, and hasn't been discussed as something the public landing page should
surface. Don't add it without asking first.

## Structure
- Hero section + a card grid (`sm:grid-cols-2 lg:grid-cols-3`), one card per portal: icon,
  description, Sign in / Register links opening `target="_blank" rel="noopener"` to that portal's
  frontend (`localhost:7001` employee, `:7002` pension, `:7003` vendor).
- A "help strip" at the bottom with a "New employee?" / "New pensioner?" / "New vendor?" quick-link
  row (4-column grid).

## How to preview
No dev server needed -- it's static. `python -m http.server 8888` from `E:\IFMS\landing` and open
`localhost:8888`, or open `index.html` directly in a browser.

## Status (as of 2026-09-03)
Up to date with all three public portals (the Vendor Portal card was the most recent addition,
mirroring the Employee/Pension cards already there). Verified via browser screenshot and a
`javascript_exec` check that every portal's links carry the correct `target`/`rel` attributes.

## Related
`E:\IFMS\emp_mgmt_pro\CONTEXT.md`, `E:\IFMS\pension_mgmt\CONTEXT.md`, `E:\IFMS\vendor_mgmt\CONTEXT.md`,
`E:\IFMS\admin_portal\CONTEXT.md`.
