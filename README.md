Client-Settings
===============

Future MODX Extra to edit context settings via a resource on the front end

How to use:

1. Create a new snippet in MODX, name it client-settings
2. Copy the client-settings code into the snippet
3. Create Context Settings in MODX, if you create an Area Lexicon Entry to group your settings you will need to pass the Area Lexicon Entry value as the &category parameter in the snippet call, otherwise you can leave it empty for all entries and leave the &category value empty ie: &category=``. Need to make this a default value
4. Create a New Resource in MODX and place the snippet call with two parameters these are: &category and &target. The Category parameter is used to select your settings from an Area Lexicon Entry if you use one to group your settings. The &target parameter is used to specify the target ID of the resource you want to go to once you submit the form. The Final snippet call should look like this: [[client-settings? &category=` ` &target=`[[~[[*id]]]]`]] or [[client-settings? &category=`Area Lexicon Entry Value Goes Here` &target=`[[~[[*id]]]]`]] if using an Area Lexicon Entry.

Things to improve or features to add.

1. Chunk templating
2. Default values for Category and Target parameters
3. Code optimization & clean up
4. Need to add support to get the custom name to display instead of the key value since theres an issue with updating settings that have spaces
5. Support for multiple snippet calls via categories with a single save button.
