# Settings

> This document is aimed to intoduce and explain the steps to manage settings within Atlas. These actions are only possible if you are a manager with access to the admin permissions.


The amount of settings available will increase overtime. If you see a new setting that you dont understand never hesitate to reach out before using the setting.

Most settings are self explanatory and are global settings meaning what is changed there will be set for everyone.

##### General Settings
-  ###### Ship To settings
   - This is where ship to settings are globally set. It is a unique internal identifier for all location entities.
   - They must setup in the following format Ex. L-[LeaseCode] or B-[LeaseCode].[BatteryCode]
   - The multi location Format is for locations that are attached to multiple batteries/leases
- ###### Product Management
  - Truck Stop Charge
    - This is synonmous with the truck stop charge used within netsuite and must be the same for the correct charge to be sent over accurately.
- ###### Barcode Settings
  - These are for the lab barcodes that are generated and can be modified temporarily in the barcode generation
  - This will streamline the barcode generation but not necessary 
- ###### Timezone
  - This is the global timezone for the system
- ###### Is negative product value allowed
  - This setting is to prevent or allow negative quanities on sales/devilvery orders
##### User Management
- User related settings can be configured under this tab. You can force email confirmation for login. Also, you can enable cookie consent so Atlas shows a cookie consent bar for the users to accept cookie policy of your application.
- You can also enable/disable session timeout control. If it is enable and the user does not provide any input to the site during the timeout period, a countdown modal will be displayed to user. If the user still does not provide an entry to the site during the modal countdown period, user will be log out.
- Each tenant can allow tenant users to use Gravatar profile picture or not.
##### Security
- Security tab in the settings page contains password complexity settings. Host can define system wide password complexity settings in this tab.

- This tab also contains user lock-out settings to prevent users from inserting the incorrect password too many times.
##### Invoice
- Under this tab, you can configure the legal name and the address of the Host company which will be displayed on the generated invoices as the service provider.