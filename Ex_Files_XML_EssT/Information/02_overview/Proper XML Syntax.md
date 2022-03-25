* XML documents must have exactly one root tag
* XML documents must be "well-formed"
    * Empty tags must be closed with `/>`
        * Instead of `<elem></elem>`, use `<elem />`
    * Attribute values cannot be minimized
        * `<option selected>` is illegal; use `<option selected="selected">`
    * Attribute values must be inside of quotes, single or double.
        * `<elem attr=val>` is illegal; use `<elem attr="val">`
    * Tags have to be properly nested inside of each other