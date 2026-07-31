# Meridian Smile Studio — Image Generation Prompts

Generate all images using the aspect ratios available in your tool. Use a warm, editorial photography style throughout — soft natural light, warm color grading, shallow depth of field. Avoid clinical white backgrounds.

---

## Available Aspect Ratios

| Tool Option | Ratio | Use For |
|-------------|-------|---------|
| `crop_portrait` | 3:4 | Hero portrait, about portrait |
| `crop_landscape` | 4:3 | Gallery cards |
| `crop_16_9` | 16:9 | Blog images, full-bleed section, OG image |
| `crop_square` | 1:1 | (not used) |
| `crop_9_16` | 9:16 | (not used) |

---

## 1. Hero Portrait — Dr. Elena Cross

| Property | Value |
|----------|-------|
| **Aspect Ratio** | **3:4** |
| **Tool Setting** | `crop_portrait` |
| **Placement** | Homepage hero section, right side |

**Prompt:**
```
Professional portrait of a female dentist in her early 40s, warm smile, wearing a modern navy blazer over a cream blouse, standing in a elegantly designed dental consultation room with warm wood accents and soft natural light from a large window. Editorial magazine style photography, shallow depth of field, warm color grading, soft shadows. The background shows a blurred modern dental office with brass fixtures and ivory walls. Professional headshot style, confident and approachable expression. Shot on 85mm lens, natural lighting.
```

**Alternative (simpler):**
```
Editorial portrait of a professional woman in her early 40s, dentist, warm confident smile, navy blazer, cream blouse, soft natural light, warm tones, shallow depth of field, modern office background blurred, magazine photography style.
```

---

## 2. About Section Portrait — Dr. Cross at Work

| Property | Value |
|----------|-------|
| **Aspect Ratio** | **3:4** |
| **Tool Setting** | `crop_portrait` |
| **Placement** | About section, left side |

**Prompt:**
```
Candid editorial photograph of a female dentist in her early 40s reviewing a 3D dental scan on a large monitor with a patient, modern dental office with warm wood cabinets and brass fixtures, soft natural light from window, warm color grading, shallow depth of field. The dentist is pointing at the screen explaining something, patient is nodding. Professional yet warm atmosphere, magazine editorial style. Shot from slightly behind the dentist's shoulder.
```

---

## 3. Full-Bleed Section — Studio Environment

| Property | Value |
|----------|-------|
| **Aspect Ratio** | **16:9** |
| **Tool Setting** | `crop_16_9` |
| **Placement** | Full-width break section between process and gallery |

**Prompt:**
```
Wide editorial photograph of a luxury dental treatment room, warm wood accents, brass fixtures, ivory walls, modern dental chair, large window with natural light streaming in, plants, warm and inviting atmosphere, no clinical white surfaces. The room looks more like a high-end spa than a dental office. Soft warm lighting, architectural photography style, clean composition, no people.
```

---

## 4. Blog Featured Image — "Digital Smile Design"

| Property | Value |
|----------|-------|
| **Aspect Ratio** | **16:9** |
| **Tool Setting** | `crop_16_9` |
| **Placement** | Blog card 1 |

**Prompt:**
```
Close-up of a dentist's hands using a digital tablet to design a smile overlay on a patient's photo, 3D dental software visible on screen, warm office lighting, modern dental office background blurred, editorial photography style, warm color tones, shallow depth of field. Focus on the tablet screen showing the digital smile design.
```

---

## 5. Blog Featured Image — "Invisalign at 40+"

| Property | Value |
|----------|-------|
| **Aspect Ratio** | **16:9** |
| **Tool Setting** | `crop_16_9` |
| **Placement** | Blog card 2 |

**Prompt:**
```
Professional woman in her 40s sitting in a modern dental consultation room, smiling confidently, holding clear Invisalign aligners, warm natural light, editorial magazine style photography, warm color grading, soft focus background with modern dental office details. The subject looks relaxed and confident, not clinical.
```

---

## 6. Blog Featured Image — "Practice News / New Location"

| Property | Value |
|----------|-------|
| **Aspect Ratio** | **16:9** |
| **Tool Setting** | `crop_16_9` |
| **Placement** | Blog card 3 |

**Prompt:**
```
Exterior photograph of a modern office building entrance at 88 Battery Street San Francisco, Financial District, warm afternoon light, elegant brass signage, glass doors, clean architectural lines, warm color grading, editorial photography style. The entrance looks premium and welcoming, not corporate or cold.
```

---

## 7. Gallery Cards (6 images)

| Property | Value |
|----------|-------|
| **Aspect Ratio** | **4:3** |
| **Tool Setting** | `crop_landscape` |
| **Placement** | Gallery section, 6 cards in 3x2 grid |

**Note:** These are **sample/placeholder** before-and-after cases. Do NOT generate realistic medical before/after photos. Instead, generate abstract/artistic representations.

### Card 1 — "Porcelain Veneers"
```
Abstract artistic close-up of a perfect white smile, extreme close-up of teeth with soft warm lighting, golden hour light, editorial beauty photography style, shallow depth of field, warm tones. The image should feel aspirational and artistic, not clinical.
```

### Card 2 — "Invisalign"
```
Artistic flat lay photograph of clear Invisalign aligners on a warm marble surface with brass accessories, soft natural light, warm color grading, editorial product photography style. Clean composition, luxury aesthetic.
```

### Card 3 — "Full Smile Makeover"
```
Editorial portrait of a woman touching her chin thoughtfully, warm smile visible, soft natural light from window, warm color grading, shallow depth of field, modern interior background. The image should convey confidence and satisfaction, magazine editorial style.
```

### Card 4 — "Dental Bonding"
```
Close-up artistic photograph of a dentist's hands working with precision tools, warm office lighting, shallow depth of field, editorial medical photography style, warm tones. The focus is on the craft and precision, not the clinical procedure.
```

### Card 5 — "Professional Whitening"
```
Bright, airy photograph of a modern bathroom vanity with premium dental care products, warm natural light, clean minimalist aesthetic, warm color grading, editorial lifestyle photography. The image should feel like a premium self-care moment.
```

### Card 6 — "Full Arch Restoration"
```
Architectural photograph of a modern dental laboratory with precision equipment, warm wood and brass details, soft lighting, editorial photography style, warm tones. The image should convey craftsmanship and precision.
```

---

## 8. OG Image (Social Share)

| Property | Value |
|----------|-------|
| **Aspect Ratio** | **16:9** |
| **Tool Setting** | `crop_16_9` |
| **Placement** | Social media share preview (meta tag) |
| **Note** | Crop from 16:9 to 1.91:1 (1200x630) after generation |

**Prompt:**
```
Minimalist branded social media card for Meridian Smile Studio. Warm ivory background (#F7F3EC), elegant brass circle logo mark with letter M in center, "Meridian Smile Studio" in serif typography below, "Porcelain Veneers | Invisalign | Smile Design" as subtitle, "San Francisco" at bottom. Clean, editorial, luxury aesthetic. No photographs, just typography and logo on warm background.
```

**Note:** This may be easier to design in a tool like Figma/Canva than generate with AI, since it requires exact typography and branding.

---

## Quick Reference: All Images

| # | Image | Tool Setting | Ratio | File Name |
|---|-------|-------------|-------|-----------|
| 1 | Hero portrait | `crop_portrait` | 3:4 | hero-portrait.jpg |
| 2 | About portrait | `crop_portrait` | 3:4 | about-dr-cross.jpg |
| 3 | Full-bleed studio | `crop_16_9` | 16:9 | studio-environment.jpg |
| 4 | Blog: Digital Smile | `crop_16_9` | 16:9 | blog-digital-smile.jpg |
| 5 | Blog: Invisalign 40+ | `crop_16_9` | 16:9 | blog-invisalign.jpg |
| 6 | Blog: New Location | `crop_16_9` | 16:9 | blog-location.jpg |
| 7a | Gallery: Veneers | `crop_landscape` | 4:3 | gallery-veneers.jpg |
| 7b | Gallery: Invisalign | `crop_landscape` | 4:3 | gallery-invisalign.jpg |
| 7c | Gallery: Makeover | `crop_landscape` | 4:3 | gallery-makeover.jpg |
| 7d | Gallery: Bonding | `crop_landscape` | 4:3 | gallery-bonding.jpg |
| 7e | Gallery: Whitening | `crop_landscape` | 4:3 | gallery-whitening.jpg |
| 7f | Gallery: Restoration | `crop_landscape` | 4:3 | gallery-restoration.jpg |
| 8 | OG image | `crop_16_9` | 16:9 | og-image.jpg |

---

## Style Guide for All Images

| Property | Value |
|----------|-------|
| Color temperature | Warm (5500K–6500K) |
| Lighting | Soft natural, window light preferred |
| Depth of field | Shallow (f/1.8–f/2.8) |
| Color grading | Warm highlights, slightly desaturated |
| Mood | Editorial, premium, warm, approachable |
| Avoid | Clinical white, blue tones, harsh flash, stock photo poses |
| Reference aesthetic | Kinfolk magazine, Monocle, Cereal magazine |

---

## Post-Generation Processing

After generating images:

1. **Crop** if needed (OG image: crop 16:9 down to 1200x630)
2. **Compress** for web (target < 150KB per image)
3. **Convert** to WebP format for better compression (keep JPG fallback)
4. **Name** descriptively using the file names in the quick reference table
5. **Add alt text** when inserting into HTML:
   - Hero: "Dr. Elena Cross, cosmetic dentist in San Francisco"
   - About: "Dr. Cross reviewing a digital smile design with a patient"
   - Blog: Descriptive text matching the post topic
   - Gallery: "Sample case: [treatment type]"
