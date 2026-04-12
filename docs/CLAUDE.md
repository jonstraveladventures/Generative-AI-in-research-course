# Generative AI in Research — Course Materials

## Project Overview

Course materials for **MAM5020F 2026: Generative AI for Research** at the University of Cape Town. A 12-week, NQF Level 9 (postgraduate) course requiring no prior ML, CS, or programming background. Taught by Assoc. Prof. Jonathan Shock.

**Repository:** https://github.com/jonstraveladventures/Generative-AI-in-research-course
**GitHub Pages site:** https://jonstraveladventures.github.io/Generative-AI-in-research-course/ (served from `/docs` on `main`)

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
| 6 | AI for Writing, Communication & Research Ideation | Built |
| 7 | AI for Data, Code & Computation | Built |
| 8 | Critical Evaluation & Limitations of AI | Not started |
| 9 | Agentic AI, RAG & Advanced Research Tools | Not started |
| 10 | Future of AI in Research & Africa's Sovereign AI Capacity | Not started |
| 11 | Flexible / TBD | Not started |
| 12 | Integrative Workshop & Student Presentations | Not started |

**Note on restructured schedule (Weeks 7-12):** The original Weeks 7 (Data Analysis) and 8 (Coding/Computational Research) were merged into Week 7 because they overlap heavily — data analysis IS coding for most researchers. Original Week 9 (Domain-Specific Applications) content is woven into other weeks as case studies. Original Week 10 (Critical Evaluation/Limitations) was moved up to Week 8. This freed a slot for Week 11 (Flexible/TBD) to adapt to cohort needs. See the plan file at `.claude/plans/goofy-whistling-journal.md` for full rationale.

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
  Ubuntu Relational Ethics and the Just AI Framework.html
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

Week 6/          (AI for Writing, Communication & Research Ideation)
  Table of Contents.html
  Writing as Thinking.html
  Research Ideation with AI.html
  AI Writing Tools Landscape and Honest Assessment.html
  Scientific Integrity and the Writing Pipeline.html
  Building Your AI Writing Workflow.html
  Hands-On Activities and Assessment.html
  Using AI to Review Your Own Work.html    (supplementary — based on paper-review skill)

Week 7/          (AI for Data, Code & Computation)
  Table of Contents.html
  Natural Language to Code.html
  AI-Assisted Data Analysis in Practice.html
  Visualization with AI.html
  Verification of AI-Generated Code.html
  Building Your Data Analysis Workflow.html
  Hands-On Activities and Assessment.html

From Amathuba/           (Amathuba/Brightspace export — the live/edited versions of all lessons)

docs/                    (GitHub Pages site — served at jonstraveladventures.github.io)
  index.html             (Landing page with full course navigation)
  course-orientation/    (Overview, Meet the Course Team)
  course-introduction/   (Introduction, Course Caveats, AI Content Disclaimer)
  week-1/ through week-5/  (All lesson pages from Amathuba export, organised by week)

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
6. **Update docs/ site** — Copy the Amathuba-exported versions of new lesson pages into the appropriate `docs/week-N/` folder, add back-nav links, and update `docs/index.html` with new lesson links
7. **Push to GitHub** — Commit and push all changes (source files, docs/, CLAUDE.md). GitHub Pages auto-deploys from `/docs` on `main`
8. **Upload to Amathuba** — Use Claude in Chrome to automate page creation (Create Module → Create Page → paste HTML via source code editor). **🔴 IMPORTANT: Before pasting into Amathuba's source code editor, sanitise the HTML** to convert emojis to the correct format: CSS `content` properties need unicode escapes (`\1F3AF`), HTML body content needs HTML entities (`&#127919;`). Use this script to prepare the clipboard:
   ```bash
   python3 -c "
   import sys, re
   with open(sys.argv[1], 'r') as f: content = f.read()
   def css_fix(m):
       r = []
       for ch in m.group(0):
           r.append('\\\\\\\\' + format(ord(ch), 'X') if ord(ch) > 127 else ch)
       return ''.join(r)
   content = re.sub(r\"content:\s*'[^']*'\", css_fix, content)
   sys.stdout.write(''.join(f'&#{ord(c)};' if ord(c) > 127 else c for c in content))
   " FILENAME.html | pbcopy
   ```
   Without this step, Brightspace's editor corrupts UTF-8 emojis into garbled characters (lesson learned from Week 6).
9. **Update CLAUDE.md** — Mark the week as Built, add file structure, content details, and any new CSS components or notes

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
2. **Ubuntu, Relational Ethics and the Just AI Framework** — Ubuntu philosophy, Mhlambi's "From Rationality to Relationality" (linked to perma.cc/Q5ZL-TTD8), Birhane's algorithmic injustice (linked to abebabirhane.com), RIA Just AI Framework (9 core inquiries as card grid, 4 structural challenges), Esethu Framework case study (Rajab et al., 2025 — community-driven data governance for low-resource languages), comparison table (individualist vs ubuntu/Just AI), Global South perspectives.
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

## Week 6 Content Details

Week 6 has 6 core sub-lessons plus 1 supplementary page. It folds in the research ideation content from the original lesson plan's Week 5.

1. **Writing as Thinking — Why the Process Matters** — Cognitive science of writing-as-thinking, Harvard Gazette (2025) "Is AI dulling our minds?", MIT Media Lab "Your Brain on ChatGPT" study (now published in PMC), Frontiers in AI (2025) cognitive dissonance study, the "first draft trap", a spectrum of AI assistance (5 levels from proofreading to generating sections), connection to Week 4 virtue ethics. Readings: Harvard Gazette, Frontiers in AI, Frontiers in Education, Psychology Today, Holmner et al. (ASIS&T).
2. **Research Ideation with AI** — Folded in from original Week 5. Five prompting strategies (chain-of-thought, role-playing, constraint-based, adversarial, cross-disciplinary) with practical examples. Si et al. (2024) study (LLM ideas rated more novel but less feasible/diverse). Idea monoculture: Nature Comms Psychology (2026) "scientific monoculture" paper, ScienceDirect (2025) homogenisation study. Five ideation risks (anchoring, confirmation bias, premature convergence, novelty illusion, loss of serendipity). When NOT to use AI. Girotra, Meincke, Terwiesch & Ulrich (2023) with caveat that AI has improved since. Sakana AI "AI Scientist" (Nature 2026) as supplementary reading.
3. **AI Writing Tools — Landscape and Honest Assessment** — Four tool categories (general LLMs, specialist academic, grammar/style, translation). Multilingual equity: Amano, Bowker & Burton-Jones (2025, PLOS Biology) two futures for multilingual publishing, writing time ~50% longer for non-native speakers. Homogenisation: Agarwal, Naaman & Vashistha (2025, CHI) Indian writing becoming more American. African context. Usdan, Connell Pensky & Chang (2024, CMU/SSRN) — 64.5% time reduction, B+ to A grades. Comparison table (8 tools). Daryani et al. (2026) homogenising engine.
4. **Scientific Integrity and the Writing Pipeline** — Integrity spectrum (6 levels, colour-coded risk cards). Nuanced data description section distinguishing with/without data access, modern models pushing back rather than fabricating, subtler risks (instructed fabrication, over-claiming, silent gap-filling). "When AI knows more than you" warning box. Journal policy comparison table with hyperlinked policies: Science/AAAS (updated Nov 2023, now disclosure-based), Nature, Elsevier (Sept 2025), IEEE, ACM, COPE. AI detection unreliability (Pangram Labs 2025). Practical auditing techniques (5 cards). Data integrity and fabrication detection tools. Disclosure templates (3 levels). "Practice what we preach" note that these course materials themselves are Template 3. Frontiers in AI (2025) scientific integrity paper. AMEE Guide No.192.
5. **Building Your AI Writing Workflow** — 5-stage principled workflow (think → outline → draft with AI → audit → revise in your voice). Prompt examples for: blank page paralysis, structuring arguments, translation/polishing, clarity feedback, audience summarisation. Warning about subtle argument changes even with explicit preservation instructions. Reverse outline technique. Version control for AI-assisted writing. Disclosure templates (3 levels with guidance).
6. **Hands-On Activities and Assessment** — Activity 1: Writing Process Experiment (300 words human vs AI, compare). Activity 2: Prompt Engineering for Ideation (4 rounds: naive, chain-of-thought, persona, constraint). Activity 3: Audit Exercise (systematic audit of AI-assisted writing). Weekly assessment: 800-word AI-assisted writing sample with process log, self-audit (3+ corrections), and disclosure statement. Criteria: Writing Quality 30%, Process Log 25%, Self-Audit 25%, Disclosure 20%. Full week summary with forward pointer to Week 7.
7. **Using AI to Review Your Own Work** (Supplementary) — Based on the paper-review skill. What AI can check (6 dimensions: logical consistency, writing quality, positioning, methodology, statistics, figures). What AI cannot reliably judge (novelty, domain conventions, significance, ethics, reviewer taste) — with caveat that AI's outsider perspective can catch author blind spots. Multi-agent review approach. Practical prompting guide (5 steps). Limitations warning. Venue-specific review standards.

## Week 7 Content Details

Week 7 has 6 core sub-lessons. It merges the original Weeks 7 (Data Analysis) and 8 (Coding/Computational Research) into one richer week.

1. **Natural Language to Code — The New Interface** — The paradigm shift: describing analysis in plain English. Tools landscape: Claude Code, ChatGPT Code Interpreter, GitHub Copilot, Cursor, Google Colab AI, Gemini Code Assist. Comparison table (6 tools, free vs paid tiers). Free vs paid quality gap (context window, model quality, rate limits, file access) with honest assessment and strategies for maximising free tier value. "Vibe coding" — when useful (prototyping, exploration), when dangerous (publication, consequences). Minimum code literacy for AI-assisted researchers (variables, functions, loops, error messages). "Runs vs correct" case study (t-test vs Mann-Whitney on Likert data). Readings: Mineault (2026) Claude Code for Scientists, Dataquest (2025) Claude Code for Data Scientists, Cheng, Li & Bing (2023) "Is GPT-4 a Good Data Analyst?", Wickham, Çetinkaya-Rundel & Grolemund (2023) R4DS 2e, Hong et al. (2024) Data Interpreter.
2. **AI-Assisted Data Analysis in Practice** — Data cleaning with AI (strengths, blind spots, silent fixes danger, transformation logs, before-and-after checks). Exploratory data analysis (promise vs reality, 4-step EDA walkthrough with South African survey example). The silent error problem (6 types: wrong variable, off-by-one time series, incorrect missing data, wrong statistical test, grouping/aggregation errors, data leakage). Domain expertise as essential complement (spurious correlations via tylervigen.com, Simpson's paradox, overfitting, confounding variables). Statistical pitfalls AI introduces (correlation≠causation, multiple comparisons, cherry-picking, p-hacking, garden of forking paths). Kapoor & Narayanan (2023) "Leakage and the Reproducibility Crisis" as key reading. Supplementary: Narayanan & Kapoor normaltech.ai (formerly AI Snake Oil), Mollick's One Useful Thing.
3. **Visualization with AI** — What AI can generate (Claude Code/matplotlib, ChatGPT Code Interpreter, LIDA/Dibia 2023, Google Colab AI). Six good visualisation principles AI often violates (misleading axes, poor colours, overplotting, wrong chart type, missing context, chartjunk/Tufte). Help vs mislead (default settings trap, publication quality as different standard). Accessibility (colourblind-safe palettes: ColorBrewer, viridis, Okabe-Ito; redundant encoding; alt text for figures; 8% colour vision deficiency stat). Five-step practical workflow (explore → audit → fix accessibility → polish → verify). Readings: Dibia (2023) LIDA, Wilke (2019) Fundamentals of Data Visualization (free online), ColorBrewer 2.0, Coblis simulator.
4. **Verification of AI-Generated Code** — Why verification matters more than generation. Reading code you didn't write as essential skill. Practical verification techniques (test with known data, edge cases, sanity checks, comparison with established tools, "change one thing" test). Six common failure patterns (wrong library/function, incorrect statistical assumptions, off-by-one errors, silent data type conversions, scope/variable shadowing, incorrect aggregation). Building a verification habit (5-step checklist). Version control for reproducibility. Readings: Cheng, Li & Bing (2023), Wickham et al. R4DS 2e, software testing resources.
5. **Building Your Data Analysis Workflow** — Five-stage workflow (question → data preparation → analysis → verification → interpretation). Prompt templates for common tasks (loading data, summary statistics, group comparisons, regression, visualisation). Claude Code + Jupyter notebook side-by-side workflow adapted from Mineault (2026). CLAUDE.md for project context. When to use AI vs established statistical packages. Reproducibility and documentation. Privacy considerations (what data can you paste into AI tools? UCT data classification, anonymisation, institutional agreements). Readings: Mineault (2026), Dataquest (2025).
6. **Hands-On Activities and Assessment** — Activity 1: Data Cleaning Challenge (messy dataset with planted errors, use AI to clean, document every change). Activity 2: Code Generation and Verification (describe analysis in plain English, AI generates code, critically verify outputs against known answers). Activity 3: Interpretation Challenge (AI-generated analyses, some correct, some with classic statistical errors — identify which). Weekly assessment: Use AI to analyse a dataset relevant to your research, submit code, outputs, and critical commentary (1000 words). Full week summary with forward pointer to Week 8.

## GitHub Pages Site

The public course website is served from the `docs/` folder on the `main` branch via GitHub Pages.

- **URL:** https://jonstraveladventures.github.io/Generative-AI-in-research-course/
- **Source:** `docs/` folder — contains Amathuba-exported (live/edited) versions of all lesson pages, organised into week subfolders
- **index.html** — Landing page with UCT styling, links to all built weeks, "coming soon" placeholders for future weeks
- **AI Content Disclaimer** — `docs/course-introduction/AI Content Disclaimer.html` — explains AI-assisted creation, known risks, contact for corrections
- **Back navigation** — Every lesson page has a "Back to Contents" bar at the top linking to `index.html`
- **Course Orientation pages** use Brightspace/Bootstrap templates (different from Week 1-5 inline CSS pages). Their `/shared/HTML-Template-Library/` CSS references won't resolve on GitHub Pages — the content is still readable but styling is limited
- **When adding new weeks:** copy Amathuba-exported files to `docs/week-N/`, add back-nav, update `docs/index.html` links, and change the "coming soon" placeholder to active links

## Notes

- Week 3 folder is lowercase (`week 3`); other weeks use title case (`Week 1`, `Week 2`, `Week 4`)
- **Week 3 key stat to include:** 1 month of heavy Claude Code usage ≈ 30–40 kWh ≈ driving ~150 km in a car
- The course has a strong emphasis on African context (ubuntu ethics, AU AI strategy, South African grid, RIA Just AI Framework, Esethu Framework)
- Week 4 Sub-Lesson 2 integrates the RIA Just AI Framework of Inquiry (Chetty & Sey, 2025) alongside ubuntu philosophy
- Week 4 Sub-Lesson 2 includes the Esethu Framework (Rajab et al., 2025) as a case study on data sovereignty for low-resource languages
- Key external links in Week 4: Mhlambi paper (perma.cc/Q5ZL-TTD8), Birhane website (abebabirhane.com), RIA Just AI Framework (researchictafrica.net), Esethu Framework (arxiv.org/abs/2502.15916), UCT Ethics Lab (health.uct.ac.za/ethics-lab), Global Center on AI Governance (globalcenter.ai)
- Week 5 introduces new CSS components: `.prompt-example` (monospace prompt boxes), `.prompt-label` (blue label badges), `.code-block` (dark terminal-style block), `.level-card` + `.level-tag` (level summary cards), `.tool-card` with pricing badges and verdict boxes
- Week 5 Sub-Lesson 5 (Claude workflow) is NEW content not in the original lesson plan — added to cover Claude skills, CLAUDE.md, and personalised research workflows
- Week 5 CSS template source: `Week 5/Building Your Research Workflow with Claude.html` (widest Week 5 component set)
- Key external tool links in Week 5: Semantic Scholar (semanticscholar.org), ResearchRabbit (researchrabbit.ai), Connected Papers (connectedpapers.com), NotebookLM (notebooklm.google.com), Elicit (elicit.com), Consensus (consensus.app), Scite.ai (scite.ai), SciSpace (scispace.com), Litmaps (litmaps.com), Retraction Watch (retractionwatch.com)
- **CSS lesson learned (Week 5):** `.step-list` must use `> li` direct child selectors to prevent nested lists from inheriting the counter and blue circle styling. Fixed in Sub-Lesson 6; apply same pattern in future weeks when nesting lists inside step-list items.
- Week 5 Sub-Lesson 4 hallucination statistics were all verified against primary sources and corrected. Key sources: Stanford HAI (hai.stanford.edu), Chelli et al. 2024 (jmir.org/2024/1/e53164), Linardon et al. 2025 (mental.jmir.org/2025/1/e80371), GPTZero NeurIPS analysis (gptzero.me/news/neurips/), Niimi 2025 (arxiv.org/html/2510.25378)
- Week 5 assessment is 1000 words (not 2000) — changed from original lesson plan to better suit scope
- Week 6 folds in research ideation content from original lesson plan's Week 5 (prompt engineering, brainstorming, idea generation)
- Week 6 verification caught 5 hallucinated author names (Girotra co-authors, PLOS Biology authors, CHI paper authors), 1 wrong arXiv URL, 1 wrong statistic (2.5-3x → 1.5x writing time), 1 outdated policy (Science/AAAS), and 1 outdated fact (SA languages 11→12)
- Week 6 Sub-Lesson 4 includes nuanced discussion of AI and data: modern models push back rather than fabricate, risks shift to over-claiming and silent gap-filling. Also covers "when AI knows more than you" (both positive and dangerous sides)
- Week 6 Sub-Lesson 5 includes warning about AI subtly changing arguments even when instructed to preserve meaning
- Week 6 Supplementary page (AI review) is based on the paper-review skill at `.claude/skills/paper-review/SKILL.md`
- Week 6 Sub-Lesson 4 notes that course materials themselves are a "Template 3" (substantial AI use) example
- Key journal policy links in Week 6: Science (science.org/content/page/science-journals-editorial-policies), Nature (nature.com/nature-portfolio/editorial-policies/ai), Elsevier (elsevier.com/about/policies-and-standards/generative-ai-policies-for-journals), IEEE (journals.ieeeauthorcenter.ieee.org), ACM (acm.org/publications/policies/new-acm-policy-on-authorship), COPE (publicationethics.org/guidance/cope-position/authorship-and-ai-tools)
- Week 6 assessment is 800 words (not 2000 from original plan)
- Week 7 merges original Weeks 7 (Data Analysis) and 8 (Coding/Computational Research) — they overlap too heavily to justify separate weeks
- Week 7 introduces `.code-block` CSS component (dark terminal-style) in Sub-Lesson 5 for project structure examples
- Week 7 verification caught: wrong Cheng et al. authors (fixed to Cheng, L., Li, X., & Bing, L.), missing R4DS co-author (added Çetinkaya-Rundel), Mineault year wrong (2025→2026), aisnakeoil.com redirect to normaltech.ai, hallucinated Mollick post title
- Week 7 key external links: Mineault (neuroai.science/p/claude-code-for-scientists), Dataquest Claude Code guide, Cheng et al. (arxiv.org/abs/2305.15038), R4DS (r4ds.hadley.nz), Hong et al. (arxiv.org/abs/2402.18679), Kapoor & Narayanan (doi.org/10.1016/j.patter.2023.100804), Tyler Vigen (tylervigen.com/spurious-correlations), Dibia LIDA (arxiv.org/abs/2303.02927), Wilke (clauswilke.com/dataviz), ColorBrewer (colorbrewer2.org), Narayanan & Kapoor blog (normaltech.ai, formerly aisnakeoil.com), Mollick (oneusefulthing.org)
- Week 7 assessment is 1000 words (critical commentary on AI-assisted data analysis)
- Week 7 Sub-Lesson 2 has the most important pedagogical content: the "silent error problem" — code that runs without errors but produces wrong results. This is the central risk message of the entire week
- Week 7 Sub-Lesson 3 covers accessibility as non-optional (colourblind-safe palettes, redundant encoding, alt text) — 8% of men have colour vision deficiency
- Week 7 Sub-Lesson 5 covers privacy/data classification for AI tools — important for researchers handling sensitive data
