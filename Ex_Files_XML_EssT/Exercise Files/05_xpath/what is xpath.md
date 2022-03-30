## What is XPath?
* W3C standard for accessing data in XML
* Fundamental part of XSLT, Xquery, and others
* Defines a **path** into an XML document
* Learn more at http://www.w3.org/TR/xpath

## Important XPath Concepts
* Very compact syntax, quick to learn
* The path expression is a series of location steps
    * Context node - path evaluation starts from here
    * Axis - relation between context and selected nodes
    * Predicates - further refinements to selection process

## Important XPath Expressions
* **/** - Select the root tag in the document
* **/rootTag** - Select the root tag, but only if it is named "rootTag"
* **//tagName** - Find all "tagName" elements anywhere in the document
* **text()** - Select the text content of the current node
* **@name** - Select the "name" attribute of the current node
* **..** - Select the parent of the current node

## Some Selected XPath Examples
* **/doc/chapter[5]** - Select the fifth chapter under the doc tag
* **/body/p[last()]** - Select the last paragraph tag in the body element
* **/body/p[@class="a"]** - Select p tags that have a class attribute equal to "a"
* **//p[@class and @style]** - Select all p tags in the document with class and style attributes