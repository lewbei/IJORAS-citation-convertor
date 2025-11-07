# Testing Checklist for IJORAS Citation Converter

## Pre-Deployment Testing

### ✅ Basic Functionality Tests

#### 1. Page Load
- [ ] Open `index.html` in Chrome
- [ ] Open `index.html` in Firefox
- [ ] Open `index.html` in Safari
- [ ] No console errors on load
- [ ] All UI elements render correctly
- [ ] Dark mode toggle visible
- [ ] Stats show "0" initially

#### 2. API Key Management
- [ ] Enter API key in the field
- [ ] Click "Save Key" button
- [ ] See success notification
- [ ] Refresh page - API key persists
- [ ] Click "Show/Hide" - key visibility toggles
- [ ] Try to convert without API key - see error message

#### 3. Reference Conversion
- [ ] Click "Load Example" button
- [ ] Input counter updates (should show 3)
- [ ] Click "Convert References"
- [ ] Loading spinner appears
- [ ] Output appears in right panel
- [ ] Output counter updates
- [ ] References are properly formatted
- [ ] Italics render correctly

#### 4. Export Functions
- [ ] Click "Copy to Clipboard"
- [ ] See success notification
- [ ] Paste somewhere to verify it copied
- [ ] Click "Export TXT"
- [ ] TXT file downloads
- [ ] Open TXT file - content is correct
- [ ] Click "Export HTML"
- [ ] HTML file downloads
- [ ] Open HTML file in browser - formatting preserved

#### 5. Clear Functions
- [ ] Click "Clear" in input section
- [ ] Confirm dialog appears
- [ ] Input clears
- [ ] Input counter resets to 0
- [ ] Click "Clear" in output section
- [ ] Output clears
- [ ] Output counter resets to 0

---

### ⌨️ Keyboard Shortcuts Tests

#### Windows/Linux (Use Ctrl)
- [ ] `Ctrl + Enter` - Converts references
- [ ] `Ctrl + K` - Clears input (with confirmation)
- [ ] `Ctrl + L` - Loads example
- [ ] `Ctrl + D` - Toggles dark mode
- [ ] `Ctrl + Shift + C` - Copies output
- [ ] `Ctrl + S` - Saves API key (prevents browser save dialog)
- [ ] `F1` - Shows keyboard shortcuts alert

#### Mac (Use ⌘)
- [ ] `⌘ + Enter` - Converts references
- [ ] `⌘ + K` - Clears input
- [ ] `⌘ + L` - Loads example
- [ ] `⌘ + D` - Toggles dark mode
- [ ] `⌘ + Shift + C` - Copies output
- [ ] `⌘ + S` - Saves API key
- [ ] `F1` - Shows keyboard shortcuts

---

### 🌓 Dark Mode Tests

- [ ] Toggle dark mode ON
- [ ] All colors change appropriately
- [ ] Text is readable
- [ ] Buttons have proper contrast
- [ ] Input fields are visible
- [ ] Refresh page - dark mode persists
- [ ] Toggle dark mode OFF
- [ ] Returns to light theme
- [ ] All elements render correctly

---

### 📱 Responsive Design Tests

#### Mobile (375px width)
- [ ] Layout stacks vertically
- [ ] All buttons are tappable
- [ ] Text is readable
- [ ] No horizontal scroll
- [ ] API key input fits screen
- [ ] Textareas are usable
- [ ] Notifications appear correctly

#### Tablet (768px width)
- [ ] Layout appropriate for screen size
- [ ] All elements accessible
- [ ] Good use of space
- [ ] No UI overlap

#### Desktop (1920px width)
- [ ] Side-by-side panels work
- [ ] Good spacing and padding
- [ ] Content centered
- [ ] No weird stretching

---

### 🔔 Notifications Tests

- [ ] Success notification (green) for successful actions
- [ ] Error notification (red) for errors
- [ ] Warning notification (yellow) for warnings
- [ ] Notifications auto-dismiss after 3 seconds
- [ ] Notification animation smooth
- [ ] Multiple notifications don't overlap
- [ ] Welcome message appears on first load
- [ ] Welcome message doesn't repeat in same session

---

### 🔐 Security Tests

- [ ] API key not visible in page source
- [ ] API key stored in localStorage only
- [ ] No API key in URL
- [ ] No sensitive data in console logs
- [ ] Input sanitized (try entering `<script>alert('XSS')</script>`)
- [ ] No XSS vulnerabilities

---

### 🌐 API Integration Tests

#### With Valid API Key
- [ ] References convert successfully
- [ ] Output formatted correctly
- [ ] DOIs converted to links
- [ ] Author names formatted properly
- [ ] Italics applied to journal names
- [ ] Year extracted correctly
- [ ] Complex references handled

#### With Invalid API Key
- [ ] Clear error message
- [ ] User notified of invalid key
- [ ] No crash

#### Rate Limiting
- [ ] Convert 10 times rapidly
- [ ] If rate limited, see appropriate message
- [ ] Application handles gracefully

#### Network Issues
- [ ] Disconnect internet
- [ ] Try to convert
- [ ] See network error message
- [ ] Reconnect internet
- [ ] Try again - works

---

### 🎨 UI/UX Tests

#### Visual Elements
- [ ] Fonts load correctly
- [ ] Icons display properly
- [ ] Colors match design
- [ ] Shadows render
- [ ] Border radius applied
- [ ] Spacing consistent

#### Interactions
- [ ] Buttons have hover effects
- [ ] Buttons show active state on click
- [ ] Disabled states work correctly
- [ ] Focus states visible (for accessibility)
- [ ] Smooth transitions
- [ ] Loading states clear

#### Help Section
- [ ] Opens/closes correctly
- [ ] All text readable
- [ ] Examples formatted properly
- [ ] Keyboard shortcuts list visible

---

### ♿ Accessibility Tests

- [ ] Tab through all interactive elements
- [ ] Tab order makes sense
- [ ] Focus indicators visible
- [ ] Can use keyboard only (no mouse)
- [ ] Screen reader friendly (test with NVDA/JAWS if possible)
- [ ] Color contrast meets WCAG standards
- [ ] Alt text on images (if any)

---

### 🐛 Edge Cases & Error Handling

#### Empty Inputs
- [ ] Try to convert with no input
- [ ] Appropriate error message
- [ ] No crash

#### Very Large Input
- [ ] Paste 100+ references
- [ ] Application handles it
- [ ] Performance acceptable
- [ ] No browser freeze

#### Special Characters
- [ ] Input with emoji
- [ ] Input with unicode characters
- [ ] Input with HTML entities
- [ ] All handled correctly

#### Browser Storage
- [ ] Clear localStorage
- [ ] Page still works
- [ ] API key prompt shown
- [ ] Clear sessionStorage
- [ ] Welcome message appears again

---

### 🔄 Cross-Browser Testing

#### Chrome (Latest)
- [ ] All features work
- [ ] No console errors
- [ ] Performance good

#### Firefox (Latest)
- [ ] All features work
- [ ] No console errors
- [ ] Keyboard shortcuts work

#### Safari (Latest)
- [ ] All features work
- [ ] Clipboard API works
- [ ] Dark mode works

#### Edge (Latest)
- [ ] All features work
- [ ] No compatibility issues

---

### 📊 Performance Tests

- [ ] Page loads in < 2 seconds
- [ ] API response in < 5 seconds
- [ ] Smooth animations (60fps)
- [ ] No memory leaks (test with DevTools)
- [ ] File exports instant
- [ ] No lag when typing

---

### 📝 Content Tests

- [ ] All text is spelled correctly
- [ ] No lorem ipsum placeholders
- [ ] Links work (Help section, footer)
- [ ] Example references are real
- [ ] Documentation links work
- [ ] GitHub link correct

---

## Post-Deployment Tests

### GitHub Pages
- [ ] Site loads at GitHub Pages URL
- [ ] All features work on live site
- [ ] HTTPS enabled
- [ ] No mixed content warnings
- [ ] Fast loading (CDN working)
- [ ] Mobile works on live site

### SEO & Metadata
- [ ] Page title correct
- [ ] Meta description (if added)
- [ ] Favicon (if added)
- [ ] Open Graph tags (optional)

---

## Critical Issues (Must Fix Before Deploy)

- [ ] No console errors
- [ ] All core features work
- [ ] No security vulnerabilities
- [ ] Responsive on mobile
- [ ] Cross-browser compatible

## Nice to Have (Can Fix After Deploy)

- [ ] Perfect pixel alignment
- [ ] Advanced animations
- [ ] Additional export formats
- [ ] More keyboard shortcuts

---

## Testing Sign-Off

**Tester Name:** ___________________
**Date:** ___________________
**Browser Tested:** ___________________
**Device:** ___________________

**Overall Status:**
- [ ] ✅ Ready to Deploy
- [ ] ⚠️ Minor Issues (deploy anyway)
- [ ] ❌ Critical Issues (fix before deploy)

**Notes:**
_____________________________________________
_____________________________________________
_____________________________________________

---

## Quick Test (5 Minutes)

If you're short on time, test these critical items:

1. ✅ Page loads without errors
2. ✅ Load example works
3. ✅ Convert references works (with API key)
4. ✅ Copy to clipboard works
5. ✅ Dark mode toggles
6. ✅ Keyboard shortcut (Ctrl/⌘ + Enter) works
7. ✅ Mobile responsive
8. ✅ No console errors

If all 8 pass ✅ - You're good to deploy!

---

**Last Updated:** 2025-11-07
**Version:** 2.0
