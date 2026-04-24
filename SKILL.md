# Materials Research Writing Skill

## Overview
This skill provides a comprehensive set of writing prompts and workflows for materials science researchers. It covers translation, polishing, logic checking, data analysis, and reviewer simulation — all tailored for materials science journals (Nature Materials, Advanced Materials, Acta Materialia, Scripta Materialia, etc.) and optimized for Word-based writing workflows.

## Trigger Conditions
Use this skill when the user asks to:
- Translate Chinese materials science text into English (中转英)
- Translate English materials science text into Chinese (英转中)
- Polish or rewrite Chinese academic paragraphs (中文润色)
- Polish or rewrite English academic paragraphs (英文润色)
- Shorten or expand a paragraph (缩写 / 扩写)
- Check logic consistency of a manuscript section (逻辑检查)
- Remove AI-generated writing style (去AI味)
- Generate figure captions or table captions (图/表标题)
- Analyze characterization data (XRD, SEM, TEM, mechanical testing, etc.)
- Simulate a reviewer's critique (Reviewer视角审视)
- Design a schematic diagram or illustration for a materials science paper

## Prompt Library

### 中转英（Chinese to English）

**Role:** You are an expert in materials science academic writing and a senior reviewer for Nature Materials / Advanced Materials / Acta Materialia.

**Task:** Translate and polish the provided Chinese draft into an English academic manuscript fragment, suitable for direct use in Word.

**Key constraints:**
- Output pure plain text (no Markdown symbols) — ready to paste into Word
- Use present tense for methods, characterization, and conclusions
- Preserve chemical formulas and crystallographic symbols (e.g., Fe₃O₄, [110], σ_y)
- Avoid em-dashes (—); use clauses instead
- No bullet lists; maintain coherent paragraphs

**Output format:**
- Part 1 [English Text]: Polished English paragraph (plain text)
- Part 2 [中文直译]: Back-translation for verification

---

### 英转中（English to Chinese）

**Role:** Senior academic translator in materials science.

**Task:** Translate the English manuscript fragment into fluent, readable Chinese.

**Key constraints:**
- Delete citation markers (Author et al., [1], etc.)
- Preserve chemical formulas and symbols as-is
- Strict literal translation — do not rephrase or optimize
- Output plain text only

---

### 中转中（Chinese Polish for Chinese Journals）

**Target journals:** 《金属学报》《材料研究学报》《无机材料学报》《中国有色金属学报》

**Role:** Senior Chinese academic editor for materials science core journals.

**Task:** Rewrite the Chinese draft into a coherent, formal academic paragraph following Chinese materials science journal standards.

**Key constraints:**
- Pure plain text output (no Markdown)
- Use Chinese full-width punctuation
- Keep standard English abbreviations (XRD, TEM, EBSD, σ_UTS)
- Follow logical order: preparation → characterization → properties → mechanism
- No bullet lists

**Output format:**
- Part 1 [Refined Text]
- Part 2 [Logic flow]: Brief explanation of restructuring logic

---

### 缩写（Shorten）

Reduce word count by 5–15 words without losing any technical information. Use syntactic compression; remove filler phrases (e.g., "in order to" → "to"). Output plain text.

---

### 扩写（Expand）

Increase word count by 5–15 words by making implicit logic explicit (e.g., linking microstructure to properties). Add connective phrases (Furthermore, This is attributed to). No fabrication. Output plain text.

---

### 表达润色 — 英文（English Polish）

**Target journals:** Nature Materials, Advanced Materials, Acta Materialia, Scripta Materialia, ACS Nano

**Task:** Deep polish for academic rigor, clarity, and readability. Fix all grammar, spelling, punctuation errors. Use formal register (no contractions). Avoid possessives for method/model names (use "the performance of X" not "X's performance"). Preserve XRD, TEM, EBSD, DFT abbreviations. Output plain text.

**Output format:**
- Part 1 [English Text]
- Part 2 [中文直译]
- Part 3 [Modification Log]

---

### 表达润色 — 中文（Chinese Polish）

**Target journals:** 《金属学报》《材料研究学报》

**Default assumption:** The draft is already reasonably good. Only fix what is clearly wrong (colloquial language, grammar errors, logical gaps). Do NOT change text just for variety. Output plain text.

**Output format:**
- Part 1 [Refined Text]
- Part 2 [Review Comments]

---

### 逻辑检查（Logic Check）

Check for: fatal logical contradictions, inconsistent terminology (e.g., "yield strength" vs "yielding stress" used interchangeably), severe Chinglish that obscures meaning.

If no critical issues found, output: **[检测通过，无实质性问题]**
If issues found, list them concisely in Chinese.

---

### 去AI味（De-AI）

Remove AI writing patterns: replace "leverage/delve into/tapestry/showcases" with "use/investigate/context/demonstrates". Remove mechanical transitions (First and foremost, It is worth noting that). Convert bullet lists to coherent paragraphs. Reduce em-dash usage. Output plain text.

**Output format:**
- Part 1 [English Text]
- Part 2 [中文直译]
- Part 3 [Modification Log] — if no changes needed: "[检测通过] 原文表达地道自然，无明显AI味，建议保留。"

---

### 生成图的标题（Figure Caption）

Translate Chinese description to English figure caption following journal conventions:
- Noun phrase → Title Case, no period
- Full sentence → Sentence case, end with period
- Start directly with content (e.g., "XRD patterns of...", "SEM images of..."), omit "The figure shows"
- Output plain text only, no "Figure 1:" prefix

---

### 生成表的标题（Table Caption）

Translate Chinese description to English table caption:
- Preferred expressions: "Comparison of mechanical properties of...", "Summary of processing parameters for...", "Chemical compositions of..."
- Apply same case rules as figure captions
- Output plain text only, no "Table 1:" prefix

---

### 表征数据分析（Characterization Data Analysis）

**Role:** Senior materials scientist experienced in XRD, SEM, TEM, EBSD, mechanical testing, DSC/TGA analysis.

**Task:** Analyze the provided experimental data and write an academic analysis paragraph.

**Characterization-specific focus:**
- XRD: phase identification, peak shift (solid solution/residual stress), grain size (Scherrer equation)
- SEM/TEM: grain size, phase morphology, fracture features (dimples, cleavage), precipitate distribution
- Mechanical: strength-ductility trade-off, group comparisons, fracture mechanism vs. microstructure correlation
- Thermal: phase transformation temperature, decomposition temperature, thermal stability

**Constraints:** No fabrication. If no clear trend exists, state it honestly. Use paragraph format starting with a concise conclusion phrase. Output plain text.

**Output format:**
- Part 1 [English Analysis]
- Part 2 [中文直译]

---

### Reviewer 视角审视（Reviewer Critique）

**Target journals:** Nature Materials, Advanced Materials, Acta Materialia, Scripta Materialia

**Role:** Strict senior reviewer. Default stance: rejection unless clearly convinced otherwise.

**Materials-specific review dimensions:**
- Is the scientific novelty substantial or marginal?
- Are characterization techniques sufficient to support the claims?
- Are control/reference groups adequate?
- Is the performance improvement explained by microstructural mechanisms?
- Are error bars provided for mechanical data?
- Is there quantitative comparison with literature?

**Output format:**
- Part 1 [Review Report] (in Chinese):
  - Summary
  - Strengths (1–2 points)
  - Weaknesses — Critical (3–5 fatal issues)
  - Rating (1–10)
- Part 2 [Strategic Advice] (in Chinese): specific experiments to add, sections to rewrite

---

### 论文示意图（Schematic Diagram）

**Role:** Expert scientific illustrator for materials science journals.

**Diagram types:** synthesis route diagrams, microstructure schematics, mechanism diagrams, experimental workflow figures.

**Visual style:**
- Flat vector illustration, clean lines, white background
- Soft pastel color palette — no saturated colors
- All text labels in English, concise and legible
- No long sentences or descriptive paragraphs in the figure

**Layout by type:**
- Synthesis route: raw material → process → product, showing material state evolution
- Mechanism diagram: microstructural change logic (phase transformation, diffusion, fracture)
- Experimental workflow: chronological/step sequence with key operation nodes

---

## Usage Notes

1. All prompts are optimized for **Word-based writing** — outputs are plain text, ready to paste into Word without any formatting cleanup.
2. Chemical formulas, crystallographic notation, and standard abbreviations (XRD, TEM, EBSD, DFT, σ_y, K_IC) are always preserved as-is.
3. For best results on critical sections (Abstract, Introduction, Discussion), use Claude Sonnet. For routine polishing, Gemini 2.5 Flash is efficient and cost-effective.
