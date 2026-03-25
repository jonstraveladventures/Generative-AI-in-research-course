# Generative AI in Research — Course Materials

## Project Overview

Course materials for **MAM5020F 2026: Generative AI for Research** at the University of Cape Town. A 12-week, NQF Level 9 (postgraduate) course requiring no prior ML, CS, or programming background. Taught by Assoc. Prof. Jonathan Shock.

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
| 5 | AI-Assisted Literature Review | Built |
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

Week 5/          (AI-Assisted Literature Reviews)
  Table of Contents.html
  The AI Literature Review Landscape.html
  Free Tools Deep Dive.html
  Paid Tools and When They Are Worth It.html
  The Hallucinated Citation Crisis.html
  Building Your Research Workflow with Claude.html
  Hands-On Activities and Assessment.html

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
| `.step-list` | Numbered steps with blue circle counters. **Important:** uses `> li` direct child selectors so nested lists inside step items are not affected by the counter or blue circle styling |

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

## Build Process for New Weeks

When building a new week's content, follow these steps in order:

1. **Research & plan** — Read the lesson plan, research the topic with web searches, propose structure to user for approval
2. **Build sub-lesson HTML pages** — Follow the design system, CSS conventions, and page template structure documented above
3. **Build Table of Contents page** — Link to all sub-lesson files
4. **🔴 MANDATORY: Run `/verify-references`** — Before considering a week complete, run the reference verification skill against all new HTML files. This checks every URL, academic citation, and statistical claim against primary sources. Do NOT skip this step. Experience from Week 5 showed that web search summaries and AI-generated content frequently contain incorrect statistics, hallucinated citation details, and broken URLs.
5. **Fix any issues** — Present the verification report to the user, get approval, then correct any problems found
6. **Update CLAUDE.md** — Mark the week as Built, add file structure, content details, and any new CSS components or notes

## Key References for Building New Weeks

- **CSS template source:** `week 3/Sustainable AI - Practices and Possibilities.html` (widest component set)
- **Week 4 CSS template:** `Week 4/The Broader Landscape of AI Ethics.html` (full component set including case-study, comparison-table)
- **Case study styling:** `week 3/Critical Minerals and AI.html`
- **Full page structure:** `week 3/The Cost of Every Prompt.html`
- **Lesson plans for all 12 weeks:** `Lesson plans.docx`
- **Design system details:** `Style guide.rtf`
- **Reference verification skill:** `.claude/skills/verify-references/SKILL.md`

## Week 4 Content Details

Week 4 has 4 core sub-lessons plus 1 supplementary page:

1. **Ethical Frameworks and Four Lenses** — The ethics gap, four philosophical lenses (consequentialism, deontology, virtue ethics, ubuntu), worked example scenario, all week readings. Includes forward reference to RIA Just AI Framework (info-box after "Why Four Lenses, Not One?") and pointer to the broader landscape page.
2. **Ubuntu and Relational Ethics** — Ubuntu philosophy, Mhlambi's "From Rationality to Relationality" (linked to cyber.harvard.edu), Birhane's algorithmic injustice (linked to abebabirhane.com), RIA Just AI Framework (9 core inquiries as card grid, 4 structural challenges), Esethu Framework case study (Rajab et al., 2025 — community-driven data governance for low-resource languages), comparison table (individualist vs ubuntu/Just AI), Global South perspectives.
3. **Transparency, Authorship and Integrity** — Disclosure norms, journal policy comparison table (Nature, Science, IEEE, ACM, Elsevier, PLOS), AI authorship debate, bias in AI-assisted research, privacy/data handling, academic integrity spectrum, intellectual property.
4. **Applying Ethics: Case Studies and Your Framework** — 6-step decision framework (step-list), 4 case studies (Dr. Amara, Thabo, Dr. Nkosi, Fatima), personal ethical framework guide, journal policy audit, weekly assessment. Full week summary with forward pointer to Week 5 and to the broader landscape page.
5. **The Broader Landscape of AI Ethics** (Supplementary) — 12 dimensions not fully covered: labour exploitation, surveillance/carceral AI, autonomous weapons, corporate power, deepfakes/democracy, gender, disability, emotional/psychological impacts, accountability/liability, indigenous data sovereignty (CARE Principles), feminist ethics of care, AI and labour market. Institutions section linking to UCT Ethics Lab, Global Center on AI Governance, Research ICT Africa, AI Now Institute, Algorithmic Justice League, GovAI, Data & Society.

## Week 5 Content Details

Week 5 has 6 core sub-lessons:

1. **The AI Literature Review Landscape** — Why AI changes literature review (6 pain point/solution cards), three categories of tools (citation-based, semantic search, grounded chat/RAG), how tools work under the hood (graph analysis, embeddings, RAG), building a combined workflow (6-step strategy), all week readings (3 core + 5 supplementary).
2. **Free Tools Deep Dive** — Detailed coverage of Semantic Scholar, ResearchRabbit (post-2025 merger with Litmaps), Connected Papers, NotebookLM, Google Scholar. Each tool has strengths/limitations cards and best-use-case guidance. Comparison table including Perplexity and Gemini Deep Research. Combined free workflow recommendation.
3. **Paid Tools and When They Are Worth It** — Honest assessments of Elicit (~$12/mo, killer data extraction), Consensus (~$9/mo, Consensus Meter), Scite.ai (~$12/mo, smart citations supporting/contrasting), SciSpace (~$12/mo, all-in-one), Litmaps Premium (best visualisations). Each has pricing, worth-it/not-worth-it verdicts. Comparison table. Institutional access note for UCT.
4. **The Hallucinated Citation Crisis** — All statistics properly sourced and cited. Scale of the problem: Stanford HAI legal AI study (Magesh et al., 2024 — 17-34% for purpose-built tools, 58-82% for general chatbots), JMIR comparative analysis (Chelli et al., 2024 — GPT-3.5 39.6%, GPT-4 28.6%, Bard 91.4%), JMIR Mental Health (Linardon et al., 2025 — GPT-4o 19.9% overall, 28-29% for niche topics vs 6% for well-studied). NeurIPS 2025 scandal sourced from GPTZero analysis, Fortune, TechCrunch (4,841 papers scanned, 100+ hallucinated citations across 51 papers, "vibe citing" term). Partial hallucinations sourced from GPTZero's "uncanny valley" findings. Citation frequency correlation from Niimi (2025, arxiv). Also covers: why it happens (pattern completion vs knowledge), the pollution loop, Five-Point Citation Check verification toolkit, red flags, Retraction Watch.
5. **Building Your Research Workflow with Claude** — Three levels: Level 1 (better prompts — structured literature, synthesis, critical reading, anti-hallucination templates), Level 2 (Claude Projects for persistent research context), Level 3 (Claude Code skills and CLAUDE.md for power users, Teresa Torres approach). Privacy and data warning. Includes prompt-example and code-block custom CSS components.
6. **Hands-On Activities and Assessment** — Activity 1: Comparative Search Challenge (same question through 4 tools). Activity 2: Citation Verification Exercise (10 AI-generated references, verify all). Activity 3: Literature Map Construction (Connected Papers or ResearchRabbit). Weekly assessment: 1000-word AI-assisted mini literature review with reliability audit (3+ verified/corrected claims) and ethical reflection. Submit via Amathuba. Full week summary with forward pointer to Week 6.

## Notes

- Week 3 folder is lowercase (`week 3`); other weeks use title case (`Week 1`, `Week 2`, `Week 4`)
- The course has a strong emphasis on African context (ubuntu ethics, AU AI strategy, South African grid, RIA Just AI Framework, Esethu Framework)
- Week 4 Sub-Lesson 2 integrates the RIA Just AI Framework of Inquiry (Chetty & Sey, 2025) alongside ubuntu philosophy
- Week 4 Sub-Lesson 2 includes the Esethu Framework (Rajab et al., 2025) as a case study on data sovereignty for low-resource languages
- Key external links in Week 4: Mhlambi paper (cyber.harvard.edu), Birhane website (abebabirhane.com), RIA Just AI Framework (researchictafrica.net), Esethu Framework (arxiv.org/abs/2502.15916), UCT Ethics Lab (health.uct.ac.za/ethics-lab), Global Center on AI Governance (globalcenter.ai)
- Week 5 introduces new CSS components: `.prompt-example` (monospace prompt boxes), `.prompt-label` (blue label badges), `.code-block` (dark terminal-style block), `.level-card` + `.level-tag` (level summary cards), `.tool-card` with pricing badges and verdict boxes
- Week 5 Sub-Lesson 5 (Claude workflow) is NEW content not in the original lesson plan — added to cover Claude skills, CLAUDE.md, and personalised research workflows
- Week 5 CSS template source: `Week 5/Building Your Research Workflow with Claude.html` (widest Week 5 component set)
- Key external tool links in Week 5: Semantic Scholar (semanticscholar.org), ResearchRabbit (researchrabbit.ai), Connected Papers (connectedpapers.com), NotebookLM (notebooklm.google.com), Elicit (elicit.com), Consensus (consensus.app), Scite.ai (scite.ai), SciSpace (scispace.com), Litmaps (litmaps.com), Retraction Watch (retractionwatch.com)
- **CSS lesson learned (Week 5):** `.step-list` must use `> li` direct child selectors to prevent nested lists from inheriting the counter and blue circle styling. Fixed in Sub-Lesson 6; apply same pattern in future weeks when nesting lists inside step-list items.
- Week 5 Sub-Lesson 4 hallucination statistics were all verified against primary sources and corrected. Key sources: Stanford HAI (hai.stanford.edu), Chelli et al. 2024 (jmir.org/2024/1/e53164), Linardon et al. 2025 (mental.jmir.org/2025/1/e80371), GPTZero NeurIPS analysis (gptzero.me/news/neurips/), Niimi 2025 (arxiv.org/html/2510.25378)
- Week 5 assessment is 1000 words (not 2000) — changed from original lesson plan to better suit scope
