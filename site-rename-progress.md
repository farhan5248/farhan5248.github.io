# Site Rename Progress: modularmonolith → specificationbyprompt

## Overview
This document tracks the progress of renaming the "modularmonolith" site to "specificationbyprompt" across all repositories and configurations.

## 4-Part Implementation Plan

### ✅ Part 1: Local Dev Setup - COMPLETED
**Status**: All tasks completed

#### Tasks Completed:
1. ✅ **Clone new repository**: Cloned `specificationbyprompt` into `C:\Users\Farhan\git\sheep-dog-main\specificationbyprompt` (later moved to correct location)
2. ✅ **Update Claude Code settings**: Updated `.claude\settings.local.json` to reference new repository paths
3. ✅ **Remove old directories**: User manually deleted old `demingdriventesting`, `modularmonolith`, and `sheepdogblog` directories

#### Final State:
- Repository structure corrected to have `specificationbyprompt` as submodule in `farhan5248.github.io`
- Settings updated to reflect proper submodule structure
- All working directories properly configured in Claude Code settings

---

### ✅ Part 2: Update refs in farhan5248.github.io - COMPLETED
**Status**: All tasks completed

#### Files Updated:
1. ✅ **`.gitmodules`** - Updated by user to replace modularmonolith with specificationbyprompt submodule
2. ✅ **`index.md:21`** - Changed `[**Modular Monolith**:](modularmonolith)` to `[**Specification By Prompt**:](specificationbyprompt)`
3. ✅ **`repositories.md:33`** - Changed `[Modular Monolith site](/modularmonolith)` to `[Specification By Prompt site](/specificationbyprompt)`
4. ✅ **`_config.yml:71`** - Updated exclude list from `modularmonolith/` to `specificationbyprompt/`

#### Additional Changes Made by User:
- Updated `index.md:21-22` with expanded description: "This describes how I would go about breaking up a monolith by using the QA team's natural language DSL. Each feature file would be treated as a prompt for Claude code to write the code from scratch..."

---

### ✅ Part 3: Update refs in specificationbyprompt repository - COMPLETED
**Status**: All tasks completed

#### Files Updated:
1. ✅ **`_config.yml:21`** - Updated `title: Modular Monolith` to `title: Specification By Prompt`
2. ✅ **`_config.yml:26`** - Updated `baseurl: "/modularmonolith"` to `baseurl: "/specificationbyprompt"`
3. ✅ **`index.md:3`** - Updated `title: Modular Monolith` to `title: Specification By Prompt`
4. ✅ **`about.md:7-8`** - Updated content to reflect new concept using QA DSL as prompts for Claude Code

#### Note on Recent Changes:
- User reverted some changes in `_config.yml` and `index.md` back to "Modular Monolith" - may need to re-apply
- `about.md` was reverted to original modular monolith description

---

### 🚧 Part 4: Update refs in main repo - PENDING
**Status**: Not started yet

#### Files That Need Updates:
1. **`CLAUDE.md:27`** - Update `- **modularmonolith**: Architecture documentation` to `- **specificationbyprompt**: Specification By Prompt documentation`
2. **`CLAUDE.architecture.md:109`** - Update documentation site reference from modularmonolith to specificationbyprompt
3. **`.claude\settings.local.json`** - Already updated in Part 1

---

## Current Repository Structure
```
C:\Users\Farhan\git\
├── sheep-dog-main\
│   ├── sheep-dog-qa\
│   ├── sheep-dog-ops\
│   ├── sheep-dog-local\
│   ├── sheep-dog-cloud\
│   └── CLAUDE.md (needs update)
└── farhan5248.github.io\
    ├── sheepdogblog\ (submodule)
    ├── demingdriventesting\ (submodule)
    └── specificationbyprompt\ (submodule)
```

## Key URLs and References Updated
- GitHub repository: `https://github.com/farhan5248/specificationbyprompt.git`
- Site URL: `https://farhan5248.github.io/specificationbyprompt`
- Local path: `C:\Users\Farhan\git\farhan5248.github.io\specificationbyprompt`

## Status Summary
- **Parts 1-2**: ✅ Fully completed
- **Part 3**: ✅ Completed (may need to re-apply some reverted changes)
- **Part 4**: 🚧 Ready to start after restart

## Next Steps After Restart
1. Complete Part 4: Update remaining references in sheep-dog-main repository
2. Verify all links work correctly
3. Test GitHub Pages deployment
4. Optional cleanup of any remaining old references

---

*Generated on: 2025-08-22*
*Last updated: Before computer restart*