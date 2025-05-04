A Microsoft Access database application designed to simplify and automate inventory tracking for small to mid‑sized businesses.
Features:
-->Relational Data Model: Products, Suppliers, and Inventory Transactions tables with enforced referential integrity.
-->Barcode Scanning Integration: Scan SKUs directly into a form to auto‑populate lookup fields.
-->Automated Daily Reports: VBA SendObject macro (AutoExec) emails a snapshot of current stock levels each morning.
-->Low‑Stock Alerts: Parameter queries identify products below their reorder threshold.
-->Front‑End/Back‑End Split: Separate UI (forms, reports, queries) from data storage for secure, multi‑user access.
Installation & Setup:
Open the database:
--> Launch `InventoryManagement.accdb` in Access.
Usage:
1. Adding Products & Suppliers
- Open frmProducts: enter new products (SKU, name, category, price, reorder level).
- Open frmSuppliers: add or edit suppliers and contact info.
2. Recording Inventory Transactions
--> Open frmTransactions.
--> Scan or type an SKU into the Scan box, then Tab:
   - ProductID populates automatically.
--> Enter Quantity (positive for In, negative for Out) and any Notes.
--> Save the record.
3. Viewing Current Stock Levels
- Run qryStockOnHand to see aggregated on‑hand quantities per SKU.
4. Low‑Stock Alerts
- Run qryLowStock to list products where stock < reorder level.
