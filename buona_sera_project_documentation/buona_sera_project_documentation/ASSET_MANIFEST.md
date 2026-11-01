# Asset Manifest

## 1. Asset policy

No real café photo, logo or brand asset should be used without a legitimate source and permission/usage rights. AI-generated or stock assets must not be presented as actual photographs of Buona Sera Cafe.

## 2. Required asset inventory

| Asset | Purpose | Preferred source | Status |
|---|---|---|---|
| Official logo | Header/footer | Owner-supplied vector or high-resolution file | NOT PROVIDED |
| Hero food/space image | Hero | Owner-approved café photography | NOT PROVIDED |
| Food images | Menu/feature section | Owner-approved item photography | NOT PROVIDED |
| Interior/exterior images | Atmosphere/gallery | Owner-approved photography | NOT PROVIDED |
| Brand textures/patterns | Supporting visual detail | Created for concept, subject to direction | NOT STARTED |
| Favicon | Browser identity | Approved concept mark | NOT STARTED |
| Social preview image | Sharing preview | Created after visual identity approval | NOT STARTED |

## 3. File organisation proposal

```text
public/
  assets/
    brand/
    hero/
    menu/
    gallery/
    icons/
    social/
```

Use descriptive, lowercase, hyphenated filenames. Avoid spaces and ambiguous names.

## 4. Asset record template

For every asset, record:
- Filename and path.
- Asset type and intended placement.
- Source/creator.
- Licence or permission status.
- Whether it depicts the actual café.
- Alt text.
- Crop/aspect ratio.
- Optimised file size and format.
- Approval status.

## 5. Image quality

- Use responsive image sizes.
- Prefer WebP/AVIF where supported by the build pipeline.
- Avoid oversized images.
- Set width/height or aspect ratio to reduce layout shift.
- Lazy-load below-the-fold imagery.
- Do not lazy-load the main hero image if it is the primary LCP asset.
- Use meaningful alt text for informative images; decorative images should have empty alt text.

## 6. Temporary concept imagery

If temporary imagery is needed for the private demo:
- Mark it internally as `concept` or `illustrative`.
- Do not use it to imply actual menu items or actual premises.
- Replace it before any public launch unless the business approves its use and representation.
