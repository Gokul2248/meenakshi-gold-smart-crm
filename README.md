# Meenakshi Jewels Smart Visitor CRM

Mobile-first exhibition visitor capture for **Meenakshi Jewels**, using the same workflow and backend architecture as the Varaa Gold Smart CRM.

## Branding
- Brand: **Meenakshi Jewels**
- Theme: deep maroon/burgundy, cream, gold and teal accents
- Logo: extracted from the supplied Meenakshi Jewels branding image and stored as `public/meenakshi-logo.png`

## Collection interests
1. 1 Stone
2. Traditional Nosepin
3. Trending Side Studs
4. Plain Bali
5. Stone Balli
6. Koppu
7. Casting Nosepin & Side Studs
8. Casting Side Studs
9. Twister
10. Dual Look Studs
11. Bluetooth Ear cuff with Screw

Multiple collections can be selected for one visitor and are stored in the `Interests` field in Google Sheets.

## Visitor flow
- Take Photo opens the phone camera.
- Choose Photo selects a card image from the phone album.
- Original card image is stored in Google Drive.
- Staff captures mobile/WhatsApp number, shop/company name and Place.
- Staff selects collection interests, notes, priority and follow-up.
- Backend generates a unique MJ record ID/index.
- Existing-customer matching uses normalized mobile number or shop name.

## Configuration
Worker variables/secrets:
`GOOGLE_APPS_SCRIPT_URL`, `GOOGLE_APPS_SCRIPT_SECRET`, `ADMIN_PASSWORD`

Google Apps Script properties:
`CRM_SECRET`, `CRM_SHEET_ID`, `CRM_FOLDER_ID`

Run `setup()` once in Google Apps Script to create the Meenakshi Jewels Sheet and Drive folder.
