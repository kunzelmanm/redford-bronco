# Using Categories in Your Blog Posts

## How It Works

Categories are displayed as colored tags on your blog post cards (like "Trail Run", "Mods & Builds", etc.).

## Adding Categories to Posts

Edit your blog post markdown files in `src/content/blog/` and add a `category` field to the frontmatter:

```markdown
---
title: 'Your Post Title'
description: 'Post description'
pubDate: 'April 21, 2026'
category: 'Trail Run'
---

Your post content here...
```

## Suggested Categories

Based on the Claude Design mockup, here are good categories for a Bronco blog:

- **Trail Run** - Off-road adventures, trail reports
- **Mods & Builds** - Upgrades, installations, modifications
- **Day Trip** - Shorter adventures, local drives
- **Gear Review** - Equipment and accessory reviews
- **Maintenance** - Service, repairs, upkeep

## If You Don't Add a Category

If a post doesn't have a `category` field, it will show "Post" as a fallback.

## Examples

### Trail Run Post
```markdown
---
title: 'First Blood at Sand Hollow'
description: 'Broke in the new Bronco properly...'
pubDate: 'April 14, 2026'
category: 'Trail Run'
---
```

### Mod Post
```markdown
---
title: 'Installing Rock Rails'
description: 'A weekend project that took longer than expected'
pubDate: 'April 15, 2026'
category: 'Mods & Builds'
---
```

### Day Trip
```markdown
---
title: 'Quick Escape to Zion Overlook'
description: 'Golden hour on a Tuesday'
pubDate: 'April 16, 2026'
category: 'Day Trip'
---
```

## Changing Existing Posts

Just edit the markdown file and add the `category:` line to the frontmatter. The site will automatically update when you save.
