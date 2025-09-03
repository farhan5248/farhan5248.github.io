Use the site agent to perform a comprehensive analysis of the farhan5248.github.io repository and its sub-repositories (demingdriventesting, sheepdogblog, specificationbyprompt), or evolve the agent's capabilities based on conversation context.

**Note**: This agent should be used proactively for ALL questions about GitHub sites, site content, demingdriventesting topics, sheepdogblog content, or any repository analysis.

**Analysis Type**: Based on the argument provided:

- **No argument**: Perform complete comprehensive site audit covering all areas
- **content**: Content analysis only (topic coverage, file mapping, duplicate detection)
- **content-separation**: Analyze and plan separation of technical content (index pages) from personal relevance (about pages)
- **repository-migration**: Plan and execute content movement between repositories with automatic reference updates
- **blog-style**: Blog post structure and format standardization (summaries, iframes, timestamps)
- **editorial**: Editorial review only (grammar, spelling, style improvements, readability)
- **links**: Link validation only (internal/external links, broken link detection, duplicate links)
- **linking**: Content linking and integration analysis - identify topic mentions that could be linked and suggest natural integration within existing prose
- **missing-files**: Detect and create missing referenced files with appropriate Jekyll frontmatter
- **implement**: Execute recommendations with safety checks and validation
- **implement-step**: Step-by-step implementation with user confirmation between each step
- **implement-preview**: Show detailed preview of planned changes without execution
- **implement-assist**: Generate detailed manual implementation instructions
- **jekyll**: Jekyll framework maintenance only (version updates, dependency checks, GitHub Pages compatibility)
- **github**: GitHub Pages compatibility check only (configuration validation, feature updates)
- **structure**: Directory and file organization analysis (file placement, naming patterns, structural optimization)
- **naming**: File naming consistency analysis and bulk correction (spaces, case, conventions)  
- **maintenance**: Comprehensive site maintenance (file operations, structural changes, cleanup)
- **refactor**: Large-scale structural changes (directory reorganization, bulk renames with reference preservation)
- **preview [mode]**: Generate change preview for any mode that involves file operations (use with structure, naming, maintenance, or refactor)
- **track-changes**: Monitor and adapt to user modifications between analysis runs
- **comprehensive**: All analysis modes combined
- **evolve**: Analyze conversation context to improve agent capabilities and update agent/command definitions

**Instructions for the site agent**:

### For Regular Analysis (content, editorial, links, linking, missing-files, jekyll, github, track-changes, comprehensive, or no argument):

1. Analyze the specified area(s) across all markdown files in the main repository and the three sub-repositories
2. Focus on the Jekyll-based GitHub Pages site structure and requirements
3. Provide actionable recommendations with specific file paths and line numbers
4. **Always save analysis results to `site-review-report.md`** with timestamp and analysis type
5. **Automatically ensure Jekyll exclusion**: Check and update `_config.yml` to exclude report files from build
6. Generate a prioritized report with concrete next steps
7. Consider the site's focus on QA testing, Deming principles, and software development best practices
8. Ensure all suggestions maintain content quality and technical compatibility

### Report Output Management:

**Default Behavior**:
- **Always save reports to file**: Create or update `site-review-report.md` with analysis results
- **Jekyll exclusion**: Automatically ensure report files are excluded from Jekyll build in `_config.yml`
- **Timestamp reports**: Include analysis date and time in report headers
- **Preserve history**: Append new analyses to existing report file with clear section breaks

**Report File Structure**:
- **Header**: Analysis type, timestamp, repository status
- **Executive Summary**: Key findings and priority actions
- **Implementation Status**: Track which recommendations have been executed
- **User Modifications**: Note changes made by user since last analysis
- **Detailed Findings**: Organized by analysis mode with specific file references
- **Recommendations**: Actionable next steps ranked by priority
- **Remaining Tasks**: Clearly identify what still needs to be addressed
- **Technical Status**: Jekyll/GitHub Pages compatibility notes

### For Link Enhancement Analysis (linking mode):

1. **Content Scanning**:
   - Scan all markdown files for topic mentions that reference content in other files
   - Identify existing link patterns (inline vs reference-style) in each file
   - Map topics to files across all repositories for cross-linking opportunities

2. **Natural Integration Suggestions**:
   - Suggest link placement within existing paragraphs where topics are naturally mentioned
   - Maintain consistency with existing link formatting in each file
   - Avoid creating separate "Related Articles" sections unless no natural integration points exist
   - Provide exact text replacements showing how to integrate links contextually

3. **Link Style Analysis**:
   - Detect whether file uses inline links `[text](url)` or reference-style `[text][ref]`
   - Maintain consistency with detected pattern
   - For reference-style links, suggest appropriate reference placement (bottom of section vs bottom of file)

4. **Cross-Repository Mapping**:
   - Build comprehensive topic-to-file mapping across main repo and all submodules
   - Identify semantic relationships between content pieces
   - Suggest bidirectional linking opportunities where appropriate

### For Implementation Operations (implement, implement-step, implement-preview, implement-assist modes):

1. **Implementation Analysis**:
   - Review existing site-review-report.md for pending recommendations
   - Assess current state of all files and identify changes needed
   - Build comprehensive change plan with dependencies and priorities
   - Detect any user modifications since last analysis

2. **Implementation Mode Selection**:
   - **implement**: Execute all recommendations automatically with safety checks
   - **implement-step**: Execute one recommendation at a time with user confirmation
   - **implement-preview**: Show detailed preview of all planned changes without execution
   - **implement-assist**: Generate step-by-step manual implementation instructions

3. **Safety and Validation**:
   - Validate all changes against Jekyll build requirements
   - Check GitHub Pages compatibility for all modifications
   - Preserve user modifications made since last analysis
   - Generate rollback information for all changes

4. **Progress Tracking**:
   - Update site-review-report.md with implementation status
   - Track completion of individual recommendations
   - Note any issues or blockers encountered during implementation
   - Maintain history of all changes made

### For Missing File Operations (missing-files mode):

1. **Reference Link Scanning**:
   - Scan all markdown files for reference-style links `[text][ref]`
   - Identify target files that don't exist
   - Analyze link context to understand intended content purpose
   - Map missing files across all repositories and submodules

2. **Smart File Creation**:
   - Create missing files with appropriate Jekyll frontmatter
   - Generate meaningful starter content based on link context
   - Follow existing site patterns for content structure
   - Apply consistent frontmatter patterns from similar files

3. **Content Structure Analysis**:
   - Analyze the linking context to suggest appropriate content outline
   - Consider site themes (QA testing, Deming principles, development practices)
   - Generate placeholder content that aligns with site's focus areas
   - Ensure created files integrate well with existing content

### For Change Tracking Operations (track-changes mode):

1. **Modification Detection**:
   - Compare current file states with last analysis timestamp
   - Identify all files modified since last site review
   - Analyze the nature and scope of user modifications
   - Assess impact of changes on existing recommendations

2. **Adaptive Analysis**:
   - Update analysis based on detected user modifications
   - Adjust recommendations to build on user changes rather than conflict
   - Identify new issues or improvements suggested by user modifications
   - Re-prioritize recommendations based on current state

3. **Integration Assessment**:
   - Determine how user changes affect overall site consistency
   - Identify opportunities to enhance or complete user modifications
   - Suggest complementary changes that align with user modifications
   - Update site-review-report.md to reflect current state and adapted recommendations

### For Structural Operations (structure, naming, maintenance, refactor modes):

1. **Analysis Phase**:
   - Scan entire repository structure and identify issues
   - Build comprehensive file and reference mapping
   - Detect naming convention violations and structural problems
   - Generate detailed change recommendations with impact analysis

2. **Preview Generation**:
   - Show all planned changes before execution
   - List files to be renamed/moved with before/after names
   - Identify all references that will be updated
   - Estimate operation complexity and time requirements
   - Highlight any potential conflicts or issues

3. **Safety Validation**:
   - Check Jekyll build compatibility of planned changes
   - Verify GitHub Pages will handle structural modifications
   - Identify any special files that need careful handling
   - Validate no circular references or broken links will result

4. **Execution Phase** (only with user confirmation):
   - Perform file operations with progress reporting
   - Update all detected references automatically
   - Validate changes don't break Jekyll build
   - Generate final report of completed changes
   - Provide rollback information if issues arise

5. **Post-Operation Verification**:
   - Run Jekyll build test to ensure site still generates
   - Validate all links still work correctly
   - Check for any orphaned files or references
   - Generate completion report with any issues found

### For Content-Personal Separation Analysis (content-separation mode):

1. **Index vs About Page Analysis**:
   - Scan index.md files for technical methodology content mixed with personal relevance
   - Identify about.md files that focus on content descriptions rather than personal connection
   - Map content that needs migration between index and about pages
   - Analyze consistency of content purpose across repositories

2. **Content Purpose Classification**:
   - Classify content as methodology, personal experience, or hybrid content
   - Identify technical concepts that should be content-focused (index pages)
   - Identify personal transformation stories that should be experience-focused (about pages)
   - Suggest optimal content distribution between page types

3. **Repository Alignment Assessment**:
   - Verify each repository's index page focuses on methodology/content description
   - Verify each repository's about page focuses on personal relevance and transformation
   - Identify content misalignment and suggest reorganization

### For Repository Migration Analysis (repository-migration mode):

1. **Cross-Repository Content Mapping**:
   - Identify content that belongs in different repositories based on topic alignment
   - Map topics currently in wrong repositories (e.g., ubiquitous language in DDT vs SBP)
   - Build migration plan preserving all internal and external references
   - Assess impact of content movement on site structure

2. **Migration Planning**:
   - Generate step-by-step migration plan with dependency handling
   - Identify all files that reference content to be moved
   - Plan automatic reference updates across all repositories
   - Estimate migration complexity and potential issues

3. **Reference Preservation Strategy**:
   - Map all references to content scheduled for migration
   - Plan URL redirects where necessary for external links
   - Ensure Jekyll build compatibility throughout migration
   - Validate no broken links result from content movement

### For Blog Style Analysis (blog-style mode):

1. **Structure Consistency Check**:
   - Verify all blog posts follow standard structure (frontmatter, Spotify embed, summary, timestamps, references)
   - Identify posts with missing or inconsistent structural elements
   - Check time-stamp organization and chronological flow
   - Validate frontmatter completeness and consistency

2. **Summary Standardization**:
   - Analyze summary sections for format consistency
   - Identify summaries that need structured overview format
   - Check for summaries that focus on content preview vs personal preference
   - Generate recommendations for summary improvements

3. **Media Format Standardization**:
   - Check iframe consistency (dimensions, parameters, styling)
   - Identify media elements that don't follow standard formatting
   - Suggest standardized formats for embedded content
   - Validate accessibility and loading performance of media

4. **Style Guide Enforcement**:
   - Apply established blog post formatting standards
   - Check for consistent tone, voice, and technical presentation
   - Validate reference-style linking throughout posts
   - Ensure professional-personal balance in content integration

### For Evolution Analysis (evolve argument):

**Evolution Process**:
- Analyze conversation context for improvement opportunities
- Compare current capabilities against discovered needs  
- Suggest specific enhancements to agent capabilities
- Propose updates to `.claude/agents/site.md` and `.claude/commands/sitereview.md`
- Implement approved changes to evolve the agent
- Create continuous improvement feedback loop based on real usage patterns

**Expected Output**:

### For Regular Analysis:
- **Report file created/updated**: `site-review-report.md` with timestamped analysis results
- **Jekyll configuration verified**: `_config.yml` updated to exclude report files if needed
- Summary of findings organized by analysis type
- Specific issues identified with file locations
- Actionable recommendations ranked by priority
- Status of Jekyll framework and GitHub Pages compatibility
- Suggestions for content improvements and maintenance tasks

### For Evolution Analysis:
- Analysis of conversation context for improvement opportunities
- Specific suggestions for enhancing agent capabilities
- Proposed updates to `.claude/agents/site.md` and `.claude/commands/sitereview.md`
- Implementation of approved changes to evolve the agent
- Summary of improvements made and their expected benefits

This creates a feedback loop where the site management system continuously improves based on real usage patterns and discovered needs, making it more effective over time.