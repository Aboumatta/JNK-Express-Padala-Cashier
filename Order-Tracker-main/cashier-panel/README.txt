JNK Express — Cashier Panel
--------------------------

Files added:
- cashier-panel/index.html  -> Cashier web UI for scanning tracking numbers and simple product sales.
- This panel expects your Firebase initialization code to be available in the project; the script attempts to include a detected firebase config file automatically.

How it works:
- Scanning input will mark tracking documents in Firestore (collection 'tracking') as status='Claimed' and log an entry to 'cashierLogs'.
- If 'This is a product sale' is checked, it will look up the 'products' collection by 'code' or barcode and decrement quantity, then record a 'sales' entry.

If your project uses a different collection/field names, open cashier-panel/index.html and adjust the Firestore collection names and fields accordingly.
