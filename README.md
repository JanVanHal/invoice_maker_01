# Invoice Generator

A single-file HTML invoice tool. No installation, no login, no internet required. Open the file in any browser and start invoicing.

---

## Getting Started

1. - Download the file from : https://shorturl.at/iHJGX 
   - Or use the link https://janvanhal.github.io/invoice_maker_01/ and Bookmark.
2. Open it in your browser (double-click or drag into a browser window)
3. Fill in the fields on the left — the invoice preview updates live on the right
4. Click **↓ Save as PDF** when ready

That's it. Nothing to install.

---

## Filling In the Invoice

### Invoice Number & Date
Enter your invoice number manually. The date defaults to today and can be changed freely.

### Invoice To (Client)
Fields for the receiving party:
- Company Name
- Address Line 1, Line 2, Country
- Email, Telephone
- VAT NR, KvK

Any field left blank will not appear on the PDF.

### Invoice From (You)
Your own details: name, up to three address lines, email, and phone.

### Subject
An optional reference line that appears as **Re: …** on the invoice. Leave blank to hide it.

### Line Items
Each line has a description, quantity, and unit price. The total per line and the overall subtotal are calculated automatically.

Use **+ Add line** to add more rows. Use **×** to remove a row (minimum one line is kept).

### VAT
Enter a VAT percentage (e.g. `21`). Set to `0` for VAT-exempt invoices. The subtotal, VAT amount, and total due are shown separately.

### Payment Details
Bank account number, account name, account holder address, bank name, IBAN or SWIFT/BIC, and bank address. Toggle between **IBAN** and **SWIFT / BIC** using the radio buttons — this changes the label on the PDF accordingly.

---

## PDF Filename — How It Is Generated

The filename is built automatically from two fields:

```
Invoice_<YourName>_<Month>_<Year>.pdf
```

| Part | Source |
|---|---|
| `YourName` | **Invoice From → Name** (spaces replaced with underscores) |
| `Month` | Month from the **Date** field (e.g. `May`) |
| `Year` | Year from the **Date** field (e.g. `2026`) |

**Example:** If your name is `Jan de Vries` and the date is `2026-05-25`, the file saves as:
```
Invoice_Jan_de_Vries_May_2026.pdf
```

The generated filename is shown in the grey preview box below the **Save as PDF** button and updates as you type. If either the name or date is missing, the file falls back to `invoice.pdf`.

---

## Saving & Restoring Your Data

Your data is saved automatically in the browser as you type. If you close and reopen the file in the same browser, all fields will be restored exactly as you left them.

### Export
Click **↑ Export** to download your current data as a `.json` file. The export file is named after your own name:
```
invoice_data_Jan_de_Vries.json
```
Use this to back up your data or transfer it to another device.

### Import
Click **↓ Import** and select a previously exported `.json` file. All fields will be restored immediately.

### Clear
Click **✕ Clear** to wipe all fields and start fresh. A confirmation prompt appears before any data is deleted. Today's date is restored automatically.

---

## Notes

- All data stays in your browser — nothing is sent to any server.
- The app works offline.
- Each browser on each device has its own separate saved data.
- If the same file is opened in a different browser, it will start blank.
