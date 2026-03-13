# Generative AI in Research — Course Materials

## Project Overview

Course materials for **MAM5020F 2026: Generative AI for Research** at the University of Cape Town. A 12-week, NQF Level 9 (postgraduate) course requiring no prior ML, CS, or programming background. Taught by Prof. Jonathan Shock.

**Repository:** https://github.com/jonstraveladventures/Generative-AI-in-research-course

## Course Structure

Each week follows a three-phase structure: **Pre-Class** (readings/videos), **In-Class** (discussions/activities), **Post-Class** (deeper reading and assignments). All readings are freely accessible.

**Assessment:** Weekly practical exercises (40%), research enhancement project with presentation (40%), ethical framework development (20%).

## 12-Week Topic Map

| Week | Topic | Status |
|------|-------|--------|
| 1 | Foundations of Generative AI | Built |
| 2 | LLM Deep Dive | Built |
| 3 | Environmental Implications of AI | Built |
| 4 | Ethical Frameworks for AI in Research | Built |
| 5 | AI-Assisted Literature Review | Not started |
| 6 | AI for Writing & Communication | Not started |
| 7 | AI for Data Analysis & Visualization | Not started |
| 8 | AI for Coding & Computational Research | Not started |
| 9 | Domain-Specific AI Applications | Not started |
| 10 | Critical Evaluation of AI-Generated Content | Not started |
| 11 | Future of AI in Research (incl. Africa's sovereign AI capacity) | Not started |
| 12 | Integrative Workshop & Student Presentations | Not started |

## File Structure

```
Course introduction/
  Introduction to the course.html
  Table of Contents.html

Week 1/          (Foundations of Generative AI)
  Table of Contents.html
  Course Caveats.html
  Class introductions.html
  A lightning tour of AI - video.html
  But what is a neural network.html
  An introduction to Transformers - from 3Brown1Blue.html
  Import - 1770828860589/    (additional imported content)

Week 2/          (LLM Deep Dive)
  Table of Contents.html
  LLM Architecture Deep Dive.html
  Fine-Tuning, RLHF and Alignment.html
  Untitled.html

week 3/          (Environmental Implications of AI)
  Table of Contents.html
  The Cost of Every Prompt.html
  Infrastructure, Scale and the Rebound Problem.html
  Critical Minerals and AI.html
  Sustainable AI - Practices and Possibilities.html
  Environmental Impacts of AI.docx    (supplementary reference doc)

Week 4/          (Ethical Frameworks for AI in Research)
  Table of Contents.html
  Ethical Frameworks and Four Lenses.html
  Ubuntu and Relational Ethics.html
  Transparency Authorship and Integrity.html
  Applying Ethics Case Studies and Your Framework.html
  The Broader Landscape of AI Ethics.html    (supplementary — topics not fully covered)

Lesson plans.docx        (full 12-week lesson plans with readings/activities)
Style guide.rtf          (HTML/CSS design system for Brightspace pages)
RIA_JustAI_Framework_Summary.md   (summary of RIA Just AI Framework, used in Week 4)
```

## Design System

All sub-lesson pages use **inline CSS** following UCT branding (no external stylesheets beyond Brightspace CDN). Key design tokens:

- **Primary colour:** `#003A70` (UCT blue)
- **Secondary colour:** `#2a5298` (lighter blue for headings)
- **Font:** Lato via Brightspace CDN (`https://s.brightspace.com/lib/fonts/0.6.1/fonts.css`)
- **Brightspace CSS:** `https://templates.lcs.brightspace.com/lib/assets/css/styles.min.css`
- **Responsive breakpoint:** 768px

### CSS Components

| Class | Purpose |
|-------|---------|
| `.ai-notice` | Blue banner noting Claude enhancement |
| `header` + `.week-badge` | Dark blue header with "Week X • Sub-Lesson Y" badge |
| `.content` | Main content wrapper (padding: 50px 40px) |
| `.intro-text` | Gray box with left blue border — always first section ("What We'll Cover") |
| `.section-title` | Large blue h2 with bottom border and emoji prefix |
| `.card-grid` + `.card` | Responsive grid of hoverable cards (min 300px, border-left) |
| `.styled-list` | Custom triangle (▸) bullet points |
| `.highlight-box` | Dark blue (#003A70) background call-out for key insights |
| `.warning-box` | Yellow (#fff8e1) box with orange border for cautions |
| `.info-box` | Light gray box with blue left border for notes/tips |
| `.resource-placeholder` | Dashed border box for readings/resources |
| `.technical-detail` | White box with blue border for detailed content |
| `.comparison-table` | Styled table with dark blue header row |
| `.case-study` | Gradient background with blue border for scenarios |
| `.decision-framework` | Gradient background with solid border for frameworks |
| `.tool-card` | Top-bordered card for tool listings |
| `.step-list` | Numbered steps with blue circle counters |

### Page Template Structure

Every sub-lesson follows this skeleton:
1. `<!DOCTYPE html>` with charset, viewport, title (`Week X.Y - Title`)
2. Brightspace fonts CDN link
3. Full inline `<style>` block (duplicated per page)
4. Brightspace CSS link at end of `<head>`
5. `.container` > `.ai-notice` > `<header>` > `.content`
6. `.intro-text` ("What We'll Cover") — always first
7. Multiple `h2.section-title` sections with content components
8. Final `.intro-text` summary with forward pointer to next session

### Table of Contents Template

ToC pages use a simpler Brightspace/D2L format: a `<table>` with `<font class="title">` for the week title and `<p class='d2l'>` entries linking to sub-lesson files.

## Conventions

- All links use `target="_blank" rel="noopener"`
- Emojis appear inside h2 section titles (before text) and in h1 headers
- Header h1 text wrapped in `<span style="color: #ffffff;">`
- Sub-lesson intro paragraphs are conversational, not bullet-point
- Each page has an AI transparency notice at the top: "This page's design, presentation and content have been created and enhanced using Claude (Anthropic's AI assistant) to improve visual quality and educational experience."
- Summary sections use `.intro-text` with `margin-top: 50px`
- The final sub-lesson of each week provides a full-week summary and "Next week" pointer
- Supplementary pages use `Week X • Supplementary` in the week-badge (not a numbered sub-lesson)

## Key References for Building New Weeks

- **CSS template source:** `week 3/Sustainable AI - Practices and Possibilities.html` (widest component set)
- **Week 4 CSS template:** `Week 4/The Broader Landscape of AI Ethics.html` (full component set including case-study, comparison-table)
- **Case study styling:** `week 3/Critical Minerals and AI.html`
- **Full page structure:** `week 3/The Cost of Every Prompt.html`
- **Lesson plans for all 12 weeks:** `Lesson plans.docx`
- **Design system details:** `Style guide.rtf`

## Week 4 Content Details

Week 4 has 4 core sub-lessons plus 1 supplementary page:

1. **Ethical Frameworks and Four Lenses** — The ethics gap, four philosophical lenses (consequentialism, deontology, virtue ethics, ubuntu), worked example scenario, all week readings. Includes forward reference to RIA Just AI Framework (info-box after "Why Four Lenses, Not One?") and pointer to the broader landscape page.
2. **Ubuntu and Relational Ethics** — Ubuntu philosophy, Mhlambi's "From Rationality to Relationality" (linked to cyber.harvard.edu), Birhane's algorithmic injustice (linked to abebabirhane.com), RIA Just AI Framework (9 core inquiries as card grid, 4 structural challenges), Esethu Framework case study (Rajab et al., 2025 — community-driven data governance for low-resource languages), comparison table (individualist vs ubuntu/Just AI), Global South perspectives.
3. **Transparency, Authorship and Integrity** — Disclosure norms, journal policy comparison table (Nature, Science, IEEE, ACM, Elsevier, PLOS), AI authorship debate, bias in AI-assisted research, privacy/data handling, academic integrity spectrum, intellectual property.
4. **Applying Ethics: Case Studies and Your Framework** — 6-step decision framework (step-list), 4 case studies (Dr. Amara, Thabo, Dr. Nkosi, Fatima), personal ethical framework guide, journal policy audit, weekly assessment. Full week summary with forward pointer to Week 5 and to the broader landscape page.
5. **The Broader Landscape of AI Ethics** (Supplementary) — 12 dimensions not fully covered: labour exploitation, surveillance/carceral AI, autonomous weapons, corporate power, deepfakes/democracy, gender, disability, emotional/psychological impacts, accountability/liability, indigenous data sovereignty (CARE Principles), feminist ethics of care, AI and labour market. Institutions section linking to UCT Ethics Lab, Global Center on AI Governance, Research ICT Africa, AI Now Institute, Algorithmic Justice League, GovAI, Data & Society.

## Notes

- Week 3 folder is lowercase (`week 3`); other weeks use title case (`Week 1`, `Week 2`, `Week 4`)
- The course has a strong emphasis on African context (ubuntu ethics, AU AI strategy, South African grid, RIA Just AI Framework, Esethu Framework)
- Week 4 Sub-Lesson 2 integrates the RIA Just AI Framework of Inquiry (Chetty & Sey, 2025) alongside ubuntu philosophy
- Week 4 Sub-Lesson 2 includes the Esethu Framework (Rajab et al., 2025) as a case study on data sovereignty for low-resource languages
- Key external links in Week 4: Mhlambi paper (cyber.harvard.edu), Birhane website (abebabirhane.com), RIA Just AI Framework (researchictafrica.net), Esethu Framework (arxiv.org/abs/2502.15916), UCT Ethics Lab (health.uct.ac.za/ethics-lab), Global Center on AI Governance (globalcenter.ai)
