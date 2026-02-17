# 📸 Quick Guide: Adding Your Photo & Certifications

This guide will help you easily add your profile photo and certification images to your portfolio.

---

## 🖼️ Adding Your Profile Photo

### Method 1: Using Your Own Photo (Recommended)

1. **Prepare your photo:**
   - Use a professional headshot or a clear photo of yourself
   - Recommended format: JPG or PNG
   - Recommended size: 500x500 pixels (square) for best results
   - File size: Keep under 500KB for fast loading

2. **Save your photo:**
   - Save your photo in the same folder as `index.html`
   - Name it: `profile.jpg` or `profile.png`

3. **Update the HTML:**
   - Open `index.html` in a text editor
   - Find line ~93 (search for "TO ADD YOUR PHOTO")
   - Remove the `<!--` and `-->` around this line:
     ```html
     <img src="profile.jpg" alt="Sujal Dhinakar Raj" class="profile-image">
     ```
   - Add `<!--` before and `-->` after the default div:
     ```html
     <!-- <div class="profile-image"></div> -->
     ```

4. **Save and refresh** your browser to see your photo!

### Final Result Should Look Like:
```html
<!-- <div class="profile-image"></div> -->
<img src="profile.jpg" alt="Sujal Dhinakar Raj" class="profile-image">
```

---

## 📜 Adding Your Certifications

### Step 1: Organize Your Certificate Images

1. **Create a folder** named `certifications` in the same folder as `index.html`

2. **Prepare your certificate images:**
   - Format: JPG or PNG
   - Recommended size: 800x600 pixels minimum
   - File naming: `cert1.jpg`, `cert2.jpg`, `cert3.jpg`, etc.
   - Or use descriptive names: `microsoft-lyzr.jpg`, `data-analytics.jpg`

3. **Save all certificate images** in the `certifications` folder

### Step 2: Add Certificate Cards to HTML

1. **Open `index.html`** in a text editor

2. **Find the Certifications section** (around line 468)

3. **Copy the template card** (it's in the comments):
   ```html
   <div class="certification-card glass-card">
       <div class="cert-image-wrapper">
           <img src="certifications/cert1.jpg" alt="Microsoft Lyzr AI Workshop Certificate" class="cert-image">
           <div class="cert-overlay">
               <a href="certifications/cert1.jpg" target="_blank" class="view-cert-btn">
                   <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                       <path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z" stroke-width="2"/>
                       <circle cx="12" cy="12" r="3" stroke-width="2"/>
                   </svg>
                   View Certificate
               </a>
           </div>
       </div>
       <div class="cert-details">
           <h3>Microsoft Lyzr AI Workshop</h3>
           <p class="cert-issuer">Microsoft & Lyzr AI</p>
           <p class="cert-date">2024</p>
       </div>
   </div>
   ```

4. **Customize each card:**
   - Change `src="certifications/cert1.jpg"` to your image path
   - Update the `alt` text to describe your certificate
   - Change the `<h3>` to your certification name
   - Update `<p class="cert-issuer">` with the issuing organization
   - Update `<p class="cert-date">` with the year

5. **Remove placeholder cards** (optional):
   - Once you add your real certificates, you can delete the three placeholder cards

### Step 3: Add Multiple Certificates

**Example: Adding 3 Certificates**

```html
<div class="certifications-grid">
    <!-- Certificate 1: Microsoft Lyzr AI -->
    <div class="certification-card glass-card">
        <div class="cert-image-wrapper">
            <img src="certifications/microsoft-lyzr.jpg" alt="Microsoft Lyzr AI Workshop" class="cert-image">
            <div class="cert-overlay">
                <a href="certifications/microsoft-lyzr.jpg" target="_blank" class="view-cert-btn">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                        <path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z" stroke-width="2"/>
                        <circle cx="12" cy="12" r="3" stroke-width="2"/>
                    </svg>
                    View Certificate
                </a>
            </div>
        </div>
        <div class="cert-details">
            <h3>Microsoft Lyzr AI Workshop</h3>
            <p class="cert-issuer">Microsoft & Lyzr AI</p>
            <p class="cert-date">2024</p>
        </div>
    </div>

    <!-- Certificate 2: Data Analytics -->
    <div class="certification-card glass-card">
        <div class="cert-image-wrapper">
            <img src="certifications/data-analytics.jpg" alt="Data Analytics Certification" class="cert-image">
            <div class="cert-overlay">
                <a href="certifications/data-analytics.jpg" target="_blank" class="view-cert-btn">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                        <path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z" stroke-width="2"/>
                        <circle cx="12" cy="12" r="3" stroke-width="2"/>
                    </svg>
                    View Certificate
                </a>
            </div>
        </div>
        <div class="cert-details">
            <h3>Data Analytics Professional</h3>
            <p class="cert-issuer">Google Analytics Academy</p>
            <p class="cert-date">2024</p>
        </div>
    </div>

    <!-- Certificate 3: Machine Learning -->
    <div class="certification-card glass-card">
        <div class="cert-image-wrapper">
            <img src="certifications/ml-certification.jpg" alt="Machine Learning Certification" class="cert-image">
            <div class="cert-overlay">
                <a href="certifications/ml-certification.jpg" target="_blank" class="view-cert-btn">
                    <svg width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor">
                        <path d="M1 12s4-8 11-8 11 8 11 8-4 8-11 8-11-8-11-8z" stroke-width="2"/>
                        <circle cx="12" cy="12" r="3" stroke-width="2"/>
                    </svg>
                    View Certificate
                </a>
            </div>
        </div>
        <div class="cert-details">
            <h3>Machine Learning Specialization</h3>
            <p class="cert-issuer">Coursera - Stanford University</p>
            <p class="cert-date">2024</p>
        </div>
    </div>
</div>
```

---

## 📁 Final Folder Structure

Your folder should look like this:

```
frrontend website/
├── index.html
├── styles.css
├── script.js
├── README.md
├── launch.bat
├── profile.jpg (or profile.png) ← Your photo
└── certifications/
    ├── cert1.jpg
    ├── cert2.jpg
    ├── cert3.jpg
    └── ... (more certificates)
```

---

## ✅ Checklist

### Profile Photo:
- [ ] Photo saved as `profile.jpg` or `profile.png`
- [ ] Photo is in the same folder as `index.html`
- [ ] HTML updated to use `<img>` tag
- [ ] Default `<div>` commented out
- [ ] Tested in browser

### Certifications:
- [ ] Created `certifications` folder
- [ ] Certificate images saved in folder
- [ ] Copied template card code
- [ ] Updated image paths
- [ ] Customized certificate details
- [ ] Removed placeholder cards (optional)
- [ ] Tested in browser

---

## 🎨 Image Optimization Tips

### For Profile Photo:
- Use a neutral or professional background
- Ensure good lighting
- Center your face in the frame
- Use editing tools to enhance quality if needed
- Compress image using tools like TinyPNG.com

### For Certificates:
- Scan at 300 DPI for best quality
- Crop to remove excess white space
- Save as JPG (smaller file size) or PNG (better quality)
- Use online tools to compress if file is too large
- Ensure text is readable when zoomed in

---

## 🚀 Quick Test

After adding your images:

1. Open `index.html` in your browser
2. Scroll to the Hero section - Your photo should appear!
3. Scroll to the Certifications section - Your certificates should display!
4. Hover over certificates to see the "View Certificate" button
5. Click to open the full certificate in a new tab

---

## 💡 Pro Tips

1. **High-Quality Images**: Use high-resolution images for professional look
2. **Consistent Naming**: Name files descriptively (e.g., `coursera-ml.jpg`)
3. **Backup**: Keep original certificate files in a separate backup folder
4. **Update Alt Text**: Always use descriptive alt text for accessibility
5. **Test Mobile**: Check how images look on mobile devices

---

## ❓ Troubleshooting

**Photo not showing?**
- Check file name matches exactly (case-sensitive)
- Ensure file is in the correct folder
- Verify HTML changes were saved
- Try hard-refresh browser (Ctrl + F5)

**Certificate not displaying?**
- Check folder name is `certifications` (lowercase, plural)
- Verify image paths are correct
- Ensure HTML is not still commented out
- Check browser console for errors (F12)

**Images too large/slow?**
- Compress images using online tools
- Resize to recommended dimensions
- Convert to JPG format for smaller size

---

## 🎯 Next Steps

After adding your photo and certifications:
1. Update your projects with real project images
2. Add actual GitHub and LinkedIn links
3. Create and link your real resume PDF
4. Deploy your portfolio to Vercel or Netlify

---

**Need Help?** Check the main README.md for more information!

**Built with 💜 by Sujal Dhinakar Raj**
