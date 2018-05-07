# Block content template Drupal 8

Block content entities are not rendered within a template outside the block rendering system. Placing a content block in
a node for instance with the new layout builder works fine, or rendering with views too, but there's no way to edit them
from the frontend directly because there are no contextual links, even though the $build contains those!

This module alters the rendering of a content block by adding a theming function with suggestions per block type and id
Important, this only happens within the layout builder context or views (using 'default' view mode), see
block_content_template_block_content_view_alter().

Theming suggestions:

- block-content-template--BUNDLE
- block-content-template--ID

See following issues on drupal.org for more background:

- https://www.drupal.org/node/2704331
- https://www.drupal.org/project/drupal/issues/2666578
- https://www.drupal.org/project/drupal/issues/2859197

## Development, issues and releases.

Currently living on GitHub, I'll sync back to d.o in case more people are interested in the module.
