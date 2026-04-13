# STYLEBOOK (minimal)

This minimal stylebook defines the color palette, typography, and basic spacing used in the React Club app.

## Color palette
- Primary (brand teal): #0F766E
- CTA / Accent (warm coral): #FF6B4A
- Background (deep charcoal): #0B1220
- Surface / Card (dark slate): #0F1724
- Text primary (light): #E6EEF8
- Text secondary (muted): #97A3B3
- Success: #2ECC71
- Error: #FF4D4F

## Typography
- Font family: system stack ("Inter", "Segoe UI", Roboto, Helvetica, Arial, sans-serif)
- Base font-size: 16px
- Headings: bold, scale (h1 28px, h2 22px, h3 18px)

## Spacing & radius
- Spacing unit: 8px
- Border radius: 8px

## Buttons
- Primary button: background `--color-primary`, text white, padding 10px 14px, border-radius 6px
- Disabled button: reduced opacity

## Notes for usage
- Styles are implemented via `src/styles.css` using CSS variables. Components use utility classes `.card`, `.btn`, `.btn--primary`, `.muted`.
