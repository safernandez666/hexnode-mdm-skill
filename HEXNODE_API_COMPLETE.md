# Hexnode API - Complete Documentation

**Scraped:** 2026-11-09 12:33:48

**Total Endpoints:** 104

---

## Table of Contents

- [Actions](#actions) (37 endpoints)
- [App Catalogs](#app-catalogs) (6 endpoints)
- [App Groups](#app-groups) (6 endpoints)
- [Applications](#applications) (6 endpoints)
- [Automations](#automations) (2 endpoints)
- [Content Management](#content-management) (3 endpoints)
- [Device Groups](#device-groups) (6 endpoints)
- [Devices](#devices) (6 endpoints)
- [General](#general) (5 endpoints)
- [Organizational Units](#organizational-units) (1 endpoints)
- [Policies](#policies) (9 endpoints)
- [Reports](#reports) (2 endpoints)
- [Setup](#setup) (3 endpoints)
- [User Groups](#user-groups) (6 endpoints)
- [Users](#users) (6 endpoints)

---

# Actions

**Total endpoints:** 37

## Scan Device

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/scan-device/](https://www.hexnode.com/mobile-device-management/developers/actions/scan-device/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Scan Location

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/scan-location/](https://www.hexnode.com/mobile-device-management/developers/actions/scan-location/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Lock Device

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/lock-device/](https://www.hexnode.com/mobile-device-management/developers/actions/lock-device/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| message | String | Optional. Message to be displayed on the device | Optional |
| phone_number | String | Optional. Phone number | Optional |
| user | Array | Optional. IDs of the users | Optional |
| usergroup | Array | Optional. IDs of the user groups | Optional |
| device | Array | Optional. IDs of the devices | Optional |
| devicegroup | Array | Optional. IDs of the device groups | Optional |
| system_lock_pin | String | Required for macOS devices without Apple Silicon Chip. A 6-digit PIN to unlock the device. | Yes |

---

## Clear Passcode

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/clear-passcode/](https://www.hexnode.com/mobile-device-management/developers/actions/clear-passcode/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | IDs of the users | Optional |
| usergroups | Array | IDs of the user groups | Optional |
| devices | Array | IDs of the devices | Optional |
| devicegroups | Array | IDs of the device groups | Optional |

---

## Change Owner

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/change-owner/](https://www.hexnode.com/mobile-device-management/developers/actions/change-owner/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| devices | Array | Required. IDs of the devices | Yes |
| user | String | Required. IDs of the user | Yes |

---

## Wipe Device

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/wipe-device/](https://www.hexnode.com/mobile-device-management/developers/actions/wipe-device/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Enable Lost Mode

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/enable-lost-mode/](https://www.hexnode.com/mobile-device-management/developers/actions/enable-lost-mode/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |
| message | String | Optional. Add a message to display on the device screen. | Optional |
| phone_number | String | Optional. Add a phone number. | Optional |
| footnote | String | Optional. Add a footnote to be displayed on the device. | Optional |

---

## Disable Lost Mode

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/disable-lost-mode/](https://www.hexnode.com/mobile-device-management/developers/actions/disable-lost-mode/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Disenroll Devices

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/disenroll-devices/](https://www.hexnode.com/mobile-device-management/developers/actions/disenroll-devices/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Install Application

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/install-application/](https://www.hexnode.com/mobile-device-management/developers/actions/install-application/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| apps | Array | Required. IDs of the apps to be installed | Yes |
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Uninstall Applications

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/uninstall-applications/](https://www.hexnode.com/mobile-device-management/developers/actions/uninstall-applications/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| apps | Array | IDs of the apps to be removed | Optional |
| user | Array | IDs of the users | Optional |
| usergroup | Array | IDs of the user groups | Optional |
| device | Array | IDs of the devices | Optional |
| devicegroup | Array | IDs of the device groups | Optional |

---

## Enable Kiosk

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/enable-kiosk/](https://www.hexnode.com/mobile-device-management/developers/actions/enable-kiosk/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Associate policy

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/associate-policy/](https://www.hexnode.com/mobile-device-management/developers/actions/associate-policy/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| policies | Array | Required. IDs of the policy | Yes |
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Remove Policy

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/remove-policy/](https://www.hexnode.com/mobile-device-management/developers/actions/remove-policy/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| policies | Array | Required. IDs of the policy | Yes |
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Mark as disenrolled

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/mark-as-disenrolled/](https://www.hexnode.com/mobile-device-management/developers/actions/mark-as-disenrolled/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Set Friendly Name

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/set-friendly-name/](https://www.hexnode.com/mobile-device-management/developers/actions/set-friendly-name/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| set_collective_name | Boolean type | Not mandatory. | Optional |

---

## Change Device Ownership

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/change-device-ownership/](https://www.hexnode.com/mobile-device-management/developers/actions/change-device-ownership/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| devices | Array | Required. IDs of the devices | Yes |
| devicegroups | Array | Required. IDs of the devicegroups | Yes |
| ownership | Integer | Required.Specify the ownership of the devices. Choose1 for Personaland2 for Corporate. | Yes |

---

## Broadcast Message

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/broadcast-message/](https://www.hexnode.com/mobile-device-management/developers/actions/broadcast-message/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | IDs of the users | Optional |
| usergroups | Array | IDs of the user groups | Optional |
| devices | Array | IDs of the devices | Optional |
| devicegroups | Array | IDs of the device groups | Optional |

---

## Edit Device Attribute

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/edit-device-attribute/](https://www.hexnode.com/mobile-device-management/developers/actions/edit-device-attribute/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| Update_in_bulk | Boolean type | Update attributes of devices in bulk. | Optional |
| Update_single_device | Boolean type | Update attributes of a single device. | Optional |
| Device_ID | Array | Mandatory.Specify the list of device IDs. | Optional |
| Device_name | Character | Optional.Specify the device name of the devices. | Optional |
| Asset_Tag | Character | Optional.Specify the asset tag of the devices. | Optional |
| Department | Character | Optional.Specify the department of the devices. | Optional |
| Device_Notes | Character | Optional.Specify the device notes to be added to the devices. | Optional |
| Description | Character | Optional.Specify the description of the devices. | Optional |
| Ownership | Integer | Optional.Specify the ownership of the devices. Choose1 for Personaland2 for Corporate. | Optional |
| Device_name_append_number | Boolean | Optional.If set true, append number is added to device name. | Optional |
| Asset_tag_append_number | Boolean | Optional.If set true, append number is added to asset tag. | Optional |
| Department_append_number | Boolean | Optional.If set true, append number is added to department. | Optional |
| Asset_tag_starting_number | Integer | Mandatory whenAsset_tag_append_numberis set true.Specify the starting number. | Optional |
| Department_starting_number | Integer | Mandatory whenDepatment_append_numberis set true.Specify the starting number. | Optional |
| Device_name_starting_number | Integer | Mandatory whenDevice_name_append_numberis set true.Specify the starting number. | Optional |
| Use_suffix_for_DeviceNotes | Boolean | Optional.If set true, suffix will be added to device notes. | Optional |
| Use_suffix_for_Description | Boolean | Optional.If set true, suffix will be added to description. | Optional |
| Suffix_devicenotes | Integer | Mandatory whenUse_suffix_for_DeviceNotesis set to true.Specify the starting number of the suffix. | Optional |
| Suffix_description | Integer | Mandatory whenUse_suffix_for_Descriptionis set to true.Specify the starting number of the suffix. | Optional |
| deviceID | Integer | Mandatory.Specify the Device ID of the device. | Optional |
| device_name | Character | Optional.Specify the device name of the device. | Optional |
| asset_tag | Character | Optional.Specify the asset tag of the device. | Optional |
| department | Character | Optional.Specify the department of the device. | Optional |
| device_notes | Character | Optional.Specify the device notes to be added to the device. | Optional |
| description | Character | Optional.Specify the description of the device. | Optional |
| ownership | Integer | Optional.Specify the ownership of the device. Choose1 for Personaland2 for Corporate. | Optional |

---

## Clear App Data

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/clear-app-data/](https://www.hexnode.com/mobile-device-management/developers/actions/clear-app-data/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |
| apps | Array | Required. IDs of the apps for which the data needs to be cleared. | Yes |

---

## Sync Local Accounts

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/sync-local-accounts/](https://www.hexnode.com/mobile-device-management/developers/actions/sync-local-accounts/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |

---

## Set Password

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/set-password/](https://www.hexnode.com/mobile-device-management/developers/actions/set-password/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |
| password | String | Required. Specify the password for Android device enrolled in Android Enterprise Program. | Yes |

---

## Rename Device

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/rename-device/](https://www.hexnode.com/mobile-device-management/developers/actions/rename-device/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |
| name | Char | Mandatory. The same name is given for all the selected devices. | Optional |
| use_suffix | Boolean type | Not mandatory. Check whether suffix is needed. | Optional |
| suffix | Integer | Mandatory when use_suffix=true. Starting number of the suffix. | Optional |

---

## Remote Ring

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/remote-ring/](https://www.hexnode.com/mobile-device-management/developers/actions/remote-ring/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |
| message | String | Optional. Sample message. | Optional |

---

## Clear Activation Lock

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/clear-activation-lock/](https://www.hexnode.com/mobile-device-management/developers/actions/clear-activation-lock/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |

---

## Request Application Feedback

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/request-application-feedback/](https://www.hexnode.com/mobile-device-management/developers/actions/request-application-feedback/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |

---

## Enable Personal Hotspot

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/enable-personal-hotspot/](https://www.hexnode.com/mobile-device-management/developers/actions/enable-personal-hotspot/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |

---

## Disable Personal Hotspot

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/disable-personal-hotspot/](https://www.hexnode.com/mobile-device-management/developers/actions/disable-personal-hotspot/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |

---

## Join AD Domain

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/join-ad-domain/](https://www.hexnode.com/mobile-device-management/developers/actions/join-ad-domain/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| domain | String | Required. Name of the domain to be linked. | Yes |
| server | String | Required. Specify the full name of the domain controller that hosts the domain. | Yes |
| username | String | Required. Enter the username of the corresponding user’s AD login credentials. | Yes |
| password | String | Optional. Enter the password of the corresponding user’s AD login credentials. | Optional |
| restart | Boolean | If true == Restarts the device,If false == Doesn’t restart the device. | Optional |
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |

---

## Unjoin AD Domain

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/unjoin-ad-domain/](https://www.hexnode.com/mobile-device-management/developers/actions/unjoin-ad-domain/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| username | String | Required. Enter the username of the corresponding user’s AD login credentials | Yes |
| password | String | Optional. Enter the password of the corresponding user’s AD login credentials. | Optional |
| restart | Boolean | If true == Restarts the device,If false == Doesn’t restart the device. | Optional |
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |

---

## Hexnode App Logs

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/hexnode-app-logs/](https://www.hexnode.com/mobile-device-management/developers/actions/hexnode-app-logs/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users. | Optional |
| usergroups | Array | Optional. IDs of the user groups. | Optional |
| devices | Array | Optional. IDs of the devices. | Optional |
| devicegroups | Array | Optional. IDs of the device groups. | Optional |

---

## Add to device group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/add-to-device-group/](https://www.hexnode.com/mobile-device-management/developers/actions/add-to-device-group/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| devices | Array | Required. IDs of the devices. | Yes |
| devicegroups | Array | Required. IDs of the device groups. | Yes |

---

## Add To User Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/add-to-user-group/](https://www.hexnode.com/mobile-device-management/developers/actions/add-to-user-group/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Required. IDs of the users. | Yes |
| usergroups | Array | Required. IDs of the user groups. | Yes |

---

## Delete Device

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/delete-device/](https://www.hexnode.com/mobile-device-management/developers/actions/delete-device/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| devices | Array | Required. IDs of the devices. | Yes |

---

## Delete User

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/delete-user/](https://www.hexnode.com/mobile-device-management/developers/actions/delete-user/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Required. IDs of the users. | Yes |

---

## Deploy Files

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/file-deployment-via-api/](https://www.hexnode.com/mobile-device-management/developers/actions/file-deployment-via-api/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| file_ids | Array | IDs of the files to deploy (must be active and exist) | Optional |
| file_path | String | Destination path on the device (leading / added if missing) | Optional |
| users | Array | IDs of the users | Optional |
| usergroups | Array | IDs of the user groups | Optional |
| devices | Array | IDs of the devices | Optional |
| devicegroups | Array | IDs of the device groups | Optional |

---

## Remove files

**Source:** [https://www.hexnode.com/mobile-device-management/developers/actions/api-to-remove-files/](https://www.hexnode.com/mobile-device-management/developers/actions/api-to-remove-files/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| file_paths | Array | Destination path or path/filename to be removed | Optional |
| users | Array | IDs of the users | Optional |
| usergroups | Array | IDs of the user groups | Optional |
| devices | Array | IDs of the devices | Optional |
| devicegroups | Array | IDs of the device groups | Optional |

---

# App Catalogs

**Total endpoints:** 6

## List App Catalogs

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-catalogs/list-app-catalogs/](https://www.hexnode.com/mobile-device-management/developers/app-catalogs/list-app-catalogs/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| order_by | String | Optional. Order the result by app catalog name. Useascordesc | Optional |
| page | Integer | Optional | Optional |
| per_page | Integer | Optional | Optional |

---

## Create a Catalog

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-catalogs/create-a-catalog/](https://www.hexnode.com/mobile-device-management/developers/app-catalogs/create-a-catalog/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| name | String | Required. Name of the app catalog | Yes |
| description | String | Optional | Optional |
| apps | Integer array | Optional. The applications IDs | Optional |
| app_groups | Integer array | Optional. The App group IDs | Optional |

---

## Retrieve App Catalog Details

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-catalogs/retrieve-app-catalog-details/](https://www.hexnode.com/mobile-device-management/developers/app-catalogs/retrieve-app-catalog-details/)

Category Filter

---

## Update App Catalogs

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-catalogs/update-app-catalogs/](https://www.hexnode.com/mobile-device-management/developers/app-catalogs/update-app-catalogs/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| name | String | Required. Name of the app group | Yes |
| description | String | Required. Description for the group | Yes |
| apps | Integer array | Optional. IDs of the applications | Optional |
| app_groups | Integer array | Optional. IDs of the app group | Optional |

---

## Add/Remove Apps

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-catalogs/add-remove-apps/](https://www.hexnode.com/mobile-device-management/developers/app-catalogs/add-remove-apps/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| add_apps | Integer array | Required. An array of app IDs | Yes |
| remove_apps | Integer array | Required. An array of app IDs | Yes |
| add_groups | Integer array | Required. An array of app group IDs | Yes |
| remove_groups | Integer array | Required. An array of app group IDs | Yes |

---

## Delete App Catalog

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-catalogs/delete-app-catalog/](https://www.hexnode.com/mobile-device-management/developers/app-catalogs/delete-app-catalog/)

Category Filter

---

# App Groups

**Total endpoints:** 6

## List App Groups

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-groups/list-app-groups/](https://www.hexnode.com/mobile-device-management/developers/app-groups/list-app-groups/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| order_by | String | Optional. Order the result by app group name. Useascordesc | Optional |
| page | Integer | Optional | Optional |
| per_page | Integer | Optional | Optional |

---

## Create App Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-groups/create-app-group/](https://www.hexnode.com/mobile-device-management/developers/app-groups/create-app-group/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| name | String | Required. Name of the app group | Yes |
| description | String | Optional | Optional |
| apps | Array | Optional. IDs of the applications | Optional |

---

## Retrieve App Group Details

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-groups/retrieve-app-group-details/](https://www.hexnode.com/mobile-device-management/developers/app-groups/retrieve-app-group-details/)

Category Filter

---

## Update App Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-groups/update-app-group/](https://www.hexnode.com/mobile-device-management/developers/app-groups/update-app-group/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| name | String | Required. Name of the app group | Yes |
| description | String | Required. Description for the group | Yes |
| apps | Integer array | Optional. IDs of the app | Optional |

---

## Add/Remove Apps

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-groups/add-remove-apps/](https://www.hexnode.com/mobile-device-management/developers/app-groups/add-remove-apps/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| add_apps | Integer array | Required. An array of app IDs | Yes |
| remove_apps | Integer array | Required. An array of app IDs | Yes |

---

## Delete App Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/app-groups/delete-app-group/](https://www.hexnode.com/mobile-device-management/developers/app-groups/delete-app-group/)

Category Filter

---

# Applications

**Total endpoints:** 6

## List All Apps

**Source:** [https://www.hexnode.com/mobile-device-management/developers/applications/list-all-apps/](https://www.hexnode.com/mobile-device-management/developers/applications/list-all-apps/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| order_by | String | Optional. Order the result by application name. Useascordesc | Optional |
| app_type | String | Optional. Values can bestore,weborenterprise | Optional |
| platform | String | Optional. Values can beiosorandroid | Optional |
| page | Integer | Optional | Optional |
| per_page | Integer | Optional. Themaximum valueis250 | Optional |

---

## Search App

**Source:** [https://www.hexnode.com/mobile-device-management/developers/applications/search-app/](https://www.hexnode.com/mobile-device-management/developers/applications/search-app/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| keyword | String | Required. Name of the app to be searched | Yes |
| platform | String | Required. Useiosfor App Store app search andandroidfor Play Store app search | Yes |
| country | String | Optional. ISO alpha-2 country code. For example, us,ca | Optional |

---

## Add App to List

**Source:** [https://www.hexnode.com/mobile-device-management/developers/applications/add-app-to-list/](https://www.hexnode.com/mobile-device-management/developers/applications/add-app-to-list/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| name | String | Required. Name of the app | Yes |
| app_type | String | Required. Usestoreorweb | Yes |
| platform | String | Required. Useiosfor App Store app search andandroidfor Play Store app search | Yes |
| price | String | Optional. For example, $5 | Optional |
| category | String | Required. Category for the app. For example, entertainment | Yes |
| vendor | String | Optional | Optional |
| icon | String | Required. URL or base64 encoded data of the icon | Yes |
| average_user_rating | String | Optional. For example, rating 3 out of 5 | Optional |
| content_rating | String | Optional | Optional |
| remove_with_mdm | Boolean | Optional | Optional |
| prevent_backup | Boolean | Optional | Optional |
| identifier | String | Required. Identifier of the app. For example, com.hexnode.hexnodeMDM | Yes |
| appstore_id | Integer | Required. App Store ID of the app | Yes |
| version | String | Required. The version of the app | Yes |
| bundle_size | Float | Required. The size of the app | Yes |
| description | String | Required. Values can be null | Yes |
| primaryGenreId | Integer | Required. Value can be null | Yes |
| appstore_ulr | Integer | Required. URL for the app in the App Store | Yes |
| identifier | String | Required. Identifier of the app | Yes |
| version | String | Optional. The version of the app | Optional |
| bundle_size | Float | Optional. Size of the app | Optional |
| webapp_url | String | Required. URL for the web app | Yes |

---

## Retrieve App Details

**Source:** [https://www.hexnode.com/mobile-device-management/developers/applications/retrieve-app-details/](https://www.hexnode.com/mobile-device-management/developers/applications/retrieve-app-details/)

Category Filter

---

## Update Web App

**Source:** [https://www.hexnode.com/mobile-device-management/developers/applications/update-web-app/](https://www.hexnode.com/mobile-device-management/developers/applications/update-web-app/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| name | String | Required. Name of the app. | Yes |
| app_type | String | Required. Useweb. | Yes |
| webapp_url | String | Required. URL for the web app. | Yes |
| category | String | Required. Category for the app. For example, entertainment | Yes |
| icon | String | Required. URL or base64 encoded data of the icon | Yes |

---

## Remove App

**Source:** [https://www.hexnode.com/mobile-device-management/developers/applications/remove-app/](https://www.hexnode.com/mobile-device-management/developers/applications/remove-app/)

Category Filter

---

# Automations

**Total endpoints:** 2

## List all Automations

**Source:** [https://www.hexnode.com/mobile-device-management/developers/automations/api-to-list-automations/](https://www.hexnode.com/mobile-device-management/developers/automations/api-to-list-automations/)

Category Filter

---

## Initiate Automation

**Source:** [https://www.hexnode.com/mobile-device-management/developers/automations/initiate-automation-via-api/](https://www.hexnode.com/mobile-device-management/developers/automations/initiate-automation-via-api/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| automationList | Array | A list of identifiers for the automation profiles you wish to run (e.g., [1, 2, 3, 4]). These IDs de | Optional |
| applyFilter | Boolean | A boolean value (true or false) that determines whether the system should cross-check and filter the | Optional |
| targets | Dictionary | Defines the scope of the deployment. See the target parameters below. | Optional |
| devices | Array | A list of unique IDs for individual devices (e.g., [1, 2, 3, 4]). | Optional |
| deviceGroups | Array | A list of IDs for specific device groups (e.g., [1, 2, 3, 4]). | Optional |
| users | Array | A list of unique IDs for individual users (e.g., [1, 2, 3, 4]). | Optional |
| userGroups | Array | A list of IDs for specific user groups (e.g., [1, 2, 3, 4]). | Optional |
| domains | Array | A list of IDs for managed network domains (e.g., [1, 2, 3, 4]). | Optional |
| ou | Array | A list of IDs for Organizational Units (OUs) (e.g., [1, 2, 3, 4]). | Optional |

---

# Content Management

**Total endpoints:** 3

## Generate pre-signed upload URL

**Source:** [https://www.hexnode.com/mobile-device-management/developers/content-management/api-to-generate-pre-signed-upload-url/](https://www.hexnode.com/mobile-device-management/developers/content-management/api-to-generate-pre-signed-upload-url/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| file_name | String | Name of the file with extension (e.g., report.pdf) | Optional |
| content_type | String | Optional MIME type; defaults to application/octet-stream | Optional |

---

## Verify file upload to Amazon S3

**Source:** [https://www.hexnode.com/mobile-device-management/developers/content-management/api-to-verify-file-upload/](https://www.hexnode.com/mobile-device-management/developers/content-management/api-to-verify-file-upload/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| file_uuid | String | The UUID returned from the generate-presigned-upload-url endpoint | Optional |

---

## Delete files from Amazon S3

**Source:** [https://www.hexnode.com/mobile-device-management/developers/content-management/api-to-delete-files-from-amazon-s3/](https://www.hexnode.com/mobile-device-management/developers/content-management/api-to-delete-files-from-amazon-s3/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| file_ids | Array | IDs of the files to be permanently deleted from the catalog | Optional |

---

# Device Groups

**Total endpoints:** 6

## List Device Groups

**Source:** [https://www.hexnode.com/mobile-device-management/developers/device-groups/list-device-groups/](https://www.hexnode.com/mobile-device-management/developers/device-groups/list-device-groups/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | Integer | Optional | Optional |
|  | Integer | Optional | Optional |

---

## Create Device Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/device-groups/create-device-group/](https://www.hexnode.com/mobile-device-management/developers/device-groups/create-device-group/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | String | Required. Name of the device group | Yes |
|  | String | Required. Description for the group | Yes |
|  | Integer array | Optional. Array of enrolled device IDs | Optional |

---

## Retrieve Device Group Details

**Source:** [https://www.hexnode.com/mobile-device-management/developers/device-groups/retrieve-device-group-details/](https://www.hexnode.com/mobile-device-management/developers/device-groups/retrieve-device-group-details/)

Category Filter

---

## Update Device Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/device-groups/update-device-group/](https://www.hexnode.com/mobile-device-management/developers/device-groups/update-device-group/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | String | Required. Name of the device group | Yes |
|  | String | Required. Description for the group | Yes |
|  | Integer array | Optional. IDs of the devices | Optional |

---

## Add/Remove Devices

**Source:** [https://www.hexnode.com/mobile-device-management/developers/device-groups/add-remove-devices/](https://www.hexnode.com/mobile-device-management/developers/device-groups/add-remove-devices/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | String | Required. An array of device IDs of enrolled devices | Yes |
|  | Integer array | Required. An array of device IDs of enrolled devices | Yes |

---

## Delete Device Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/device-groups/delete-device-group/](https://www.hexnode.com/mobile-device-management/developers/device-groups/delete-device-group/)

Category Filter

---

# Devices

**Total endpoints:** 6

## List All Devices

**Source:** [https://www.hexnode.com/mobile-device-management/developers/devices/list-all-devices/](https://www.hexnode.com/mobile-device-management/developers/devices/list-all-devices/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | String | Optional. Order the result by device name. Useascordesc | Optional |
|  | String | Optional. Filter by OS. Useios,androidorwindows | Optional |
|  | Boolean | Optional. Filter by active or inactive devices. UseTrueorFalse | Optional |
|  | String | Optional. Usesmartphoneortablet | Optional |
|  | Integer | Optional | Optional |
|  | Integer | Optional. Themaximum valueis250 | Optional |

---

## Retrieve Device Details

**Source:** [https://www.hexnode.com/mobile-device-management/developers/devices/retrieve-device-details/](https://www.hexnode.com/mobile-device-management/developers/devices/retrieve-device-details/)

Category Filter

---

## List Device Policies

**Source:** [https://www.hexnode.com/mobile-device-management/developers/devices/list-device-policies/](https://www.hexnode.com/mobile-device-management/developers/devices/list-device-policies/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | Integer | Optional | Optional |
|  | Integer | Optional | Optional |

---

## List All Applications

**Source:** [https://www.hexnode.com/mobile-device-management/developers/devices/list-all-applications/](https://www.hexnode.com/mobile-device-management/developers/devices/list-all-applications/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | Integer | Optional | Optional |
|  | Integer | Optional. Themaximum valueis250 | Optional |

---

## List Device Locations

**Source:** [https://www.hexnode.com/mobile-device-management/developers/devices/list-device-locations/](https://www.hexnode.com/mobile-device-management/developers/devices/list-device-locations/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | Integer | Optional | Optional |
|  | Integer | Optional | Optional |

---

## Action Status

**Source:** [https://www.hexnode.com/mobile-device-management/developers/devices/action-status/](https://www.hexnode.com/mobile-device-management/developers/devices/action-status/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | Integer | Optional | Optional |
|  | Integer | Optional | Optional |

---

# General

**Total endpoints:** 5

## Developers

**Source:** [https://www.hexnode.com/mobile-device-management/developers/](https://www.hexnode.com/mobile-device-management/developers/)

Category Filter

---

## Disable Kiosk

**Source:** [https://www.hexnode.com/mobile-device-management/developers/disable-kiosk/](https://www.hexnode.com/mobile-device-management/developers/disable-kiosk/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Power-Off Device

**Source:** [https://www.hexnode.com/mobile-device-management/developers/power-off-device/](https://www.hexnode.com/mobile-device-management/developers/power-off-device/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Restart Device

**Source:** [https://www.hexnode.com/mobile-device-management/developers/restart-device/](https://www.hexnode.com/mobile-device-management/developers/restart-device/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| users | Array | Optional. IDs of the users | Optional |
| usergroups | Array | Optional. IDs of the user groups | Optional |
| devices | Array | Optional. IDs of the devices | Optional |
| devicegroups | Array | Optional. IDs of the device groups | Optional |

---

## Developers

**Source:** [https://www.hexnode.com/mobile-device-management/developers/?_gl=1%2A1fqfuuu%2A_ga%2AMTQ4NzgwOTc2OS4xNzcxMzIwMjQy%2A_ga_3EGK3S7FRS%2AczE3NzEzOTgzMTUkbzQkZzEkdDE3NzEzOTgzNjUkajEwJGwwJGgw%2A_gcl_au%2AOTkzNjA3MTEyLjE3NzEzMjAyNDA.](https://www.hexnode.com/mobile-device-management/developers/?_gl=1%2A1fqfuuu%2A_ga%2AMTQ4NzgwOTc2OS4xNzcxMzIwMjQy%2A_ga_3EGK3S7FRS%2AczE3NzEzOTgzMTUkbzQkZzEkdDE3NzEzOTgzNjUkajEwJGwwJGgw%2A_gcl_au%2AOTkzNjA3MTEyLjE3NzEzMjAyNDA.)

Category Filter

---

# Organizational Units

**Total endpoints:** 1

## List all Organizational Units

**Source:** [https://www.hexnode.com/mobile-device-management/developers/organizational-units/api-to-list-all-organizational-units/](https://www.hexnode.com/mobile-device-management/developers/organizational-units/api-to-list-all-organizational-units/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| domain_id | Integer | The unique identifier of the domain from which to fetch the Organizational Units. (Passed as a query | Optional |

---

# Policies

**Total endpoints:** 9

## List Policies

**Source:** [https://www.hexnode.com/mobile-device-management/developers/policies/list-policies/](https://www.hexnode.com/mobile-device-management/developers/policies/list-policies/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| page | Integer | Optional | Optional |
| per_page | Integer | Optional | Optional |

---

## Create Policy

**Source:** [https://www.hexnode.com/mobile-device-management/developers/policies/create-policy/](https://www.hexnode.com/mobile-device-management/developers/policies/create-policy/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | String | Name of the policy | Optional |
|  | String | Description of the policy | Optional |
|  | Dictionary | Optional. If provided this dictionary, provide the following keys:password,restrictions,advanced_res | Optional |
|  | Dictionary | Optional. If provided this dictionary, provide the following keys:password,restrictions,wifi,email,a | Optional |
|  | Dictionary | Optional. Dictionary for general_settings currently contains only alocation_settingskey. Its value i | Optional |
|  | Boolean |  | Optional |
|  | Integer |  | Optional |

---

## iOS Policies

**Source:** [https://www.hexnode.com/mobile-device-management/developers/policies/ios-policies/](https://www.hexnode.com/mobile-device-management/developers/policies/ios-policies/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| allow_simple | Boolean | Optional | Optional |
| require_alphanumeric | Boolean | Optional | Optional |
| min_length | Integer | Optional. Values can be from 1 to 16 | Optional |
| min_complex_char | Integer | Optional. Values can be from 1 to 4 | Optional |
| max_pinage_in_days | Integer | Optional. Specifies the number of days for which the passcode can remain unchanged | Optional |
| max_inactivity | Integer | Optional. This dictionary contains email configurations | Optional |
| pin_history | Dictionary | Optional. When the user changes the passcode, it has to be unique within the last N entries in the h | Optional |
| max_grace_period | Integer | Optional. The maximum grace period (in minutes) to unlock the phone without entering a passcode.Supp | Optional |
| max_failed_attempts | Integer | Optional. Specifies the number of allowed failed attempts to enter the passcode on the device’s lock | Optional |
| allow_app_installation | Boolean | Optional | Optional |
| allow_airdrop_managemendapps | Boolean | Optional | Optional |
| allow_camera | Boolean | Optional | Optional |
| allow_video_conferencing | Boolean | Optional | Optional |
| allow_screen_shot | Boolean | Optional | Optional |
| allow_global_background_fetch_when_roaming | Boolean | Optional | Optional |
| allow_touchId | Boolean | Optional | Optional |
| allow_assistant | Boolean | Optional | Optional |
| allow_assistant_while_locked | Boolean | Optional | Optional |
| allow_voice_dialing | Boolean | Optional | Optional |
| allow_passbook_while_locked | Boolean | Optional | Optional |
| allow_inapp_purchases | Boolean | Optional | Optional |
| force_itunes_store_password_entry | Boolean | Optional | Optional |
| allow_multiplayer_gaming | Boolean | Optional | Optional |
| allow_adding_game_center_friends | Boolean | Optional | Optional |
| allow_enterprise_app_trust | Boolean | Optional | Optional |
| allow_enterprise_app_trust_modification | Boolean | Optional | Optional |
| allow_enterprise_book_backup | Boolean | Optional | Optional |
| allow_managed_app_sync | Boolean | Optional | Optional |
| allow_youtube | Boolean | Optional | Optional |
| allow_itunes | Boolean | Optional | Optional |
| allow_safari | Boolean | Optional | Optional |
| safari_allow_auto_fill | Boolean | Optional | Optional |
| safari_force_fraud_warning | Boolean | Optional | Optional |
| safari_allow_java_script | Boolean | Optional | Optional |
| safari_allow_popups | Boolean | Optional | Optional |
| safari_accept_cookies | String | Optional. Values can bealways,visitedornever | Optional |
| allow_cloud_backup | Boolean | Optional | Optional |
| allow_cloud_document_sync | Boolean | Optional | Optional |
| allow_photo_stream | Boolean | Optional | Optional |
| allow_shared_stream | Boolean | Optional | Optional |
| allow_icloud_photo | Boolean | Optional | Optional |
| allow_lockscreen_notify | Boolean | Optional | Optional |
| allow_lockscreen_todayView | Boolean | Optional | Optional |
| allow_lockscreen_control | Boolean | Optional | Optional |
| allow_ota_pki_update | Boolean | Optional | Optional |
| limit_ad_tracking | Boolean | Optional | Optional |
| allow_diagnostic_submission | Boolean | Optional | Optional |
| allow_untrusted_tls_prompt | Boolean | Optional | Optional |
| force_encrypted_backup | Boolean | Optional | Optional |
| force_applewatch_Detection | Boolean | Optional | Optional |
| allow_explicit_content | Boolean | Optional | Optional |
| allow_bookstore_erotica | Boolean | Optional | Optional |
| rating_region | String | Optional. Values can beus,au,ca,de,fr,ie,jp,nzorgb | Optional |
| rating_movies | String | Optional. Values can beallow,nc-17,r,pg-13,pg,gornever | Optional |
| rating_tv_shows | String | Optional. Values can beallow,tv-ma,tv-14,tv-pg,tv-g,tv-y7,tv-yornever | Optional |
| rating_apps | String | Values can beallow,17+,12+,9+,4+,never | Optional |
| allow_airdrop | Boolean | Optional | Optional |
| allow_app_cellular_data_modification | Boolean | Optional | Optional |
| allow_app_removal | Boolean | Optional | Optional |
| allow_bookstore | Boolean | Optional | Optional |
| allow_touchId_modify | Boolean | Optional | Optional |
| allow_chat | Boolean | Optional | Optional |
| allow_game_center | Boolean | Optional | Optional |
| allow_host_pairing | Boolean | Optional | Optional |
| allow_ui_configuration_profile_installation | Boolean | Optional | Optional |
| allow_podcasts | Boolean | Optional | Optional |
| allow_definition_lookup | Boolean | Optional | Optional |
| allow_predictive_keyboard | Boolean | Optional | Optional |
| allow_auto_correction | Boolean | Optional | Optional |
| allow_spell_check | Boolean | Optional | Optional |
| allow_music_service | Boolean | Optional | Optional |
| allow_radio_service | Boolean | Optional | Optional |
| allow_news | Boolean | Optional | Optional |
| allow_ui_app_installation | Boolean | Optional | Optional |
| allow_keyboard_shortcuts | Boolean | Optional | Optional |
| allow_paired_watch | Boolean | Optional | Optional |
| allow_account_modification | Boolean | Optional | Optional |
| allow_erase_content_and_settings | Boolean | Optional | Optional |
| allow_assistant_user_generated_content | Boolean | Optional | Optional |
| allow_find_my_friends_modification | Boolean | Optional | Optional |
| force_assistant_profanity_filter | Boolean | Optional | Optional |
| allow_spotlight_internet_results | Boolean | Optional | Optional |
| allow_enabling_restrictions | Boolean | Optional | Optional |
| allow_passcode_modification | Boolean | Optional | Optional |
| allow_device_name_modification | Boolean | Optional | Optional |
| allow_wallpaper_modification | Boolean | Optional | Optional |
| allow_notifications_modification | Boolean | Optional | Optional |
| Allow_automatic_app_downloads | Boolean | Optional | Optional |
| autonomous_single_apps | Integer array | Optional. Can contain IDs of the iOS apps | Optional |
| filter_type | String | Required. Values can be white_list or black_list | Yes |
| auto_filter_enabled | Boolean | Optional. Use only when filter_type is black_list | Optional |
| permitted_urls | String array | Optional. Used only when auto_filter_enabled is true. Otherwise, this field is ignored | Optional |
| blacklisted_urls | String array | Optional. Array of URLs. Use only when filter_type is black_list. Otherwise, this field is ignored | Optional |
| whitelist_urls | String array | Optional. Array of URLs. Use only when filter_type is white_list. Otherwise, this field is ignored | Optional |
| service_set_identifier | String |  | Optional |
| autojoin | Boolean |  | Optional |
| hidden_network | Boolean |  | Optional |
| security_type | String |  | Optional |
| proxy_type | String |  | Optional |
| password | String |  | Optional |
| user_name | String | Required | Yes |
| user_password | String | Required if use_per_connection_pwd is set to false | Yes |
| use_per_connection_pwd | Boolean | Optional | Optional |
| tls | Boolean | Optional | Optional |
| leap | Boolean | Optional | Optional |
| ttls | Boolean | Optional | Optional |
| peap | Boolean | Optional | Optional |
| eap_fast | Boolean | Optional | Optional |
| eap_sim | Boolean | Optional | Optional |
| provision_pac | Boolean | Optional | Optional |
| provision_pac_anonymously | Boolean | Optional | Optional |
| use_pac | Boolean | Optional | Optional |
| inner_authentication | String | Optional. The possible values arePAP,CHAP,MSCHAP,MSCHAPv2 | Optional |
| outer_identity | String | Optional. | Optional |
| proxyserver | String | Required. The proxy server’s network address | Yes |
| proxy_server_port | Integer | Required. The proxy server’s port | Yes |
| proxy_user_name | String | Required. Username used to authenticate the proxy server | Yes |
| proxy_password | String | Required. Password used to authenticate proxyserver | Yes |
| proxy_pac_url | String | Required. The URL of the PAC file that defines the proxy configuration | Yes |
| account_description | String | Required. User visible description of the email account | Yes |
| user_display_name | String | Required. Username of the account. Use%name%for user’s name | Yes |
| account_type | String | Required. The possible values arePOPandIMAP | Yes |
| imap_path_prefix | String | Optional. Required ifaccount_typeis set toIMAP | Yes |
| email_address | String | Required. The email address for the account. Use%email%for user’s email | Yes |
| allow_move | Boolean | Required. The email address for the account. Use%email%for user’s email | Yes |
| incoming_server_host_name | String | Required. The email address for the account. Use%email%for user’s email | Yes |
| incoming_server_port | Integer | Required. The email address for the account. Use%email%for user’s email | Yes |
| incoming_server_username | String | Required. Use%username%for username | Yes |
| incoming_server_auth | String | Required. Possible values areNone,Password,MD5,NTLMandHTTP | Yes |
| incoming_password | String | Required ifincoming_server_authis notNone | Yes |
| incoming_server_use_ssl | Boolean | Optional | Optional |
| out_server_host_name | String | Required. Outgoing mail server host name | Yes |
| out_server_port | Integer | Required | Yes |
| out_server_username | Integer | Required. Value can benull. Use%username%for username | Yes |
| out_server_auth | String | Required. Possible values areNone,Password,MD5,NTLMandHTTP | Yes |
| out_pwd_as_incoming_pwd | Boolean | Required ifout_server_authis notNone | Yes |
| out_password | String | Required ifout_pwd_as_incoming_pwdis set tofalse | Yes |
| allow_recent_syncing | Boolean | Optional | Optional |
| mail_app_only | Boolean | Optional. Use only in mail | Optional |
| out_server_use_ssl | Boolean | Optional | Optional |
| smime_enabled | Boolean | Optional | Optional |
| account_name | String | Required | Yes |
| host_name | Boolean | Required | Yes |
| allow_move | Boolean | Optional | Optional |
| recent_address_syncing | Boolean | Optional | Optional |
| mail_app_only | Boolean | Optional | Optional |
| use_ssl | Boolean | Optional | Optional |
| smime_enabled | Boolean | Optional | Optional |
| domain | String | Required. Value can be blank. Use%domain%for user’s domain | Yes |
| username | String | Required. Use%username%for username and%email%for user’s email address | Yes |
| email_address | String | Required. Use%email%for user’s email address | Yes |
| password | String | Optional. Value can benull | Optional |
| no_past_days_to_sync | Integer | Optional. Possible values are0,1,3,7,14,31 | Optional |
| cert_compatible_ios4 | Boolean | Optional | Optional |
| account_name | String | Required. Visible description of the LDAP account. Value can be null | Yes |
| host_name | String | Required | Yes |
| username | String | Required. Value can be null | Yes |
| password | String | Required. Value can be null | Yes |
| use_ssl | Boolean | Optional | Optional |
| account_name | String | Required. Visible description of the LDAP account. Value can be null | Yes |
| hostname | String | Required. Host name of the account | Yes |
| username | String | Required. Username of the account. Value can be null | Yes |
| password | String | Required. Password of the account. Value can be null | Yes |
| use_ssl | Boolean | Optional | Optional |
| port | Integer | Optional | Optional |
| principal_url | String | Required. Value can be null | Yes |
| account_name | String | Required. Visible info about the account. Value can be null | Yes |
| url | String | Required | Yes |
| username | String | Required. Value can be null | Yes |
| password | String | Required. Value can be null | Yes |
| use_ssl | Boolean | Optional | Optional |
| account_name | String | Required. Visible description. Value can be null | Yes |
| host_name | String | Required. | Yes |
| username | String | Required. Username of the account. Value can be null | Yes |
| password | String | Required. Value can be null | Yes |
| use_ssl | Boolean | Optional | Optional |
| port | Integer | Optional | Optional |
| principal_url | String | Required. Value can be null | Yes |
| label | String | Required. Name of the webclip | Yes |
| is_removable | Boolean | Optional | Optional |
| url | Boolean | Optional | Optional |
| precomposed_icon | Boolean | Required | Yes |
| fullscreen_icon | Boolean | Optional | Optional |
| icon | String | Required. Base64 encoded image | Yes |
| apn_name | String | Required | Yes |
| apn_username | String | Required. Value can be null | Yes |
| apn_password | String | Required. Value can be null | Yes |
| proxy_server | String | Optional. Value can be null | Optional |
| proxy_server_port | Integer | Optional | Optional |
| app | Integer | Required. App ID | Yes |
| disable_touch | Boolean | Optional | Optional |
| disable_device_rotation | Boolean | Optional | Optional |
| disable_volume_buttons | Boolean | Optional | Optional |
| disable_ringer_switch | Boolean | Optional | Optional |
| disable_sleep_wake_button | Boolean | Optional | Optional |
| disable_auto_lock | Boolean | Optional | Optional |
| enable_voice_over | Boolean | Optional | Optional |
| enable_zoom | Boolean | Optional | Optional |
| enable_invert_colors | Boolean | Optional | Optional |
| enable_assistive_touch | Boolean | Optional | Optional |
| enable_speak_selection | Boolean | Optional | Optional |
| voice_over | Boolean | Optional | Optional |
| zoom | Boolean | Optional | Optional |
| invert_colors | Boolean | Optional | Optional |
| assistive_touch | Boolean | Optional | Optional |
| home_screen_wallpaper | Integer | Required. Base64 encoded image. | Yes |
| lock_screen_wallpaper | Boolean | Required. Base64 encoded image. Value can be null | Yes |
| proxy_type | String | Required. Values can beManual,Auto | Yes |
| proxyserver | String | Required whenproxy_typeis set toManual | Yes |
| proxy_server_port | String | Required whenproxy_typeis set toManual | Yes |
| proxy_user_name | String | Required whenproxy_typeis set toManual. Value can be null | Yes |
| proxy_password | String | Required whenproxy_typeis set toManual. Value can be null | Yes |
| proxy_pac_url | String | Required whenproxy_typeis set toAuto | Yes |
| proxy_pac_fallback_allowed | Boolean |  | Optional |
| proxy_captive_login_allowed | Boolean |  | Optional |
| lock_screen_footnote | String | Required. Value can be null | Yes |
| asset_tag_information | String | Required. Value can be null | Yes |
| whitelist_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| blacklist_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| mandatory_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| catalogues | List / Array | Optional. List of integers representing the corresponding catalogue IDs. | Optional |

---

## Android Policies

**Source:** [https://www.hexnode.com/mobile-device-management/developers/policies/android-policies/](https://www.hexnode.com/mobile-device-management/developers/policies/android-policies/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| passcode_requirement | String | Optional.Possible values can besimple,numbers,alphanumeric,alphabet,complexvalue | Optional |
| min_password_complexity | String | Optional. Possible values can benone,low,medium,high | Optional |
| min_length | Integer | Optional. Possible values are from4 to 16. Ignored ifpasscode_requirementis set tosimpleornumbers | Optional |
| max_pinage_in_days | Integer | Optional. Specifies the number of days for which the passcode can remain unchanged. Minimum value is | Optional |
| max_inactivity | Integer | Optional. Possible values are1,2,3,4,5,10and15 | Optional |
| pin_history | Integer | Optional. Possible values are from1to50 | Optional |
| max_failed_attempts | Integer | Optional. Possible values are from4to10 | Optional |
| min_uppercase_letters | Integer | Optional. Possible values are from1to5 | Optional |
| min_lowercase_letters | Integer | Optional. Possible values are from1to5 | Optional |
| min_non_alphapets | Integer | Optional. Possible values are from1to5 | Optional |
| min_num_letters | Integer | Optional. Possible values are from1to5 | Optional |
| min_symbols | Integer | Optional. Possible values are from1to5 | Optional |
| allow_camera | Boolean | Optional | Optional |
| allow_usb_mass_storage | Boolean | Optional | Optional |
| allow_network_time | Boolean | Optional | Optional |
| allow_wifi | Boolean | Optional | Optional |
| enforce_wifi | Boolean | Optional | Optional |
| allow_bluetooth | Boolean | Optional | Optional |
| allow_data_network | Boolean | Optional | Optional |
| allow_bgdata_sync | Boolean | Optional | Optional |
| allow_auto_background_sync | Boolean | Optional | Optional |
| allow_mobile_app | Boolean | Optional | Optional |
| allow_usb_tethering | Boolean | Optional | Optional |
| allow_mock_locations | Boolean | Optional | Optional |
| allow_wireless_location | Boolean | Optional | Optional |
| allow_gps_location | Boolean | Optional | Optional |
| allow_non_google_app | Boolean | Optional | Optional |
| enforce_app_verification | Boolean | Optional | Optional |
| allow_backup_google | Boolean | Optional | Optional |
| allow_auto_restore | Boolean | Optional | Optional |
| allow_roaming | Boolean | Optional | Optional |
| enforce_device_encrypt | Boolean | Optional | Optional |
| disable_keyguard | Boolean | Optional | Optional |
| allow_password_visible | Boolean | Optional | Optional |
| enforce_gps_location | Boolean | Optional | Optional |
| allow_mdm_removal | Boolean | Optional | Optional |
| service_set_identifier | String | Required | Yes |
| autojoin | Boolean |  | Optional |
| hidden_network | Boolean |  | Optional |
| security_type | String | Required. Possible values arenone,wep,wpa,eap | Yes |
| password | String | Required ifsecurity_typeis set toweporwpa | Yes |
| eap_type | String | Required ifsecurity_typeis set toeap. Possible values arepeap,ttls,pwd | Yes |
| user_name | String | Required ifsecurity_typeis set toeap | Yes |
| enterprise_password | String | Optional. Value can be set to null | Optional |
| phase2_authentication | String | Required ifeap_typeis set topeap. Possible values areNone,PAP,MSCHAP,MSCHAPv2,GTC | Yes |
| outer_identity | String | Required ifeap_typeis set topeap. | Yes |
| account_name | String | Value can be null | Optional |
| account_description | String | Required. Account description | Yes |
| incoming_account_type | String | Optional. Possible values arepop3andimap | Optional |
| email_address | String | Optional. Email address for the account. Value can be set to null | Optional |
| incoming_server_host_name | String | Required | Yes |
| incoming_server_port | Integer | Optional | Optional |
| incoming_server_username | Integer | Optional. Value can be null | Optional |
| incoming_password | String | Optional. Value can be null | Optional |
| incoming_server_use_ssl | Boolean | Optional | Optional |
| incoming_server_use_tls | Boolean | Optional | Optional |
| incoming_server_use_certificate | Boolean | Optional | Optional |
| out_account_type | Boolean | Required. Possible values arepop3andsmtp | Yes |
| out_server_host_name | String | Required | Yes |
| out_server_port | Integer | Optional | Optional |
| out_server_username | String | Optional. Outgoing username for the email. Value can be null | Optional |
| out_password | String | Optional. Password for account authentication. Value can be null | Optional |
| out_server_use_ssl | Boolean | Optional | Optional |
| out_server_use_tls | Boolean | Optional | Optional |
| out_server_use_certificate | Boolean | Optional | Optional |
| account_name | String | Optional. Visible account description | Optional |
| host | String | Required. Exchange ActiveSync Host | Yes |
| domain | String | Optional. Use%domain%as user’s domain. Value can be null | Optional |
| email_address | String | Required. Email address for the account. Use%email%for users’ email address. | Yes |
| username | String | Required. Use%username%for the username | Yes |
| password | String | Optional. Value can be null | Optional |
| no_past_days_to_sync | String | Optional. Possible values areauto,manual,15,30,60,120,240 | Optional |
| use_ssl | Boolean | Optional | Optional |
| apps | Array | Optional. Apps array have dictionaries which contain keysidwhose value is the app ID andhidewhose va | Optional |
| toggle_wifi | Boolean | Optional | Optional |
| allow_wifi | Boolean | Optional | Optional |
| enable_hexnode_browser | Boolean | Optional | Optional |
| auto_launch_app | Integer | Optional. ID of app added in apps. Ignored if apps key is missing | Optional |
| auto_launch_delay | Integer | Optional. Delay in seconds. Ignored if apps key is missing | Optional |
| allow_change_brightness | Boolean | Optional | Optional |
| brightness_level | Integer | Required ifallow_change_brightnessis set tofalse | Yes |
| keep_screen_on | Boolean | Optional | Optional |
| allow_bluetooth | Boolean | Optional | Optional |
| allow_user_location_checkin | Boolean | Optional | Optional |
| kiosk_manual_exit | Boolean | Optional | Optional |
| kiosk_password | String | Optional. If this field is not configured, set to null, or given an empty string (“”), the value spe | Optional |
| exit_passcode_tap_count | Integer | Required ifkiosk_manual_exitis set to true. Specify the number of taps to display the popup to enter | Yes |
| exit_kiosk_with_app_open | Boolean | Optional. Specify if the user can exit manually from kiosk mode while an app is open. | Optional |
| exit_kiosk_after_reboot | Boolean | Optional. Allows exiting kiosk mode during launch delay after a reboot. Users can exit the kiosk mod | Optional |
| relaunch_app | Integer | Required, ifexit_kiosk_after_rebootis set true. Specify the time in seconds after which the app rela | Yes |
| mobile_wallpaper | String | Required. Base64 image | Yes |
| tablet_wallpaper | String | Required. Base64 image | Yes |
| whitelist_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| blacklist_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| mandatory_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| catalogues | List / Array | Optional. List of integers representing the corresponding catalogue IDs. | Optional |

---

## macOS Policies

**Source:** [https://www.hexnode.com/mobile-device-management/developers/policies/macos-policies/](https://www.hexnode.com/mobile-device-management/developers/policies/macos-policies/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| allow_simple | Boolean | Optional. | Optional |
| require_alphanumeric | Boolean | Optional. | Optional |
| change_at_next_auth | Boolean | Optional. The option to enforce password change in the next login. | Optional |
| min_length | Integer | Optional. Values can be from 1 to 16. | Optional |
| min_complex_chars | Integer | Optional. Values can be from 1 to 4. | Optional |
| max_pinage_in_days | Integer | Optional. Values can be from 0 to 730. Specifies the maximum number of days the passcode can be used | Optional |
| max_inactivity | String | Optional.Specifies the maximum period of inactivity before the device locks. Values can be never, 1_ | Optional |
| pin_history | Integer | Optional. Values can be from 0 to 50. | Optional |
| max_grace_period | String | Optional. Values can be none, immediately,1_minute, 5_minutes, 15_minutes, 1_hour, or 4_hours. | Optional |
| service_set_identifier | String | Required. | Yes |
| autojoin | Boolean | Optional. | Optional |
| hidden_network | Boolean | Optional. | Optional |
| security_type | String | Optional. The possible values arenone,WEP,WPA/WPA2,Any*(Personal),WEP_Enterprise,WPA/WPA2_Enterprise | Optional |
| password | String | Required if WEP, WPA/WPA2 or Any*(Personal) is set. | Yes |
| proxy_type | String | Optional. The possible values areNone,ManualorAutomatic. | Optional |
| proxyserver | String | Required when proxy_type is Manual. The proxy server’s network address. | Yes |
| proxy_server_port | Integer | Required when proxy_type is Manual. The proxy server’s port number. | Yes |
| proxy_user_name | String | Required when proxy_type is Manual. Username for proxy authentication. | Yes |
| proxy_password | String | Required when proxy_type is Manual. Password for proxy authentication. | Yes |
| proxy_pac_url | String | Required when proxy_type is Automatic. The URL of the Proxy Auto Configuration (PAC) file. | Yes |
| tls | Boolean | Optional. | Optional |
| leap | Boolean | Optional. | Optional |
| eap_fast | Boolean | Optional. | Optional |
| user_password | String | The user password for authentication. | Optional |
| outer_identity | String | The outer identity for authentication. | Optional |
| inner_authentication | String | Available if eap_fast is enabled. The inner authentication method for EAP. Values can be PAP, CHAP,  | Optional |
| identity_cert_id | String | The ID of the identity certificate for authentication. | Optional |
| provision_pac | Boolean | Available if eap_fast is enabled. | Optional |
| provision_pac_anonymously | Boolean | Available if eap_fast is enabled. | Optional |
| user_name | String | The username for authentication. | Optional |
| ttls | Boolean | Optional. | Optional |
| peap | Boolean | Optional. | Optional |
| eap_sim | Boolean | Optional. | Optional |
| use_per_connection_pwd | Boolean | Optional. | Optional |
| use_pac | Boolean | Optional. | Optional |
| certificate_id | String | Required when machine_authentication is a certificate. | Yes |
| account | String | Optional. The username for the connection. | Optional |
| connection_name | String | Optional. | Optional |
| connection_type | String | Optional. Values can be L2TP, PPTP, IPSec(Cisco), Cisco_AnyConnect, Juniper_SSL, F5_SSL, SonicWALL_M | Optional |
| encryption_level | String | Available when the connection type is PPTP. Values can be None, Automatic, or Maximum(128_bit). | Optional |
| group | String | Specifies group information. Available when the connection type is Cisco_AnyConnect. | Optional |
| identifier | String | Optional. Specifies the identifier for the connection. | Optional |
| include_user_pin | Boolean | Optional. | Optional |
| ipsec_account | String | Optional. The IPSec account information. | Optional |
| ipsec_auth_password | String | Optional. The password for IPSec authentication. | Optional |
| ipsec_certificate_id | String | Optional. The ID of the IPSec certificate. | Optional |
| ipsec_group_name | String | Optional. | Optional |
| ipsec_shared_secret | String | Optional. | Optional |
| l2tp_account | String | Optional. The L2TP account information. | Optional |
| l2tp_password | String | Optional. | Optional |
| l2tp_server | String | Optional. | Optional |
| l2tp_shared_secret | String | Optional. | Optional |
| l2tp_user_authentication | String | The authentication method for an L2TP user. Values can be‘RSA_SecureID’, or ‘Password’. | Optional |
| l2tp_user_authentication_method | Integer | Optional. | Optional |
| login_group | String | Required when the connection type is SONIC_WALL_Mobile_Connect. Specifies the login group informatio | Yes |
| machine_authentication | String | Required when the connection type is IPSec(Cisco). The type of machine authentication. Values can be | Yes |
| password | String | Optional. The password for authentication. | Optional |
| prompt_for_password | String | Optional. | Optional |
| proxy_pac_url | String | Required when proxy_type is Automatic | Yes |
| proxy_password | String | Available when proxy_type is Manual | Optional |
| proxy_server_port | Integer | Required when proxy_type is Manual | Yes |
| proxy_type | String | Values can be ‘None’, ‘Manual’ or ‘Automatic’. | Optional |
| proxy_user_name | String | Available when proxy_type is Manual. Specifies the username for proxy authentication | Optional |
| proxyserver | String | Required when proxy_type is Manual. The server address of proxy. | Yes |
| realm | String | Optional. Specifies the realm information. | Optional |
| remote_address | String | Optional. Specifies the remote address for the connection. | Optional |
| role | String | Optional.Specifies the role information | Optional |
| send_all_traffic | Boolean | Optional. The option to enable sending of all traffic through the connection. | Optional |
| server | String | Optional. Specifies the server information. | Optional |
| use_hybrid_authentication | Boolean | Optional. | Optional |
| user_authentication_type | String | Optional. Values can be ‘password’ or ‘certificate’. | Optional |
| enable_vpn_ondemand | Integer | Optional. | Optional |
| http_enable | Integer | Optional. | Optional |
| https_enable | Integer | Optional. | Optional |
| proxy_autoconfig | String | Optional. | Optional |
| https_proxyserver | String | Optional. Specifies the server address of the HTTPS proxy server. | Optional |
| https_proxy_server_port | Integer | Optional. Specifies the port number of the HTTPS proxy server. | Optional |
| connection_sub_type | String | Optional. | Optional |
| auth_protocol | Boolean | Optional. The option to enable authentication protocol. | Optional |
| auth_plugins | Boolean | Optional. The option to enable authentication plugins. | Optional |
| token_key | Boolean | Optional. | Optional |
| ipsec_auth_enabled | Integer | Optional. | Optional |
| local_identifier_type | String | Optional. | Optional |
| firewall_enabled | String | Optional. Values can be allow_incoming_connections or block_incoming_connections | Optional |
| Enable_Firewall | Boolean | Optional. | Optional |
| Block_AllIncoming | Boolean | Optional. | Optional |
| Enable_StealthMode | Boolean | Optional. | Optional |
| application | Array | Optional. The application details to be included in Firewall. The details should be in the following | Optional |
| preventfromdisabled | Boolean | Optional. The option to prevent users from turning off FileVault encryption on the device. | Optional |
| escrow_recovery_key | Boolean | Optional. The option to encrypt the key with a certificate and escrow it to Hexnode for safekeeping. | Optional |
| preventfromenabled | Boolean | Optional. The option to prevent users from turning on FileVault encryption on the device. | Optional |
| escrow_encryption-key_manual | Boolean | Optional. The possible value is allow_hexnode_to_automatically_to_encrypt_and_decrypt_the_recovery_k | Optional |
| unlock_hibernation | Boolean | Optional.The option to enforce the use of the device password for unlocking FileVault after hibernat | Optional |
| max_bypass_attempt | Integer | Optional. | Optional |
| enable_bypassing | Boolean | Optional. | Optional |
| encryption_type | String | Optional. The possible values are institutional_recovery_key, personal_recovery_key, or institutiona | Optional |
| escrow_local_desc | String | Optional.The description for escrow local. | Optional |
| show_recovery_key | Boolean | Optional. | Optional |
| selected_cert_id | Integer | Optional. | Optional |
| escrow_message | String | Optional. | Optional |
| enable_filevault | Boolean | Optional. | Optional |
| escrow_encrypt_key_cert | String | Optional. | Optional |
| enter_missing_info | Boolean | Optional. | Optional |
| ask_at_logout | Boolean | Optional. The option to define the maximum number of times a user can bypass the prompt to enable Fi | Optional |
| allow_system_user_overrides | Boolean | Optional | Optional |
| allowed_system_teamids | Array | Optional. The team identifiers should be specified within [] | Optional |
| allowed_system_extensions | Object | Optional. The system extensions should be specified within {}. | Optional |
| allowed_system_extension_type | Object | Optional. The system extension types should be specified within {}. | Optional |
| allow_user_overrides | Boolean | Optional | Optional |
| allowed_kernel_extensions | Object | Optional. The kernel extensions should be specified within {}. | Optional |
| allowed_teamids | String | Optional. The team identifiers should be specified within []. | Optional |
| whitelist_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| blacklist_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| mandatory_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| catalogues | List / Array | Optional. List of integers representing the corresponding catalogue IDs. | Optional |

---

## Windows Policies

**Source:** [https://www.hexnode.com/mobile-device-management/developers/policies/windows-policies/](https://www.hexnode.com/mobile-device-management/developers/policies/windows-policies/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| allow_simple | Boolean | Optional. | Optional |
| require_alphanumeric | String | Optional.Values can bealphanumeric,numericoruser_can_choose. | Optional |
| min_length | Integer | Optional. Values can be from 4 to 16. | Optional |
| min_complex_chars | String | Optional. Values can bedigits_only,digits_lower_lettersordigits_lower_upper_letters. | Optional |
| max_pinage_in_days | Integer | Optional. Values can be from0to730. | Optional |
| max_inactivity | Integer | Optional. Values can be from0to999 | Optional |
| pin_history | Integer | Optional. Possible values are from0to24 | Optional |
| max_failed_attempts | Integer | Optional. | Optional |
| service_set_identifier | String | Required | Yes |
| connection_mode | String | Optional. Values can be Auto, Manual. | Optional |
| non_broadcast | Boolean | Optional | Optional |
| security_type | String | Required. Possible values areopen,WEP,WPA-PSK/WPA2-PSK,WPA/WPA2 enterprise | Yes |
| proxy_type | String | Optional. Values can be None and Manual | Optional |
| password | String | Required | Yes |
| authentication | String | Required if WPA-PSK/WPA2-PSK, or WPA/WPA2 enterprise is set. Values can be WPA, WPA2, or open. | Yes |
| eap_type | String | Required ifsecurity_typeis set toWPA/WPA2. Values can bePEAP-MSCHAPv2orEAP TLS | Yes |
| proxyserver | String | Required. The proxy server’s network address. | Yes |
| proxy_server_port | Integer | Required. The proxy server’s port number. | Yes |
| nativeprotocoltype | String | Values can beL2TP,PPTP, orIKEv2. | Optional |
| profilename | String | Required. Specifies the profile name for the VPN connection. | Yes |
| server | String | Required. Specifies the server address for the VPN connection. | Yes |
| advanceconnection | Boolean | Optional | Optional |
| routelist | Array | Required if advanceconnection is true. Specifies the list of routes for the VPN connection. | Yes |
| domainnameinfolist | Array | Required if advanceconnection is true. Specifies the list of domain names for the VPN connection. | Yes |
| routingpolicytype | String | Required if advanceconnection is true. Specifies the routing policy type for VPN connection. Values  | Yes |
| proxytype | String | Optional. Values can benone, manual or auto_detect. | Optional |
| proxyserver | String | Required if proxytype is manual. Specifies the proxy server for the VPN connection. | Yes |
| proxyurl | String | Required if proxytype is auto_detect. Specifies the proxy server for the VPN connection. | Yes |
| connprcol | String | Required if connection type is IKEv2. Specifies the connection protocol for the VPN connection. Valu | Yes |
| userauth | String | The user authentication type for the VPN connection. Values can be password or shared_secret. | Optional |
| presharedkey | String | Required if the connection type is L2TP. The pre-shared key for the VPN connection. | Yes |
| traficfiltriplst | Array | The list of traffic rules for the VPN connection. | Optional |
| remembrcredntil | Boolean | Optional. The option to remember credentials for the VPN connection. | Optional |
| alwayson | Boolean | Optional. The option to enable always-on VPN for the connection. | Optional |
| bypassforlocal | Boolean | Optional. The option to allow local intranet traffic to bypass the VPN connection. | Optional |
| trustednetwork | String | The trusted network for the VPN connection. Multiple entries should be comma-separated. | Optional |
| enable_application_guard | Boolean | Required. | Yes |
| clipboard_settings | String | Required. Specifies the clipboard settings for the application guard. Values can becompletely_turn_o | Yes |
| clipboard_file_type | String | Required. Specifies allowed file types for clipboard operations in the application guard. Values can | Yes |
| printing_settings | Array | Specifies the printing settings for the application guard. | Optional |
| block_non_enterprise_content | Boolean | Optional. | Optional |
| allow_data_persistence | Boolean | Optional | Optional |
| allow_virtual_gpu | Boolean | Optional | Optional |
| save_files_to_host | Boolean | Optional | Optional |
| certificate_thumbprints | String | Specifies the certificate thumbprints for the application guard. | Optional |
| allow_camera_microphone_redirection | Boolean | Optional | Optional |
| hide_account_protection_area | Boolean | Optional | Optional |
| hide_app_and_browser_protection_area | Boolean | Optional | Optional |
| prevent_users_from_modifying_settings | Boolean | Optional | Optional |
| hide_device_security_area | Boolean | Optional | Optional |
| hide_tpm_firmware_update_recommendation | Boolean | Optional | Optional |
| hide_tpm_troubleshooter_page | Boolean | Optional | Optional |
| disable_clear_tpm_button | Boolean | Optional | Optional |
| hide_secure_boot_area | Boolean | Optional | Optional |
| notifications | String | Optional. Specifies the notification settings for the application guard. Values can bedisplay_all_no | Optional |
| hide_family_options_area | Boolean | Optional | Optional |
| hide_device_performance_and_health_area | Boolean | Optional | Optional |
| hide_firewall_and_network_protection_area | Boolean | Optional | Optional |
| hide_virus_and_threat_protection_area | Boolean | Optional | Optional |
| hide_ransomware_data_recovery_area | Boolean | Optional | Optional |
| configure_customized_notifications | Boolean | Optional | Optional |
| show_customized_contact_information | Boolean | Optional | Optional |
| contact_company_name | String | Required if‘show_customized_contact_information’is true. Specifies the company name for customized c | Yes |
| contact_email | String | Required if‘show_customized_contact_information’is true and when ‘contact_phone’ and ‘contact_websit | Yes |
| contact_phone | String | Required if‘show_customized_contact_information’is true. and when ‘contact_email’ and ‘contact_websi | Yes |
| contact_website | String | Required if‘show_customized_contact_information’is true and when ‘contact_email’ and ‘contact_phone’ | Yes |
| hide_windows_security_systray | Boolean | Optional. | Optional |
| whitelist_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| blacklist_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| mandatory_apps | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(wh | Optional |
| catalogues | List / Array | Optional. List of integers representing the corresponding catalogue IDs. | Optional |

---

## Policy Details

**Source:** [https://www.hexnode.com/mobile-device-management/developers/policies/policy-details/](https://www.hexnode.com/mobile-device-management/developers/policies/policy-details/)

Category Filter

---

## Edit Policy

**Source:** [https://www.hexnode.com/mobile-device-management/developers/policies/edit-policy/](https://www.hexnode.com/mobile-device-management/developers/policies/edit-policy/)

Category Filter

---

## Archive Policy

**Source:** [https://www.hexnode.com/mobile-device-management/developers/policies/archive-policy/](https://www.hexnode.com/mobile-device-management/developers/policies/archive-policy/)

Category Filter

---

# Reports

**Total endpoints:** 2

## List app data usage statistics

**Source:** [https://www.hexnode.com/mobile-device-management/developers/reports/list-app-data-usage-statistics/](https://www.hexnode.com/mobile-device-management/developers/reports/list-app-data-usage-statistics/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| range | Integer | Optional | Optional |
| startdate & enddate | Integer | Optional | Optional |
| order_by | String | Optional | Optional |
| count | Integer | Optional | Optional |

---

## List data usage statistics

**Source:** [https://www.hexnode.com/mobile-device-management/developers/reports/list-data-usage-statistics/](https://www.hexnode.com/mobile-device-management/developers/reports/list-data-usage-statistics/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| range | Integer |  | Optional |
| startdate & enddate | Integer |  | Optional |

---

# Setup

**Total endpoints:** 3

## Authentication

**Source:** [https://www.hexnode.com/mobile-device-management/developers/setting-up-an-api/authentication/](https://www.hexnode.com/mobile-device-management/developers/setting-up-an-api/authentication/)

Category Filter

---

## Retrieve API Key

**Source:** [https://www.hexnode.com/mobile-device-management/developers/setting-up-an-api/retrieve-api-key/](https://www.hexnode.com/mobile-device-management/developers/setting-up-an-api/retrieve-api-key/)

Category Filter

---

## Status and Error Codes

**Source:** [https://www.hexnode.com/mobile-device-management/developers/setting-up-an-api/status-and-error-codes/](https://www.hexnode.com/mobile-device-management/developers/setting-up-an-api/status-and-error-codes/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  |  | Success | Optional |
|  |  | Created one or more resource(s) | Optional |
|  |  | The server has successfully fulfilled the request. | Optional |
|  |  | The web-service request was invalid. | Optional |
|  |  | Authentication failed! Invalid credentials. | Optional |
|  |  | Requested a resource to which the server does not allow access. | Optional |
|  |  | Requested resource not found. | Optional |
|  |  | The requested payload format is in an unsupported format. | Optional |
|  |  | User has sent too many requests in a given amount of time. | Optional |
|  |  | An internal server error occurred while processing the request. | Optional |
|  |  | Hexnode MDM Web service server is not reachable. | Optional |
|  |  | The server is currently unable to handle the request due to a temporary overload or maintenance of t | Optional |

---

# User Groups

**Total endpoints:** 6

## List User Groups

**Source:** [https://www.hexnode.com/mobile-device-management/developers/user-groups/list-user-groups/](https://www.hexnode.com/mobile-device-management/developers/user-groups/list-user-groups/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | Integer | Optional | Optional |
|  | Integer | Optional | Optional |

---

## Create User Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/user-groups/create-user-group/](https://www.hexnode.com/mobile-device-management/developers/user-groups/create-user-group/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | String | Required. Name of the user group | Yes |
|  | String | Required. Description of the group | Yes |
|  | Integer array | Optional. Array of ID’s of the enrolled users | Optional |

---

## Retrieve User Group Details

**Source:** [https://www.hexnode.com/mobile-device-management/developers/user-groups/retrieve-user-group-details/](https://www.hexnode.com/mobile-device-management/developers/user-groups/retrieve-user-group-details/)

Category Filter

---

## Update User Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/user-groups/update-user-group/](https://www.hexnode.com/mobile-device-management/developers/user-groups/update-user-group/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | String | Required. New name for the user group | Yes |
|  | String | Required. Description for the group | Yes |
|  | Integer array | Optional. Updated list of the users | Optional |

---

## Add/Remove Users

**Source:** [https://www.hexnode.com/mobile-device-management/developers/user-groups/add-remove-users/](https://www.hexnode.com/mobile-device-management/developers/user-groups/add-remove-users/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | Integer array | Required. An array of user IDs to be added into the group | Yes |
|  | Integer array | Required. Array of user IDs to be removed from the group | Yes |

---

## Delete User Group

**Source:** [https://www.hexnode.com/mobile-device-management/developers/user-groups/delete-user-group/](https://www.hexnode.com/mobile-device-management/developers/user-groups/delete-user-group/)

Category Filter

---

# Users

**Total endpoints:** 6

## List all Users

**Source:** [https://www.hexnode.com/mobile-device-management/developers/users/list-all-users/](https://www.hexnode.com/mobile-device-management/developers/users/list-all-users/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
|  | String | Optional. Order by username. Useascordesc | Optional |
|  | String | Optional. Use local or active directory | Optional |
|  | String | Optional. Use enrolled or unenrolled | Optional |
|  | Integer | Optional | Optional |
|  | Integer | Optional. Themaximum valueis250 | Optional |

---

## Create User

**Source:** [https://www.hexnode.com/mobile-device-management/developers/users/create-user/](https://www.hexnode.com/mobile-device-management/developers/users/create-user/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| name | String | Required. The display name of the user | Yes |
| email | String | Required. Unique email address of the user | Yes |
| phoneno | Integer | Optional. The contact number of the user | Optional |
| password | String | Optional. User password | Optional |

---

## Retrieve User Details

**Source:** [https://www.hexnode.com/mobile-device-management/developers/users/retrieve-user-details/](https://www.hexnode.com/mobile-device-management/developers/users/retrieve-user-details/)

Category Filter

---

## Edit User

**Source:** [https://www.hexnode.com/mobile-device-management/developers/users/edit-user/](https://www.hexnode.com/mobile-device-management/developers/users/edit-user/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| name | String | Required. The display name of the user | Yes |
| email | String | Required. Unique email address of the user | Yes |
| phoneno | Integer | Optional. The contact number of the user | Optional |
| password | String | Optional. User password | Optional |

---

## Delete User

**Source:** [https://www.hexnode.com/mobile-device-management/developers/users/delete-user/](https://www.hexnode.com/mobile-device-management/developers/users/delete-user/)

Category Filter

---

## Send Enrollment Request

**Source:** [https://www.hexnode.com/mobile-device-management/developers/users/send-enrollment-request/](https://www.hexnode.com/mobile-device-management/developers/users/send-enrollment-request/)

Category Filter

### Parameters

| Argument | Type | Description | Required |
|----------|------|-------------|----------|
| ownership | String | Required. Specify the type of ownership, eitherpersonal,corporateoruser_choice | Yes |

---
