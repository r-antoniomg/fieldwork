---
title: 'prototype notes'
layout: single
date: 2026-07-14
---
## NOTES TO SELF
Code to remember
`bundle exec jekyll serve`

## Session 1
2026-07-14

### Goal
Get Minimal Mistakes running locally.

### Results
[x] Jekyll site created
[x] Minimal Mistakes theme installed
[x] Site generated
[x] Localhost working

### Issues
* `bundle install` initially failed
  * cause: command executed outside project directory
  * resolution: `cd` into site directory before running `bundle install`

## Session 2
2026-07-15

### Goal
Create navigation and prototype 'inquiry' page

### Results
[x] Created `_data/navigation.yml`
[x] Created `inquiry.md` with placeholder text

### Notes
- Layout: the page seems to be using the theme properly
- Readability: the page might work with real content, but the 'examples' section might need some customization to behave in a more 'gallery' or 'portfolio' style
- Architecture: the single page architecture seems fine, might need to add section that links to relevant related practices. Previously thought about a section called 'beyond [practice name]'. This might be a preferred form of navigation than the nav bar itself.

## Session 3
2026-07-15

Observation

- The Fieldwork philosophy feels more networked and horizontal than traditional website hierarchies.

Hypothesis

'Manifestations' may function like semi-independent domains of practice.

Open Question

Should this independence be expressed through multiple technical sites, or through strongly differentiated sections within a single site?

Current Assessment
Single site with manifestation-specific hubs may provide the same conceptual benefits while remaining significantly more maintainable.

## Session 4
2026-07-15

### Goal
Transform Inquiry from a placeholder page into a prototype manifestation hub

### Session 4 tasks

[x] Add real structure to inquiry: replace placeholder headings with actual working structure.
[x] Create a visual hierarchy experiment using theme's native features
[x] Build a first 'example'
[x] Prototype 'Beyond Inquiry'
[x] Create a placeholder 'orientation page'
[x] Test internal linking (inquiry -> fieldwork and fieldwork -> inquiry)

### Session 4 questions and answers

[x] Task 1 completed
[x] Task 2 completed. Related questions and answers:
1. Can we make the page easier to scan without introducing custom mode? To some degree we can. The default theme options are still creating very large text that's visually overwhelming and does not allow to properly capture hierarchical structure beyond bolding text for headings.
2. How much customization is actually required? Font changes essential; colour changes to be tested (simple black and white seems to work well and might not require additional colour features, maybe colour can be used strategically in printed contexts, tbd); image display: was able to include a gallery of some images that link out to specific projects on github using theme-native front-matter text and liquid code on the page. However, I couldn't identify a theme-native option to have text below and/or overlaid on top of the images describing the project and/or warning users that they'll be taken to external sites; images need to be selected/created either as thumbnails for the project gallery and/or the header backgrounds.
[x] Task 3 partially completed (build a 'first example'): rather than build a separate page, I chose to use a gallery of images that link out to the GitHub repositories I'm trying to highlight in this context. Need to learn how to add a description to accompany the images in the gallery.
[x] Task 4 partially completed: a similar 'gallery' layout approach might be preferred, but pending test on how to add a second gallery using the front matter and liquid include code on the page.
[] Tasks 5–6 pending

### Current Assessment
* Theme remains viable.
* Customization appears necessary primarily in presentation rather than core architecture.

Emerging Finding

Fieldwork architecture appears reasonably compatible with Minimal Mistakes.

Current friction points are primarily presentation problems:
* typography hierarchy
* example representation
* relationship mapping

rather than structural or technical problems.

## Session 5

### Goal
Complete outstanding tasks from session 4

### Tasks
[x] Create the 'orientation hub'
[x] Prototype a second gallery (for Beyond Inquiry)
[x] First typography experiment: test a single change related to the typography

### Session 5 reflection
* Task: create the 'orientation hub'
 - I created the basic page without focusing on content for now (filename = `fieldwork.md`)
 - In the front matter, I chose `layout: home` because the name seemed appropriate, however, it doesn't seem to work quite as expected: the `single` and `splash` layouts allow for front-matter 'excerpt' which nicely displays text in a header section of sorts. For 'inquiry', that's where I included some of the introduction content and I like the way that displays.
 - I am not convinced that the navigation is working as expected: there is a nav bar with buttons for each of the sections mapped out in the `_data/navigation.yml` file. I'm not sure that the current configuration in the `navigation.yml` file is working correctly because fieldwork is not being displayed as the 'home page', but rather as one of the various nav bar buttons, and in the http address, it is not the root file but rather `[server address]/fieldwork`.
* Task: prototype a second gallery (for Beyond Inquiry)
  - The first gallery (for the examples) is accomplished by: front matter yaml code that starts with the line `gallery:` followed by indent and specific data for each image (url to redirect on click, image file location, alt text, image caption); in the main body of the inquiry page, below the `examples` heading, I added liquid code `include gallery`.
  - Since 'gallery' is already 'taken' by the examples, my assumption was that I could mirror the 'gallery' to create a 'beyond' section as follows: in front matter, add `beyond:` line break, indent, and similar metadata fields as in 'gallery'; on the main body of 'inquiry', I added liquid code to `include beyond`, thinking that it would add the content from the 'beyond' section in the front matter. This hypothesis was incorrect and it resulted in an error message. I don't know how to fix it. Help needed.
* Task: first typography experiment
  - Help needed to understand which of the Jekyll repository files I should update and how.
  - Hypothesis: `_site/assets/css` two files are there: `main.css` and `main.css.map`.

## Sidequest : Inquiry Through Technology

### Topic Minimal Mistakes gallery include
### What I learned
The built-in gallery include does not automatically use any front-matter variable. By default, `{% include gallery %}` uses the page's `gallery:` front-matter array. To use a second gallery, create a differently named front-matter array, such as `beyond_gallery:`, and call it with `{% include gallery id="beyond_gallery" %}`.
### Current limitation
The default gallery is useful for visual linking, but it may not provide enough visible descriptive text for Fieldwork examples or related manifestations. A custom card/gallery include may be needed later.
### Research question
Can the default gallery function well enough for the prototype, or does Fieldwork need a custom relationship-card component?


Technical questions and learning opportunities that emerged while building the prototype.

* What are Jekyll includes?
* How should gallery metadata be stored?
* How do layouts differ from pages?

## Radom notes

Homepage manifestation cards are generated from practice_manifestations.yml.
A card displays only when a matching page permalink exists.
Additional manifestations can be added to the data file before pages exist; they will remain hidden until their pages are created.