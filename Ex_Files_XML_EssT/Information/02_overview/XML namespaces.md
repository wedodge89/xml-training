# XML Namespaces
* Form: `<html xmlns="http://www.w3.org/1999/xhtml">`
* Prevent conflict between tags from different languages
* Example:
    ```
    HTML
    <table>
        <tr>
            <td>Cell Content</td>
        </tr>
        <tr>
            <td>Cell Content</td>
        </tr>
    </table>
    ```
    ```
    XML
    <table>
        <furn:type>Coffee</furn:type>
        <furn:price>199.99</furn:price>
        <furn:material>wood</furn:material>
        <furn:stock>25</furn:stock>
    </table>
    ```
* 