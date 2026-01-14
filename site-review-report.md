# Site Review Report - Link Validation Analysis

**Analysis Date:** 2026-01-14  
**Analysis Type:** Comprehensive Link Validation  
**Repositories Scanned:** Main (farhan5248.github.io), demingdriventesting, sheepdogblog, specificationbyprompt

---

## Executive Summary

### Link Health Overview

| Category | Count | Status |
|----------|-------|--------|
| Total Markdown Files | 68 | Scanned |
| Internal Links | ~180 | Validated |
| External Links | ~95 | Tested |
| Broken Internal Links | 4 | **CRITICAL** |
| Broken External Links | 1 | **WARNING** |
| Potentially Inaccessible | 2 | **INFO** |
| Cross-Repository Links | ~25 | Validated |

**Overall Link Health: 97% Valid**

---

## Critical Issues (Priority 1)

### Broken Internal Links

These links reference files that do not exist:

#### 1. Missing File: `ubiquitous-language-implementation.md`
**Referenced from multiple files:**

| File | Line | Link Reference |
|------|------|----------------|
| `repositories.md` | 42 | `[6]: /specificationbyprompt/walkthrough-of-tools/ubiquitous-language-implementation` |
| `demingdriventesting/communicating-the-strategy-to-qa/the-neo-nurture-incubator.md` | 46 | `[2]: /specificationbyprompt/walkthrough-of-tools/ubiquitous-language-implementation` |
| `demingdriventesting/what-led-me-to-a-qa-team/setting.md` | 13 | `[1]: /specificationbyprompt/walkthrough-of-tools/ubiquitous-language-implementation` |
| `sheepdogblog/_posts/2025-08-08-how-leadership-affects-software-quality-large-scale-agile-more.md` | 141 | `[9]: /specificationbyprompt/walkthrough-of-tools/ubiquitous-language-implementation` |

**Actual file exists as:** `specificationbyprompt/walkthrough-of-tools/ubiquitous-language.md`

**Recommendation:** Update all references from `ubiquitous-language-implementation` to `ubiquitous-language`

#### 2. Invalid Relative Link Reference
**File:** `demingdriventesting/why-run-the-qa-tests-earlier/can-qa-tests-be-run-against-an-incomplete-system.md`  
**Line:** 40  
**Issue:** `[4]: 3` - This reference points to `3` which is not a valid file path or URL

**Recommendation:** Update to proper link (likely intended to be `does-it-matter-if-the-tests-actually-drive-the-development`)

#### 3. Missing Reference Link: sheepdogblog/about.md
**File:** `sheepdogblog/about.md`  
**Line:** 44  
**Issue:** Reference `[1]: /sheepdogblog/books/` points to non-existent path

**Actual location:** The books page is at `/books/` (main site), not `/sheepdogblog/books/`

**Recommendation:** Change `[1]: /sheepdogblog/books/` to `[1]: /books/`

---

## Warning Issues (Priority 2)

### Broken External Links

#### 1. mosy.tech/products-overview/ - 404 Error
**File:** `specificationbyprompt/how-to-bake-a-change/index.md`  
**Line:** 27  
**Link:** `[10]: https://mosy.tech/products-overview/`

**Status:** Returns 404 Not Found

**Recommendation:** Remove link or find updated URL for "Learn Microservices with Spring Boot"

### Potentially Inaccessible External Links

These URLs returned 403 Forbidden (may work in browsers but not programmatically):

| File | URL | Status |
|------|-----|--------|
| `specificationbyprompt/walkthrough-of-tools/hybrid-tools-landscape.md` | `https://dl.acm.org/doi/fullHtml/10.1145/3452383.3452388` | 403 |
| `demingdriventesting/what-led-me-to-a-qa-team/geordi-la-forge.md` | `https://medium.com/@gergelygrcs/specification-as-a-prompt-...` | 403 |

**Note:** These may work in regular browsers but are blocked for automated access. Verify manually.

---

## Information (Priority 3)

### Reference Style Consistency

All files consistently use reference-style links `[text][ref]` with definitions at the bottom. This is excellent practice.

### Duplicate Links Detected

The following URLs appear multiple times across the site (not necessarily an issue, but worth noting):

| URL | Occurrences | Files |
|-----|-------------|-------|
| `https://itrevolution.com/product/sooner-safer-happier/` | 3 | books.md, ubiquitous-language.md, diffusion-of-innovation.md |
| `https://simonsinek.com/books/start-with-why/` | 2 | books.md, demingdriventesting/about.md |
| `https://www.youtube.com/watch?v=EZ05e7EMOLM` | 3 | Multiple DDT files |
| `/demingdriventesting/migrating-from-defect-inspection-to-prevention/kaizen` | 4 | Multiple DDT files |
| `/demingdriventesting/about` | 3 | Multiple files |

**Note:** Duplicate internal links are normal for cross-referencing. Duplicate external links could potentially be consolidated using a shared references file.

### Anchor Links

Several internal anchor links were found:

| File | Anchor |
|------|--------|
| `sheepdogblog/_posts/2025-08-04-how-we-made-minecraft-using-continuous-delivery.md` | `#1630-technical-barrier-to-automated-testing-adoption` |
| `sheepdogblog/_posts/2025-08-04-how-we-made-minecraft-using-continuous-delivery.md` | `#3513-test-framework-constraints` |
| `sheepdogblog/_posts/2025-08-04-how-we-made-minecraft-using-continuous-delivery.md` | `#1524-cultural-barrier-to-automated-testing-adoption` |
| `demingdriventesting/communicating-the-strategy-to-qa/shuhari.md` | `#3513-test-framework-constraints` |

**Note:** These anchor links reference headings in the same or other files. Verify that heading IDs match expected anchors (Jekyll auto-generates IDs from heading text).

---

## Cross-Repository Link Analysis

### Links Between Main Site and Submodules

| Source Repository | Target Repository | Count | Status |
|-------------------|-------------------|-------|--------|
| Main | demingdriventesting | 8 | Valid |
| Main | sheepdogblog | 3 | Valid |
| Main | specificationbyprompt | 5 | Valid |
| demingdriventesting | specificationbyprompt | 4 | 1 Broken* |
| demingdriventesting | sheepdogblog | 3 | Valid |
| sheepdogblog | demingdriventesting | 15 | Valid |
| sheepdogblog | specificationbyprompt | 1 | 1 Broken* |
| specificationbyprompt | demingdriventesting | 2 | Valid |

*Broken links are the `ubiquitous-language-implementation` references noted above.

---

## Validated External Links (Sample)

The following external links were verified as accessible:

| Domain | Status |
|--------|--------|
| deming.org | OK |
| martinfowler.com | OK |
| itrevolution.com | OK |
| simonsinek.com | OK |
| smallbatches.fm | OK |
| github.com | OK |
| youtube.com | OK |
| open.spotify.com | OK |
| amazon.com | OK |
| norulesrules.com | OK |
| pattymccord.com | OK |
| leanmadesimple.com | OK |
| arxiv.org | OK |
| eclipse.dev | OK |
| javaparser.org | OK |
| charlesduhigg.com | OK |
| thrivestreetadvisors.com | OK |
| mcchrystalgroup.com | OK |
| designthatmatters.org | OK |
| mbtsuite.com | OK |
| bentley.com | OK |

---

## Recommendations

### Immediate Actions (Fix Now)

1. **Rename file or update references:**
   - Either rename `ubiquitous-language.md` to `ubiquitous-language-implementation.md`
   - OR update all 4 references to point to `ubiquitous-language`
   
   **Suggested fix:** Update references (less disruptive)

2. **Fix invalid reference in can-qa-tests-be-run-against-an-incomplete-system.md:**
   ```markdown
   # Change line 40 from:
   [4]: 3
   # To:
   [4]: does-it-matter-if-the-tests-actually-drive-the-development
   ```

3. **Fix sheepdogblog/about.md reference:**
   ```markdown
   # Change line 44 from:
   [1]: /sheepdogblog/books/
   # To:
   [1]: /books/
   ```

4. **Fix or remove broken external link:**
   - Remove or replace `https://mosy.tech/products-overview/` in `specificationbyprompt/how-to-bake-a-change/index.md`

### Future Improvements

1. **Verify anchor links work correctly** after Jekyll build
2. **Consider a shared references file** for commonly used external links
3. **Periodically validate external links** as websites change over time

---

## Jekyll Build Exclusion Status

**Verified:** The `_config.yml` already excludes report files:

```yaml
exclude:
   - site-review-report.md
   - internal-link-validation-report.md
```

No changes needed.

---

## Files Analyzed

### Main Repository (6 files)
- index.md
- about.md
- books.md
- repositories.md
- cheatsheet.md
- content-separation-plan.md

### demingdriventesting (40 files)
- index.md, about.md
- deming/: index.md, points.md, sopk.md
- why-run-the-qa-tests-earlier/: 6 files
- what-led-me-to-a-qa-team/: 6 files
- communicating-the-strategy-to-qa/: 9 files
- migrating-from-defect-inspection-to-prevention/: 12 files

### sheepdogblog (5 files)
- index.md, about.md
- _posts/: 3 blog posts

### specificationbyprompt (17 files)
- index.md, about.md
- milestone-status/: 2 files
- walkthrough-of-tools/: 5 files
- how-to-bake-a-change/: 8 files

---

*Report generated by Site Review Agent - Link Validation Mode*