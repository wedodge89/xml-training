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
    * Elements
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
    * Attributes
        * Attributes are specified on opening element tags
        * Must start with letter or underscore
            * Can be followed by digits, letters, hyphens, periods, underscores
        * Attributes that begin with "xml" are reserved
        * Attributes appear only once on a given element
* **Comments** <br>
    `<!-- This is an XML Comment -->`
    * Comments embed human-readable information
    * Defined with `<!--` and end with `-->`
    * Can go almost anywhere, except:
        * Inside element brackets
        * Before the document declaration
    * Invalid: `<element <!-- comment -->>`
    * Valid:
     ```
        <element>
            <!-- comment -->
        <element>
    ```

* **Character Data** <br>
    `<[CDATA[This is unparsed text & data]]>`
    * Part of document, but not parsed by the XML parser
    * Defined using `<! [CDATA[` and end with `]]>`
    * Typically used to contain unescaped textual data
        * Not parsed, so `&` and `<` and `>` are legal
    * Example:
    ```
    <script>
    <![CDATA[
    function f(a, b) {
        return a < b;
        }
    ]]>
    </script>
    ```
* **Processing Instructions** <br>
    `<?SpellCheckMode mode="us-english"?>`
    * Special instructions to the XML parse
    * Have the form `<?targetName instruction ?>`
        * The "xml" target name is reserved
        * Can start with number or letter, then be followed by digits, letters, hyphens, periods, underscores
    * Example: your app has multiple spell-checking modes
        * `<?SpellCheckMode mode="en-GB" ?>`
* **Entity References** <br>
    `Character (&#60;) and General (&copyright;)`
    * Help shorten and modularize XML documents
    * Provide markup for otherwise illegal characters
    * General entities
        * Replaced by parser with a full string
        * Examples: `&copyright;` or `&author;`
    * Character entities
        * Examples: `&#060;`, `&amp;`, or `&quot;`