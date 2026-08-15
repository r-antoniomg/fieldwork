---
title: Technical documentation
layout: single
permalink: /technical-documentation/
active: true
---
## Images
Status : `Adopted (v1)`
Date adopted : `2026-08-03`

As of 2026-08-03 images are stored in the repository's assets/images without additional subdirectories

### File-naming conventions

General principle: `fw-[prefix]-[descriptor].[extension]`

Where:

* `fw-` = abbreviation for 'fieldwork'
* `prefix` =
  * br- : branding images (logo and logo variants such as transparent background vs. white background)
  * de- : decorative images (example: images for 'hero' banner)
  * ob- : object images (collages, drawings, illustrations, etc.)
  * pr- : project images (most project images are't stored in the repository's assets, but may be external)
  * th- : thumbnail (inactive at present; placeholder in case of future derivatives)
* `descriptor` =
  * branding images : 1–3 word or phrase describing file
    * Example : `fw-br-logo.jpg`
  * decorative images : 1–3 word or phrase describing file
    * Example : `fw-de-inquiry-hero.jpg`
  * object + project images : unique, five-digit consecutive number (objects and projects each have their own unique sequencing)
    * Example : `fw-ob-00001.jpg` ; `fw-pr-00001.jpg`
* `.[extension]` = file extension (`.jpg`, `.png`, etc.)

### Image policies

#### Files
* Source files are stored separate from the fieldwork repository and are used for generating derivatives
* Derivatives are generated following the file-naming conventions and technical requirements; they are stored in the repository's `/assets/images/` directory (may be migrated to separate hosting platform as collection grows)
* Thumbnail derivatives are not currently generated or used
* Thumbnail functionality may be implemented in the future if performance requirements justify it.

#### Technical requirements for derivatives
* Orientation and aspect ratio : must respect the original file
* Maximum image dimensions : 1600 px ; the longest side of the image (width or height) must not exceed 1600 px
* DPI/PPI values : not defined as part of the website standard for fieldwork
* File formats :
  * `WebP` preferred
  * `.jpg` acceptable when compatibility or sharing requirements take precedence
  * `.png` when transparent background is required
  * `.svg` for vector branding assets
* File size : target under 500 KB whenever possible; images exceeding this value should be reviewed.


#### Metadata requirements
* Metadata for object images must be included in the appropriate `practice_objects.yml` file
* `image_path` and `original_filename` must be included in the records.
  * `original_filename` corresponds to the name of the source file if different from the normalized file name at the time of creating derivatives