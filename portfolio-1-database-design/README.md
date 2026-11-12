# Portfolio 1 – Database Design and Modelling

## Case study
Chowdeck is a simplified food-delivery platform. Customers order from vendors, and riders deliver the orders. The database stores customers, vendors, menu items, orders, payments and delivery tracking.

## Users
- **Customers** browse menus, place orders and track deliveries.
- **Vendors** manage menu items and stock, and accept orders.
- **Riders** pick up and deliver orders.
- **Operations staff** assign riders and handle cancellations and refunds.

## Main operations
1. Register a customer and save a delivery address.
2. Add a vendor and its menu items.
3. Place an order with one or more items.
4. Record a payment for an order.
5. Assign a rider and update delivery status.
6. Cancel an order and refund its payment.
7. View an order's tracking history and vendor sales.

## Business rules
1. Each customer and rider has a unique phone number.
2. Each menu item belongs to one vendor. Its name is unique within that vendor.
3. An order belongs to one customer, one vendor and one delivery address.
4. An order has at least one item. Each item has a positive quantity.
5. An order's total equals its subtotal plus its delivery fee.
6. An order is paid once, with a unique payment reference.
7. An order's status moves forward from placed to delivered, or ends as cancelled. Delivery time cannot be earlier than placed time.
8. Stock cannot be negative. Item prices are copied onto the order, so later price changes do not alter past orders.

## Scope
Included: one platform with fictional data in Nigerian naira, covering ordering, payment, delivery and refunds. Excluded: real payments, live GPS tracking, promotions, ratings, vendor payouts and authentication.

## Assumptions to confirm
- Each order is from a single vendor and paid by one payment.
- A rider handles one order at a time.
