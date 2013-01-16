Client-Settings
===============

Future MODX Extra to edit context settings via a resource on the front end

How to use:

1. Create a new snippet in MODX, name it client-settings
2. Copy the client-settings code into the snippet
3. Create Context Settings in MODX
4. Create a New Resource in MODX and place the snippet call with two parameters these are: <pre>&category</pre> and <pre>&target</pre>.
5. The <pre>&category</pre> parameter is used to select your settings from an Area Lexicon Entry if you use one to group your settings, otherwise you can leave it empty for all context settings and leave the <pre>&category</pre> value empty ie: <pre>&category=` `</pre>. (Need to make this a default value).
6. The <pre>&target</pre> parameter is used to specify the target ID of the resource you want to go to once you submit the form, (Need to make a default value for this to be the current ID of the page).
7. The Final snippet call should look like this: <pre>[[client-settings? &category=` ` &target=`[[~[[*id]]]]`]]</pre> or <pre>[[client-settings? &category=`Area Lexicon Entry Value Goes Here` &target=`[[~[[*id]]]]`]]</pre> if using an Area Lexicon Entry.

Things to improve or features to add.

1. Chunk templating
2. Default values for Category and Target parameters
3. Code optimization & clean up
4. Need to add support to get the custom name to display instead of the key value since theres an issue with updating settings that have spaces
5. Support for multiple snippet calls via categories with a single save button.
