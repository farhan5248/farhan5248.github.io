Use the site agent to perform a comprehensive analysis of the farhan5248.github.io repository and its sub-repositories (demingdriventesting, sheepdogblog, specificationbyprompt), or evolve the agent's capabilities based on conversation context.

**Note**: This agent should be used proactively for ALL questions about GitHub sites, site content, demingdriventesting topics, sheepdogblog content, or any repository analysis.

**Analysis Type**: Based on the argument provided:

- **No argument**: Perform complete comprehensive site audit covering all areas
- **content**: Content analysis only (topic coverage, file mapping, duplicate detection)
- **editorial**: Editorial review only (grammar, spelling, style improvements, readability)
- **links**: Link validation only (internal/external links, broken link detection, duplicate links)
- **linking**: Content linking and integration analysis - identify topic mentions that could be linked and suggest natural integration within existing prose
- **jekyll**: Jekyll framework maintenance only (version updates, dependency checks, GitHub Pages compatibility)
- **github**: GitHub Pages compatibility check only (configuration validation, feature updates)
- **structure**: Directory and file organization analysis (file placement, naming patterns, structural optimization)
- **naming**: File naming consistency analysis and bulk correction (spaces, case, conventions)  
- **maintenance**: Comprehensive site maintenance (file operations, structural changes, cleanup)
- **refactor**: Large-scale structural changes (directory reorganization, bulk renames with reference preservation)
- **preview [mode]**: Generate change preview for any mode that involves file operations (use with structure, naming, maintenance, or refactor)
- **comprehensive**: All analysis modes combined
- **evolve**: Analyze conversation context to improve agent capabilities and update agent/command definitions

**Instructions for the site agent**:

### For Regular Analysis (content, editorial, links, linking, jekyll, github, comprehensive, or no argument):

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
- **Detailed Findings**: Organized by analysis mode with specific file references
- **Recommendations**: Actionable next steps ranked by priority
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