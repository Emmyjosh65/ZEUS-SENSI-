ZEUS SENSI — PIN FOLDER
========================

WHAT THIS FOLDER DOES
---------------------
This folder controls the premium access PINs of your site.
Users must enter one of these PINs to unlock the premium tools
(Sensitivity Generator + HUD Configuration).

HOW TO ADD A PIN (more than 1 works)
------------------------------------
1. Open pin/pin.js
2. Find this section:

   window.VALID_PINS = [
     "ZEUS2026",
     "DANNY777",
   ];

3. Add your own pin on a new line, like this:

   window.VALID_PINS = [
     "ZEUS2026",
     "DANNY777",
     "MYNEWPIN123",
   ];

4. Save. Done. The new pin now works on your site.

RULES FOR PINS
--------------
- Letters and numbers only (A-Z and 0-9)
- No spaces, no symbols
- Pins are case-insensitive (zeus2026 = ZEUS2026)
- You can have as many pins as you want

HOW TO REMOVE A PIN
-------------------
Just delete that line from the list.

CAN I LOCK THE HUD SECTION BEHIND A PIN?
----------------------------------------
Yes. In pin/pin.js, find:

   window.ZEUS_CONFIG = {
     protectHudSection: false
   };

Change "false" to "true". Now the CREATORS CUSTOM HUD section
stays hidden until someone enters a valid PIN.

HOW TO UPLOAD TO GITHUB (emmyjosh65/ZEUS-SENSI-)
------------------------------------------------
1. In your repo, create a new folder called  "pin"
2. Upload pin/pin.js (and this README) into that folder
3. Upload the new index.html to the repo ROOT (replace the old one)
4. Keep every other file you already have — nothing else is removed
5. Wait 1-2 minutes for GitHub Pages to update

TESTING
-------
Open https://emmyjosh65.github.io/ZEUS-SENSI-/
Click any "Open" button on a premium tool -> enter a PIN from the list.
Valid PIN  -> unlocked (stays unlocked on that device)
Wrong PIN  -> error message
