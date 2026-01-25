# Junior Developer Guide

**Professional Development Standards & Workflow for wgo Project**

---

## Your Role

You're a **junior developer** transitioning from learning to building. This guide establishes professional practices that will serve you throughout your career.

---

## Weekly Workflow

### Monday: Planning
- [ ] Review last week's work
- [ ] Read this week's tasks (from PROJECT_STATUS.md)
- [ ] Break tasks into small, testable pieces
- [ ] Estimate time for each piece
- [ ] Plan your week (which task each day)

### Tuesday-Thursday: Building
- [ ] Work on assigned tasks
- [ ] Test changes locally before committing
- [ ] Write clear Git commit messages
- [ ] Keep code organized and commented
- [ ] Ask for help if stuck > 30 minutes

### Friday: Review & Polish
- [ ] Test all changes made this week
- [ ] Review code for quality
- [ ] Update documentation
- [ ] Commit final changes
- [ ] Update PROJECT_STATUS.md with progress

### Weekend: Learn (Optional)
- [ ] Study code you wrote
- [ ] Research technologies needed
- [ ] Plan improvements
- [ ] Rest and recharge

---

## Code Quality Standards

### Before You Commit

Ask yourself these questions:

1. **Does it work?**
   - [ ] Tested locally
   - [ ] No console errors
   - [ ] Works on mobile view
   - [ ] Works with keyboard navigation

2. **Is it readable?**
   - [ ] Clear variable/class names
   - [ ] Proper indentation (2 spaces)
   - [ ] Comments explain "why"
   - [ ] No commented-out code (delete it)

3. **Is it consistent?**
   - [ ] Follows project style
   - [ ] Matches existing patterns
   - [ ] Uses CSS variables
   - [ ] Semantic HTML throughout

4. **Is it accessible?**
   - [ ] Keyboard navigation works
   - [ ] Color contrast sufficient
   - [ ] Focus indicators visible
   - [ ] ARIA labels where needed

### Code Review Checklist

Before marking code "done":

- [ ] Functionality works as intended
- [ ] No console errors or warnings
- [ ] Mobile responsive (test at 375px, 768px, 1024px)
- [ ] Keyboard navigation works (Tab, Enter, Escape)
- [ ] Code is readable and commented
- [ ] Follows naming conventions
- [ ] Uses CSS variables (not hardcoded values)
- [ ] No unused code or variables
- [ ] Git commit message is clear
- [ ] No breaking changes to existing features

---

## Git Workflow

### Commit Message Format

**Pattern:** `[Type] Description`

**Types:**
- `[Feature]` - New functionality
- `[Fix]` - Bug fix
- `[Refactor]` - Code cleanup (no behavior change)
- `[Style]` - CSS/styling changes
- `[Docs]` - Documentation updates
- `[Test]` - Testing changes

### Examples

```bash
# Good commits
git commit -m "[Feature] Add bulletin board grid styling"
git commit -m "[Fix] Correct mobile menu breakpoint"
git commit -m "[Docs] Update README with new design"
git commit -m "[Style] Improve event card hover effects"

# Bad commits
git commit -m "updates"                    # Not descriptive
git commit -m "fixed stuff"               # Too vague
git commit -m "asdf"                      # Not professional
```

### Daily Workflow

```bash
# At start of day - get latest changes
git pull origin main

# While working - commit frequently (every 30-60 minutes)
git add .
git commit -m "[Feature] Add event card styling"

# At end of day - push all changes
git push origin main
```

---

## Testing Methodology

### Level 1: Self-Testing (Before committing)

```
1. Open in browser
2. Does it look right?
3. Click/interact with new feature
4. Does it work?
5. Try on mobile view
6. Try with Tab key
7. No console errors?
8. ✅ Good to commit
```

### Level 2: Browser Testing (Weekly)

After completing a feature:
- [ ] Chrome (Windows)
- [ ] Firefox (Windows)
- [ ] Safari (if available)
- [ ] Chrome Mobile (DevTools emulation)
- [ ] Safari Mobile (if available)

### Level 3: Accessibility Testing (Before launch)

- [ ] Keyboard-only navigation (no mouse)
- [ ] Tab through all elements (logical order?)
- [ ] Focus indicators visible?
- [ ] Color contrast sufficient? (use WebAIM tool)
- [ ] Screen reader check (if possible)

### Level 4: Mobile Device Testing (Before MVP)

Test on actual devices if possible:
- [ ] iPhone (latest)
- [ ] Android phone (latest)
- [ ] Tablet (iPad or Android)
- [ ] Different orientations (portrait/landscape)

---

## Debugging Process

### When Something Breaks

**Step 1: Understand the problem** (5 min)
- What were you working on?
- What changed?
- What's the expected behavior?
- What's the actual behavior?

**Step 2: Check the obvious** (10 min)
- Refresh the browser
- Check browser console for errors
- Is this feature new or was it working before?
- Did you save the file?

**Step 3: Read error messages carefully** (5 min)
- Error messages tell you exactly what's wrong
- Look at line numbers
- Search the exact error online
- Check official documentation

**Step 4: Isolate the problem** (15 min)
- Comment out recent changes one by one
- Refresh after each change
- Does it work when that code is commented?
- Uncomment slowly to find the exact line

**Step 5: Ask for help** (after 30 min of above)
- Describe what you've tried
- Share the error message
- Share your code snippet
- Others can often see what you missed

**Rule:** If stuck > 30 minutes, ask for help. Don't spin your wheels.

---

## Common Issues & Solutions

### CSS Issues

**Problem:** Button not styling correctly
```css
/* ❌ Wrong - too specific */
#submit-button.subscribe-form button { color: red; }

/* ✅ Right - simple, reusable */
.btn-primary { color: red; }
```

**Problem:** Mobile layout broken
```css
/* ❌ Wrong - desktop first */
.card { grid-template-columns: repeat(3, 1fr); }
@media (max-width: 768px) { .card { grid-template-columns: 1fr; } }

/* ✅ Right - mobile first */
.card { grid-template-columns: 1fr; }
@media (min-width: 768px) { .card { grid-template-columns: repeat(3, 1fr); } }
```

### HTML Issues

**Problem:** Form not submitting
```html
<!-- ❌ Wrong - no type attribute -->
<button>Submit</button>

<!-- ✅ Right - explicit type -->
<button type="submit">Submit</button>
```

**Problem:** Link not clicking
```html
<!-- ❌ Wrong - div instead of link -->
<div onclick="navigate()">Click me</div>

<!-- ✅ Right - semantic anchor -->
<a href="/page">Click me</a>
```

---

## Learning Resources

### Official Documentation
- **HTML:** [MDN Web Docs - HTML](https://developer.mozilla.org/en-US/docs/Web/HTML)
- **CSS:** [MDN Web Docs - CSS](https://developer.mozilla.org/en-US/docs/Web/CSS)
- **JavaScript:** [JavaScript.info](https://javascript.info/) (for future)
- **Accessibility:** [WebAIM](https://webaim.org/)

### Tutorials & Guides
- **Responsive Design:** [CSS Tricks - A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)
- **Accessibility:** [Web Content Accessibility Guidelines (WCAG)](https://www.w3.org/WAI/WCAG21/quickref/)
- **Git:** [Git Documentation](https://git-scm.com/doc)

### Tools
- **Browser DevTools:** Chrome/Firefox right-click → Inspect
- **Color Checker:** [WebAIM Contrast Checker](https://webaim.org/resources/contrastchecker/)
- **Responsive Design:** [Responsive Design Checker](https://responsivedesignchecker.com/)
- **Accessibility:** [Lighthouse](https://developers.google.com/web/tools/lighthouse) (built into Chrome)

---

## Professional Communication

### Writing Clear Task Descriptions

**Bad:**
```
Fix the thing that's broken
```

**Good:**
```
Fix responsive grid layout on mobile (375px breakpoint)
- Grid showing 3 columns on mobile (should be 1)
- Text overlapping due to narrow width
- Affects events.html and index.html
```

### Asking for Help Effectively

**Bad:**
```
Help, something's broken
```

**Good:**
```
The event cards aren't stacking on mobile view.
- Expected: 1 column on mobile
- Actual: 3 columns
- Error: None in console
- I've tried: Adjusting media query breakpoint, clearing cache
- Code snippet:
  @media (max-width: 768px) {
    .bulletin-board { grid-template-columns: 1fr; }
  }
```

---

## Career Growth Path

### Month 1: Foundation
- Learn semantic HTML deeply
- Master CSS Grid/Flexbox
- Understand responsive design
- Get comfortable with Git
- Practice writing clean code

### Month 2: Intermediate
- Learn JavaScript basics
- Understand form validation
- Learn about accessibility
- Practice debugging
- Start writing more complex features

### Month 3: Advanced
- Learn backend basics (Node.js)
- Understand databases
- Learn authentication
- Practice security best practices
- Build features end-to-end

### Month 6: Professional
- Lead code reviews
- Mentor others
- Make architectural decisions
- Optimize performance
- Think about scalability

---

## Mindset

### Growth Mindset
- **Believe:** You can learn anything with effort
- **View challenges:** As opportunities, not threats
- **Embrace mistakes:** They're the best learning tool
- **Learn from others:** Study code, ask questions, accept feedback

### Developer Mindset
- **Be curious:** Why does this work this way?
- **Read error messages:** They're your friends
- **Test thoroughly:** Don't assume it works
- **Simplify:** Simpler is almost always better
- **Document:** Your future self will thank you

### Professional Mindset
- **Communicate clearly:** Write good commit messages, ask good questions
- **Own your work:** Be proud of quality code
- **Be reliable:** Deliver what you promise
- **Keep learning:** Technology changes, stay sharp
- **Help others:** Teaching reinforces your own learning

---

## Decision-Making Framework

When faced with a choice:

1. **Simple vs. Complex**
   - Choose simple when possible
   - Complex is OK only if necessary
   - Document why complex approach was needed

2. **Now vs. Later**
   - Do features now that you understand well
   - Defer features you need to learn for
   - Balance "shipping fast" with "shipping quality"

3. **Perfect vs. Good Enough**
   - Perfect code takes forever
   - Good enough + iterating beats perfection
   - Ship working features, improve later based on feedback

4. **My Way vs. Project Way**
   - Always follow project conventions
   - Your style can emerge after mastering the foundation
   - Consistency beats personal preference

---

## Performance Habits

### Daily Habits
- [ ] Start work with Git pull
- [ ] Test before committing
- [ ] Write clear commit messages
- [ ] End day with Git push
- [ ] Document what you learned

### Weekly Habits
- [ ] Review code quality
- [ ] Test on multiple browsers
- [ ] Update project status
- [ ] Learn something new
- [ ] Get feedback on work

### Monthly Habits
- [ ] Refactor old code
- [ ] Update documentation
- [ ] Review and improve processes
- [ ] Plan next month's growth
- [ ] Reflect on what you've learned

---

## Self-Care (Important!)

### Don't Burn Out
- Set work hours and stick to them
- Take breaks every 60-90 minutes
- Sleep is more valuable than extra coding
- Exercise helps creativity
- Weekends are for rest

### Manage Frustration
- It's normal to get stuck
- Experienced devs get stuck too
- Take a break, come back fresh
- Ask for help sooner than later
- Celebrate small wins

### Keep Perspective
- You're learning valuable skills
- Early mistakes are OK
- Progress > Perfection
- You're doing better than you think
- Be kind to yourself

---

## Metrics for Success

### Code Quality
- [ ] Fewer bugs each week
- [ ] Faster debugging
- [ ] Cleaner code
- [ ] Better naming
- [ ] Less commented-out code

### Professional Growth
- [ ] More independence
- [ ] Fewer questions needed
- [ ] Helping others
- [ ] Teaching what you learned
- [ ] Feeling confident

### Project Progress
- [ ] Features shipping weekly
- [ ] Tests passing
- [ ] Users happy
- [ ] Revenue growing
- [ ] Roadmap on track

---

## Key Principles

### 1. **Semantic HTML**
- Use tags that describe purpose (not `<div>` for everything)
- Helps accessibility, SEO, maintainability

### 2. **Mobile First**
- Design for smallest screen first
- Add complexity with breakpoints
- Ensures everyone can use it

### 3. **Accessibility Always**
- Not a feature, it's a foundation
- Test with keyboard, test with screen reader
- Everyone deserves to use the web

### 4. **Clean Code**
- Clear naming
- Proper indentation
- Comments that explain why
- No dead code

### 5. **User First**
- Fast loading
- Easy navigation
- Clear errors
- No confusing UX

---

## Quick Reference

### When You're Stuck
1. Take a break (5 min)
2. Read error message carefully
3. Check recent changes
4. Search the error online
5. Ask for help

### Before You Commit
1. Test locally
2. Check console for errors
3. Verify on mobile view
4. Test with Tab key
5. Write good commit message

### Weekly Review
1. Did I complete my tasks?
2. What did I learn?
3. What went well?
4. What can I improve?
5. What's next week?

---

## Final Words

**You have everything you need to succeed.**

This roadmap is your guide, but remember:
- Everyone starts as a junior developer
- Mistakes are how you learn
- Questions are welcome
- Progress matters more than speed
- You're building real skills

Focus on:
- Writing clean, readable code
- Testing thoroughly
- Understanding why things work
- Helping others
- Continuous improvement

**You've got this.** 🚀

---

**Version:** 1.0  
**Last Updated:** January 24, 2026  
**Next Review:** Monthly

Remember: The best time to learn was yesterday. The second best time is now.
