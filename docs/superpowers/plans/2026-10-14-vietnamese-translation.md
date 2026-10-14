# Vietnamese Translation Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:subagent-driven-development (recommended) or superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Translate all 18 markdown files in the repo from English to Vietnamese (overwriting originals), add a new `GLOSSARY.md`, per `docs/superpowers/specs/2026-10-14-vietnamese-translation-design.md`.

**Architecture:** Content-translation task, not code. Each task group translates one directory's files (prose + headings), preserves all URLs/code blocks/table structure, and is verified by an automated URL-integrity diff (not unit tests — there is no executable code here). Final task builds the glossary from terms actually kept in English across the translated set, then fixes the README TOC anchors.

**Tech Stack:** Markdown only. Bash/grep for verification (no test framework applies).

## Global Constraints

- Overwrite original files in place; no `.vi.md` or `/vi/` duplicates (spec §Quyết định 1).
- Proper nouns (course/book/tool names) and their URLs stay in English/unchanged; only surrounding prose is translated (spec §2).
- Technical terms (Machine Learning, Deep Learning, Agent, Prompt, Fine-tuning, Embedding, RAG, LLM, Transformer, and similar) stay in English, no inline Vietnamese gloss in parentheses (spec §3).
- New `GLOSSARY.md` at repo root lists every such kept-English term with a short Vietnamese explanation, grouped by topic area (spec §4).
- All headings translated to Vietnamese; README's TOC must be updated to match new anchors — no backward-compat anchors kept (spec §5).
- Directory/file names, code blocks, table structure, badges, numeric data, and URLs stay unchanged (spec §6).
- Every URL present before translation must still be present, byte-identical, after translation (verification mechanism for every task below).

---

### Task 1: README.md — translate + fix TOC anchors + add GLOSSARY link

**Files:**
- Modify: `README.md`
- Test: none (markdown), verified via URL-diff command below

**Interfaces:**
- Produces: final Vietnamese heading text for README's top-level sections — Task 7 (GLOSSARY.md) will reference this file's "Mục lục" section for cross-linking.

- [ ] **Step 1: Snapshot current URLs as the baseline**

```bash
cd /Users/ho.duc.haib/Documents/Game/Ai-Engineering-Roadmap
git show HEAD:README.md | grep -oE '\(https?://[^)]+\)' | sort > /tmp/readme_urls_before.txt
wc -l /tmp/readme_urls_before.txt
```

Expected: a non-zero line count (baseline captured).

- [ ] **Step 2: Translate the file**

Read `README.md`. Translate all prose and headings to Vietnamese. Keep proper nouns (e.g. "OSSU-CS") and all URLs unchanged. Keep technical terms in English per Global Constraints (e.g. "AI Engineer", "Machine Learning", "Deep Learning", "LLMs", "Agentic AI", "RAG", "Prompt Engineering" stay as-is). Rewrite the "Table of Contents" section so each `[Vietnamese heading](#new-anchor)` link matches the translated heading's actual GitHub-style slug (lowercase, spaces→hyphens, punctuation stripped). Add one new TOC entry + section link pointing to `GLOSSARY.md` for term definitions, placed near "How to Use This".

- [ ] **Step 3: Verify URL integrity**

```bash
grep -oE '\(https?://[^)]+\)' README.md | sort > /tmp/readme_urls_after.txt
diff /tmp/readme_urls_before.txt /tmp/readme_urls_after.txt
```

Expected: no output (empty diff = every URL preserved).

- [ ] **Step 4: Verify every TOC link resolves to a real heading**

```bash
grep -oE '^#{1,6} .+' README.md | sed -E 's/^#+ //' > /tmp/readme_headings.txt
cat /tmp/readme_headings.txt
grep -oE '\(#[a-z0-9-]+\)' README.md | sort -u
```

Manually confirm each `(#anchor)` from the TOC corresponds to one slugified heading in `/tmp/readme_headings.txt` (lowercase heading, spaces→`-`, strip punctuation other than `-`).

- [ ] **Step 5: Commit**

```bash
git add README.md
git commit -m "Translate README.md to Vietnamese, fix TOC anchors"
```

---

### Task 2: Governance files — CONTRIBUTING.md, CODE_OF_CONDUCT.md, SECURITY.md, CHANGELOG.md

**Files:**
- Modify: `CONTRIBUTING.md`, `CODE_OF_CONDUCT.md`, `SECURITY.md`, `CHANGELOG.md`
- Test: none (markdown), verified via URL-diff command below

**Interfaces:**
- Consumes: none
- Produces: nothing other tasks depend on

- [ ] **Step 1: Snapshot URLs for all four files**

```bash
cd /Users/ho.duc.haib/Documents/Game/Ai-Engineering-Roadmap
for f in CONTRIBUTING.md CODE_OF_CONDUCT.md SECURITY.md CHANGELOG.md; do
  git show HEAD:"$f" | grep -oE '\(https?://[^)]+\)' | sort > "/tmp/$(basename "$f").before"
done
ls -la /tmp/*.before
```

Expected: four `.before` files listed (some may be empty if a file has no links — that's fine).

- [ ] **Step 2: Translate each file**

Read and translate each of the four files to Vietnamese, same rules as Task 1 (keep proper nouns/URLs/technical terms in English, translate headings and prose). `CHANGELOG.md` entries: translate the descriptive text, keep version numbers/dates unchanged.

- [ ] **Step 3: Verify URL integrity per file**

```bash
for f in CONTRIBUTING.md CODE_OF_CONDUCT.md SECURITY.md CHANGELOG.md; do
  grep -oE '\(https?://[^)]+\)' "$f" | sort > "/tmp/$(basename "$f").after"
  echo "--- $f ---"
  diff "/tmp/$(basename "$f").before" "/tmp/$(basename "$f").after"
done
```

Expected: no diff output under any `--- file ---` header.

- [ ] **Step 4: Commit**

```bash
git add CONTRIBUTING.md CODE_OF_CONDUCT.md SECURITY.md CHANGELOG.md
git commit -m "Translate governance docs to Vietnamese"
```

---

### Task 3: 01_foundation/ — programming, math, machine-learning, deep-learning

**Files:**
- Modify: `01_foundation/01_programming.md`, `01_foundation/02_math.md`, `01_foundation/03_machine-learning.md`, `01_foundation/04_deep-learning.md`
- Test: none (markdown), verified via URL-diff command below

**Interfaces:**
- Consumes: none
- Produces: list of English technical terms encountered — carry forward informally to Task 7 (glossary), no formal interface needed since Task 7 re-scans all files itself

- [ ] **Step 1: Snapshot URLs for all four files**

```bash
cd /Users/ho.duc.haib/Documents/Game/Ai-Engineering-Roadmap
for f in 01_foundation/01_programming.md 01_foundation/02_math.md 01_foundation/03_machine-learning.md 01_foundation/04_deep-learning.md; do
  git show HEAD:"$f" | grep -oE '\(https?://[^)]+\)' | sort > "/tmp/$(basename "$f").before"
done
```

- [ ] **Step 2: Translate each file**

Translate headings and prose to Vietnamese. Keep course/book/tool names and their URLs unchanged. Keep technical terms in English (e.g. "Data Structures", "Linear Algebra" is a math field name — translate as "Đại số tuyến tính" since it's a generic math subject, not an AI-specific technical term; but keep AI/CS-specific terms like "Neural Networks", "CNNs", "RNNs", "Transformers", "Machine Learning", "Deep Learning" in English per Global Constraints).

- [ ] **Step 3: Verify URL integrity per file**

```bash
for f in 01_foundation/01_programming.md 01_foundation/02_math.md 01_foundation/03_machine-learning.md 01_foundation/04_deep-learning.md; do
  grep -oE '\(https?://[^)]+\)' "$f" | sort > "/tmp/$(basename "$f").after"
  echo "--- $f ---"
  diff "/tmp/$(basename "$f").before" "/tmp/$(basename "$f").after"
done
```

Expected: no diff output under any header.

- [ ] **Step 4: Commit**

```bash
git add 01_foundation/
git commit -m "Translate 01_foundation docs to Vietnamese"
```

---

### Task 4: 02_specializations/ — computer-vision, nlp, reinforcement-learning

**Files:**
- Modify: `02_specializations/computer-vision.md`, `02_specializations/nlp.md`, `02_specializations/reinforcement-learning.md`
- Test: none (markdown), verified via URL-diff command below

- [ ] **Step 1: Snapshot URLs**

```bash
cd /Users/ho.duc.haib/Documents/Game/Ai-Engineering-Roadmap
for f in 02_specializations/computer-vision.md 02_specializations/nlp.md 02_specializations/reinforcement-learning.md; do
  git show HEAD:"$f" | grep -oE '\(https?://[^)]+\)' | sort > "/tmp/$(basename "$f").before"
done
```

- [ ] **Step 2: Translate each file**

Translate headings and prose to Vietnamese. Keep course/book/tool names and URLs unchanged. Keep "Computer Vision", "NLP", "Reinforcement Learning", "CNNs", "Transformers", and similar technical terms in English.

- [ ] **Step 3: Verify URL integrity per file**

```bash
for f in 02_specializations/computer-vision.md 02_specializations/nlp.md 02_specializations/reinforcement-learning.md; do
  grep -oE '\(https?://[^)]+\)' "$f" | sort > "/tmp/$(basename "$f").after"
  echo "--- $f ---"
  diff "/tmp/$(basename "$f").before" "/tmp/$(basename "$f").after"
done
```

Expected: no diff output under any header.

- [ ] **Step 4: Commit**

```bash
git add 02_specializations/
git commit -m "Translate 02_specializations docs to Vietnamese"
```

---

### Task 5: 03_modern-Ai/ — llms, agentic-ai, rag, prompt-engineering, ai-tooling

**Files:**
- Modify: `03_modern-Ai/01_llms.md`, `03_modern-Ai/02_agentic-ai.md`, `03_modern-Ai/03_rag.md`, `03_modern-Ai/04_prompt-engineering.md`, `03_modern-Ai/05_ai-tooling.md`
- Test: none (markdown), verified via URL-diff command below

- [ ] **Step 1: Snapshot URLs**

```bash
cd /Users/ho.duc.haib/Documents/Game/Ai-Engineering-Roadmap
for f in 03_modern-Ai/01_llms.md 03_modern-Ai/02_agentic-ai.md 03_modern-Ai/03_rag.md 03_modern-Ai/04_prompt-engineering.md 03_modern-Ai/05_ai-tooling.md; do
  git show HEAD:"$f" | grep -oE '\(https?://[^)]+\)' | sort > "/tmp/$(basename "$f").before"
done
```

- [ ] **Step 2: Translate each file**

Translate headings and prose to Vietnamese. Keep course/book/tool names and URLs unchanged. Keep "LLMs", "Agentic AI", "RAG", "Prompt Engineering", "Fine-tuning", "Embedding", "Agent", "Prompt" in English per Global Constraints.

- [ ] **Step 3: Verify URL integrity per file**

```bash
for f in 03_modern-Ai/01_llms.md 03_modern-Ai/02_agentic-ai.md 03_modern-Ai/03_rag.md 03_modern-Ai/04_prompt-engineering.md 03_modern-Ai/05_ai-tooling.md; do
  grep -oE '\(https?://[^)]+\)' "$f" | sort > "/tmp/$(basename "$f").after"
  echo "--- $f ---"
  diff "/tmp/$(basename "$f").before" "/tmp/$(basename "$f").after"
done
```

Expected: no diff output under any header.

- [ ] **Step 4: Commit**

```bash
git add 03_modern-Ai/
git commit -m "Translate 03_modern-Ai docs to Vietnamese"
```

---

### Task 6: Capstone docs — 04_capstone-project/capstone-projects.md, 07_capstone-projects_README.md

**Files:**
- Modify: `04_capstone-project/capstone-projects.md`, `07_capstone-projects_README.md`
- Test: none (markdown), verified via URL-diff command below

- [ ] **Step 1: Snapshot URLs**

```bash
cd /Users/ho.duc.haib/Documents/Game/Ai-Engineering-Roadmap
for f in 04_capstone-project/capstone-projects.md 07_capstone-projects_README.md; do
  git show HEAD:"$f" | grep -oE '\(https?://[^)]+\)' | sort > "/tmp/$(basename "$f").before"
done
```

- [ ] **Step 2: Translate each file**

Translate headings and prose to Vietnamese. Keep project/tool names and URLs unchanged. Keep AI-specific technical terms in English per Global Constraints.

- [ ] **Step 3: Verify URL integrity per file**

```bash
for f in 04_capstone-project/capstone-projects.md 07_capstone-projects_README.md; do
  grep -oE '\(https?://[^)]+\)' "$f" | sort > "/tmp/$(basename "$f").after"
  echo "--- $f ---"
  diff "/tmp/$(basename "$f").before" "/tmp/$(basename "$f").after"
done
```

Expected: no diff output under any header.

- [ ] **Step 4: Commit**

```bash
git add 04_capstone-project/ 07_capstone-projects_README.md
git commit -m "Translate capstone docs to Vietnamese"
```

---

### Task 7: Create GLOSSARY.md and link it from README

**Files:**
- Create: `GLOSSARY.md`
- Modify: `README.md` (verify the link added in Task 1 Step 2 resolves)

**Interfaces:**
- Consumes: the full set of English-kept technical terms across all translated files (Tasks 1–6)
- Produces: `GLOSSARY.md` with one `##` section per topic area (Foundation, Specializations, Modern AI) and a bullet list of `**Term** — Vietnamese explanation.` per term

- [ ] **Step 1: Collect every English technical term actually left in the translated files**

```bash
cd /Users/ho.duc.haib/Documents/Game/Ai-Engineering-Roadmap
grep -rhoE '\b[A-Z][a-zA-Z]*( [A-Z][a-zA-Z]*)*\b' 01_foundation/ 02_specializations/ 03_modern-Ai/ 04_capstone-project/ README.md | sort | uniq -c | sort -rn | head -80
```

Read the translated files directly to compile the authoritative list — this grep is a starting aid, not the source of truth (it will catch proper nouns too; filter manually to only the technical terms named in Global Constraints and any others you kept in English during translation).

- [ ] **Step 2: Write GLOSSARY.md**

Create `GLOSSARY.md` with a short intro line explaining its purpose, then one `##` section per topic area (Foundation, Specializations, Modern AI, Capstone), each with a bullet per English term found in Step 1, formatted as `- **Term** — giải thích ngắn gọn bằng tiếng Việt.`

- [ ] **Step 3: Add/verify the README link**

Confirm `README.md` (from Task 1 Step 2) has a working link to `GLOSSARY.md`, e.g. `[Thuật ngữ](GLOSSARY.md)` in the TOC or a dedicated section. If missing, add it now.

```bash
grep -n "GLOSSARY.md" README.md
```

Expected: at least one match.

- [ ] **Step 4: Commit**

```bash
git add GLOSSARY.md README.md
git commit -m "Add GLOSSARY.md for English technical terms"
```

---

### Task 8: Final full-repo verification

**Files:** none created/modified — read-only verification pass

- [ ] **Step 1: Full-repo URL integrity check against the pre-translation commit**

```bash
cd /Users/ho.duc.haib/Documents/Game/Ai-Engineering-Roadmap
BASE=$(git log --oneline | grep "Add design spec for Vietnamese translation" | cut -d' ' -f1)
for f in README.md CONTRIBUTING.md CODE_OF_CONDUCT.md SECURITY.md CHANGELOG.md 07_capstone-projects_README.md $(find 01_foundation 02_specializations 03_modern-Ai 04_capstone-project -name "*.md"); do
  git show "$BASE":"$f" | grep -oE '\(https?://[^)]+\)' | sort > /tmp/final_before.txt
  grep -oE '\(https?://[^)]+\)' "$f" | sort > /tmp/final_after.txt
  if ! diff -q /tmp/final_before.txt /tmp/final_after.txt > /dev/null; then
    echo "MISMATCH in $f"
    diff /tmp/final_before.txt /tmp/final_after.txt
  fi
done
echo "Done."
```

Expected: only "Done." printed, no "MISMATCH" lines.

- [ ] **Step 2: Confirm no file was missed**

```bash
grep -rliE '\b(the|and|with|this|that|should|your)\b' README.md CONTRIBUTING.md CODE_OF_CONDUCT.md SECURITY.md CHANGELOG.md 07_capstone-projects_README.md 01_foundation/*.md 02_specializations/*.md 03_modern-Ai/*.md 04_capstone-project/*.md
```

Review any matches manually — common English filler words surviving in bulk (not inside a kept English term or proper noun) signal a missed paragraph. Expected: no unexplained matches, or only matches inside intentionally-English proper nouns/terms.

- [ ] **Step 3: Confirm GLOSSARY.md exists and README links to it**

```bash
test -f GLOSSARY.md && echo "GLOSSARY.md exists"
grep -n "GLOSSARY.md" README.md
```

Expected: both lines print.
