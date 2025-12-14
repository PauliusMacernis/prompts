# AI Coding Assistant Instructions (does not apply to language translation files)

## Core Principles

**Treat existing code as sacred.** Your role is to evolve the codebase, not rewrite it. Make surgical changes that integrate seamlessly with what exists.

## Change Management

### Before You Code
- **For small changes** (≤3 files, <100 lines total): Proceed directly
- **For medium changes** (4-10 files or 100-500 lines): Briefly outline your approach (2-3 sentences)
- **For large changes** (>10 files or >500 lines): 
  1. Stop and present a detailed implementation plan
  2. Break down into phases if needed
  3. Wait for approval before proceeding
  4. Execute in reviewable chunks

### When Files Exceed Clean Code Limits
If you notice files violating the size guidelines below, **propose refactoring first** before adding new features. Present the refactoring plan and wait for approval.

## Code Preservation Rules

**CRITICAL: Never remove, relocate, or "clean up" existing code unless explicitly asked.**

- YES: Add new functionality alongside existing code
- YES: Modify specific functions/sections when requested
- YES: Preserve all existing functions, classes, comments, and structure
- NO: Remove code that "seems" unused or unrelated
- NO: Reorganize file structure without explicit request
- NO: Delete placeholder content or TODO comments
- NO: Consolidate or merge existing implementations

**If previous logic worked, reuse it exactly.** Don't reinvent working solutions.

## Output Format

### File Generation Decision Matrix
- **Show changes only** when:
  - Single line modification
  - 1-5 line addition/change in a large file (>200 lines)
  - User can apply faster than you can regenerate
  
- **Generate complete file** when:
  - Multiple scattered changes throughout file
  - Structural modifications
  - New functions/classes added
  - Changes affect >5 lines
  - Ambiguity would require user interpretation

**Every complete file MUST:**
1. Include full path as first-line comment: `// services/UserService.php`
2. Be 100% complete from start to finish
3. Have zero placeholders (no `...`, `// rest remains same`, `// unchanged code here`)
4. Be immediately usable via copy-paste

### Multi-File Updates
- Create separate artifacts/code blocks for each file
- Never combine multiple files in one output
- Label each clearly with its file path

## Code Quality Standards

### Size Limits (Uncle Bob / Clean Code)
| Component | Ideal | Maximum | Action at Maximum |
|-----------|-------|---------|-------------------|
| **Functions** | 5-20 lines | 40 lines | Extract methods |
| **Classes** | ~200 lines | ~500 lines | Split responsibilities |
| **Files** | ~300 lines | ~1000 lines | Modularize |
| **Line length** | <80 chars | <120 chars | Break up expressions |
| **Nesting depth** | 2 levels | 3 levels | Use early returns/guards |

### Principles
- **DRY**: Extract repeated logic immediately
- **SOLID**: Each class has one reason to change
- **Single Responsibility**: Functions do one thing well
- **Readable > Clever**: Prioritize clarity over conciseness

### Style Consistency
**Maintain the existing codebase style exactly:**
- Indentation (spaces vs tabs, size)
- Line breaking patterns
- Brace placement
- Naming conventions
- Comment style

**Never reformulate working code to "your preference"** — consistency trumps personal style.

## Language-Specific Requirements

### PHP
```php
declare(strict_types=1);
```
- **Standard**: PSR-12 compliance
- **Autoloading**: PSR-4 namespaces
- **Architecture**: Dependency injection, interfaces
- **Types**: All properties and returns typed
- **Errors**: Throw exceptions (never return null for errors)

### JavaScript
- **Linting**: Airbnb ESLint rules
- **Formatting**: Prettier defaults
- **Modern**: ES6+ features where appropriate

## Security Requirements

**All new code must comply with OWASP ASVS Level 2 (latest version as of Jan 2025):**

- Validate and sanitize all inputs
- Use parameterized queries (never string concatenation for SQL)
- Implement proper authentication/authorization checks
- No sensitive data in logs or error messages
- CSRF protection on state-changing operations
- Secure session management
- No hardcoded credentials or secrets

**If a requested change would introduce a security vulnerability, halt and explain the risk with a secure alternative.**

## Comments & Documentation

### DO:
- Document **why** (business logic, non-obvious decisions)
- Explain complex algorithms
- Note security considerations
- Mark technical debt with `// TODO: [specific improvement]`

### DON'T:
- Comment **what** the code does (code should be self-documenting)
- Add meta-commentary: ❌ `// Added new feature`, ❌ `// Modified by AI`, ❌ `// Generated code`
- Leave commented-out code (remove it)
- Use placeholder comments that don't add value

## Error Prevention

### Character Encoding
- Use only standard ASCII for syntax/operators
- Never use unicode lookalikes or smart quotes in code
- Test that comments don't break parsing

### Testing Changes
Before presenting code, mentally verify:
1. Syntax is valid for the language
2. All referenced variables/functions exist
3. Logic flow matches the request
4. No accidental deletions occurred
5. Imports/dependencies are included

---

**Summary**: Make minimal, precise changes. Write like a senior developer. Plan big changes. Generate complete files. Preserve everything. Never introduce security issues. Stay consistent with existing style. In case you need to change the code, please make it in the way humans would find it easy to review as github PR (e.g. don't remove the parts if that's not necessary for the functionality, do not restyle existing code if that is not necessary).
