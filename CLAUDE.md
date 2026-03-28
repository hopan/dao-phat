# CLAUDE.md — AI Assistant Guide for dao-phat

This file documents the codebase structure, conventions, and workflows for AI assistants (including Claude Code) working on this project.

---

## Project Overview

**dao-phat** is a Vietnamese Buddhist knowledge base published as a static website at [hopan.vn](https://hopan.vn). It compiles Buddhist teachings, concepts, practices, history, and texts into a searchable, accessible reference site.

- **Technology:** Jekyll 4.x static site generator (Ruby)
- **Content format:** Markdown with YAML front matter
- **Primary language:** Vietnamese (all content and responses to users must be in Vietnamese)
- **Hosting:** GitHub Pages → hopan.vn

---

## Repository Structure

```
dao-phat/
├── _config.yml                 # Jekyll site configuration
├── _layouts/default.html       # Base HTML template (includes Google Analytics, back-to-top)
├── _includes/
│   ├── breadcrumbs.html        # Navigation breadcrumbs
│   └── gtag.html               # Google Analytics snippet
├── _sass/                      # Sass stylesheets
├── assets/css/                 # Compiled CSS
├── index.md                    # Home page
├── dao_phat.md                 # Buddhism introduction page
├── noi_dung_chinh.md           # Main content index
├── chi_muc.md                  # Alphabetical concept index
│
├── khai_niem/                  # Buddhist concepts A–Z (alphabetical index)
│   └── chi_muc.md              # Master alphabetical index
├── khai_niem_so/               # Buddhist concepts grouped by number (e.g. Tứ Diệu Đế = 4)
│   └── khai_niem_so.md         # Index page
├── con_nguoi/                  # Buddhist figures (Buddha, monks, laity)
├── kinh_dien/                  # Canonical texts and scriptures
├── phap/                       # Dharma teachings
├── phap_thoai_hien_dai/        # Modern dharma talks (contemporary applications)
├── thien_hang_ngay/            # Mindfulness in daily activities
├── lich_su_dia_ly/             # Buddhist history and geography
├── tong_phai/                  # Buddhist schools and sects
├── cham_soc_than_tam/          # Mind-body care
├── dao_phat_va_khoa_hoc/       # Buddhism and science
├── sach/                       # Books and PDFs
│
├── agent-plan.md               # Current work plan and progress tracking
├── agent-templates/            # 14 planning templates (BRD, persona, MVP canvas, etc.)
├── guide-coding-agent.md       # Detailed guidelines for coding agents (read this)
├── context.md                  # Running context notes (updated every ~10 prompts)
├── tools/tool.py               # Minimal Python utility script
├── Gemfile                     # Ruby gem dependencies
└── .github/workflows/pylint.yml # CI: runs pylint on Python files
```

---

## Development Commands

```bash
# Install dependencies
bundle install

# Run local development server (http://localhost:4000)
bundle exec jekyll serve

# Build static site to _site/
bundle exec jekyll build
```

The `_site/` directory is git-ignored; it is generated at build time.

---

## Content File Conventions

### Required Front Matter

Every content page **must** have a `title` front matter. Do **not** add an H1 heading — Jekyll uses the title automatically:

```yaml
---
title: Tên trang ở đây
---
```

### Standard Page Structure

Follow this structure for all concept pages (canonical example: `khai_niem_so/bat_chinh_dao.md`):

```markdown
---
title: <Tên khái niệm>
---

**Mục lục**

- TOC
{:toc}

Tham khảo:

- <https://vi.wikipedia.org/wiki/...>
- <https://en.wikipedia.org/wiki/...>

<Mô tả khái quát khái niệm, liệt kê các thành phần theo số thứ tự>

| # | Thành phần | Ý nghĩa | Chi tiết |
|---|-----------|---------|---------|
| 1 | ... | ... | [link](#anchor) |
...

## Nội dung chi tiết

### Thành phần 1

<Mô tả chi tiết>

### Thành phần 2

<Mô tả chi tiết>

## Tham chiếu

- [Khái niệm liên quan](../khai_niem_so/related.md)
```

Key rules:
- **TOC** is generated with `- TOC\n{:toc}` (Jekyll kramdown syntax)
- **References** (Tham khảo) go near the top, after the TOC
- **Numbered concepts** use a summary table listing all components with anchor links
- **Each numbered component** gets its own `###` sub-section
- **Cross-references** (Tham chiếu) go at the bottom of the page

### Numbered Concept Files (`khai_niem_so/`)

These represent Buddhist teachings identified by a number (e.g., Four Noble Truths = 4, Eightfold Path = 8). The filename uses the Vietnamese name in snake_case: `tu_dieu_de.md`, `bat_chinh_dao.md`.

### Alphabetical Concept Files (`khai_niem/`)

Concept definitions organized alphabetically. After creating or modifying files in this directory, update `khai_niem/chi_muc.md` to reflect the changes.

---

## Naming Conventions

| Item | Convention | Example |
|------|-----------|---------|
| Filenames | snake_case Vietnamese | `bat_chinh_dao.md` |
| Directories | snake_case Vietnamese | `khai_niem_so/` |
| Internal links | Relative paths | `../khai_niem_so/tu_dieu_de.md` |
| Anchor links | Lowercase, Vietnamese with diacritics | `#chánh-kiến` |

**Never use spaces in filenames.** Use underscores `_` as word separators.

---

## Internal Linking

- Within the same directory: `[text](filename.md)`
- Across directories: `[text](../target_dir/filename.md)`
- Anchor links within a page: `[text](#heading-anchor)`
- Jekyll converts Vietnamese headings to anchors by lowercasing and replacing spaces with `-`

---

## Encoding

All files must be **UTF-8 encoded**. Carefully preserve Vietnamese tone marks (diacritics) — incorrect diacritics change meaning entirely. Always verify diacritics before saving.

---

## Agent Workflow Guidelines

> Detailed guidelines are in `guide-coding-agent.md`. Read it at the start of each session.

### Session Startup Checklist

1. Read `README.md` for project overview
2. Read `guide-coding-agent.md` for agent conventions
3. Read `context.md` and files in `agent-contexts/` for current session context
4. Read `agent-plan.md` for current work plan and progress status
5. Resume from the latest checkpoint if applicable

### Context Management

- Update `context.md` approximately every 10 prompts with conversation history and current state
- Store detailed per-feature context in `agent-contexts/` directory
- Track all work items in `agent-plan.md` with completion status

### Current Work Plan (`agent-plan.md`)

The main ongoing task is filling in concept pages for `khai_niem/chi_muc.md`. Progress:
- **Completed:** Letter groups A, C, D, G, H, K
- **Pending:** Letter groups L and beyond (see roadmap table in `agent-plan.md`)

After completing each letter group:
1. Create/update individual concept `.md` files
2. Update `khai_niem/chi_muc.md` index
3. Verify all internal links work
4. Note progress in `agent-plan.md`

### Communication

- **Always respond in Vietnamese** when talking to the user
- Ask only **one question at a time** if clarification is needed
- When the user sends `.` (a single period), it means "agree / proceed automatically"

---

## CI/CD

- **Workflow:** `.github/workflows/pylint.yml`
- **Trigger:** Push or PR to `main`
- **What it does:** Runs `pylint` on all `.py` files
- Currently minimal (only `tools/tool.py` exists with one `import os` statement)

---

## Key Reference Sources

When writing or expanding Buddhist content, use these authoritative sources:

- Wikipedia tiếng Việt: `https://vi.wikipedia.org/wiki/...`
- Wikipedia English: `https://en.wikipedia.org/wiki/...`
- Stanford Encyclopedia of Philosophy: for philosophical analysis
- Original sutras and Pali Canon translations
- Internal project files: `khai_niem_so/`, `dao_phat_va_khoa_hoc/`

Always cite sources in the `Tham khảo:` section near the top of each page.

---

## What NOT to Do

- Do not add H1 headings to content pages (the `title` front matter renders as H1)
- Do not commit the `_site/` build output directory
- Do not create files with spaces in the filename
- Do not write content in English (all content is in Vietnamese)
- Do not break internal links — verify cross-references after moves/renames
- Do not add features, refactoring, or cleanup beyond what is asked
