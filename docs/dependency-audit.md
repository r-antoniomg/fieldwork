| component | local copy? | dependency type | comments or recommended actions |
|-----|-----|-----|-----|
| _data/navigation.yml | yes | data for navigation bar | keep local file or files as we explore the future behaviour of the navigation bar |
| _data/ui-text.yml | no | render consistent labels for user interface. example date_label = 'Updated:' | we manually changed the date_label for field notes, this file controls overall behaviour of all labels and includes other languages |
| _includes/analytics-providers/ | no | directory with code files to incorporate google analytics and other options | no immediate need for analytics |
| _includes/comments-providers/ | no | directory with code files to incorporate comments from other platforms like Facebook, discourse, disqus | no immediate need for this content |
| _includes/footer/ | no | directory with single, mostly empty file that allows to add custom footer snippets | can be easily downloaded or replicated if needed |
| _includes/head/ | no | directory with single, mostly empty file, that allows to add custom head snippets and favicons | can easily be downloaded or replicated if needed |
| _includes/search/ | no | directory with code files to implement searching functionalities | no immediate need for searching functionality, potentially no need in the future either |