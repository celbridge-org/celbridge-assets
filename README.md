# repo: celbridge-assets
Collection of data about Celbridge assets.

The asset definitions listed in assets are used by the Asset Portal on the Celbridge website, and in the Celbridge application itself.

see: 
- https://www.celbridge.org/assets

## Licence

The MIT licence in [LICENSE](LICENSE) covers this repository only: 
- build scripts, site code, schema and metadata

Each listed asset is distributed under its own licence, stated at its `url`. Every asset entry must have a `url` field linking to where the asset lives, as defined in [schema/asset.schema.json](schema/asset.schema.json).

## Asset entries

Each asset has its own folder containing an `asset.json` file and its two images. The file must match [schema/asset.schema.json](schema/asset.schema.json). All fields are required, and fields not listed below are not allowed.

| Field | Type | Description |
|---|---|---|
| `name` | string | Display name of the asset. Must not be empty. |
| `summary` | string | Short plain-text description of the asset, typically 3-4 sentences (max 1000 characters). |
| `category` | string | One of: `template`, `example`, `starter`, `document-editor`, `utility`, `library`. |
| `tags` | array of strings | Keywords for searching and filtering. No duplicates. May be an empty list `[]`. |
| `min_version` | string | Minimum Celbridge version the asset requires, e.g. `1.8` or `1.9.2`. |
| `url` | string (URI) | Source repository of the asset, where its full licence text can be found. |
| `thumbnail` | string | Filename of the thumbnail image in the same folder (`.webp`, `.png`, `.jpg` or `.jpeg`). |
| `screenshot` | string | Filename of the screenshot image in the same folder (`.webp`, `.png`, `.jpg` or `.jpeg`). |
| `updated` | string (date) | Date the entry was last updated, as `YYYY-MM-DD`. |

Example:

```json
{
  "name": "Story tool for presentations",
  "summary": "Story Builder is a Celbridge package that adds an editor for .story files, used to build slide decks and choose-your-own-adventure stories from Markdown passages. ...",
  "category": "document-editor",
  "tags": ["interactive", "presentation"],
  "min_version": "1.8",
  "url": "https://github.com/dr-matt-smith/celbridge-package-story-tool",
  "thumbnail": "thumbnail.webp",
  "screenshot": "screenshot.webp",
  "updated": "2026-10-01"
}
```

## Images

Each submission must include 2 images:
1. thumbnail
   - recommended size is 900x600 pixels (3:2 aspect ratio).
2. screenshot

WebP is preferred; PNG, JPG, and JPEG are also accepted as submission sources.

