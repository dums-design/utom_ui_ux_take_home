# Quick Reference Guide

**Keep this handy while working! ⚡**

---

## ⏱️ Time Budget (3 hours total)

| Task | Time | Priority |
|------|------|----------|
| Read all docs | 20 min | MUST DO |
| Landing page | 40 min | HIGH |
| Movie details | 30 min | HIGH |
| Browse page | 25 min | MEDIUM |
| Search results | 20 min | MEDIUM |
| Watchlist | 20 min | MEDIUM |
| Polish & QA | 20 min | HIGH |
| Write README | 10 min | MUST DO |

**Pro tip**: Better to have 3 polished pages than 5 mediocre ones!

---

## 📋 Pre-Flight Checklist

Before you start coding:

- [ ] Read `task_instructions.md` completely
- [ ] Open `design_guide.html` in browser (keep it open!)
- [ ] Review `ui_screens.md` for each page
- [ ] Skim `product_requirements.md` for context
- [ ] Check `ai_prompting_guide.md` for tips
- [ ] Review `evaluation_criteria.md` (know how you'll be judged!)

---

## 🚀 The Cursor Workflow (Core Approach)

### For Each Page:

1. **Provide Context**
   ```
   @design_guide.html @product_requirements.md @ui_screens.md
   ```
   Tell Cursor which page you want to build

2. **AI Analyzes & Creates**
   - AI understands design system, product goals, and page requirements
   - AI generates initial HTML prototype

3. **You Review**
   - Open in browser
   - Identify what needs improvement

4. **Iterate in Batches**
   ```
   @[page].html @design_guide.html
   
   Please make these improvements:
   - [Design fixes]
   - [Interaction improvements]
   - [Content updates]
   ```

5. **Repeat Until Polished**
   - Keep iterating until page feels excellent
   - Move to next page

### Key: Always attach @design_guide.html for consistency!

---

## 🎨 Essential Design Tokens

**Copy these into every HTML file:**

```css
:root {
  /* Core Colors */
  --cm-deep-blue: #2C5F87;
  --cm-coral-red: #E94B3C;
  --cm-charcoal: #1A1D23;
  --cm-dark-bg: #0F1419;
  --cm-light-gray: #F5F5F5;
  --cm-pearl: #FFFFFF;
  
  /* Fonts */
  --font-display: 'Playfair Display', serif;
  --font-primary: 'Inter', sans-serif;
  
  /* Spacing */
  --space-md: 16px;
  --space-lg: 24px;
  --space-xl: 32px;
  
  /* Animation */
  --anim-normal: 0.3s;
  --ease-out: cubic-bezier(0.25, 1, 0.5, 1);
  
  /* Shadows */
  --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.1);
  --shadow-md: 0 4px 12px rgba(0, 0, 0, 0.15);
  --shadow-lg: 0 8px 24px rgba(0, 0, 0, 0.2);
}
```

---

## 🎯 Must-Have Features Per Page

### Landing (`landing.html`)
- ✅ Hero with search bar
- ✅ Trending carousel
- ✅ Curated collections
- ✅ Working navigation

### Browse (`browse.html`)
- ✅ Filter sidebar
- ✅ Movie grid
- ✅ Sort controls
- ✅ Active filters display

### Movie Details (`movie_details.html`)
- ✅ Hero backdrop
- ✅ Movie info panel
- ✅ Plot synopsis
- ✅ Add to Watchlist button

### Watchlist (`watchlist.html`)
- ✅ Saved movies grid
- ✅ Empty state
- ✅ Remove functionality
- ✅ Sort options

### Search Results (`search_results.html`)
- ✅ Search bar
- ✅ Results grid
- ✅ Results count
- ✅ No results state

---

## 💡 Cursor Prompting Cheat Sheet

### First Page Setup (Landing):
```
@design_guide.html @product_requirements.md @ui_screens.md

I want to build HTML prototype pages for CineMatch. Let's start with the landing page.

Please:
1. Analyze these files to understand the design system, product goals, and page requirements
2. Create a complete standalone HTML file for the landing page with inline CSS
3. Follow the design guide exactly (colors, fonts, spacing)
4. Include all sections specified in ui_screens.md for the landing page

After you create it, I'll review and give you improvement requests.
```

### Iterative Improvements (Batched):
```
@landing.html @design_guide.html

Please make these improvements:

DESIGN:
- Increase hero section height and make headline more dramatic
- Add smooth hover effects to movie cards (lift 8px, shadow increase)
- Adjust spacing between sections to 48px

INTERACTIONS:
- Add 0.3s ease-out transitions to all interactive elements
- Create modal for "Add to Watchlist" with fade-in animation
- Add smooth carousel scroll behavior

CONTENT:
- Generate 12 popular movie entries with realistic titles
- Use Pexels placeholder images for posters
- Add genre tags and ratings to all cards
```

### Building Next Page (Reuse Components):
```
@landing.html

Please analyze this page and extract/describe all reusable components:
- Navigation header
- Movie card component
- Footer
- Any other reusable elements

I want to reuse these across other pages.
```

```
@design_guide.html @ui_screens.md @landing.html

Now create the [NEXT PAGE] page:
1. Reuse navigation and footer from landing.html exactly
2. Reuse movie card component styling
3. Add the specific sections required for this page from ui_screens.md
4. Maintain consistency with landing page
```

---

## ✨ Must-Have Interactions

Every page needs:

- ✅ **Hover states** on all interactive elements
- ✅ **Smooth transitions** (0.3s ease-out)
- ✅ **Consistent styling** with design guide
- ✅ **Focus states** on inputs/buttons
- ✅ **Card lift effect** on hover (transform + shadow)
- ✅ **Smooth animations** for modals and interactions

### Example Hover Effect:
```css
.movie-card {
  transition: all 0.3s cubic-bezier(0.25, 1, 0.5, 1);
}
.movie-card:hover {
  transform: translateY(-8px);
  box-shadow: 0 8px 24px rgba(0, 0, 0, 0.2);
}
```

### Key Cursor Tips:
- ⚡ **Always attach @design_guide.html** - Every single conversation
- 📦 **Batch your improvement requests** - Save free credits
- 🔁 **Extract components before building page 2** - Ensure consistency
- 🎨 **Review in browser between iterations** - Catch issues early

---

## 🚨 Common Mistakes to Avoid

❌ **Don't**: Forget to attach @design_guide.html  
✅ **Do**: Attach it in EVERY Cursor conversation

❌ **Don't**: Make multiple small requests  
✅ **Do**: Batch improvements to save credits

❌ **Don't**: Use random colors not in design guide  
✅ **Do**: Always use CSS variables (--cm-deep-blue, etc.)

❌ **Don't**: Skip hover states  
✅ **Do**: Add smooth transitions on all interactive elements

❌ **Don't**: Use different fonts across pages  
✅ **Do**: Consistently use Inter and Playfair Display

❌ **Don't**: Build page 2 without extracting components first  
✅ **Do**: Have Cursor analyze page 1 for reusable components

❌ **Don't**: Submit without testing in browser  
✅ **Do**: Open each page and check it looks polished

---

## 🎬 Sample Movie Data

Use these for your prototype:

1. **Inception** (2010) - Sci-Fi, Thriller - ⭐ 8.8
2. **The Shawshank Redemption** (1994) - Drama - ⭐ 9.3
3. **The Dark Knight** (2008) - Action, Crime - ⭐ 9.0
4. **Pulp Fiction** (1994) - Crime, Drama - ⭐ 8.9
5. **Interstellar** (2014) - Sci-Fi, Adventure - ⭐ 8.7
6. **The Matrix** (1999) - Sci-Fi, Action - ⭐ 8.7
7. **Parasite** (2019) - Thriller, Drama - ⭐ 8.5
8. **La La Land** (2016) - Musical, Romance - ⭐ 8.0
9. **Get Out** (2017) - Horror, Thriller - ⭐ 7.7
10. **Mad Max: Fury Road** (2015) - Action - ⭐ 8.1

---

## 📦 Submission Checklist

Before submitting, verify:

- [ ] All HTML files present and named correctly (aim for 3-5 pages)
- [ ] `[YourName]_README.md` included with your approach
- [ ] Design system colors used consistently across all pages
- [ ] No console errors in DevTools
- [ ] Hover states and smooth transitions on all interactive elements
- [ ] Each page looks polished when opened in browser
- [ ] Components are consistent across pages (nav, footer, cards)
- [ ] Files organized in folder named `[YourName]_cinematch_prototype`

---

## 🆘 If You Get Stuck

1. **Attach @design_guide.html again** - Cursor may have forgotten
2. **Review ui_screens.md** - Detailed specs for each page
3. **Check ai_prompting_guide.md** - Full Cursor workflow examples
4. **Ask Cursor for help** - "What's wrong with this design?" 
5. **Simplify** - Better to do 3 pages really well than 5 poorly
6. **Take a breath** - Open page in browser, make a list, then batch fixes

### Quick Debug Prompt:
```
@[your-page].html @design_guide.html

Please review this page and identify:
1. What doesn't match the design guide
2. Missing or weak interactions
3. Spacing or alignment issues
4. Content that needs improvement

Then fix all issues.
```

---

## 📊 Evaluation Breakdown

You're being judged on 5 equal dimensions (20% each):

1. **Cursor Leverage** - Effective use of Cursor with file context, component reuse, and documented workflow
2. **Design System** - Perfect consistency with design guide across all pages
3. **Visual Design** - Modern aesthetics, polish, and attention to detail
4. **Interactions** - Smooth animations, hover states, and delightful UX
5. **Technical** - Clean code, no console errors, professional implementation

**Minimum target**: 75+ points (Good submission)  
**Stretch goal**: 90+ points (Excellent submission)

### What "Excellent" Looks Like:
- 🎯 Landing page is stunning and sets clear design language
- 🔄 Components are extracted and reused across pages
- 📦 Every Cursor conversation shows @design_guide.html attached
- ✨ All interactions are smooth and polished
- 📝 README clearly documents the Cursor workflow used

---

## ⚡ Speed Tips for Cursor Workflow

### The Efficient Process:
1. **Page 1 (Landing)** - Establish design language (40 min)
   - Attach: @design_guide.html @product_requirements.md @ui_screens.md
   - Get initial version, then batch improvements
   
2. **Extract Components** - Before page 2 (5 min)
   - Attach: @landing.html
   - Ask Cursor to describe all reusable components
   
3. **Pages 2-5** - Faster with reuse (20-30 min each)
   - Attach: @design_guide.html @ui_screens.md @landing.html
   - Tell Cursor to reuse extracted components
   - Focus on unique page-specific sections

### Maximize Your Free Credits:
- ✅ Batch 4-5 improvements into one message
- ✅ Be specific to avoid back-and-forth
- ✅ Review in browser before next request
- ✅ Manually fix tiny CSS tweaks
- ❌ Don't ask Cursor for one change at a time

### Test as You Go:
- Open HTML in browser after each major iteration
- Check that design matches design guide
- Test hover effects as you add them
- Fix issues immediately (easier than later)

---

## 🎯 Success Formula

```
Great Submission = 
  Always Attach @design_guide.html (consistency!)
  + Batch Your Improvement Requests (save credits)
  + Extract & Reuse Components (efficiency)
  + Smooth Interactions (hover, transitions)
  + Attention to Detail (alignment, spacing)
  + Strategic Cursor Use (documented in README)
  + Time Management (3 hours max!)
```

### Priority Ranking:
1. 🥇 **Landing Page** - Must be excellent (40 min)
2. 🥈 **Movie Details** - Core to product (30 min)
3. 🥉 **One More Page** - Shows consistency (25 min)
4. 📝 **README** - Documents your process (10 min)
5. ⭐ **Bonus Pages** - If time allows

---

**Good luck! You've got this! 🎬✨**

*Remember: Quality > Quantity. Better 3 polished pages than 5 mediocre ones!*

