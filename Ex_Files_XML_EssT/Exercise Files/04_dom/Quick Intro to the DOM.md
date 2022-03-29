## The Document Object Model (DOM)
* Standard set of APIs for working with document content
* Platform, browser, and language neutral
* Represents document content as a tree structure
* Contents of the tree are called **nodes**

## Important DOM Properties
* **nodeName** - The name of the node; for tags, it is the tag name. For comments and text, it is a special name like "#comment" or "#text".
* **nodeType** - The node's type; Element, Comment, Text, etc.
* **nodeValue** - The node's value; varies based on node type
* **attributes** - For elements only; an array of attributes and values
* **parentNode** - The parent of this node; null if there is no parent or "#text"
* **childNodes** - Array of child nodes; empty if there are none
* **firstChild**, **lastChild** - References to first and last child of this node

## Important DOM Functions
* **appendChild()** - Inserts an element at the end of a given element's children
* **removeChild()** - Removes an element from the parent
* **insertBefore()** - Inserts a new node before the given node
* **replaceChild()** - Replaces an existing node inside the parent with a new one

## Document Functions and Properties
* **documentElement** - Reference to the root document element
* **createElement()** - Creates new element that can be inserted in the document
* **createTextNode()** - Creates new text node
* **createComment()** - Creates new comment
* **createCDATASection()** - Creates new CDATA section
* **getElementsByTagName()** - Returns array of tags that match given tag name
* **getElementById()** - Returns a single element with a given ID

## Other Important Properties
* **getAttribute()** - Gets the value of a given attribute on an element
* **setAttribute()** - Sets the value of an attribute on an element
* **removeAttribute()** - Removes an attribute from an element
* **innerHTML** - Gets or sets the HTML content of the given tag
* **data** - Gets the text data of an Element, Comment, or Text node