# STYLEBOOK (minimal)

This minimal stylebook defines the color palette, typography, and basic spacing used in the React Club app.

## Color palette
- Primary: #1e88e5 (blue)
- Secondary: #ff7043 (orange)
- Background: #ffffff (white)
- Surface / Card: #f7f9fc (light gray)
- Text primary: #0f1724 (dark)
- Text secondary: #586069 (muted)
- Success: #2e7d32 (green)
- Error: #c62828 (red)

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
