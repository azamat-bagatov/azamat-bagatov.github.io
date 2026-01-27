# Book Landing Page - Setup Instructions

## What You Have
A professional, mobile-friendly landing page for your book with:
- Clean, modern design
- Book cover display area
- Description sections
- Shopify Buy Button integration area
- About the author section
- Fully responsive (works on phones, tablets, desktops)

## How to Customize

### 1. Replace Placeholder Text
Open `index.html` and update these sections:

**Line 45:** Your book title
```html
<h1>Your Book Title Here</h1>
```

**Line 46:** Your subtitle
```html
<p class="subtitle">A compelling subtitle that hooks your readers</p>
```

**Lines 56-65:** Book description (3 paragraphs)

**Lines 68-73:** Key benefits/insights list

**Lines 107-113:** About the author section

**Line 117:** Copyright info

### 2. Add Your Book Cover Image

**Option A - Upload your image to GitHub:**
1. Upload your book cover to your GitHub repository
2. Name it something like `book-cover.jpg`
3. Replace line 54:
```html
<img src="book-cover.jpg" alt="Your Book Title">
```

**Option B - Use an external image host:**
Replace the image source with your image URL:
```html
<img src="https://yourimage.url/cover.jpg" alt="Your Book Title">
```

### 3. Add Your Shopify Buy Button

1. **Get your Buy Button code:**
   - Log into Shopify admin
   - Go to: Sales channels > Buy Button (or install the app if needed)
   - Create a Buy Button for your product
   - Copy the generated embed code

2. **Add it to your page:**
   - Find the comment on line 86 that says "REPLACE THIS SECTION"
   - Delete the placeholder button (lines 101-106)
   - Paste your Shopify embed code in its place

The Shopify code will look something like:
```html
<div id='product-component-1234567890'></div>
<script type="text/javascript">
  // Shopify's generated JavaScript code
</script>
```

## How to Deploy on GitHub Pages

### Step 1: Create GitHub Account
Go to github.com and sign up (if you don't have an account)

### Step 2: Create Repository
1. Click "New repository" (green button)
2. Name it: `yourusername.github.io` (use your actual GitHub username)
3. Make it Public
4. Click "Create repository"

### Step 3: Upload Your File
1. Click "uploading an existing file"
2. Drag and drop your `index.html` file
3. Scroll down and click "Commit changes"

### Step 4: Enable GitHub Pages
1. Go to repository Settings
2. Scroll to "Pages" section (left sidebar)
3. Under "Source" select "main" branch
4. Click Save

Your site will be live at: `https://yourusername.github.io`

### Step 5: Add Custom Domain (Optional)

1. **In GitHub:**
   - Go to Settings > Pages
   - Under "Custom domain" enter your domain (e.g., `yourbook.com`)
   - Click Save

2. **In Your Domain Registrar (Namecheap/Porkbun):**
   
   **Option A - Using A Records (recommended):**
   Add these A records pointing to:
   ```
   185.199.108.153
   185.199.109.153
   185.199.110.153
   185.199.111.153
   ```

   **Option B - Using CNAME:**
   Create a CNAME record pointing to: `yourusername.github.io`

3. **Wait:** DNS changes can take up to 24 hours to propagate

4. **Enable HTTPS:** Back in GitHub Pages settings, check "Enforce HTTPS"

## Customization Tips

### Change Colors
The main colors are defined in the CSS:
- Primary green: `#5E8E3E` (Buy button)
- Dark text: `#1a1a1a`
- Light background: `#f9f9f9`

Search for these in the file and replace with your preferred colors.

### Adjust Layout
The page is responsive and will automatically adjust for mobile devices.

### Add More Sections
You can duplicate the `.about-author` or `.features` sections and customize them for:
- Testimonials/Reviews
- Sample chapters
- FAQs
- Press mentions

## Need Help?

Common issues:
- **Image not showing?** Check the file path and make sure the image is uploaded
- **Shopify button not working?** Make sure you copied the entire script code
- **Domain not working?** DNS can take 24 hours; check your A records are correct

## Files Included
- `index.html` - Your landing page (this is all you need!)

Good luck with your book launch! 🚀
