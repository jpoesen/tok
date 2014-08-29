tok
===

This is a simple proof-of-concept Drupal 7 module to demo custom tokens to target field_collection values on a node.

This module is meant as a starting point for developers. In its current state this module provides a new token 
'foo' that references a specific field_collection (in code).

Usage:
* install token, token_filter and this module
* enable token filtering on, for instance, the 'filtered_html' input format
* create a field_collection and add it to a node type
* update tok's code and make sure the foo token corresponds with your new fieldcollection_field
* use the [foo] token in, for isntance, your node body to reference one ore more values on that node's field_collection field.

Token examples:

[foo] 
will be substituted with the entire corresponding field_collection (so if it's a multivalue field_collection, 
all values will be rendered).

[foo:n] 
With n being an integer number, the token will be substituted with the n'th value in the corresponding field_collection.
