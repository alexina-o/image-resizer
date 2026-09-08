# image-resizer
Resizes images for use on PDPs

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
