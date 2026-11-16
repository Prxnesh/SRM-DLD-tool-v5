SRM eCurricula AutoFill

A Tampermonkey userscript that automates filling session links, submitting updates, handling TOTP verification, and navigating between sessions on the SRM eCurricula portal.

Version: 5.1.2
Author: Pranesh D.

⸻

Features

* Automatic Link Filling – Automatically fills SLO 1 and SLO 2 Google Docs links for each session.
* JSON Import – Import session links in bulk instead of entering them manually.
* TOTP Integration – Generates time-based one-time passwords for verification.
* Auto Update – Automatically triggers the UPDATE action after filling links.
* Auto-Chain – Moves through sessions automatically.
* Cross-Unit Navigation – Supports continuing from one unit to the next.
* Floating Control Panel – Provides an easy-to-use interface directly on the eCurricula page.
* Persistent Settings – Saves imported links and preferences using Tampermonkey storage.

Requirements

* Google Chrome or Microsoft Edge
* Tampermonkey
* Access to the SRM eCurricula portal
* Google Docs links for the required sessions
* Your own TOTP secret, if TOTP verification is required

Installation

1. Install the Tampermonkey browser extension from tampermonkey.net.
2. Open the Tampermonkey dashboard.
3. Select Create a new script.
4. Remove the default template.
5. Paste the complete SRM eCurricula AutoFill userscript.
6. Save the script using Ctrl + S or Cmd + S.

Setup

1. Log in to the SRM eCurricula portal.
2. Wait for the AutoFill floating control panel to appear.
3. Open the settings using the ⚙️ button.
4. Enter your own TOTP secret if required and save it.
5. Select the unit you want to work on.
6. Open the JSON import section.
7. Paste the session data in the supported JSON format.
8. Click Apply Links.
9. Review the imported links to make sure they are correct.

JSON Format

The script accepts both a direct array and a unit-wrapped JSON object.

Example:

{
  "5": [
    {
      "slo": 1,
      "comp1Link": "https://docs.google.com/document/d/EXAMPLE1/edit",
      "comp2Link": "https://docs.google.com/document/d/EXAMPLE2/edit"
    },
    {
      "slo": 2,
      "comp1Link": "https://docs.google.com/document/d/EXAMPLE3/edit",
      "comp2Link": "https://docs.google.com/document/d/EXAMPLE4/edit"
    }
  ]
}

Replace the example URLs with the actual Google Docs links.

How to Run

1. Open the required unit and session in eCurricula.
2. Click the SLO 1 segment in the session wheel.
3. Make sure the correct session and unit are selected in the control panel.
4. Enable the required options:
    * UPDATE
    * TOTP
    * Auto-Next
    * Cross-Unit Chaining (if required)
5. Click Start Auto-Chain.
6. The script will fill the stored links, trigger the update process, handle TOTP verification, and proceed to the next session when possible.
7. Use Stop to stop the automation.

Tip: Keep the eCurricula tab open while the script is running. Test one session manually before starting a longer sequence.

Important Notes

* Use your own TOTP secret. Never share it with anyone.
* Ensure that the Google Docs links are accessible through your SRM account.
* Verify imported links before starting automation.
* Keep the browser tab open during execution.
* Website changes may affect the script’s functionality.
* This script is intended to assist with repetitive data entry. Always verify that the correct links have been submitted.

Disclaimer

This is an independent, unofficial userscript created for convenience and educational purposes.

It is not affiliated with, endorsed by, or officially supported by SRM Institute of Science and Technology.

Use responsibly and ensure that its usage complies with applicable university policies and portal guidelines.

⸻

Developed by Pranesh D.