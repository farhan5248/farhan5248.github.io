# Content Separation Implementation Plan

*Analysis Date: 2025-09-03*
*Objective: Restructure files to properly separate content descriptions (index) from personal relevance (about)*

## Implementation Steps

### Step 1: Main Site Index Page Content Focus
**File**: `index.md`
**Changes**:
- Remove personal journey details ("I'm not a traditional QA professional...")
- Remove "Unfortunately there wasn't much information online..." explanation
- Focus on what visitors will learn from each site
- Expand site navigation descriptions with clear value propositions
- Keep high-level goal but make it content-focused

### Step 2: Deming Driven Testing Index Page Enhancement
**File**: `demingdriventesting/index.md`
**Changes**:
- Add detailed learning outcomes for each numbered section
- Include "The Approach" methodology details moved from about page
- Expand descriptions of what each section covers
- Add clear takeaways visitors will gain

### Step 3: Deming Driven Testing About Page Restructuring
**File**: `demingdriventesting/about.md`
**Changes**:
- Move technical methodology details ("The Approach" 4-point section) to index page
- Move "Ubiquitous language" section to appropriate content pages  
- Keep "Why Deming Driven Testing" section as personal motivation
- Expand personal transformation journey details
- Focus on human side of the methodology adoption

### Step 4: Specification By Prompt About Page Restructuring  
**File**: `specificationbyprompt/about.md`
**Changes**:
- Move technical "Why" questions with detailed technical answers to content pages
- Keep personal problem statement about monolith challenges
- Expand 2018-2022 personal journey details
- Add personal reflections on pre-AI to post-AI evolution
- Focus on lessons learned and thinking evolution

### Step 5: Sheep Dog Blog Index Page Enhancement
**File**: `sheepdogblog/index.md`
**Changes**:
- Add brief descriptions of what readers gain from each episode
- Include thematic categories covered across episodes
- Enhance value proposition for visitors

### Step 6: Sheep Dog Blog About Page Expansion
**File**: `sheepdogblog/about.md`
**Changes**:
- Significantly expand from current brief content
- Explain personal connection to selected podcasts
- Detail how these podcasts influenced transformation approach
- Share selection criteria for episodes
- Add personal insights gained from these sources

### Step 7: Review All Links Across the Site
**Files**: All markdown files across all repositories
**Changes**:
- Validate all internal and external links work correctly
- Check for broken links and fix or remove them
- Ensure consistent link formatting (reference-style vs inline)
- Verify cross-repository links function properly
- Update outdated external links

### Step 8: Review Blog Posts for Consistent Style
**Files**: All blog post articles in sheepdogblog and other content
**Changes**:
- Ensure each article has a summary at the top
- Divide articles by time or topic with clear sections
- Standardize formatting and structure across posts
- Check for consistent tone and style
- Verify proper use of headings and organization

## Files Not Requiring Changes
- **Main site about.md**: Already excellent personal focus
- **Specification By Prompt index.md**: Already well-structured for content

## Expected Outcomes
- **Index pages**: Focus on content value, learning outcomes, methodology descriptions
- **About pages**: Focus on personal motivation, journey, and relevance to the author
- Clear separation between "what the site offers" vs "why this matters to me"