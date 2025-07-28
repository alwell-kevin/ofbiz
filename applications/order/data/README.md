# Order Data Overview

This document provides an overview of the XML files under this directory and what they are used for. These files seed or demonstrate various order management features in OFBiz.

## XML Files

### OrderDemoData.xml
Sample customer request and related entities used to demonstrate order and customer request features.

### OrderDemoUser.xml
Demo user login accounts for testing order management functionality.

### OrderHelpData.xml
Registers help content for the Order Manager. The `objectInfo` attributes point to files inside `helpdata/` providing docbook XML help topics.

### OrderPortletData.xml
Defines portal portlets, categories, and portal pages used to display order related widgets in a portal interface.

### OrderQuoteDemoData.xml
Example product and quote records illustrating how quotes can be stored and linked to orders.

### OrderScheduledServices.xml
JobSandbox entries scheduling recurring services such as inventory checks, automatic reorders, or other order related maintenance tasks.

### OrderSecurityGroupDemoData.xml
Demonstrates security groups and permissions used by the order component.  Maps groups to permissions for different user roles.

### OrderSecurityPermissionSeedData.xml
Seed data for individual security permissions that control access to order manager screens and actions.

### OrderSystemPropertyData.xml
System properties that configure order component behaviour (e.g. cancellation grace periods, feature flags).

### OrderTypeData.xml
Defines various types and enumerations for orders, items, statuses, adjustments and returns.

## helpdata Directory

The `helpdata` subdirectory contains docbook XML files referenced by `OrderHelpData.xml`.  They describe how to use the order manager, view orders and run reports.  Each file corresponds to a DataResource used by the help system:

- `HELP_ORDERMGR.xml` – general introduction.
- `HELP_ORDERMGR_View.xml` – help for viewing and editing orders.
- `HELP_ORDERMGR_Report.xml` – help for running order related reports.

