# AI Prompting Guide: Building Prototypes with Cursor

## Overview

This guide will help you effectively leverage **Cursor** (or similar AI coding assistants) to build high-quality HTML prototypes in the 3-hour time limit. The key is **passing in complete context** and having **conversational iterations** with the AI.

---

## Recommended Tool: Cursor

**Cursor** is an AI-powered code editor that allows you to:
- Chat with AI about your code with full file context
- Attach multiple files to provide complete context
- Iterate conversationally without copying/pasting
- Get real-time code suggestions and edits

**Note**: Free tier has limited credits, so be strategic about your queries!

---

## General Strategy

### The Cursor Workflow:

1. **Start with context** → Pass in all relevant files (design guide, PRD, UI specs)
2. **Use generic prompts** → Start with a proven prompt template
3. **Iterate conversationally** → Refine through back-and-forth dialogue
4. **Extract and reuse** → Get AI to identify components for reuse across pages
5. **Polish iteratively** → Keep refining until satisfied (but watch your credits!)

### Time Allocation:
- 🏗️ **70% of time**: Generating and refining with AI in Cursor
- 🎨 **20% of time**: Visual review and tweaks
- 📝 **10% of time**: Documentation (AI-assisted README)

---

## The Generic Prompt Approach

**In Cursor's chat**, use this initial prompt and attach files:

```
I want to build HTML prototype pages for CineMatch. I'll be building one page at a time.

For each page, I'll:
1. Tell you which page I want to build
2. Provide the design guide, PRD, and UI screen specs
3. You analyze them to understand the context
4. You create the initial HTML prototype
5. I'll give you improvement requests
6. You implement them iteratively

Let's start with the landing page (homepage).

@design_guide.html @product_requirements.md @ui_screens.md

Please analyze these files and understand:
- The CineMatch brand and design system
- The product goals and user needs
- The specific requirements for the landing page (homepage)

Then create a complete standalone HTML file with inline CSS for the landing page.
```

**What happens next:**
- AI will analyze all the files you attached
- AI will understand the context and requirements
- AI will generate a complete landing page HTML
- You can then iterate with improvement requests

### Step 2: Iterate on Improvements

Once you have the initial page, provide specific improvement requests in bullet points:

```
Please make these improvements:

- Hero section: Add a gradient overlay on the background, make headline more dramatic with larger font
- Movie cards: Add smooth hover effect with lift (translateY) and shadow increase
- Trending section: Implement horizontal scroll with smooth snap behavior
- Add subtle fade-in animation when page loads
- Ensure all colors match the design guide exactly
```

**The AI will:**
- Implement each improvement
- Show you the updated code
- Explain what changes were made

### Step 3: Continue Iterating

Keep the conversation going with more specific requests:

```
Great! Now please:

- Add a "Add to Watchlist" button that appears on movie card hover
- Create a modal that opens when clicking the watchlist button
- Add more cinematic feel with film grain texture on hero
- Make movie posters more prominent with better aspect ratios
```

---

## Building Subsequent Pages

### Step 1: Extract Components from Existing Pages

**Before building your second page**, have AI extract reusable components:

```
@landing.html

Please analyze this landing page and extract/describe all reusable components:

1. Navigation header
2. Movie card
3. Footer
4. Any other reusable elements

For each component, describe:
- Structure and styling
- Interactive states (hover, active)
- CSS classes used
- Any JavaScript functionality

I want to reuse these components across other pages for consistency.
```

### Step 2: Build Next Page with Component Reuse

```
Now I want to build the Browse page.

@design_guide.html @ui_screens.md @landing.html

Requirements:
1. Reuse the navigation and footer components from landing.html
2. Add a filter sidebar as specified in ui_screens.md
3. Create a movie grid using the same movie card component
4. Add sort controls and active filter display

Please create browse.html maintaining consistency with the landing page.
```

---

## Cursor-Specific Tips

### Attaching Files

Use `@` to attach files in Cursor chat:
- `@design_guide.html` - Always attach for every page
- `@ui_screens.md` - For specific page requirements
- `@product_requirements.md` - For context and goals
- `@landing.html` - When building subsequent pages for consistency

### Managing Credit Usage

**Be strategic to avoid running out of free credits:**

1. **Batch your improvements** - Ask for 4-5 changes at once instead of one at a time
2. **Be specific** - Vague prompts lead to back-and-forth (wastes credits)
3. **Use the design guide** - Attach it every time to avoid inconsistencies
4. **Review before asking** - Look at the output first, then compile all fixes

### Example of Credit-Efficient Prompting:

❌ **Inefficient (multiple messages):**
```
Make the hero larger
[wait for response]
Change the color to match design guide
[wait for response]
Add animation
[wait for response]
```

✅ **Efficient (one message):**
```
Please make these changes to the hero:
- Increase height to 70vh
- Update all colors to match design guide variables
- Add fade-in animation on page load
- Make headline more dramatic with larger font size
```

---

## The Page Improvement Workflow

For each page, follow this cycle:

### 1. Generate Initial Version

```
@design_guide.html @ui_screens.md @product_requirements.md

Create the [page name] page for CineMatch with all sections specified in ui_screens.md.
Ensure it follows the design guide completely.
```

### 2. Visual Review

Open the HTML file in your browser and note issues:
- Color mismatches
- Spacing problems
- Missing sections
- Interaction issues

### 3. Batch Improvements

Compile ALL issues into one message:

```
Please make these improvements to [page name]:

Design fixes:
- Update button colors to match design guide exactly (--cm-deep-blue)
- Increase spacing between movie cards to 24px
- Make headlines use Playfair Display font

Interactions:
- Add hover effect on movie cards (lift 8px, shadow increase)
- Add smooth transitions (0.3s ease-out) to all interactive elements
- Create modal for "Add to Watchlist" with fade-in animation

Content:
- Generate 12 realistic movie entries with popular titles
- Use Pexels or placeholder images for posters
- Add ratings and genre tags to all cards
```

### 4. Polish Pass

Final refinements:

```
Polish pass for [page name]:

- Ensure all animations are smooth (60fps)
- Add subtle hover states to all clickable elements
- Verify all colors use CSS variables from design guide
- Add fade-in animation when page loads
- Ensure typography hierarchy is clear
```

---

## Customizing the Design System (Bonus Points!)

### Making the Design Guide Your Own

Want to stand out? Personalize the design system while maintaining cohesion:

```
@design_guide.html

I want to personalize the CineMatch design system slightly. Please:

1. Adjust the primary blue to be slightly warmer/cooler [your preference]
2. Suggest 2-3 alternative accent colors that would work well
3. Recommend a complementary font pairing that's more [modern/classic/bold]
4. Update all CSS variables to reflect these changes

Keep the overall cinematic, warm aesthetic but make it feel more unique.
```

**Then update your pages:**

```
@landing.html @updated_design_guide.html

Please update landing.html to use the new design system variables and colors.
Ensure the new palette is applied consistently throughout.
```

---

## Using Design Inspiration from Dribbble (Optional)

### Step 1: Find Inspiration

Visit [dribbble.com](https://dribbble.com) and search for:
- "movie app"
- "streaming platform" 
- "entertainment app"
- "video streaming UI"

Save 1-2 screenshots that align with CineMatch's aesthetic.

### Step 2: Upload to Cursor

**In Cursor, you can attach images directly:**

```
@design_guide.html @landing.html

[Attach Dribbble screenshot image]

I found this design inspiration on Dribbble. I'd like to incorporate these elements:

What I like:
- The card layout and shadow treatment
- The typography hierarchy  
- The hover interaction patterns
- The overall grid structure

Please update my landing page to incorporate these design patterns while:
- Maintaining CineMatch color palette exactly
- Keeping existing content structure
- Ensuring it matches our design guide
- Making it feel more polished and premium
```

### Step 3: Iterate on the Inspiration

```
That's great! Now let's refine it further:

- Make the hover effects more subtle and smooth
- Adjust spacing to feel more breathable
- Ensure typography hierarchy is even stronger
- Add one unique element that makes it distinctly CineMatch
```

---

## Ensuring Design System Consistency

### Always Attach the Design Guide

**Every time you create or update a page:**

```
@design_guide.html @[your-page].html

Please ensure this page perfectly matches the design guide:

1. All colors should use CSS variables (--cm-deep-blue, --cm-coral-red, etc.)
2. Typography should use specified fonts (Playfair Display for headings, Inter for body)
3. Spacing should use the spacing scale (--space-md, --space-lg, etc.)
4. Animations should use timing variables (--anim-normal, --ease-out)
5. Shadows should use shadow variables (--shadow-sm, --shadow-md, etc.)

Fix any inconsistencies and show me what you changed.
```

### Cross-Page Consistency Check

**After building multiple pages:**

```
@landing.html @browse.html @movie_details.html

Please analyze these pages for consistency:

1. Are navigation and footer identical across all pages?
2. Are movie cards styled consistently?
3. Are colors, fonts, and spacing uniform?
4. Are hover effects and animations similar?

List any inconsistencies and fix them.
```

---

## Common Issues & Solutions

### Issue: Output Doesn't Match Design Guide

❌ **Problem**: Colors, fonts, or spacing are off

✅ **Solution**: Always attach design guide and be explicit

```
@design_guide.html @landing.html

The colors and fonts don't match the design guide. Please fix:

- All blues should be --cm-deep-blue (#2C5F87)
- All reds should be --cm-coral-red (#E94B3C)
- Headings should use Playfair Display
- Body text should use Inter
- Replace all hardcoded values with CSS variables from the design guide
```

### Issue: Generic, Template-Like Design

❌ **Problem**: Page looks like a generic template

✅ **Solution**: Request more cinematic, branded feel

```
@landing.html

This feels too generic. Make it more distinctly CineMatch:

- Add cinematic drama (larger hero, more dramatic typography)
- Incorporate movie-themed elements (film grain texture, spotlight effects)
- Use warmer, more inviting colors from our palette
- Add personality with custom icons or illustrations
- Make hover states more delightful (not just functional)
```

### Issue: Inconsistent Across Pages

❌ **Problem**: Pages don't feel like they're part of the same product

✅ **Solution**: Extract and reuse components

```
@landing.html @browse.html

These pages feel inconsistent. Please:

1. Extract the navigation and footer from landing.html
2. Apply them exactly to browse.html
3. Ensure movie cards have identical styling
4. Make sure hover effects match across both pages
5. Verify color usage is consistent
```

### Issue: Interactions Feel Flat

❌ **Problem**: No animations or smooth transitions

✅ **Solution**: Request comprehensive interaction polish

```
@[your-page].html

Add smooth, polished interactions:

- All interactive elements need hover states
- Add 0.3s ease-out transitions to state changes
- Movie cards should lift (translateY(-8px)) on hover with shadow increase
- Buttons should scale slightly (1.02x) and shift color on hover
- Modals should fade in with backdrop and slide up content
- Page load should have subtle fade-in animation
```

---

## Generating Your README Documentation

### Let AI Write Your README

**At the end, use this prompt:**

```
@landing.html @browse.html @movie_details.html @watchlist.html @search_results.html @design_guide.html

I need to write a README for my CineMatch prototype submission. Please help me create a professional documentation file.

Include these sections:

1. **My Approach** (2-3 sentences)
   - How I tackled the assignment
   - My strategy for building pages
   
2. **Key Customizations**
   - Specific design decisions I made beyond the base requirements
   - How I personalized the design system (if I did)
   - Creative elements I added
   
3. **What I'd Improve With More Time**
   - 3-4 specific improvements or features
   - Be realistic and insightful
   
4. **Challenges & Solutions**
   - 2-3 challenges I faced
   - How I solved them using Cursor
   
5. **Technical Highlights**
   - Standout features or interactions
   - Unique implementations

Keep it professional, concise (300-400 words total), and authentic.
```

---

## Complete Example Workflow

### Building Your First Page (Landing - 40 min)

**Minute 0-2: Initial prompt**
```
@design_guide.html @product_requirements.md @ui_screens.md

Create the landing page (homepage) for CineMatch with all sections from ui_screens.md.
Follow the design guide exactly.
```

**Minute 2-5: Review in browser**
- Open HTML file
- Note any issues

**Minute 5-15: First improvement round**
```
@landing.html @design_guide.html

Please make these improvements:

Design:
- Hero section needs more dramatic feel - larger text, better gradient
- Movie cards need better hover effects (lift + shadow)
- Spacing between sections should be 48px

Content:
- Generate 12 popular movies with realistic data
- Use placeholder images from Pexels
- Add genre tags and ratings to all cards

Interactions:
- Add smooth transitions (0.3s ease-out) to all interactive elements
- Create "Add to Watchlist" modal with fade-in animation
```

**Minute 15-18: Review changes**

**Minute 18-30: Second improvement round**
```
Polish pass:

- Make all colors use CSS variables from design guide
- Ensure Playfair Display is used for all headings
- Add subtle page load fade-in animation
- Improve navigation hover states
- Make carousel smooth with snap scroll
```

**Minute 30-35: Final review**

**Minute 35-40: Cross-check with design guide**
```
@design_guide.html @landing.html

Do a final consistency check and fix any deviations from the design guide.
```

### Building Subsequent Pages (25-30 min each)

**Extract components first:**
```
@landing.html

List all reusable components and their styles so I can use them in other pages.
```

**Then build new page:**
```
@design_guide.html @ui_screens.md @landing.html

Create [page name] reusing navigation, footer, and movie card components from landing.html.
Add the specific sections needed for this page as detailed in ui_screens.md.
```

---

## Time Management Strategy

### Per Page Breakdown:

| Page | Priority | Time | Notes |
|------|----------|------|-------|
| Landing | HIGH | 40 min | Sets visual tone |
| Movie Details | HIGH | 30 min | Core user journey |
| Browse | MEDIUM | 25 min | Can reuse many components |
| Watchlist | MEDIUM | 20 min | Simpler layout |
| Search Results | MEDIUM | 20 min | Very similar to Browse |

**Buffer time:** 20 minutes for QA and final polish  
**Documentation:** 10 minutes (AI-assisted)

---

## Pro Tips for Cursor Usage

### 1. Always Attach Context Files

Every conversation should include:
- `@design_guide.html` (always!)
- `@ui_screens.md` (for requirements)
- `@existing-page.html` (when building subsequent pages)

### 2. Batch Your Requests

Instead of 5 separate messages, combine into one:
```
Please:
- Fix colors to match design guide
- Add hover effects
- Improve spacing
- Add animations
- Generate movie data
```

### 3. Use Clear Section Headers

Help AI understand your request structure:
```
Please make these changes:

DESIGN FIXES:
- [list]

INTERACTIONS:
- [list]

CONTENT:
- [list]
```

### 4. Request Before/After Summaries

```
After making changes, please summarize:
- What you changed
- Why you made those decisions
- Any trade-offs or alternatives considered
```

---

## Final Checklist

Before considering a page complete:

```
@[page-name].html @design_guide.html

Please review this page and verify:

✅ All colors use CSS variables from design guide
✅ Fonts match design guide (Playfair Display + Inter)
✅ All interactive elements have smooth hover states
✅ Spacing is consistent with design system
✅ Animations are smooth (0.3s ease-out transitions)
✅ No console errors when opened in browser
✅ Images have alt text
✅ Page feels polished and professional

Fix any issues found.
```

---

## When You're Running Low on Credits

### Prioritize These Actions:

1. ✅ **Landing page** - Must be excellent
2. ✅ **Movie details** - Core to product
3. ✅ **One more polished page** - Browse or Watchlist
4. ✅ **README documentation** - Shows your process
5. ⏭️ Skip remaining pages if needed - better to have 3 great pages than 5 mediocre ones

### Credit-Saving Tips:

- Review generated code carefully before asking for more changes
- Batch all improvements into single requests
- Use very specific prompts (less back-and-forth)
- Manually fix tiny CSS tweaks instead of asking AI

---

**Remember: Cursor is your pair programming partner. Have conversational, iterative discussions to build polished work quickly. Focus on quality over quantity, and always attach the design guide for consistency! Good luck! 🎬✨**

