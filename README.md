<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://github.com/user-attachments/assets/0aa67016-6eaf-458a-adb2-6e31a0763ed6" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally.

View your app in AI Studio: https://ai.studio/apps/drive/1qqCdWYZjwEJZDgEWQJLVVYXRpUCqjYOK

## Run Locally

**Prerequisites:**  Node.js

1. Install dependencies:
   `npm install`
2. Run the app:
   `npm run dev`

## Analytics Setup (Optional)

This app includes Google Analytics 4 for visitor tracking.

1. **Create a GA4 Property:**
   - Go to [Google Analytics](https://analytics.google.com)
   - Create a new GA4 property
   - Get your Measurement ID (format: `G-XXXXXXXXXX`)

2. **Add your Measurement ID:**
   - Open `index.html`
   - Replace both instances of `G-XXXXXXXXXX` with your actual Measurement ID

3. **What you'll track:**
   - Page views and sessions
   - Visitor location and device info
   - Time spent on site
   - Real-time visitors
   - **Slide-by-slide progression** (which of the 29 slides users view)
   - Report opens

## Viewing Slide Analytics in GA4

Your app tracks custom events for each slide view. To see this data:

1. Go to **Reports** → **Engagement** → **Events** in GA4
2. Look for the `slide_view` event
3. Click on it to see:
   - Which slides get the most views
   - Where users drop off
   - Slide completion rate (slide 29 views / slide 1 views)
4. For detailed analysis, go to **Explore** and create a custom report with:
   - **Dimension:** `slide_number`, `slide_theme`, `slide_headline`
   - **Metric:** `Event count`

Each slide view includes:
- `slide_number` (1-29)
- `slide_theme` (Intro, Market, Commercial, R&D, 2026, Closing)
- `slide_headline` (the main text on each slide)
- `slide_type` (intro, reveal-scroll, numeric, etc.)
