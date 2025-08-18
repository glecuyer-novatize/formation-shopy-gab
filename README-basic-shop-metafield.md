## Basic Shop Metafield section

Audience: Client and implementers

Overview
- Displays a shop-level metafield at the top of the homepage or any page. The metafield is `shop.metafields.custom.homepage_text`.
- Multilingual by default (English/French included). Accessible markup and semantics are built in.

Requirements
- In Shopify Admin, create a shop metafield definition:
  - Namespace and key: `custom.homepage_text`
  - Type: `Single line text` or `Rich text` (recommended)

Configuration (Theme Editor)
- Heading: Optional title displayed above the text. If left empty, the section will still be accessible using an aria-label.
- Heading level: Choose H2–H4 to fit the page outline.
- Text alignment: Left/Center/Right.

Internationalization
- Default strings are localized via translation keys:
  - `sections.basic_shop_metafield.default_heading`
  - `sections.basic_shop_metafield.region_label`
- To localize the metafield value itself, use Shopify Translate & Adapt or any translation app supporting shop metafields.

Accessibility
- The section uses `role="region"` and either:
  - `aria-labelledby` referencing the visible heading, or
  - `aria-label` using a localized label when no heading is set.
- The metafield content is rendered with `metafield_tag` for safe, type-aware output.

QA checklist
- Heading level fits the page’s semantic outline (no heading level skipping).
- Focus styles are visible (`:focus-visible` in `assets/base.css`).
- Screen reader announces the region with the section heading or label in both languages.
- Metafield content appears as expected for each locale.

Limitations
- Only one metafield (`custom.homepage_text`) is supported by this section. Duplicate the section if different metafields are needed in other contexts.

Support
- For changes or issues, provide the page URL, screenshots, current language, and the metafield content causing the problem.


