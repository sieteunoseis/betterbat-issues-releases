# <img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/logo.png" width="60px" align="center" alt="Better BAT icon"> Better BAT

Better BAT was created to improve the bulk administration experience when using Cisco's Unified Communications Manager.

<h3 align="center">
  <a href="https://github.com/sieteunoseis/betterbat-public-releases/releases/latest">
  Download Better BAT for macOS or Windows
  </a>
</h3>

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/better-bat-social-preview.png" width="640px" alt="Better BAT screenshot">
</p>

# Features

### Combine Import Files

Better BAT allows you to _merge_ similar import files into a single CSV file. For example since a phone and a device profile import file share a lot of the same fields you can combine them.

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/combine-csv1.png" alt="Better BAT screenshot">
</p>

Example CSV that combines Forced Authorizations, Single Number Reach, Extension Mobility (Device Profiles), End User and Phones in a single CSV file.

AUTHORIZATION CODE NAME|AUTHORIZATION CODE|AUTHORIZATIONLEVEL|REMOTE DESTINATION NAME|DESTINATION 1|Remote Destination Profile Name|Device Name    |Device Profile Name|Description |Device Pool|CSS       |Location|Extension Mobility|USER ID |User ID 1|Owner User ID|Device Type|Device Presence Group  |Device Security Profile                     |Device Protocol|SIP Profile         |Mobility User ID|Directory Number 1|Route Partition 1|Voice Mail Profile 1|Line CSS 1   |Line Text Label 1|Alerting Name 1|Line Description 1|ASCII Alerting Name 1|Display 1 |ASCII Display 1|Speed Dial Number 1|Speed Dial Label 1
-----------------------|------------------|------------------|-----------------------|-------------|-------------------------------|---------------|-------------------|------------|-----------|----------|--------|------------------|--------|---------|-------------|-----------|-----------------------|--------------------------------------------|---------------|--------------------|----------------|------------------|-----------------|--------------------|-------------|-----------------|---------------|------------------|---------------------|----------|---------------|-------------------|-----------------------
SMITHJ-FAC1            |1000              |15                |SMITHJ-CELL            |1375551122   |SMITHJ-RDP1                    |BAT112233445566|SMITHJ-UDP1        |LAB Phone 1 |LAB_DP     |DEVICE_CSS|LAB_LOC |f                 |SMITHJ1 |SMITHJ1  |SMITHJ1      |Cisco 8845 |Standard Presence group|Cisco 8845 - Standard SIP Non-Secure Profile|SIP            |Standard SIP Profile|SMITHJ1         |\+1375551108      |INTERNAL_PT      |NoVoiceMail         |INTL_LINE_CSS|John-2408        |John Smith     |Lab Phone 1       |John Smith           |John Smith|John Smith     |91212551212        |New York Hilton Midtown
SMITHJ-FAC2            |1001              |15                |SMITHJ-CELL            |1375551123   |SMITHJ-RDP2                    |BAT112233445567|SMITHJ-UDP2        |LAB Phone 2 |LAB_DP     |DEVICE_CSS|LAB_LOC |f                 |SMITHJ2 |SMITHJ2  |SMITHJ2      |Cisco 8845 |Standard Presence group|Cisco 8845 - Standard SIP Non-Secure Profile|SIP            |Standard SIP Profile|SMITHJ2         |\+1375551109      |INTERNAL_PT      |NoVoiceMail         |INTL_LINE_CSS|John-2409        |John Smith     |Lab Phone 2       |John Smith           |John Smith|John Smith     |91212551212        |New York Hilton Midtown
SMITHJ-FAC3            |1002              |15                |SMITHJ-CELL            |1375551124   |SMITHJ-RDP3                    |BAT112233445568|SMITHJ-UDP3        |LAB Phone 3 |LAB_DP     |DEVICE_CSS|LAB_LOC |f                 |SMITHJ3 |SMITHJ3  |SMITHJ3      |Cisco 8845 |Standard Presence group|Cisco 8845 - Standard SIP Non-Secure Profile|SIP            |Standard SIP Profile|SMITHJ3         |\+1375551110      |INTERNAL_PT      |NoVoiceMail         |INTL_LINE_CSS|John-2410        |John Smith     |Lab Phone 3       |John Smith           |John Smith|John Smith     |91212551212        |New York Hilton Midtown
SMITHJ-FAC4            |1003              |15                |SMITHJ-CELL            |1375551125   |SMITHJ-RDP4                    |BAT112233445569|SMITHJ-UDP4        |LAB Phone 4 |LAB_DP     |DEVICE_CSS|LAB_LOC |f                 |SMITHJ4 |SMITHJ4  |SMITHJ4      |Cisco 8845 |Standard Presence group|Cisco 8845 - Standard SIP Non-Secure Profile|SIP            |Standard SIP Profile|SMITHJ4         |\+1375551111      |INTERNAL_PT      |NoVoiceMail         |INTL_LINE_CSS|John-2411        |John Smith     |Lab Phone 4       |John Smith           |John Smith|John Smith     |91212551212        |New York Hilton Midtown
SMITHJ-FAC5            |1004              |15                |SMITHJ-CELL            |1375551126   |SMITHJ-RDP5                    |BAT112233445570|SMITHJ-UDP5        |LAB Phone 5 |LAB_DP     |DEVICE_CSS|LAB_LOC |f                 |SMITHJ5 |SMITHJ5  |SMITHJ5      |Cisco 8845 |Standard Presence group|Cisco 8845 - Standard SIP Non-Secure Profile|SIP            |Standard SIP Profile|SMITHJ5         |\+1375551112      |INTERNAL_PT      |NoVoiceMail         |INTL_LINE_CSS|John-2412        |John Smith     |Lab Phone 5       |John Smith           |John Smith|John Smith     |91212551212        |New York Hilton Midtown

### Live Feedback

![Screenshot: Better BAT running](https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/live-feedback.png)

Better BAT shows misconfigurations with your import file before you make any changes. This saves engineers from issues stemming from bad data collections, typo's or features not supported by all phone models.

* #### Legend
  - ![#ff4c42](https://via.placeholder.com/15/ff4c42/000000?text=+) `RED - Missing or misconfigured field.`
  - ![#add8e6](https://via.placeholder.com/15/add8e6/000000?text=+) `LIGHT BLUE - Used to identify if device or user is already configured on server.`
  - ![#ffa503](https://via.placeholder.com/15/ffa503/000000?text=+) `ORANGE - Warning that value doesn't correspond with other items in configuration. Mostly likely a misconfiguration but would not stop import. Example would be setting a Call Forward to Voicemail but the NoVoiceMail profile is set.`
  - ![#00ff7f](https://via.placeholder.com/15/00ff7f/000000?text=+) `GREEN - Fields updated by Auto-Fix Feature.`
  - ![#fcedd9](https://via.placeholder.com/15/fcedd9/000000?text=+) `IVORY - Fields updated by Search and Replace Feature.`
  
### Auto-Fix

![Screenshot: Better BAT auto-fix](https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/auto-fix.png)

Better BAT has a built in auto-fix feature to help engineers fix missing/misconfiguration of certain fields. Currently Auto-Fix will help solve the following fields:

* **Phone Button Template**
  * Auto-Fix will analyze the number of lines and speed dials configured on each device. It will then try to select the best phone template that matches the configuration. (Note: Auto-Fix will only select phone templates that match the exact phone model)
* **Device Pool**
  * Via the Settings > Options > Auto-Fix Keyword, Auto-Fix will try to select a Device Pool that contains the keyword. This is useful if you use site codes or any other naming convention. (Note: Auto-Fix will only change/update fields that are marked as incorrect)
* **Location**
  * Via the Settings > Options > Auto-Fix Keyword, Auto-Fix will try to select a Location that contains the keyword. This is useful if you use site codes or any other naming convention. (Note: Auto-Fix will only change/update fields that are marked as incorrect)
* **Max Call/Busy Trigger**
  * Auto-Fix will look up the default settings per device type and fill in the missing values
* **Device Security Profile**
  * Auto-Fix will select the default Device Security Profile for the particular device type. Example: for a Cisco 8845, Auto-Fix would select "Cisco 8845 - Standard SIP Non-Secure Profile". (Note: This feature is for phones configured as SIP in the Device Protocol)
* **MLPP Support** (MLPP Indication & MLPP Preemption)
  * Auto-Fix will look up the default settings per device type and set to off if the model does not support the feature.
* **Extension Mobility Support**
  * Auto-Fix will look up the default settings per device type and set to off if the model does not support the feature.
* **DND Support**
  * Auto-Fix will look up the default settings per device type and set to off if the model does not support the feature.
* **SIP Profile**
  * Auto-Fix will select "Standard SIP Profile" if this is missing from the import file. "Standard SIP Profile" is a non-deletable profile in Communication Manager.
* **Common Phone Profile**
  * Auto-Fix will select "Standard Common Phone Profile" if this is missing from the import file. "Standard Common Phone Profile" is a deletable profile in Communication Manager, please verify that it still there before using Better BAT.
* **Line Display and Alerting Names**
  * Auto-Fix will copy data from Display (Caller ID) to ASCII Display (Caller ID) if missing.
  * Auto-Fix will copy data from Alerting Name to ASCII Alerting Name if missing.
* **Call Forward to Voicemail Settings**
  * Auto-Fix will set fields that are incorrect or empty to either 't' or 'f' depending on what voice mail profile is selected. Example: if engineer has 'NoVoiceMail' profile selected and true set for the 'Forward Busy Internal Voice Mail', Auto-Fix will update this to be false.
* **CSS** (Calling Search Space)
  * Via the Settings > Options > Auto-Fix Keyword, Auto-Fix will try to select a CSS that contains the keyword. This is useful if you use site codes or any other naming convention. (Note: Auto-Fix will only change/update fields that are marked as incorrect)
  
### Error Button

Better BAT will count errors detected in import file and allows users to cycle to issues to speed up remediation of issues.

### Dynamic Column Dropdown

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/dynamic-dropdown.png" width="640px" alt="Better BAT screenshot">
</p>

Better BAT has a dynamic dropdown with typeable search to quickly navigate to a particular column. This reduces time spent trying to find and update a particular field.

### Customizable Options

#### Regex Options

Better BAT will help customers with naming standards. Via the Settings > Options menu, engineers can set regex for the following:

* Device Description
* Line Description
* Line Text Label
* Alerting Name
* Display

If a regex is set and the value of the import file does not match field will be shown in orange. Example: setting the Line Text Label Regex to `^[A-Z].*-(?:\d{4})$` would vaildate that the field needed to be a word followed by a hyphen and 4 digits. Josh-1234 would be valid, however Josh1234 would not be.

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/failed-regex.png" alt="Better BAT screenshot">
</p>

#### CSS Keyword Filter

Does your Unified Communications Manager have a ton of different calling search spaces? Are they named according to the type of function they do? If so you can have Better BAT filter down the selectable options. For example if your naming standards for calling search spaces used on the device level all contain the word `DEV` in them you can set this via Better BAT. That way the dropdown for this field is filtered to only include these as options.

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/css-filter1.png" alt="Better BAT screenshot">
</p>

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/css-filter2.png" alt="Better BAT screenshot">
</p>


#### ParamName and ParamValue Options

Better BAT also allows engineers to hardcode any field in an import file. This cut down on the amount of columns needed in an import file. This feature is similar to Cisco's implementation of Phone Templates, without the restriction of having to do it per phone model. Example: If your directory numbers are all in the same route partition, you can hardcode this and leave the column completely out of your import file.

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/custom-param.png" alt="Better BAT screenshot">
</p>

### Activation Code Support

Since the release of Unified Communication Manager 12.5, administrators have been able to assign an activation code for users to onboard their phone. Better BAT includes support for this feature. Simply add a column; **Enable Activation ID** to your import file and set values to either _t_ or _f_. While importing the phones, Better BAT will retrieve the code for you.

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/activation-id.png" alt="Better BAT screenshot">
</p>

### Jabber Conversion

Better BAT can convert existing phones into a CSF device. Just import a csv file that has a single column named **Jabber Convert** with the list of device names that need to have a Jabber counterpart. Better BAT will pull the configuration from the phone and convert to a Jabber desktop device. Note: only the first 8 lines will be included and any feature not supported by Jabber will be disregarded.

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/jabberconvert.png" alt="Better BAT screenshot">
</p>

Sample CSV should look like:

|Jabber Convert|
|----------------|
|SEP112233445566|

### Unity Connection Support

Better BAT can import Unity Users via REST. Support for both LDAP and Local Users (Note for LDAP you need to have the LDAP username set for field **LdapCcmUserId**). Simply select the User Template when importing and Better BAT will import users against selected template.

### Airtable Support

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/airtable-1.png" alt="Better BAT screenshot">
</p>

Better BAT has support for Airtable. Stop using spreadsheet to collect data for phone imports. Instead use a cloud based collaborative tool from Airtable.

<p align="center">
<img src="https://github.com/sieteunoseis/betterbat-public-releases/blob/master/images/airtable-2.png" width="640px" alt="Better BAT screenshot">
</p>

Airtable offers form views for each spreadsheet. Engineers can send out links to allow end-users to update or add missing information.

### Built with Electron, NodeJS and Handsontable

Better BAT includes Handsontable's excellent spreadsheet editor. This includes support for Formulas, Dropdowns, Sorting and much more. Check out more information on their [website](https://handsontable.com/).


