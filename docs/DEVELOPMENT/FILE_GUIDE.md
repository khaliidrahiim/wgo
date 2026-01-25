# wgo Project File Guide

A reference for all files in your project and what each one does.

---

## 📁 Project Structure

```
wgo/
├── 📄 HTML Pages
│   ├── index.html              ← Attractions page (main landing)
│   └── events.html             ← Events page (your working file)
│
├── 🎨 Styling & Interactivity
│   └── styles.css              ← All CSS (responsive, accessible)
│
├── 📚 Documentation (START HERE)
│   ├── START_HERE.md           ← Main index (read first)
│   ├── QUICK_REFERENCE.md      ← Keep open while coding
│   ├── PROJECT_STATUS.md       ← Current progress overview
│   ├── DEVELOPMENT_ROADMAP.md  ← 12-week strategic plan
│   ├── JUNIOR_DEVELOPER_GUIDE.md ← Your workflow & standards
│   └── COMMENT_STANDARDS.md    ← How to write good comments
│
├── 📖 Project Info
│   └── README.md               ← Project overview & features
│
├── 📷 Assets
│   └── assets/                 ← Images (CalypsoCompetition.jpg, etc.)
│
└── 🔧 Configuration
    ├── .git/                   ← Git version control
    ├── .gitattributes          ← Git configuration
    └── (no package.json yet)   ← Will add in Phase 2 (backend)
```

---

## 📄 File Descriptions

### HTML Files (Your Frontend)

#### `index.html` (560 lines)
**Purpose:** Attractions page - shows 8 permanent attractions in BVI  
**Key Features:**
- Semantic header with navigation
- 8 attraction cards in responsive grid
- About section explaining wgo
- Footer with copyright
**2-space indentation:** ✅  
**Comments:** ✅ Section headers  
**Accessibility:** ✅ ARIA labels, semantic HTML

#### `events.html` (620 lines)
**Purpose:** Events page - future paid event listings hub  
**Key Features:**
- Horizontal scroll image gallery (your working area)
- Event cards explaining vision
- Email subscription form
- Vision section connecting to Limin' Times
**2-space indentation:** ✅  
**Comments:** ✅ Section headers  
**Accessibility:** ✅ ARIA labels, tabindex for images

---

### CSS & JavaScript

#### `styles.css` (620 lines)
**Purpose:** All styling for both pages  
**Key Sections:**
- CSS Custom Properties (variables for colors, spacing, breakpoints)
- Global reset and base styles
- Header and navigation styling
- Card layout (attraction cards)
- Event cards and subscribe section
- Image zoom modal styles ← NEW
- Responsive design (3 breakpoints)
- Accessibility enhancements (focus states, reduced motion)
- Print styles

**Usage:** Included in both HTML files with `<link rel="stylesheet" href="styles.css">`  
**2-space indentation:** ✅  
**Comments:** ✅ Major sections clearly labeled

#### `image-zoom.js` (400+ lines)
**Purpose:** Image zoom modal functionality  
**Key Functions:**
- `initImageZoomModal()` - Creates modal structure
- `setupImageZoomListeners()` - Attaches event listeners
- Keyboard navigation (arrows, escape)
- Click handling for images
- Navigation buttons (prev/next)

**Usage:** Included at bottom of events.html  
**Accessibility Features:**
- Keyboard navigation (Tab, Arrow, Escape)
- ARIA labels for screen readers
- Focus management
- Image alt text preserved

**Learning Value:** Best example of professional JavaScript in the project

---

### Documentation Files (Read These!)

#### `START_HERE.md` (Your index)
**Read this first.** Everything else references this.  
**Contains:**
- Documentation index (what to read when)
- Your current task breakdown
- Weekly schedule
- Success criteria
- Quick links to all resources

**Time to read:** 10 minutes  
**Action items:** Yes, actionable tasks

#### `QUICK_REFERENCE.md` (Keep open!)
**Keep this in a separate tab while coding.**  
**Contains:**
- Today's tasks at the top
- File structure reference
- Browser testing checklist
- Code standards reference (indentation, comments, patterns)
- Git commands (most common 5 commands)
- Debugging checklist
- Accessibility checklist
- JavaScript patterns and CSS values
- Keyboard shortcuts

**Time to read:** 5 minutes (on first read)  
**Look-ups:** Quick reference, no deep reading needed

#### `PROJECT_STATUS.md`
**Understanding your current progress**  
**Contains:**
- What's complete ✅
- Current feature breakdown
- Your tasks in order (step-by-step)
- Files you should read (in order)
- Technology stack summary
- Success metrics

**Time to read:** 15 minutes  
**When to read:** After START_HERE.md

#### `DEVELOPMENT_ROADMAP.md` (Strategic plan)
**The 12-week game plan**  
**Contains:**
- Phase 1-5 breakdown (3-4 weeks each)
- Revenue model explanation
- Technology decisions (Stripe, Node.js, PostgreSQL)
- What to prioritize
- Standard web development practice
- Weekly rhythm recommendations
- Learning resources by phase

**Time to read:** 30 minutes (on first read)  
**Read when:** Planning your week

#### `JUNIOR_DEVELOPER_GUIDE.md` (Your workflow)
**How to work effectively as a junior dev**  
**Contains:**
- Your workflow (test → understand → modify → commit)
- Code quality checklist (10 items)
- Common debugging steps
- When to ask for help
- Communication templates
- Red flags vs. green flags

**Time to read:** 20 minutes  
**Read when:** Before you get stuck

#### `COMMENT_STANDARDS.md` (Code style)
**How to write good comments**  
**Contains:**
- Comment format for each file type (HTML, CSS, JS)
- When to comment (and when NOT to)
- Examples for each file type
- Section headers vs. line comments
- "Explain why, not what" principle
- Checklist before submitting code

**Time to read:** 15 minutes  
**Read when:** Before you write comments

#### `README.md` (Project overview)
**Project description and features**  
**Contains:**
- Project overview
- Design philosophy
- Semantic HTML explanation
- Accessibility features
- Marketing strategy
- Future enhancement phases
- Getting started instructions
- Tech stack details

**Time to read:** 20 minutes  
**Read when:** Understanding the bigger picture

---

## 📊 Statistics

| Metric | Value |
|--------|-------|
| HTML lines (total) | ~1,200 |
| CSS lines | ~620 |
| JavaScript lines | ~400 |
| Documentation lines | ~2,500 |
| Comments in code | 100+ |
| Total words in docs | ~12,000 |
| Files to maintain | 2 (HTML) + 1 (CSS) + 1 (JS) = 4 core |
| Documentation files | 7 guides |

---

## 🎯 What Each File Teaches You

### Learning Journey

1. **index.html** → Learn semantic HTML structure
2. **events.html** → Learn how HTML connects to JavaScript
3. **styles.css** → Learn professional CSS organization
4. **image-zoom.js** → Learn JavaScript best practices
5. **JUNIOR_DEVELOPER_GUIDE.md** → Learn professional practices
6. **COMMENT_STANDARDS.md** → Learn code documentation

### Skills Developed

| File | Skill |
|------|-------|
| HTML files | Semantic HTML, accessibility, structure |
| styles.css | CSS organization, responsive design, accessibility |
| image-zoom.js | JavaScript, DOM, event handling, accessibility |
| Documentation | Professional communication, planning, standards |

---

## 🔄 File Dependencies

```
events.html
    ├── links to → styles.css
    ├── includes → image-zoom.js
    └── references → index.html (nav links)

image-zoom.js
    └── manipulates → events.html (the DOM)

styles.css
    ├── styles → index.html
    └── styles → events.html

Documentation files
    └── explain → all of the above
```

---

## 📝 Where to Make Changes

### For Different Tasks

| Task | Edit This File |
|------|----------------|
| Add new attraction | index.html |
| Change colors/theme | styles.css (CSS variables) |
| Add image zoom logic | image-zoom.js |
| Improve accessibility | events.html + styles.css |
| Fix modal styling | styles.css (.image-zoom-modal section) |
| Change button text | image-zoom.js or events.html |
| Add new page | Create new .html file + link in nav |
| Update navigation | Both HTML files (nav section) |

---

## ✅ File Checklist

Before submitting code:

- [ ] HTML: 2-space indentation, section comments
- [ ] CSS: 2-space indentation, section headers, variables used
- [ ] JS: 2-space indentation, clear function names, why comments
- [ ] All: No trailing spaces, proper quotes (single or double)
- [ ] Accessibility: ARIA labels, keyboard navigation, contrast
- [ ] Tests: Works on Chrome, Firefox, Safari, mobile
- [ ] Git: Clear commit message, only relevant files changed

---

## 🎓 Study Order

1. Start with → START_HERE.md (this meta-guide)
2. Keep open → QUICK_REFERENCE.md
3. Understand → PROJECT_STATUS.md (your tasks)
4. Study → image-zoom.js (the code)
5. Reference → COMMENT_STANDARDS.md (while coding)
6. Review → JUNIOR_DEVELOPER_GUIDE.md (when stuck)
7. Plan → DEVELOPMENT_ROADMAP.md (weekly planning)

---

## 🚀 Using These Files

### Daily Workflow

```
Monday Morning:
1. Open START_HERE.md (5 min)
2. Keep QUICK_REFERENCE.md in another tab
3. Read PROJECT_STATUS.md (10 min)
4. Start coding using guides as reference

During Development:
- Check QUICK_REFERENCE.md when unsure
- Reference image-zoom.js for patterns
- Use COMMENT_STANDARDS.md when commenting
- Check JUNIOR_DEVELOPER_GUIDE.md if stuck

End of Day:
- Review QUICK_REFERENCE.md checklist
- Commit changes with clear message
- Update PROJECT_STATUS.md with progress
```

### Weekly Planning

```
Monday:
1. Read DEVELOPMENT_ROADMAP.md
2. Check what phase you're in
3. Plan that week's work
4. Break down into daily tasks

Friday:
1. Review QUICK_REFERENCE.md
2. Check weekly success metrics
3. Plan next week
4. Document what you learned
```

---

## 📊 File Size Reference

| File | Size | Read Time | Type |
|------|------|-----------|------|
| START_HERE.md | ~6 KB | 10 min | Reference |
| QUICK_REFERENCE.md | ~8 KB | 5 min | Quick lookup |
| PROJECT_STATUS.md | ~7 KB | 15 min | Status |
| DEVELOPMENT_ROADMAP.md | ~12 KB | 30 min | Strategic |
| JUNIOR_DEVELOPER_GUIDE.md | ~11 KB | 20 min | Workflow |
| COMMENT_STANDARDS.md | ~9 KB | 15 min | Style guide |
| README.md | ~8 KB | 20 min | Overview |
| events.html | ~11 KB | 15 min | Code |
| index.html | ~10 KB | 15 min | Code |
| styles.css | ~18 KB | 30 min | Code |
| image-zoom.js | ~9 KB | 20 min | Code |

**Total project size:** ~109 KB (very small, fast to load!)  
**Total documentation:** ~50 KB (substantial but essential)  
**Total code:** ~49 KB (clean and organized)

---

## 🔐 What NOT to Edit (Yet)

- ❌ .git directory (git manages this)
- ❌ .gitattributes (configuration file)
- ❌ assets directory (images are reference only for now)
- ❌ index.html nav (until you add new pages)

**What you CAN edit:**
- ✅ events.html (your workspace)
- ✅ image-zoom.js (your code to understand)
- ✅ styles.css (to improve UI)
- ✅ Documentation (to add notes)

---

## 📞 File Support

### "How do I...?"

| Question | Answer File |
|----------|------------|
| Get started? | START_HERE.md |
| Understand my task? | PROJECT_STATUS.md |
| Debug code? | QUICK_REFERENCE.md → Debug Checklist |
| Test accessibility? | QUICK_REFERENCE.md → Accessibility Checklist |
| Write comments? | COMMENT_STANDARDS.md |
| Know what's next? | DEVELOPMENT_ROADMAP.md |
| Follow standards? | JUNIOR_DEVELOPER_GUIDE.md |
| Use git? | QUICK_REFERENCE.md → Git Commands |

---

## 🎯 Bottom Line

You have:
- **2 HTML pages** to maintain and improve
- **1 CSS file** with comprehensive styling
- **1 JavaScript file** to understand and enhance
- **7 documentation files** to guide you
- **Clear expectations** for what to do

**Start with START_HERE.md. Everything else follows.**

You're set up for success. Now code! 🚀
