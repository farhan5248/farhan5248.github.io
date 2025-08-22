Use the site agent to perform a comprehensive analysis of the farhan5248.github.io repository and its sub-repositories (demingdriventesting, sheepdogblog, specificationbyprompt), or evolve the agent's capabilities based on conversation context.

**Analysis Type**: Based on the argument provided:

- **No argument**: Perform complete comprehensive site audit covering all areas
- **content**: Content analysis only (topic coverage, file mapping, duplicate detection)
- **editorial**: Editorial review only (grammar, spelling, style improvements, readability)
- **links**: Link validation only (internal/external links, broken link detection, duplicate links)
- **jekyll**: Jekyll framework maintenance only (version updates, dependency checks, GitHub Pages compatibility)
- **github**: GitHub Pages compatibility check only (configuration validation, feature updates)
- **evolve**: Analyze conversation context to improve agent capabilities and update agent/command definitions

**Instructions for the site agent**:

### For Regular Analysis (content, editorial, links, jekyll, github, or no argument):

1. Analyze the specified area(s) across all markdown files in the main repository and the three sub-repositories
2. Focus on the Jekyll-based GitHub Pages site structure and requirements
3. Provide actionable recommendations with specific file paths and line numbers
4. Generate a prioritized report with concrete next steps
5. Consider the site's focus on QA testing, Deming principles, and software development best practices
6. Ensure all suggestions maintain content quality and technical compatibility

### For Evolution Analysis (evolve argument):

**Evolution Analysis Process**:

1. **Review Conversation Context**: Examine the recent conversation history for:
   - Tasks or requests the site agent couldn't fully complete
   - Manual work the user had to perform instead of the agent
   - New analysis types or capabilities requested
   - User feedback about reporting format or information presentation
   - Integration needs with other tools or workflows
   - Gaps in current agent knowledge or scope

2. **Compare Against Current Capabilities**: Read and analyze:
   - `.claude/agents/site.md` - Current agent definition and capabilities
   - `.claude/commands/sitereview.md` - Current command instructions
   - Identify specific gaps between what's defined and what's needed

3. **Generate Improvement Suggestions**: For each gap identified, suggest:
   - New capabilities to add to the site agent
   - Enhanced prompts or instructions for better performance
   - Additional analysis modes or reporting options
   - Better integration with repository structure or workflow
   - Improved user experience or output formatting

4. **Propose Specific Updates**: Provide:
   - Exact text additions/modifications for `.claude/agents/site.md`
   - Updates to command instructions in `.claude/commands/sitereview.md`
   - New analysis modes or parameters if needed
   - Rationale for each suggested change

5. **Implement Approved Changes**: With user confirmation:
   - Use Edit or MultiEdit tools to update the agent and command files
   - Ensure changes maintain consistency with existing capabilities
   - Preserve the working functionality while adding new features

**Focus Areas for Evolution**:
- Content analysis depth and accuracy
- Editorial review sophistication
- Jekyll/GitHub Pages maintenance completeness
- User experience and report clarity
- Integration with development workflow
- Discovery of new site management needs

**Learning Criteria**:
- **Capability Gaps**: Tasks requested but not fully achievable with current agent definition
- **Workflow Friction**: Places where user had to perform manual work instead of automated analysis
- **Enhancement Requests**: Explicit user suggestions for new features or improvements
- **Pattern Recognition**: Recurring needs that suggest new analysis modes or capabilities
- **Tool Integration**: Opportunities to better leverage available tools (Read, Grep, Glob, WebFetch, etc.)
- **Reporting Quality**: Feedback on clarity, usefulness, and actionability of generated reports

**Improvement Implementation Process**:

1. **Identify Specific Changes**: For each improvement opportunity, specify:
   - Exact location in agent/command files where changes are needed
   - New capabilities, prompts, or instructions to add
   - Modifications to existing content for better performance
   - New analysis modes, parameters, or reporting formats

2. **Validate Changes**: Ensure proposed updates:
   - Maintain consistency with existing functionality
   - Don't break current working capabilities
   - Align with the repository's focus on QA testing and Deming principles
   - Improve user experience and workflow efficiency

3. **Implement Updates**: With user approval:
   - Use MultiEdit for multiple related changes
   - Update both agent definition and command instructions as needed
   - Add new capabilities while preserving existing ones
   - Test that changes integrate well with current setup

**Evolution Success Metrics**:
- Reduced need for manual intervention in site analysis
- More comprehensive and actionable reports
- Better coverage of user's actual site management needs
- Improved integration with development and content workflow
- Enhanced detection of issues and improvement opportunities

**Expected Output**:

### For Regular Analysis:
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