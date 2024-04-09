# Twine Story/Proofing Format Catalog

A JSON-formatted catalog of Twine story formats.

Example of use: [a catalog generated from this data](http://mcdemarco.net/tools/twine/catalog/) using vanilla JS.

## About the data

I put this data together mostly by hand, although it would have been possible to import some of it from the story format headers.  Fields are intended to match the story format's value for that field, though in some cases the data has been regularized (for regularity) or omitted (out of laziness), e.g., the license field.

I did not include the url field because I broke the web locations down into more useful data, but it could be reintroduced.  I did not include the version field because it could be a maintenance nightmare.  The format itself was not included originally but is there now for formats not named `format.js`.

### The fields

* name, author, license, proofing, ~~icon~~ image, and description are taken from the story format itself; "url" is reserved for that use but not present.
* docs: a URL providing documentation
* demo: a URL providing a demo story.
* base: the base url for getting the Twine 2 format (ideally using HTTPS) and icon files.  Note that github will not serve format files correctly by default, so use the "raw" github link if you must.
* archive: a URL providing an archive of a lost repo
* format: the filename of the story format if it isn't "format.js".
* repo: the URL of the code repository for the format.
* official (boolean): is this an official Twine 1 or 2 format?
* twine1 (boolean): the format supports Twine 1.
* twine2 (boolean): the format supports Twine 2.
* utility (boolean): the format is not intended to produce a playable file, yet is not marked as a proofing format
* tags (array of string): various notable facts about the format, including "stretchtext","markdown", "beta", "unavailable", "twee", "json".  Feel free to add more.
* extendedDescription: a more detailed or comparative description than the one included in the story format.
* basedOn: the parent format.
* notes:  additional info that didn't fit into the fields above.

### Credits

Originally compiled by M. C. DeMarco; feel free to update via pull requests or the issue tracker.
