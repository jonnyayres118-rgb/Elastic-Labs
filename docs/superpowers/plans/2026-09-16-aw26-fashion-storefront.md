# ELASTIC LABS AW26 Storefront Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Replace the legacy engineering consultancy site with a deployable AW26 high-fashion made-to-order catalogue and prepare it for later commerce integration.

**Architecture:** Keep the current static single-page architecture for the first launch preview because the repository currently contains only `index.html` plus a legacy image. Product data is defined once in JavaScript and rendered into a responsive collection grid; transactional checkout remains outside V1 until a Shopify connection and manufacturing terms exist.

**Tech Stack:** HTML5, CSS3, vanilla JavaScript, GitHub, Vercel.

**Spec:** `docs/superpowers/specs/2026-09-16-aw26-fashion-storefront-design.md`

## Global Constraints
- AW26 only.
- Black visual system and black product colourway.
- Every product price is £500 or above.
- Made-to-order and individually numbered positioning.
- Do not claim that an email enquiry is a completed purchase.
- Do not accept live payments until Shopify, consumer terms, sizing, lead times and manufacturing operations are connected.

---

### Task 1: Storefront transformation
**Files:** Modify `index.html`
**Produces:** Responsive AW26 catalogue, product SKUs, prices, process and archive.
- [x] Replace legacy consultancy metadata, styles and copy with ELASTIC LABS AW26.
- [x] Encode the seven approved AW26 objects, prices and base SKUs in one product array.
- [x] Render product catalogue cards from the array.
- [x] Add made-to-order process and archive language.
- [x] Ensure claim actions are enquiries rather than false checkout.

### Task 2: Design and implementation documentation
**Files:** Create design spec and this plan.
**Produces:** Persistent design authority and implementation record.
- [x] Record positioning, collection, SKUs and commerce boundary.
- [x] Record the current implementation and remaining launch blockers.

### Task 3: Preview verification and deployment
**Files:** No source changes expected unless verification finds defects.
**Consumes:** `index.html` from Task 1.
**Produces:** Vercel preview deployment for human review.
- [ ] Verify branch content and responsive source structure.
- [ ] Deploy preview through the existing Elastic Labs Vercel project / Git integration.
- [ ] Review deployed result before any production publish.

### Task 4: Commerce integration (blocked until store connection)
**Files:** To be determined by Shopify integration choice after connection.
**Consumes:** Product SKUs and prices from Task 1.
**Produces:** Real checkout/order flow.
- [ ] Connect Shopify store/API.
- [ ] Create products/variants and size architecture using the approved base SKUs.
- [ ] Connect checkout and order confirmation.
- [ ] Generate permanent serial after paid order.
- [ ] Finalise consumer terms, sizing, lead times, duties, returns/cancellations and factory handoff before enabling payments.