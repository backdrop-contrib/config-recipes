# backdrop-features
A directory of config features for export / experimentation

As a start, each directory should contain the config files for one feature. In theory, we should be able to add the config files from any feature directory to an existing Backdrop project and then synchronize the config files, to add that feature to the site. 

As of this time, we done very little experimentation to test how this works. 

Please, help make this documentation better. 

Currently, I am just importing the files one at a time. Would love suggestions on how to make this better. Files must be loaded in a logical order, for example you must import the node.type file before the field.field.field file and must load the field.field.field file before the field.instance file.

Here is the rough order in which I expect files must/should be loaded:

node.type
image.style
field.field
field.instance
views.view

