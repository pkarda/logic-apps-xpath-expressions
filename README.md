# Logic Apps XPath Expressions

This cheat-sheet contains various Xpath expressions used in Azure Logic Apps.

## String operations
```
xpath(variables('UniversalShipment'), 'string(/*[local-name()="UniversalShipment"]/*[local-name()="Shipment"]/*[local-name()="MilestoneCollection"]/*[local-name()="Milestone"][*[local-name()="Description" and text() ="Origin Cargo Receive"]]/*[local-name()="ActualDate"])')
```
