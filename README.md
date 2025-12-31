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

Your app tracks two custom events:

### 1. Slide Views (`slide_view`)
**What:** Tracks which slides users reach  
**Go to:** Reports → Engagement → Events → `slide_view`

### 2. Slide Duration (`slide_duration`)  
**What:** Time spent on each slide (capped at 60 seconds to avoid outliers)  
**Go to:** Reports → Engagement → Events → `slide_duration`

### See Duration Statistics (Median/Percentiles):

1. Go to **Explore** → Create new exploration
2. Select **"Free form"**
3. Add **Dimensions:** `slide_number`, `slide_theme`
4. Add **Metrics:** 
   - `Event count` (how many views)
   - `duration_seconds` (select aggregation: **Median**, Average, or Percentile)
5. You'll see: "Slide 1: Median 5.2 seconds, Slide 5: Median 8.7 seconds"

### Key Insights You Can Track:
- 📊 **Which slides users reach** (drop-off rate)
- ⏱️ **Time spent per slide** (engagement)
- 📈 **Completion rate**: Slide 29 views / Slide 1 views
- 🔥 **Most engaging slides**: Longest median duration
- 📉 **Quick skip slides**: Very short duration = not interesting

**Note:** Durations are capped at 60 seconds to filter out users who leave tabs open.
