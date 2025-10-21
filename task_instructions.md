# Task Instructions: Building CineMatch Prototypes

## Overview

Your goal is to create 5 clickable HTML prototype screens for CineMatch using AI assistance. These should be high-fidelity, interactive prototypes that demonstrate both your design sensibility and your ability to work efficiently with AI tools.

## Step-by-Step Process

### Phase 1: Preparation (15-20 minutes)

1. **Understand the Product**
   - Read `product_requirements.md` thoroughly
   - Understand the user flows and core features
   - Identify the key user problems being solved

2. **Study the Design System**
   - Open `design_guide.html` in your browser
   - Note the color palette, typography, and component styles
   - Understand the visual language and brand personality

3. **Review Screen Specifications**
   - Read `ui_screens.md` carefully
   - Note required sections, components, and functionality for each screen
   - Understand how screens connect to each other

### Phase 2: Strategy & Planning (10-15 minutes)

4. **Prioritize Your Work**
   - Decide which screens are most critical (hint: landing and movie_details are key)
   - Plan your time allocation per screen
   - Consider which screens can share components/layouts

5. **Gather Design Inspiration** (Optional but Recommended)
   - [Optional] Visit dribbble.com and search for "movie app", "streaming platform", or similar
   - Find 2-3 designs you like that align with the CineMatch aesthetic
   - Save screenshots to reference or upload to AI (see `ai_prompting_guide.md`)

### Phase 3: Development (2-2.5 hours)

6. **Start with the Landing Page**
   - This sets the visual tone for everything else
   - Pass in `design_guide.html` into the prompt to ensure consistency
   - keep prompting/tweaking till happy (however be weary of spending too much time on a page as you have limited free credits with Cursor)
   - Test that it looks good and is responsive

7. **Build Subsequent Pages**
   - Pass in all existing pages and tell LLM to extract and describe components, and then use this for subsequent pages

8. **Add Interactions & Polish**
   - Add hover states and transitions
   - Include smooth animations for modals, cards, etc.
   - Add micro-interactions (button ripples, card lifts, etc.)
   - Test all interactive elements

### Phase 4: Review & Documentation (15-20 minutes)

9. **Quality Check**
   - Open all 5 pages and click through the entire flow
   - Ensure consistent styling across all pages

10. **Write Your README**
    - Leverage AI to generate your README and touch on the following points:
        - Explain your approach and decision-making
        - Note what you'd improve with more time
        - Mention any challenges or interesting solutions

## Key Success Factors

### ✅ Do This:

- **Use the design system** - Always pass `design_guide.html` into your UI generation conversations
- **Add polish** - Transitions, hover states, smooth animations
- **Keep it simple** - You don't need a backend; use placeholder data and mock interactions
- **Test as you go** - Open pages in browser frequently to catch issues early

### ❌ Avoid This:

- **Don't ignore the design guide** - Random colors/fonts will cost you points
- **Don't over-engineer** - No need for complex JavaScript frameworks
- **Don't use generic templates** - Customize AI outputs to match the CineMatch brand
- **Don't spend time on authentication** - Not part of this assignment
- **Don't exceed 3 hours** - We value efficiency and time management

## Time Allocation Recommendation

Here's a suggested breakdown of your 3 hours:

| Phase | Time | Activities |
|-------|------|------------|
| **Preparation** | 20 min | Read docs, study design guide, understand requirements |
| **Planning** | 15 min | Prioritize screens, gather inspiration, plan approach |
| **Landing Page** | 40 min | Build homepage with navigation and hero section |
| **Movie Details** | 30 min | Create detailed movie page (critical screen) |
| **Browse Page** | 25 min | Build catalog with filters |
| **Search Results** | 20 min | Similar to browse, can reuse components |
| **Watchlist** | 20 min | Simpler page, reuse card layouts |
| **Polish & QA** | 20 min | Add animations, test links, fix bugs |
| **Documentation** | 10 min | Write README with your approach |

**Total: 180 minutes (3 hours)**

## Technical Requirements

### Baseline Requirements:
- Valid HTML5
- Modern CSS (Grid, Flexbox, CSS Variables)
- Vanilla JavaScript (if needed for interactions)
- Works in Chrome, Firefox, Safari, or Edge (latest versions)
- Responsive design (looks good on desktop and laptop sizes)

### Bonus Points:
- Smooth transitions and animations
- Micro-interactions (hover effects, loading states, etc.)
- Modal windows that open/close properly
- Skeleton loading states
- Interactive filters that work (even with dummy data)

## Using Placeholder Data

Since this is a prototype, you'll need mock movie data. Here are some approaches:

3. **Generate with AI** - Ask AI to create realistic movie metadata based on popular movies and either ge
4. **Keep it simple** - 10-15 movies is enough to demonstrate the design

## What "Clickable Prototype" Means

Your prototype should:
- Have a working navigation menu that links to all 5 pages
- Allow users to click from landing → browse → movie details
- Enable clicking on movie cards to navigate to details pages
- Include back buttons or breadcrumbs for navigation
- Have interactive buttons that show hover states (even if they don't do anything complex)

You DON'T need:
- Real API integrations
- User authentication/login
- Backend database
- Actual search functionality (can be simulated with static results)
- Complex state management

## Questions to Ask Yourself

As you work, regularly check:

1. ✅ Does this match the CineMatch design system?
2. ✅ Is the user flow clear and intuitive?
3. ✅ Are interactions smooth and delightful?
4. ✅ Would a potential user understand how to navigate?
5. ✅ Does this feel modern and polished?

## Final Checklist

Before submitting, verify:

- [ ] All 5 HTML files are present and named correctly
- [ ] Navigation links work between all pages
- [ ] Design system colors and typography are used consistently
- [ ] Pages are responsive (test by resizing browser)
- [ ] Hover states and transitions are smooth
- [ ] No console errors in browser DevTools
- [ ] README.md is included with your approach documented
- [ ] Files are organized in a folder named `[YourName]_cinematch_prototype`

## Need Help?

If you get stuck:

1. **Check `ai_prompting_guide.md`** - Tips for better AI outputs
2. **Review `design_guide.html`** - All components and styles are documented
3. **Look at `ui_screens.md`** - Detailed specs for each screen
4. **Email us** - For clarifying questions (not design decisions)

---

**Remember: Quality over quantity. Better to have 3 amazing screens than 5 mediocre ones. Good luck! 🎬**

