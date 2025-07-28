# Order Configuration Directory

This directory contains several XML and `.properties` files that provide i18n labels and operational settings for the order component.

## OrderEntityLabels.xml
Internationalized labels for Order related entities. Each `<property>` maps an entity attribute or enumeration key to a translated value in many languages. Inputs are property keys referenced from entity definitions such as `CustRequestResolution.description.DUPLICATE`. The output is the localized string used on screens and reports.

## OrderErrorUiLabels.xml
Error messages displayed by order services and screens. Many classes (e.g. `ShoppingCartHelper`, `OrderServices`) read these properties using `UtilProperties.getMessage`. Inputs are property keys representing error conditions; outputs are user-facing error texts in multiple languages.

## OrderUiLabels.xml
General user interface labels for the order application. These properties supply screen titles, button labels and other UI text. Widgets load this file with `<property-map resource="OrderUiLabels" />` to populate `uiLabelMap` used by the templates.

## order.properties
Configuration for core order behaviour.
- `daysTillCancelReplacementOrder` – number of days before a replacement order waiting for return is automatically cancelled (used in `OrderReturnServices`).
- `autosave.max.age` – maximum number of days an anonymous auto‑saved shopping list is kept (`ShoppingListServices`).
- `order.item.attr.prefix` – prefix used when naming order item attributes.
- `order.item.comment.enable` – enables or disables the "comment" attribute on order items.
The code reads these properties via `EntityUtilProperties.getPropertyValue`, so the outputs are the numeric or text settings controlling service logic.

## taxware.properties
Static configuration for the Taxware integration in `TaxwareUTL`. Inputs include company identifiers and default origin/acceptance address information (`COMPANY_ID`, `AUDIT_FILE_INDICATOR`, `SF_COUNTRY_CODE`, etc.). These values are inserted into the Taxware data record when calling the third‑party library. The resulting output is the properly populated tax record used for calculation.

## zipsales.properties
Settings for the ZipSales tax lookup service. Currently defines `zipsales.valid.states`, a `|` delimited list of state codes. The `ZipSalesServices` class checks this property to decide if ZIP‑based tax calculation should run. Output is the filtered state list that controls whether tax calculation occurs.
