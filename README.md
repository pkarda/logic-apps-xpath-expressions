# Logic Apps XPath Expressions

This cheat-sheet contains various Xpath expressions used in Azure Logic Apps.

## String operations
**Sample XML**
```xml
<Order>
  <Product>
    <Description>Espresso</Description>
    <Price>1.50</Price>
  </Product>
  <Product>
    <Description>Latte Espresso</Description>
    <Price>2.50</Price>
  </Product>
 </Order>
 ```
**XPath to get the `Price` of the `Latte Expresso` product**
```
xpath(variables('Order'), 'string(/*[local-name()="Order"]/*[local-name()="Product"][*[local-name()="Description" and text()="Latte Espresso"]]/*[local-name()="Price"])')
```
