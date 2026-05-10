# Murphy Campaign PDF - Ad Tracking Guide

## How It Works

Since PDFs can't execute Google Analytics code, we use a redirect page:
1. User clicks your ad link → goes to tracking page
2. Tracking page logs the source in Google Analytics
3. User is automatically redirected to the PDF (0.5 second delay)
4. User sees "Loading..." briefly, then gets the PDF

## Tracking Links for Each Ad Location

Use these unique URLs for each advertising placement:

1. **Facebook/Social Media Ad:**
   ```
   https://niallgalway.github.io/murphy-redirect.html?source=facebook
   ```

2. **Print/Newspaper Ad (QR Code):**
   ```
   https://niallgalway.github.io/murphy-redirect.html?source=print
   ```

3. **Instagram Ad:**
   ```
   https://niallgalway.github.io/murphy-redirect.html?source=instagram
   ```

## How to View Results in Google Analytics

### Real-time (Immediate Results):
1. Log into Google Analytics (GA4) at analytics.google.com
2. Go to **Reports** → **Realtime** → **Overview**
3. Click on any test link and you'll see it appear within seconds
4. Look for the event "murphy_pdf_view"

### Full Reports (24 hours later):
1. Go to **Reports** → **Engagement** → **Events**
2. Look for the event named "murphy_pdf_view"
3. Click on it to see breakdown by source
4. You'll see: facebook, print, instagram as separate entries with counts

## QR Codes for Print Ads

For print ads, create QR codes that point to these tracked URLs:
- Use a QR generator like qr-code-generator.com
- Generate a QR for each print location with its unique tracking URL
- This way you can tell which newspaper/poster location performs best

## Notes

- The parameters don't affect the PDF itself - they're just logged by Google Analytics
- All three URLs point to the same murphy.pdf file
- Results appear in real-time in GA4 (with ~24hr delay for full processing)
