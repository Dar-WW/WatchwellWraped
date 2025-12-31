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
