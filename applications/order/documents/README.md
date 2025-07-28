# Documentation for XML files in `applications/order/documents`

This directory contains XML resources used for generating documentation for the Order component. Below is a description of each XML file and the role it plays.

## Order.xml

- **Purpose:** Acts as the main DocBook chapter for the Order component documentation. It assembles various help documents into a single manual.
- **Inputs:**
  - `../data/helpdata/HELP_ORDERMGR.xml` – general help topics for the Order Manager.
  - `../data/helpdata/HELP_ORDERMGR_View.xml` – descriptions of Order Manager screens and views.
  - `../data/helpdata/HELP_ORDERMGR_Report.xml` – help topics related to Order Manager reports.
- **Outputs:** When processed by a DocBook toolchain, it produces the full Order component user manual that combines all referenced help files.
- **Core Functionality:** Uses `<xi:include>` elements to include the external help data files. The document defines a `<chapter>` element with the title "The Order Component." No business logic or runtime configuration is contained here—it simply gathers documentation resources for publishing.

Currently `Order.xml` is the only XML file in this directory. If additional XML documents are added in the future, they should be documented here with their respective purposes, inputs, outputs, and core functions.
