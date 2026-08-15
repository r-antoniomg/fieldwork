# Fieldwork image audit

## Image metadata sources

| file | purpose | image field | current path type | future action |
|-----|-----|-----|-----|-----|
| practice_objects.yml | field note single image; field note image gallery; tag generated view | image_path | local assets | rename files |
| practice_projects.yml | panifestation page project cards | image_path | local or external | review |
| practice_links.yml | manifestation page beyond section logo | image_path | local assets | review merge possibility with practice_manifestations |
| practice_manifestations.yml | home page manifestation cards logo | image_path | local assets | review merge possibility with practice_links |

## Includes using images

| Include | Source metadata | Image path source hardcoded or obtained | Metadata fields | Image function | css |
|-----|-----|-----|-----|-----|-----|
| practice-fieldnote-gallery.html | practice_objects.yml | obtained from metadata | image_path; title; id | field note post image gallery | custom css added to local css file |
| practice-fieldnote-image.html | practice_objects.yml | obtained from metadata | image_path; title; id | field note post single image | custom css added to local css file |
| practice-generated-tag-view.html | practice_objects.yml | obtained from metadata | image_path | reusable generated view for any tag | may have custom css added to local css file |
| practice-links-gallery.html | practice_links.yml | obtained from metadata | image_path | manifestation page Beyond section | custom css for beyond section added to local css file |
| practice-manifestation-cards.html | practice_manifestations.yml | obtained from metadata | image_path | home page manifestation cards | custom css for manifestation cards may be in local css file |
| practice-projects.html | practice_projects.yml | obtained from metadata | image_path | manifestation page project cards; some image paths are external to the repository assets images | custom css for project cards in local css file |