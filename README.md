# Locker Mail Fix

**Locker Mail Fix** is a PrestaShop module that improves the handling of parcel locker deliveries by synchronizing the selected pickup point with the order's delivery address, order confirmation email, and back-office information.

It supports **Sameday easybox, Sameday PUDO pickup points, and FAN Courier FANbox**, helping ensure that the correct delivery location is displayed throughout the order workflow.

## Features

- **Automatic delivery address replacement** — creates a separate delivery address containing the selected locker or pickup point details, while preserving the customer's original address.
- **Sameday integration** — detects the selected easybox or PUDO point using available Sameday order and cart data, with service-type validation to avoid applying an outdated locker selection.
- **FAN Courier FANbox support** — detects FANbox details from available carrier data, with configurable carrier selection.
- **Improved order confirmation emails** — provides a modern, responsive HTML email template with order details, delivery information, payment details, products, totals, and customer account links.
- **Back-office order information** — displays the delivery method, selected locker details, current delivery address, and address replacement status.
- **Manual correction and recovery** — allows administrators to apply the selected locker address to an existing order or restore the original delivery address.
- **Configuration options** — includes settings for delivery address replacement, FAN Courier carrier selection, and the enhanced order confirmation email.
- **Order tracking and logging** — stores locker-related order information and records relevant operations and errors to assist with troubleshooting.

## Supported delivery methods

- Sameday easybox
- Sameday PUDO pickup points
- FAN Courier FANbox

Actual availability depends on the installed carrier modules and the data they provide.

## Requirements

- PrestaShop 8.0 or later
- PHP and database versions compatible with the installed PrestaShop version
- The relevant Sameday and/or FAN Courier shipping modules for the delivery methods being used

## Installation

1. Download or clone this repository.
2. Ensure the module files are placed in a directory named `lockermailfix`.
3. Create a ZIP archive containing the `lockermailfix` directory and its contents.
4. In the PrestaShop back office, navigate to **Modules → Module Manager**.
5. Upload the module archive and install the module.
6. Open the module configuration page and adjust the available settings.
7. Test an order for each supported delivery method before using the module in production.

## How it works

When an order is validated, the module attempts to identify the selected locker or pickup point. If the required information is available, it can create a new delivery address for that location and associate it with the order.

The customer's original address remains unchanged. Administrators can review the delivery information in the back office, correct an order when necessary, or restore its original delivery address.

The module also prepares an enhanced order confirmation email containing the relevant delivery details.

## Important notes

- Locker detection depends on the data provided by the installed shipping modules and the configured delivery service.
- The module should be tested with the exact versions of PrestaShop and carrier modules used by your store.
- Back up your database before installation or upgrades, and test order creation, invoicing, email delivery, and address restoration in a staging environment.

## Version

**Current version:** 2.1.0

## Author

DPRO25
