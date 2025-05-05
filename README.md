How to Build the Button Structure in Webflow

Follow this structure for each copy instance. Use desktop classes or mobile classes depending on your viewport.

DESKTOP STRUCTURE:

Div with class: copy-wrap
→ Div with class: copy-text (example: SPIR)
→ Div with class: copy-btn
→ Image with class: copy-icon
→ Div with class: copy-label (text: Copy)

MOBILE STRUCTURE:

Div with class: copy-wrap-mob
→ Div with class: exchange-label (example: CSE:)
→ Div with class: copy-text-mob (example: SPIR)
→ Div with class: copy-btn-mob
→ Image with class: copy-icon
→ Div with class: copy-label (text: Copy)

Important Notes:

You only need to change the copy-text or copy-text-mob text.

The JavaScript automatically detects and copies the nearest label.

copy-label changes to say “Copied!” when clicked.

You can optionally wrap the button in a div with class: copy-pulse for animations.

How It Works:

On click, the button finds the adjacent ticker text and copies it.

Uses navigator.clipboard.writeText() for modern browser support.

Label updates to “Copied!” and resets after 1.2 seconds.

Optional CSS can handle transitions or color feedback.

Deployment Options:

CDN via jsDelivr:

<script src="https://cdn.jsdelivr.net/gh/alturamediaco/lp-copy-button/copy-button-init.js"></script>
Webflow Manual Setup:
Paste the script into Webflow Page Settings → Before </body> tag.

Internal Notes:

Developed by: Altura Media Co.

Use for any Webflow landing page with ticker copy buttons.

Keep the layout consistent between desktop and mobile.

Optional: Add your own CSS file for hover or active styles.

