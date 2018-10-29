# Twine Story/Proofing Format Catalog

A JSON-formatted catalog of Twine story formats.

Example of use: [a catalog generated from this data](http://mcdemarco.net/tools/twine/catalog/) using vanilla JS.

## About the data

I put this data together mostly by hand, although it would have been possible to import some of it from the story format headers.  Fields are intended to match the story format's value for that field, though in some cases the data has been regularized (for regularity) or omitted (out of laziness), e.g., the license field.

I did not include the url field because I broke the web locations down into more useful data, but it could be reintroduced.  I did not include the version field because it could be a maintenance nightmare.  The format itself is not included.

### The fields

* name, author, license, proofing, icon, and description are taken from the story format itself; "url" is reserved for that use but not present.
* docs: a URL providing significant documentation (in the case of Snowman clones, documentation beyond the copy of Snowman's docs).
* demo: a URL providing a demo story.
* base: the base url for getting the format, ideally using HTTPS.  Note that github will not serve format files correctly, so don't put a github link into this field.
* format: the filename of the story format if it isn't "format.js".  (Yes, someone went there.)
* repo: the URL of the code repository for the format.
* official (boolean): is this an official Twine 1 or 2 format?
* twine1 (boolean): the format supports Twine 1.
* twine2 (boolean): the format supports Twine 2.
* tags (array of string): various notable facts about the format, including "stretchtext","markdown", "beta", "unavailable", "twee".  Feel free to add more.
* extendedDescription: a more detailed or comparative description than the one included in the story format.
* basedOn: the parent format.
* notes:  additional info that didn't fit into the fields above.

### Credits

Originally compiled by M. C. DeMarco; feel free to update via pull requests or the issue tracker.
