# Global Protect in Mac

Q1: Connection Failed

Error message: 

Could not connect to the GlobalProtect service. Make sure the GlobalProtect service is running. If the issue persists, contact your administrator.

Solution:
* Remove tokens
    * Navigate to Spotlight Search
    * Type: "Keychain Access" and press Enter.
    * The Keychain Access window will open, then search for Token.
    * Delete all any tokens named: "refreshtoken-xx", "primaryrefreshtoken-xx", "idtoken-xx", and "accesstoken-xx".
    * Connect to GlobalProtect  again.

* Check service
Run command in terminal.
```
launchctl load /Library/LaunchAgents/com.paloaltonetworks.gp.pangpa.plist
```

* Re-install
    * If the service is running, then remove Global Protect and re-instal as the root admin on the Mac
    * Before re-installing. It is important to allow 3rd party apps to run.
    * Uninstall Global Protect.
    * Log in as the admin user.
    * Reinstall Global Protect
    * Once Global Protect is re-installed, head back over to the "Security and Privacy" settings. A prompt message should pop up which asks if Global Protect is allowed to run on this machine.
    * Click "YES"
