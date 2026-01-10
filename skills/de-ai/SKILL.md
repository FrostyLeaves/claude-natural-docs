---
name: de-ai
description: Remove AI-style patterns from technical documents, making them read more naturally like human-written content. Trigger when user asks to "de-AI", "humanize", or "polish" a document.
---

# De-AI: Remove AI Writing Patterns

Transform AI-assisted technical documents (especially game development & rendering docs) into more natural, human-like writing.

## Usage

```
/de-ai <file path or text content>
```

## Instructions

You are helping the user remove AI-style patterns from technical documents. Apply the following transformations:

### 1. Remove Decorative Symbols

- **Delete** all emoji-like symbols: ✓ ✗ ❌ ✅ ⚠️ 💡 🎯 📌 🔥 ⭐ etc.
- Express "correct/incorrect" or "pros/cons" using plain text instead

### 2. Minimize Table Usage

- **Do not use tables** for comparisons or summaries
- Convert tables to concise prose paragraphs or simple bullet lists
- Example: Instead of a comparison table, write: "方案A的优点是xxx，缺点是xxx；方案B则..."

### 3. Add Colloquial Tone and Subjectivity

- Use first-person pronouns: **"我们"、"我认为"、"我的理解是"**
- Allow uncertainty expressions: **"也许"、"可能"、"大概"、"应该是"**
- Be honest about uncertain information rather than stating everything as fact
- Add personal judgments: "我觉得这样做的原因可能是..."

### 4. Include Subjective Opinions and Real-World Examples

- When introducing a technique, **proactively mention** how other games or projects use it
- Examples:
  - "《原神》的渲染管线也采用了类似的方案"
  - "UE5的Nanite在处理这个问题时..."
  - "我猜测他们这样设计是因为..."
- Add speculative analysis: "这可能是出于性能考量"
- These examples and opinions add depth and authenticity

### 5. Simplify Section Structure

- **Avoid** deep nested numbering (like 1.1.1, 1.1.2)
- Use flexible structure instead:
  - Major sections: `##` headings
  - Subsections: `###` or **bold text** as lead-ins
  - No strict numbering required; use descriptive titles
- Humans rarely maintain rigid hierarchical numbering due to high maintenance cost

### 6. Additional Guidelines

- Vary sentence length; avoid uniform sentence patterns
- Use colloquial connectors: "说白了"、"换句话说"、"简单来说"
- Add transitional sentences between paragraphs instead of rigid enumeration
- Don't end every section with a summary sentence

## Output Requirements

1. If user provides a file path, read the file and rewrite it
2. If user provides text directly, rewrite that text
3. Output the rewritten result directly without explaining what was changed
4. Preserve technical accuracy; only adjust the writing style
