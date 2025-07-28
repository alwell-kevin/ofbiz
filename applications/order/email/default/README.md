# Email Templates for Order Module

This directory contains FreeMarker templates used to generate order-related email notifications. Each template expects certain input data and produces an HTML email body.

## Files

### `EmailProcessNotify.ftl`
Generates a detailed process notification email when an order moves through workflow stages.
- **Inputs**
  - `orderId` – identifier of the order.
  - `orderDate` – date when the order was created.
  - `estimatedStartDate` – planned start date of the order fulfillment process.
  - `actualStartDate` – actual start date recorded in the system.
  - `omgStatusId` – current workflow status identifier for the order.
  - `assignments` – list of assignment objects. Each assignment provides:
    - `partyId` – identifier of the party assigned to the order.
    - `roleTypeId` – role of the assignee.
    - `statusId` – status of the assignment.
  - `baseUrl` – URL base used to create a link back to the order manager.
- **Output**
  - HTML document summarizing order details and assignments, with a link to view the order in OFBiz.

### `OrderDeliveryUpdatedNotice.ftl`
Sends a short notice when delivery information for an order is modified.
- **Inputs**
  - `orderDeliverySchedule.orderId` – identifier of the affected order.
  - `orderDeliverySchedule.orderItemSeqId` – optional identifier of the specific order item, or `_NA_` when not applicable.
- **Output**
  - HTML snippet indicating that delivery details have been updated for the order (and item, if provided).

