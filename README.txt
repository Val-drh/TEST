V1.5.3 - 231005

Features
 - added new Audit class to improve line removed logging etc
 - added more data to line removed table to improve auditing
 - added currentUser object to teminal class reduces dependency on other classes
 - added company details object to reports, enable company details to be used in reports
 - added duration details to break records
 - added feature to allow some custiomization of reports for neagtive numbers and currency symbol
 - added the ability to assigned a customer as tax exempt (example duty free in UK)
 - rework of discount scripts for line and ticket
 - ability to disable reprint ticket button
 - ability to disable products from having auxiliary items, reduces data size when adding auxiliary items
 - 2 new reports added for current stock 
 


Bugs
 - 000229 Cancelling in reset reports password has changed
 - 000243 Reports not showing correct payment types
 - 000244 Line removed logging
 - 000245 Buttons not reading the size correctly and implementing them
 - 000246 Barcode button not responding correctly
 - 000247 Stocklevel bug when products are updated
 - 000248 Missing field when importing data resolved
 - 000250 Payment Selector reports Icon missing 
 

------------------------------------------------------------------------------------------------4
V1.5.2 - 230505

Features
 - added time frame to report generation window
 - added option in setup to allow users to change the default font and size for POS
 - Added ability for recipes to have auxiliary items setup
 - Added new flag option to products\recipes to allow then to have auxiliary items (reduces items listed in Auxiliary panel when not enabled)
 - Ability to disable reprint last ticket added to user roles
 
 
 Bug fixes
  - 000236 Gift card sales crash close cash screen
  - 000234 Column width in inventory
  - 000233 Reservations not saving
  - 000230 Issue on new login screen with image size
  - 000229 Passwords always reported that password has bee changed
  - Fixed an issue where values could be left on view tables after deletion
  
------------------------------------------------------------------------------------------------
V1.5.1 - 230204

Features
 - New style login screen created (password complexity on roadmap) users must have a password, blanks not allowed

Changes
 - Increased field size on combobox for screen type in setup
 - increase column size in database of name in supplier orders
 - added new system property swingfont

Bug fixes
 - 000226 Login issues database connection issues
 - 000225 Full Screen not working
 - 000224 Loyalty Info popup not relative the parent screen location
 - 000223 Dialog box & Customer card buttons sizing, Cancel throws error
 - 000222 Customer transaction history not correct
 - 000221 Unable to complete sale due to umlat in company name
 - 000217 Tables not aligning correctly after updating in POS 

------------------------------------------------------------------------------------------------
V1.5.0 - 225004

Changes
 - Moved away from exe to allow Linux version compatability, now calls jar file directly
 - Font standardization started, ready for Linux release. Fonts are installed as part of the install process
 - Tables now show covers in brackets after name
 - Reservations screen replaced, with cleaner version
 - Updated resource handling routines
 - Some resources updated to resolve customer display problems
 - Rountine updated for customer display 
 - table css remove from admin uses chromisadmin.css
 - Updated Auxiliary table view to not show system objects
 - Updated Auxiliary table added addition column to indicate if product has auxiliary items
 - Reworked backup and restore routines
 - Added repair triggers to utility menu when user is granted the permissions
 
 
 


Bug fixes
 -- Issues found in absence data and layouts
 - 000214 send ticket to printer after sending and the trying to increase line count and sending again
 - 000213 blank tickets sent to remote printer under certaion circumstances
 - 000212 employee barcodes not working
 - 000211 Hourly sales on close cash incorrect
 - 000208 Receipt panel not centring to sales screen
 - 000207 Currency not showing correctly
 - 000206 Customer transaction history
 - 000204 Incorrect discount showing against ticket
 - 000197 Customer display error on reprint of last ticket
 - 000194 Customer display does not clear after ticket deleted via bin option
 - 000193 customer display showing extra tax in price
 - 000190 Number error customer payment

------------------------------------------------------------------------------------------------
V1.4.9
3rd November 2022 

Changes
 - Started changes in the paymentsmodel class
 - Added ability to reprint closed cash reports
 - Updated closed cash reports
 - Replaced product finder with new style popup & OSK
 - Replace icon in ticket finder from hand to edit 
 - Changed the layout of the text in the list box
 - Java version check to stop any version lower than 11 from running
 - prevents application and database mismatch running
 - Import cvs trim and string entry to remove white space
 - Import kitchen description added to field list in import utility 
 - Incresed field size on payment panels
 - Added reciept prompt to Cusomter debt payment
 - Update locale settings, Chromis has control of it locale not the base OS region (these may need to changed in Chromis if required).
 - Database Creator pre populates usercountry and userlanguage based on OS
 - Added new permission to allow table lock to be overridden if required
 
  

Bugs fixes
 - 000192 Sequence tables not prepopulating with starting values
 - 000191 Lock table issue, allowing same table to be opened at the same time on multiple terminals
 - 000190 Customer debt payment, issue caused by numberfield conversions for some decimal searators
 - 000189 DB creator save pawword issue on first run for new install
 - 000186 & 000187 Fixed popups caused when operating in full screen mode, identified by customer button not working
 - 000184 Split button not populating somefields in ticketlines table
 - 000183 Password issue value not passing in from login screen
 - 000175 Wrong user in dbcreation displays wrong message
 - 000162 SQL error when user management - orders
 
 
------------------------------------------------------------------------------------------------
20th October 2022
V1.4.8
 
Changes
 - OSK created to replace the phone style option.
 - redesign of a number of forms, removing miglayout rather that swing designer
 - Rewrite of forms code to use the OSK
 - increased the debt field to allow greater number
 - Button images now read directly from zip rather than folder
 - Some locales updated with new\changed entries
 - Some core import code updated


Bugs fixes
 - 000151 Total Discount % stuck in ticket, discount can no be cancelled
 - 000156 Currency Symbol in loyalty panel
 - 000157 Printer.Payments missing payment methods
 - 000164 Attributes removed from ticket after discount applied
 - 000166 Date format from locale in orders rather than default
 - 000171 Backups not working correctly, command line parser updated
 - 000173 Backup error if non exist folder found in properties file
 - 000174 MySQL does not trim white space, MAriadb does, new validation added to resolve
 - 000177 Some tables uppercase (Liquibase created tables)
 - 000178 Barcodes not created as part of import process.
 - 000179 Closing cash report showing incorrect category data
 - xxxxxx fixed stock diary entry issue to use id rather than name
 - xxxxxx fixed average stock price caused by negative current stock values
 - xxxxxx Changed definer for SP and triggers 

 
------------------------------------------------------------------------------------------------
17th April 2022
V1.4.7

Changes
 - Updated reports setting internal report name to title allowing this to be used to populate export name automatically
 - Added tax update scheduler & manual process button
 - Updated tax related reports
 - Changing tax rate automatic refreshes product on tax saving rate (Reports updated to reflect this)
 - Added supplier selector and reference in stock diary
 - Added scheduler warning in some panels
 - Code changed to allow Kitchen screen to work with V1.4.7+
 - Dropped Kitchen screen hot fix fot MySQL 8 (required in Kitchen screen folder) 
 - Added new column to tickets, 'TicketOwner' this is set on the creation of the ticket and not on save
 - Lock shared tickets to ticketowner if required ie waiters
 - New reports added 
 - Added send cancellation ticket to remote printers if enabled for orders sent
 - Enable kitchen description on remote devices
 - Changed data structure around tickelines and stockdiary entries to assist with reporting
 - Added buy price tax rate to products used for order system
 - Resources backed up into database prior to upgrade (allowing user restore if changed)
 - Added Resource recovery options - only works with changed not deleted 
 - Now supports partial order deliveries from suppliers
 - Discounts scripts updated to allow discount to be removed
 
 
 
Bugs fixes
 - 000127 Customer not saving caused by null from migration
 - 000128 Max discount cannot be reset back to 0%
 - 000129 Stock diary entries not recording correctly
 - 000132 Report not downloading 
 - 000133 Consolidated screen, (now will also select the ticketline where the consolidation occured)
 - 000135 Warning in terminal config not showing if app is not running as local admin
 - 000137 System exits while attempting to open receipts in customer transaction (admin)
 - 000138 Recipe stock levels not calaculating correctly
 - 000139 Recipes do not have the cost price available reports
 - 000140 Discounted item not sending to kitchen
 - 000141 Splitting ticket crashes
 - 000142 Deleting ticket with sent items
 - 000143 Pickup id updating fix
 - 000147 Startup errors when DB not available shows java stack only
 - 000149 Collectx loayalty and layaway issue
 
 
------------------------------------------------------------------------------------------------
29th March 2022
V1.4.6 221403

Changes
 - Changes to the way locales work, allow for different Locale from the OS default
 - Add SQL version checker to Create Database function to prevent use of none supported versions
 - Changed the ticket.close script, this not an automatic update
 - Changed receipt buttons on payment screen removed receipt off\on button
 - Changed ticketclose dialog 
 - Added PoNumber default with prefix, can be overridden by the user, increments after each PO created
 - Updated Stock diary to use default pack size of the product, can be overriden by user
 - Updated backup routine to include stored procedures
 - Added capability to handle ISSN codes for newspapers and Magazines
 - Added SystemInfo output file
 - Changed dialog boxes in POS to be more touch screen friendly (still checking for all occurances of old style)
 - Changed discount code to work more effectively
 - Customer selector icon is disabled after customer is set on ticket
 - Admin default size can be set by adding parameters to chromisposconfig.properties height=x width=y must be separate lines min height=768 width=1024
 - Added trigger checking code with repair option
 - Improved Locale setting routines
 - Resolved Service Charge setup, also prevents multiple SC being added to the same order
 - Updated Liquibase to 4.9.1
 - Added Backup button to updater

 


Bug fixes
 - 000106 Discount message still showing ticket after removal of discounted products
 - 000107 Added debt into refund panel to send back to customer debt
 - 000108 Missing library causing crash after webcam enabled (Administration)
 - 000109 MySQL on none English machine Admin fails to start
 - 000112 List showing editable tickets incorrect amount 
 - 000113 increases\decreases to amount looses focus
 - 000115 Sales not saving, TLV encoder error
 - 000116 Supplier panels not updating
 - 000118 Refund service charge not workign correctly
 - 000119 Customer debt defaults to null instead of 0.00
 - 000120 Giftcards and loyalty always scanning even if disabled
 - 000121 Default products causes error when saving after using + key to increase count
 - 000122 Creating backup giftcard\loyalty database fails
 - 000123 Customers being retired on diabling of account
 - 000124 Not reading some localized files
 - 000125 Button line text error
 - 000126 Text colour in Hifi on alerts not changing contrast
 - 000128 max discount cannot be reset to 0%
 
 
------------------------------------------------------------------------------------------------
16th January 2022

V1.4.5  220306

 - Upgrade and new install schemas validated with Compalex

Changes
 - Key Change to the way tier pricing works, previous the disocunt value was saved, but due to the calculation in accuracy, this has change to save values, 
       + Ensure that yuou have no scheduled updates before running as these will be lost as part of the change process
 - Check if tiered price before applying discount (line and Tickt)
 - New supplier reports added
 - Updated Closecash report to allow xml include flag
 - New systemproperty entry added 
 - Added timestamp column to critical tables
 - Started to implement TinyLog logging
 - TLV code added to create encoded qrcode 
 - new XML flag to print tlv qrcode example add <line><qrcode size ="125">${ticket.getTlvCode()}</qrcode></line>
 - Installer package updated
 - database creator and update script improved
 - added in catalog switch to import routine



Bug fixes
 - 000105 Import failing due to column order changes and missing default parameter
 - 000104 Tier pricing for imported or migrated does not save
 - 000102 customer display not clearing correctly
 - 000101 Line discount with no value entered
 - 000100 Ticket resource not displaying correctly
 - 000099 duplicate bug 000096
 - 000097 Close cash error wrong data placed into the table
 - 000096 Attributes not show on kitchen tickets
 - 000095 Retired fucntion in products panel not working 
 - 000094 Listeners on some product objects not working
 
------------------------------------------------------------------------------------------------
December 12th 2021

V1.4.4rc  215007 HF1

Changes
 - Added validation prompt to create database routine
 - Updated extensions in resources


Bug fixes
 - Corrected resources issues wrong resouces updated

------------------------------------------------------------------------------------------------
December 12th 2021

V1.4.4rc  215006

Changes
 - Added new tool to allow the resouces to be saved out to local fles
 - Added new icon will be used as default for ticketline add note button
 - Added utility to allow checking of terminal and chromisposconfig.properties existence
 - Change property description from cardnotes to linenotes where used, is more descriptive
 - Added permissions for ticketlines notes
 - updated Migration added some column row checks



Bug fixes
 - 000092 search panel in POS not returning any results
 - 000093 TerminalConfig printer issues, not showing correctly in config


------------------------------------------------------------------------------------------------
December 7th 2021

V1.4.3rc  215003 (combines 214906 & 215001)

Changes
 - Added new column to tickets table (ticketdiscount)
 - Added new field to products, which allows a different product description to be sent to remote printer if required
 - Added new field to ticketlines flags if the line has been discounted
 - Add new details to printer.ticket if discount applicable then amount displayed on the ticket
 - Changed structure of ticket.buttons.xml gets image from imagefactory class
 - If ticketline has been discounted it does not count towards tiered pricing numbers
 - New Images added to indicate id discount button is line or ticket based
 - Dymanic Attribute button, is only active if the product has attribute set assigned
 - Added default flag in locations ready for future use.
 - Updated Ticket.Printer resources now displays total discount on the ticket at the bottom
 - Max discount changed to spinner with default of 10% if can discount is enabled, can be changed by the user
 - updated ticket script to show discount for ticket
 - Fixed issue with migrate for issue caused by legacy tax setup
 - Add line indicator if line discounted 
 - Basic terminalchecker added to installer
 - Moved ticket receipt headers into include file

Bug fixes
 - 0000088 Edit ticket list shows amount tendered rather than ticket amount
 - 0000087 Saving to shared tickets for discount lines
 - 0000085 Missing Icons
 - 0000081 Barcode scannings issue changed datalogic call
 - 0000077 Missing entries in properties files added
 - 0000076 Save button state not changing for certain settings in products panel
 - 0000075 Error when trying to use Loyalty in payment screen
 - 0000070 discount not working, and Icon colour
 

------------------------------------------------------------------------------------------------
November 21st 2021

V1.4.1rc 214707

This version prepares the system ready for the new updater application due shortly.

To update the current version the installer must be run for all installations


Changes
 - Update external liquibase library to resolve update issue 
 - Creates 2nd database to be used by update routine
 - Application update routines added to applications in readiness for future release
 - Removed update table from main database (record size could exceed 150meg)
 - Added new column to terminals table, to record applictaion version running on it (in multi till can be used to checked updated tills)
 - Table removed from database creation script (same code included in updater script)
 - installer changed to not ask for VC++ runtime if already present
 

Bug fixes 
 - 0000071 Customer display not clearing in resturant mode when ticket is deleted 
 - 0000072 Tax Calc admin, tax appears to be incorrect in admin panel 
 - 0000073 Customer display missing label text

------------------------------------------------------------------------------------------------
November 14th 2021

V1.4.0rc 214607

This is the first rc version of the new Chromis application stack. 
It has been written to use Java 11 LTS. (some basic testing has been done with Java 17). Chromis will only be tested with LTS versions of java and OpenJDK versions, due to Oracle now charging for the use of their implementation.

The main stack consist of a number of applications with lots of new features and a new logo.

Administration
 - All administration has been moved out of the POS element and implemented into a stand alone application. This is a JavaFX application rather than swing.

POS 
 - All sales are handled by this application.

System Config - this called using parameters passed by the bat files
 - This is used to create the database
 - Config the System
 - Config the terminal

Once a terminal is configure the only elements required are those installed by selecting Pos in the installer, any config files can be removed.

Postresql and Derby database support has been dropped (PostgreSQL may be considered again at a later date).

Some of the new features include
  * Suppliers
  * Units of measure (these work with quantities and not just descriptions)
  * Supplier Orders
  * Some areas consolidated in to a single screen 
    - Tax setup
    - Attributes
    - Floor layout
  * Recipes (originally called product kits)
  * Stock management and stock taking
  * Price update scheduler
  * Gift cards
  * Loyalty system
  * New reports (Reports are still being written)
  * Reduced properties file, setting are now stored in the database or locally as part of the OS (registry on windows)
  * New manuals (Pos manual to follow once pos is updated)


All bug reporting for this release and above MUST be logged on the Chromis bugtracker
   https://chromis.co.uk/bugtracker
You will need to create an account before it can be used.

