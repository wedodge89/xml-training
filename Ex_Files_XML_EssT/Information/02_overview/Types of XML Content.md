* **XML Document Declaration** <br>
    `<?xml version="1.0" encoding="UTF-8" standalone="yes"?>`
    * Technically optional, though W3C recommends it
    * Identifies the file as XML document
    * Provides a place for the *encoding* and *standalone* attributes
    * Must be at very beginning; not even whitespace before it
    * The *encoding* attribute
        * Defaults to UTF-8 if you don't include it
    * The *standalone* attribute
        * Indicates whether the document is complete by itself

* **Elements and Attributes** <br>
    `<element attribute="value">`
    * Elements must have valid names.
        * They can begin with underscore (_) or letter
        * Followed by letters, digits, periods, hyphens, and/or underscores
        * Cannot use the string "xml" in any case combination
    * Valid Tag Names
        * `<_Element1>`
        * `<My.Element>`
        * `<My-Element_Name>`
    * Invalid Tag Names
        * `<1Tag>` (Cannot begin with a number)
        * `<#Elem&ent>` (invalid characters in name)
        * `<XmL>` (the string "xml" is reserved)
* **Comments** <br>
    `<!-- This is an XML Comment -->`
* **Character Data** <br>
    `<[CDATA[This is unparsed text & data]]>`
* **Processing Instructions** <br>
    `<?SpellCheckMode mode="us-english"?>`
* **Entity References** <br>
    `Character (&#60;) and General (&copyright;)`