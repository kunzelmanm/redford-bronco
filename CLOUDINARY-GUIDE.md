# Using Cloudinary Images

## Setup (One Time)

1. **Get your Cloudinary cloud name:**
   - Go to cloudinary.com/console
   - Your cloud name is at the top (e.g., "dg3abc123")

2. **Update `src/consts.ts`:**
   ```ts
   export const CLOUDINARY_CLOUD_NAME = 'your_cloud_name_here';
   ```

## Upload Photos

### Option 1: Web Dashboard (Easiest)
1. Go to cloudinary.com/console/media_library
2. Create a folder called `bronco`
3. Drag & drop your photos
4. Copy the "Public ID" (e.g., `bronco/sand-hollow-hero`)

### Option 2: Organize by Folders
Create folders for different types:
- `bronco/heroes/` - Hero images for posts
- `bronco/inline/` - Inline post images
- `bronco/gallery/` - Photo gallery

## Use in Blog Posts

In your markdown frontmatter:

```markdown
---
title: 'First Blood at Sand Hollow'
description: 'Breaking in the Bronco'
pubDate: 'April 14, 2026'
category: 'Trail Run'
heroImage: 'bronco/sand-hollow-hero'  # ← Just the public ID
---
```

**That's it!** The image automatically:
- Resizes to 1920px width
- Converts to WebP/AVIF
- Compresses with smart quality
- Lazy loads

## Example Workflow

1. Export photo from Google Photos (any size is fine)
2. Upload to Cloudinary → `bronco/` folder
3. Public ID becomes: `bronco/your-photo-name`
4. Add to post frontmatter: `heroImage: 'bronco/your-photo-name'`
5. Done!

## Pro Tips

- **Naming:** Use descriptive names: `sand-hollow-hero`, `bronco-slickrock-1`
- **Folders:** Keep organized: `bronco/sand-hollow/hero.jpg` becomes `bronco/sand-hollow/hero`
- **File extensions:** Don't include in public ID (Cloudinary strips them)

## Troubleshooting

**Image not showing?**
- Check cloud name in `src/consts.ts`
- Check public ID is correct (no file extension)
- View page source - does the Cloudinary URL look right?

**Wrong size?**
- Edit `CloudinaryImage.astro` and change `width = 1920` to your preferred default
