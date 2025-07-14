# Accessibility Testing Guide

## Quick Verification for WCAG 2.2 Compliance

### 🎯 Keyboard Navigation Testing (5 minutes)

1. **Tab through the entire form:**
   - Press `Tab` to move forward through all interactive elements
   - Press `Shift+Tab` to move backward
   - Verify each element receives a **visible focus indicator** (blue outline)
   - Ensure no elements are skipped or trapped

2. **Test the skip link:**
   - Press `Tab` immediately after page loads
   - You should see "Skip to main content" appear at the top
   - Press `Enter` to activate and verify it jumps to the form

3. **Form interaction:**
   - Fill out required fields using only the keyboard
   - Use `Space` to check checkboxes and radio buttons
   - Use arrow keys within radio button groups
   - Submit the form with `Enter` key

### 🎯 Focus Visibility Testing (2 minutes)

**✅ What to look for:**
- **Blue outline** (`3px solid #0066cc`) around form inputs when focused
- **Yellow outline** (`3px solid #ffd700`) around the submit button when focused
- **2px offset** between the element and the focus indicator
- Focus indicators should **never be completely hidden**

**❌ Red flags:**
- No visible focus indicator
- Focus indicator is too thin or hard to see
- Focus indicator is cut off or obscured

### 🎯 Target Size Testing (3 minutes)

Use browser developer tools to verify:

1. **Form inputs:** Should be at least 48px tall
2. **Submit button:** Should be at least 56px tall  
3. **Checkboxes/Radio buttons:** 20px × 20px with 48px clickable area
4. **Touch testing:** On mobile, all elements should be easy to tap accurately

### 🎯 Color Contrast Testing (3 minutes)

**Automated check:**
- Use browser extension like "axe DevTools" or "WAVE"
- Look for any contrast failures

**Visual check:**
- All text should be clearly readable
- Error messages in red should still be legible
- Help text in gray should meet 4.5:1 contrast ratio

### 🎯 Form Validation Testing (5 minutes)

1. **Submit empty form:**
   - Click submit without filling anything
   - Verify error messages appear with clear text
   - Focus should move to the first error field
   - Error messages should be announced by screen readers

2. **Test specific validation:**
   - Enter invalid email (e.g., "invalid.email")
   - Enter invalid URL (e.g., "not-a-url")
   - Verify specific, helpful error messages

3. **Test success states:**
   - Fill out required fields correctly
   - Verify successful submission feedback

### 🎯 Screen Reader Testing (Optional, 10 minutes)

**For Windows users with NVDA (free):**
1. Download NVDA screen reader
2. Navigate the form with NVDA running
3. Verify all labels, help text, and error messages are announced
4. Check that form structure (sections, fieldsets) is properly conveyed

**For Mac users:**
1. Enable VoiceOver (Cmd+F5)
2. Navigate with VoiceOver controls
3. Verify proper announcements

### 🎯 Mobile Testing (5 minutes)

1. **Touch targets:**
   - All buttons and inputs should be easy to tap
   - No accidental taps on nearby elements

2. **Responsive behavior:**
   - Form should work well on small screens
   - No horizontal scrolling required
   - Text should remain readable when zoomed to 200%

### 🎯 Browser Testing

**Test in multiple browsers:**
- Chrome/Edge: Primary testing
- Firefox: Alternative engine testing
- Safari: WebKit testing (especially on mobile)

### 🎯 Automated Testing Tools

**Browser Extensions:**
- **axe DevTools**: Comprehensive accessibility testing
- **WAVE**: Web Accessibility Evaluation Tool
- **Lighthouse**: Built into Chrome DevTools

**Online Tools:**
- **WebAIM WAVE**: https://wave.webaim.org/
- **Colour Contrast Analyser**: For manual contrast checking

### 🎯 Quick Checklist Summary

- [ ] All interactive elements are keyboard accessible
- [ ] Focus indicators are clearly visible (3px blue/yellow outlines)
- [ ] Skip link appears and works correctly
- [ ] All form inputs have proper labels and help text
- [ ] Error messages are clear and specific
- [ ] Form validates properly with helpful feedback
- [ ] Target sizes meet 24px minimum (forms exceed this)
- [ ] Color contrast meets 4.5:1 ratio for AA compliance
- [ ] Form works on mobile devices with touch
- [ ] No accessibility errors in automated testing tools

### 🎯 Expected Results

**✅ WCAG 2.2 AA Compliant form should:**
- Pass all automated accessibility tests
- Be fully usable with keyboard only
- Work with screen readers
- Have clear, visible focus indicators
- Provide helpful error messages
- Meet all color contrast requirements
- Have appropriate target sizes for all interactive elements

**🔍 If you find issues:**
1. Document the specific problem
2. Note which browser/device
3. Check if it affects keyboard users or screen reader users
4. Consider if it violates any specific WCAG criteria

This form has been designed to exceed WCAG 2.2 AA requirements, so it should pass all these tests with flying colors! 🌟