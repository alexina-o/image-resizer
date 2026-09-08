# image-resizer

📝 Release Changelog (v2.0.0-beta)
🚀 New Features
Dual Drop Zones: Split the interface into two distinct staging zones: Packshot / Swatch and Lifestyle. Users can drag images into either or both drop zones in a single session.

Batch Processing Queue: Dropping images into a zone now stages them (showing a live file count badge) rather than triggering immediate download, allowing for multi-preset batch preparation.

Sequential Priority Order: Processing logic guarantees that all files in the Packshot drop zone are processed first, followed directly by files in the Lifestyle drop zone.

Sequential File Renaming:

Added Custom File Prefix input (e.g., SKU_1234).

Added Enable Sequential Numbering toggle (_01, _02, _03, etc.), which numbers across both queues seamlessly.

🔧 Improvements & Presets
Packshot Preset Defaults: Configured with Auto-Trim: Enabled, Resize: 1800x1800, Extent: 2000x2000, and Gravity: Center.

Lifestyle Preset Defaults: Configured with Auto-Trim: Disabled, Resize: 2000x2000, Extent: 2000x2000, and Gravity: Center.

Action Button: Replaced automated auto-download with a unified Process All & Download ZIP trigger button.

Still to do:
Update the naming section inside the Process All click handler in your index.html so every generated filename passes through the sanitizer before being added to JSZip.

Other potential improvements:
1. Canvas & Background Color Controls
Background Color Picker for Extended Canvas: When extending an image to a square canvas (e.g., 2000x2000), PNGs might maintain transparency, but JPEGs default to black background fills if unhandled.

Preset Hex Options: Add quick-select buttons for Pure White (#FFFFFF) (required by Amazon, Google Shopping, and most retailer guidelines) and Off-White / Light Gray (#F5F5F5) alongside a custom color picker.

2. Live Before/After Preview Thumbnail
Visual Verification: Before downloading a batch of 50 images, let users see a live side-by-side preview thumbnail of the first image in the queue (Original vs. Processed with Trim & Extent applied).

Dimension & Aspect Ratio Badge: Show live overlays comparing the original dimensions (e.g., 3400x1200) and output dimensions (e.g., 2000x2000) so merchandisers can instantly spot awkward crops or heavy stretching.

3. Smart Quality & File Size Controls
Ecommerce Compression Slider: Large PNG files slow down PDP load speeds and hurt Mobile Web Vitals (SEO). Add a quality/compression selector (e.g., Web Optimized (85%) vs. Lossless / High Quality).

Target File Size Warning: Add a check to highlight or warn if any processed image exceeds typical marketplace upload limits (e.g., > 5 MB).

4. Background Fill & Swatch Padding Control
Trim Padding Slider (0–10%): Standard img.trim() crops all whitespace right up to the outermost pixel of the product. This can leave zero breathing room around product edges inside the 1800x1800 bounding box.

Padding Margin: Allowing a 2%–5% padding margin keeps products looking naturally centered without touching the canvas edge.

5. Multi-Marketplace Preset Selector
Beyond "Packshot" and "Lifestyle", ecommerce teams often need specific export specs for different sales channels. Add dropdown presets for:

Shopify / BigCommerce Standard: 2000x2000 White background.

Amazon Main Image: 1000x1000 to 2500x2500, Pure White (#FFFFFF), product occupying 85%+ of frame.

Social / Instagram Catalog: 1080x1350 (4:5 vertical).

6. Quick Action Queue Management
Clear Queue / Reset Buttons: Individual trash icons on the drop zones to clear staged files without refreshing the browser tab.

Drag-to-Reorder: Ability to reorder queued thumbnails inside the staging zone if a specific hero image needs to be forced to position _01.
