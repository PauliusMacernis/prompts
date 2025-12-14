# Instructions for Processing Project Context File

## File Structure

This document contains a complete snapshot of a project's codebase, generated using an automated context builder. The format consists of:

1. **Header Section** - Metadata about generation time, file counts, active filters, and configuration
2. **File Tree Section** - Visual directory structure showing all included files
3. **File Contents Section** - Individual file contents with clear delimiters

## Understanding the Format

Each file entry follows this pattern:

```
📁 path/to/file.ext
────────────────────────────────────────
[file content here]

════════════════════════════════════════
```

### Special Cases

- **Media files** (images, PDFs, videos, etc.) appear in the tree but show `[MEDIA FILE - Content skipped]` instead of content
- **Truncated files** show `[Showing top N lines of file]` and end with `... [Content truncated]`
- **Context filtering** may exclude certain files from content (they appear in tree only)

## When Providing Changes

1. **Reference files by their exact path** as shown after the 📁 emoji
2. **For modifications:** Use the file's exact path and provide either:
   - Specific line replacements using old/new content pairs
   - Complete replacement file content with clear markers
3. **For new files:** Specify the full path and complete content
4. **For deletions:** Clearly state the file path to remove

## Important Considerations

- The tree shows the project structure at generation time
- Token limits may have stopped content inclusion partway through
- Some files may be intentionally excluded per project configuration
- Binary/media files cannot be modified through this context

## Best Response Format

Provide changes as actionable file operations with clear paths and content, making it easy to apply modifications systematically.
