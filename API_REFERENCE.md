# Hexnode API Complete Reference - All Platforms

**Scraped:** 2026-11-09T11:48:49.357833

---

## Summary

- **Platforms:** 4
- **Total Parameters:** 512
- **Total Sections:** 4

### By Platform

| Platform | Parameters | Sections | Required | Optional |
|----------|------------|----------|----------|----------|
| **MACOS** | 115 | 1 | 13 | 87 |
| **IOS** | 224 | 1 | 65 | 147 |
| **ANDROID** | 99 | 1 | 19 | 74 |
| **WINDOWS** | 74 | 1 | 23 | 42 |

---

## Table of Contents

- [MACOS](#macos-policies)
- [IOS](#ios-policies)
- [ANDROID](#android-policies)
- [WINDOWS](#windows-policies)

---


# MACOS Policies

**Source:** https://www.hexnode.com/mobile-device-management/developers/policies/macos-policies/

**Total Parameters:** 115

**Required:** 13

**Optional:** 87


## macOS Policies

Thepassworddictionary can contain the following keys:
Thewifidictionary contains the following keys:
If theproxy_typefield is set to Manual or Automatic, the following fields must also be provided:
If thesecurity_typefield is set to Enterprise network options namely WEP_Enterprise, WPA/WPA2_Enterprise, or Any*(Enterprise), the following fields must also be provided:
Thevpndictionary payload can contain the following keys
Thefirewalldictionary payload can contain the following keys
Thefilevaultdictionary payload can contain the following keys
Thesystemextensiondictionary payload can contain the following keys
Thekernelextensiondictionary payload can contain the following keys
Theapp_managementdictionary can contain the following keys:
HTTP Response:


### Parameters

| Argument | Type | Description | Default |
|----------|------|-------------|---------|
| `allow_simple` | Boolean | Optional. | true |
| `require_alphanumeric` | Boolean | Optional. | false |
| `change_at_next_auth` | Boolean | Optional. The option to enforce password change in the next login. | false |
| `min_length` | Integer | Optional. Values can be from 1 to 16. |  |
| `min_complex_chars` | Integer | Optional. Values can be from 1 to 4. |  |
| `max_pinage_in_days` | Integer | Optional. Values can be from 0 to 730. Specifies the maximum number of days the passcode can be used before expiration |  |
| `max_inactivity` | String | Optional.Specifies the maximum period of inactivity before the device locks. Values can be never, 1_mintue, 2_minutes, 3_minutes, 4_minutes, 5_minutes, 10_minutes, or 15_minutes. | never |
| `pin_history` | Integer | Optional. Values can be from 0 to 50. | 0 |
| `max_grace_period` | String | Optional. Values can be none, immediately,1_minute, 5_minutes, 15_minutes, 1_hour, or 4_hours. | none |
| `service_set_identifier` | String | Required. |  |
| `autojoin` | Boolean | Optional. | true |
| `hidden_network` | Boolean | Optional. | false |
| `security_type` | String | Optional. The possible values arenone,WEP,WPA/WPA2,Any*(Personal),WEP_Enterprise,WPA/WPA2_Enterprise, orAny*(Enterprise). | Any*(Personal) |
| `password` | String | Required if WEP, WPA/WPA2 or Any*(Personal) is set. |  |
| `proxy_type` | String | Optional. The possible values areNone,ManualorAutomatic. | None |
| `proxyserver` | String | Required when proxy_type is Manual. The proxy server’s network address. | - |
| `proxy_server_port` | Integer | Required when proxy_type is Manual. The proxy server’s port number. | - |
| `proxy_user_name` | String | Required when proxy_type is Manual. Username for proxy authentication. | - |
| `proxy_password` | String | Required when proxy_type is Manual. Password for proxy authentication. | - |
| `proxy_pac_url` | String | Required when proxy_type is Automatic. The URL of the Proxy Auto Configuration (PAC) file. | - |
| `tls` | Boolean | Optional. | false |
| `leap` | Boolean | Optional. | false |
| `eap_fast` | Boolean | Optional. | false |
| `user_password` | String | The user password for authentication. |  |
| `outer_identity` | String | The outer identity for authentication. |  |
| `inner_authentication` | String | Available if eap_fast is enabled. The inner authentication method for EAP. Values can be PAP, CHAP, MSCHAP, or MSCHAPv2 | PAP |
| `identity_cert_id` | String | The ID of the identity certificate for authentication. |  |
| `provision_pac` | Boolean | Available if eap_fast is enabled. | true |
| `provision_pac_anonymously` | Boolean | Available if eap_fast is enabled. | false |
| `user_name` | String | The username for authentication. |  |
| `ttls` | Boolean | Optional. | true |
| `peap` | Boolean | Optional. | false |
| `eap_sim` | Boolean | Optional. | false |
| `use_per_connection_pwd` | Boolean | Optional. | false |
| `use_pac` | Boolean | Optional. | true |
| `certificate_id` | String | Required when machine_authentication is a certificate. |  |
| `account` | String | Optional. The username for the connection. |  |
| `connection_name` | String | Optional. |  |
| `connection_type` | String | Optional. Values can be L2TP, PPTP, IPSec(Cisco), Cisco_AnyConnect, Juniper_SSL, F5_SSL, SonicWALL_Mobile_Connect, Aruba_VIA, Check_Point_Mobile_VPN and Open_VPN. | L2TP |
| `encryption_level` | String | Available when the connection type is PPTP. Values can be None, Automatic, or Maximum(128_bit). | None |
| `identifier` | String | Optional. Specifies the identifier for the connection. |  |
| `include_user_pin` | Boolean | Optional. | false |
| `ipsec_account` | String | Optional. The IPSec account information. |  |
| `ipsec_auth_password` | String | Optional. The password for IPSec authentication. |  |
| `ipsec_certificate_id` | String | Optional. The ID of the IPSec certificate. |  |
| `ipsec_group_name` | String | Optional. |  |
| `ipsec_shared_secret` | String | Optional. |  |
| `l2tp_account` | String | Optional. The L2TP account information. |  |
| `l2tp_password` | String | Optional. | false |
| `l2tp_server` | String | Optional. | false |
| `l2tp_shared_secret` | String | Optional. | false |
| `l2tp_user_authentication` | String | The authentication method for an L2TP user. Values can be‘RSA_SecureID’, or ‘Password’. | ‘RSA_SecureID’ |
| `l2tp_user_authentication_method` | Integer | Optional. | 1 |
| `login_group` | String | Required when the connection type is SONIC_WALL_Mobile_Connect. Specifies the login group information. |  |
| `machine_authentication` | String | Required when the connection type is IPSec(Cisco). The type of machine authentication. Values can be certificate, or shared_secret/group_name | shared_secret/group_name. |
| `password` | String | Optional. The password for authentication. |  |
| `prompt_for_password` | String | Optional. |  |
| `proxy_pac_url` | String | Required when proxy_type is Automatic |  |
| `proxy_password` | String | Available when proxy_type is Manual |  |
| `proxy_server_port` | Integer | Required when proxy_type is Manual |  |
| `proxy_type` | String | Values can be ‘None’, ‘Manual’ or ‘Automatic’. | ‘None’ |
| `proxy_user_name` | String | Available when proxy_type is Manual. Specifies the username for proxy authentication |  |
| `proxyserver` | String | Required when proxy_type is Manual. The server address of proxy. |  |
| `realm` | String | Optional. Specifies the realm information. |  |
| `remote_address` | String | Optional. Specifies the remote address for the connection. |  |
| `role` | String | Optional.Specifies the role information |  |
| `send_all_traffic` | Boolean | Optional. The option to enable sending of all traffic through the connection. | false |
| `server` | String | Optional. Specifies the server information. |  |
| `use_hybrid_authentication` | Boolean | Optional. | false |
| `user_authentication_type` | String | Optional. Values can be ‘password’ or ‘certificate’. |  |
| `enable_vpn_ondemand` | Integer | Optional. | 0 |
| `http_enable` | Integer | Optional. | 0 |
| `https_enable` | Integer | Optional. | 0 |
| `proxy_autoconfig` | String | Optional. |  |
| `https_proxyserver` | String | Optional. Specifies the server address of the HTTPS proxy server. |  |
| `https_proxy_server_port` | Integer | Optional. Specifies the port number of the HTTPS proxy server. |  |
| `connection_sub_type` | String | Optional. |  |
| `auth_protocol` | Boolean | Optional. The option to enable authentication protocol. | false |
| `auth_plugins` | Boolean | Optional. The option to enable authentication plugins. | false |
| `token_key` | Boolean | Optional. | false |
| `ipsec_auth_enabled` | Integer | Optional. | 1 |
| `local_identifier_type` | String | Optional. |  |
| `firewall_enabled` | String | Optional. Values can be allow_incoming_connections or block_incoming_connections | allow_incoming_connections |
| `Enable_Firewall` | Boolean | Optional. | false |
| `Block_AllIncoming` | Boolean | Optional. | false |
| `Enable_StealthMode` | Boolean | Optional. | false |
| `application` | Array | Optional. The application details to be included in Firewall. The details should be in the following format [{app_name:”, app_id:”, identifier:”}]. |  |
| `preventfromdisabled` | Boolean | Optional. The option to prevent users from turning off FileVault encryption on the device. | false |
| `escrow_recovery_key` | Boolean | Optional. The option to encrypt the key with a certificate and escrow it to Hexnode for safekeeping. | false |
| `preventfromenabled` | Boolean | Optional. The option to prevent users from turning on FileVault encryption on the device. | false |
| `escrow_encryption-key_manual` | Boolean | Optional. The possible value is allow_hexnode_to_automatically_to_encrypt_and_decrypt_the_recovery_key. | allow_hexnode_to_automatically_to_encrypt_and_decrypt_the_recovery_key |
| `unlock_hibernation` | Boolean | Optional.The option to enforce the use of the device password for unlocking FileVault after hibernation and for restoring the disk to its most recent saved state. | false |
| `max_bypass_attempt` | Integer | Optional. | 0 |
| `enable_bypassing` | Boolean | Optional. | false |
| `encryption_type` | String | Optional. The possible values are institutional_recovery_key, personal_recovery_key, or institutional_and_personal_recovery_key. | institutional_and_personal_recovery_key |
| `escrow_local_desc` | String | Optional.The description for escrow local. |  |
| `show_recovery_key` | Boolean | Optional. | true |
| `selected_cert_id` | Integer | Optional. | 2 |
| `enable_filevault` | Boolean | Optional. | true |
| `escrow_encrypt_key_cert` | String | Optional. | None |
| `enter_missing_info` | Boolean | Optional. | true |
| `ask_at_logout` | Boolean | Optional. The option to define the maximum number of times a user can bypass the prompt to enable FileVault when logging into the device. | true |
| `allow_system_user_overrides` | Boolean | Optional | false |
| `allowed_system_teamids` | Array | Optional. The team identifiers should be specified within [] |  |
| `allowed_system_extensions` | Object | Optional. The system extensions should be specified within {}. |  |
| `allowed_system_extension_type` | Object | Optional. The system extension types should be specified within {}. |  |
| `allow_user_overrides` | Boolean | Optional | false |
| `allowed_teamids` | String | Optional. The team identifiers should be specified within []. |  |
| `whitelist_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `blacklist_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `mandatory_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `catalogues` | List / Array | Optional. List of integers representing the corresponding catalogue IDs. | - |
| `-` | - | - | - |
| `-` | - | - | - |
| `-` | - | - | - |


---


# IOS Policies

**Source:** https://www.hexnode.com/mobile-device-management/developers/policies/ios-policies/

**Total Parameters:** 224

**Required:** 65

**Optional:** 147


## iOS Policies

Thepassworddictionary can contain the following keys:
Therestrictionsdictionary can contain the following keys:
Theadvanced_restrictionsdictionary can contain the following keys:
Theweb_content_filterdictionary can contain the following keys:
Thewifilist payload can contain the following keys:
If thesecurity_typefield is set towep,wpa, orany, the following fields must also be provided:
If thesecurity_typefield is set toWEP_Enterprise,WPA_Enterprise,Any_Enterpriseoreap, the following fields may also be provided:
If theproxy_typefield is set toManual, the following fields must also be provided:
If theproxy_typefield is set toAuto, the following field must also be provided:
Theemaildictionary can contain the following keys:
Theactivesyncdictionary can contain the following keys:
Theldapdictionary can contain the following keys:
Thecaldavdictionary can contain the following keys:
Thesubscribe_calendardictionary can contain the following keys:
Thecarddavdictionary can contain the following keys:
Thewebcliplist can contain the following keys:
Theaccess_pointdictionary can contain the following keys:
Theapplockdictionary can contain the following keys:
Thewallpaperdictionary can contain the following keys:
Theglobalproxydictionary can contain the following keys:
Thelock_screen_msgdictionary can contain the following keys:
Theapp_managementdictionary can contain the following keys:


### Parameters

| Argument | Type | Description | Default |
|----------|------|-------------|---------|
| `allow_simple` | Boolean | Optional | true |
| `require_alphanumeric` | Boolean | Optional | false |
| `min_length` | Integer | Optional. Values can be from 1 to 16 |  |
| `min_complex_char` | Integer | Optional. Values can be from 1 to 4 |  |
| `max_pinage_in_days` | Integer | Optional. Specifies the number of days for which the passcode can remain unchanged |  |
| `max_inactivity` | Integer | Optional. This dictionary contains email configurations |  |
| `pin_history` | Dictionary | Optional. When the user changes the passcode, it has to be unique within the last N entries in the history.The minimum value is 1, and the maximum value is 50 |  |
| `max_grace_period` | Integer | Optional. The maximum grace period (in minutes) to unlock the phone without entering a passcode.Supported values are1,5,15,60and240 |  |
| `max_failed_attempts` | Integer | Optional. Specifies the number of allowed failed attempts to enter the passcode on the device’s lock screen.Supported values are4,5,6,7,8,9and10 |  |
| `allow_app_installation` | Boolean | Optional | true |
| `allow_airdrop_managemendapps` | Boolean | Optional | false |
| `allow_camera` | Boolean | Optional | true |
| `allow_video_conferencing` | Boolean | Optional | true |
| `allow_screen_shot` | Boolean | Optional | false |
| `allow_global_background_fetch_when_roaming` | Boolean | Optional | true |
| `allow_touchId` | Boolean | Optional | true |
| `allow_assistant` | Boolean | Optional | true |
| `allow_assistant_while_locked` | Boolean | Optional | true |
| `allow_voice_dialing` | Boolean | Optional | true |
| `allow_passbook_while_locked` | Boolean | Optional | false |
| `allow_inapp_purchases` | Boolean | Optional | true |
| `force_itunes_store_password_entry` | Boolean | Optional | true |
| `allow_multiplayer_gaming` | Boolean | Optional | true |
| `allow_adding_game_center_friends` | Boolean | Optional | true |
| `allow_enterprise_app_trust` | Boolean | Optional | true |
| `allow_enterprise_app_trust_modification` | Boolean | Optional | true |
| `allow_enterprise_book_backup` | Boolean | Optional | true |
| `allow_managed_app_sync` | Boolean | Optional | true |
| `allow_youtube` | Boolean | Optional | true |
| `allow_itunes` | Boolean | Optional | true |
| `allow_safari` | Boolean | Optional | true |
| `safari_allow_auto_fill` | Boolean | Optional | true |
| `safari_force_fraud_warning` | Boolean | Optional | false |
| `safari_allow_java_script` | Boolean | Optional | true |
| `safari_allow_popups` | Boolean | Optional | true |
| `safari_accept_cookies` | String | Optional. Values can bealways,visitedornever |  |
| `allow_cloud_backup` | Boolean | Optional | true |
| `allow_cloud_document_sync` | Boolean | Optional | true |
| `allow_photo_stream` | Boolean | Optional | true |
| `allow_shared_stream` | Boolean | Optional | true |
| `allow_icloud_photo` | Boolean | Optional | true |
| `allow_lockscreen_notify` | Boolean | Optional | true |
| `allow_lockscreen_todayView` | Boolean | Optional | true |
| `allow_lockscreen_control` | Boolean | Optional | true |
| `allow_ota_pki_update` | Boolean | Optional | true |
| `limit_ad_tracking` | Boolean | Optional | false |
| `allow_diagnostic_submission` | Boolean | Optional | true |
| `allow_untrusted_tls_prompt` | Boolean | Optional | true |
| `force_encrypted_backup` | Boolean | Optional | false |
| `force_applewatch_Detection` | Boolean | Optional | false |
| `allow_explicit_content` | Boolean | Optional | true |
| `allow_bookstore_erotica` | Boolean | Optional | false |
| `rating_region` | String | Optional. Values can beus,au,ca,de,fr,ie,jp,nzorgb |  |
| `rating_movies` | String | Optional. Values can beallow,nc-17,r,pg-13,pg,gornever |  |
| `rating_tv_shows` | String | Optional. Values can beallow,tv-ma,tv-14,tv-pg,tv-g,tv-y7,tv-yornever |  |
| `rating_apps` | String | Values can beallow,17+,12+,9+,4+,never |  |
| `allow_airdrop` | Boolean | Optional | true |
| `allow_app_cellular_data_modification` | Boolean | Optional | true |
| `allow_app_removal` | Boolean | Optional | true |
| `allow_bookstore` | Boolean | Optional | true |
| `allow_touchId_modify` | Boolean | Optional | false |
| `allow_chat` | Boolean | Optional | true |
| `allow_game_center` | Boolean | Optional | true |
| `allow_host_pairing` | Boolean | Optional | true |
| `allow_ui_configuration_profile_installation` | Boolean | Optional | true |
| `allow_podcasts` | Boolean | Optional | true |
| `allow_definition_lookup` | Boolean | Optional | true |
| `allow_predictive_keyboard` | Boolean | Optional | true |
| `allow_auto_correction` | Boolean | Optional | true |
| `allow_spell_check` | Boolean | Optional | true |
| `allow_music_service` | Boolean | Optional | true |
| `allow_radio_service` | Boolean | Optional | true |
| `allow_news` | Boolean | Optional | true |
| `allow_ui_app_installation` | Boolean | Optional | true |
| `allow_keyboard_shortcuts` | Boolean | Optional | true |
| `allow_paired_watch` | Boolean | Optional | true |
| `allow_account_modification` | Boolean | Optional | true |
| `allow_erase_content_and_settings` | Boolean | Optional | true |
| `allow_assistant_user_generated_content` | Boolean | Optional | true |
| `allow_find_my_friends_modification` | Boolean | Optional | true |
| `force_assistant_profanity_filter` | Boolean | Optional | false |
| `allow_spotlight_internet_results` | Boolean | Optional | true |
| `allow_enabling_restrictions` | Boolean | Optional | true |
| `allow_passcode_modification` | Boolean | Optional | true |
| `allow_device_name_modification` | Boolean | Optional | true |
| `allow_wallpaper_modification` | Boolean | Optional | true |
| `allow_notifications_modification` | Boolean | Optional | true |
| `Allow_automatic_app_downloads` | Boolean | Optional | true |
| `autonomous_single_apps` | Integer array | Optional. Can contain IDs of the iOS apps | An empty list |
| `filter_type` | String | Required. Values can be white_list or black_list |  |
| `auto_filter_enabled` | Boolean | Optional. Use only when filter_type is black_list | false |
| `permitted_urls` | String array | Optional. Used only when auto_filter_enabled is true. Otherwise, this field is ignored |  |
| `blacklisted_urls` | String array | Optional. Array of URLs. Use only when filter_type is black_list. Otherwise, this field is ignored |  |
| `whitelist_urls` | String array | Optional. Array of URLs. Use only when filter_type is white_list. Otherwise, this field is ignored |  |
| `service_set_identifier` | String | - | - |
| `autojoin` | Boolean | - | - |
| `hidden_network` | Boolean | - | - |
| `security_type` | String | - | - |
| `proxy_type` | String | - | - |
| `password` | String | - | - |
| `user_name` | String | Required |  |
| `user_password` | String | Required if use_per_connection_pwd is set to false |  |
| `use_per_connection_pwd` | Boolean | Optional | false |
| `tls` | Boolean | Optional | false |
| `leap` | Boolean | Optional | false |
| `ttls` | Boolean | Optional | true |
| `peap` | Boolean | Optional | true |
| `eap_fast` | Boolean | Optional | false |
| `eap_sim` | Boolean | Optional | false |
| `provision_pac` | Boolean | Optional | false |
| `provision_pac_anonymously` | Boolean | Optional | false |
| `use_pac` | Boolean | Optional | false |
| `inner_authentication` | String | Optional. The possible values arePAP,CHAP,MSCHAP,MSCHAPv2 | PAP |
| `outer_identity` | String | Optional. | None |
| `proxyserver` | String | Required. The proxy server’s network address | - |
| `proxy_server_port` | Integer | Required. The proxy server’s port | - |
| `proxy_user_name` | String | Required. Username used to authenticate the proxy server | - |
| `proxy_password` | String | Required. Password used to authenticate proxyserver | - |
| `proxy_pac_url` | String | Required. The URL of the PAC file that defines the proxy configuration | - |
| `account_description` | String | Required. User visible description of the email account |  |
| `user_display_name` | String | Required. Username of the account. Use%name%for user’s name |  |
| `account_type` | String | Required. The possible values arePOPandIMAP |  |
| `imap_path_prefix` | String | Optional. Required ifaccount_typeis set toIMAP |  |
| `email_address` | String | Required. The email address for the account. Use%email%for user’s email |  |
| `allow_move` | Boolean | Required. The email address for the account. Use%email%for user’s email | false |
| `incoming_server_host_name` | String | Required. The email address for the account. Use%email%for user’s email |  |
| `incoming_server_port` | Integer | Required. The email address for the account. Use%email%for user’s email | 143 |
| `incoming_server_username` | String | Required. Use%username%for username |  |
| `incoming_server_auth` | String | Required. Possible values areNone,Password,MD5,NTLMandHTTP |  |
| `incoming_password` | String | Required ifincoming_server_authis notNone |  |
| `incoming_server_use_ssl` | Boolean | Optional | true |
| `out_server_host_name` | String | Required. Outgoing mail server host name |  |
| `out_server_port` | Integer | Required | 587 |
| `out_server_username` | Integer | Required. Value can benull. Use%username%for username |  |
| `out_server_auth` | String | Required. Possible values areNone,Password,MD5,NTLMandHTTP |  |
| `out_pwd_as_incoming_pwd` | Boolean | Required ifout_server_authis notNone |  |
| `out_password` | String | Required ifout_pwd_as_incoming_pwdis set tofalse |  |
| `allow_recent_syncing` | Boolean | Optional | false |
| `mail_app_only` | Boolean | Optional. Use only in mail |  |
| `out_server_use_ssl` | Boolean | Optional | true |
| `smime_enabled` | Boolean | Optional | false |
| `account_name` | String | Required |  |
| `host_name` | Boolean | Required |  |
| `allow_move` | Boolean | Optional | false |
| `recent_address_syncing` | Boolean | Optional | false |
| `mail_app_only` | Boolean | Optional | false |
| `use_ssl` | Boolean | Optional | true |
| `smime_enabled` | Boolean | Optional | false |
| `domain` | String | Required. Value can be blank. Use%domain%for user’s domain | false |
| `username` | String | Required. Use%username%for username and%email%for user’s email address | false |
| `email_address` | String | Required. Use%email%for user’s email address | false |
| `password` | String | Optional. Value can benull | false |
| `no_past_days_to_sync` | Integer | Optional. Possible values are0,1,3,7,14,31 | 3 |
| `cert_compatible_ios4` | Boolean | Optional | true |
| `account_name` | String | Required. Visible description of the LDAP account. Value can be null |  |
| `host_name` | String | Required |  |
| `username` | String | Required. Value can be null |  |
| `password` | String | Required. Value can be null |  |
| `use_ssl` | Boolean | Optional | true |
| `account_name` | String | Required. Visible description of the LDAP account. Value can be null |  |
| `hostname` | String | Required. Host name of the account |  |
| `username` | String | Required. Username of the account. Value can be null |  |
| `password` | String | Required. Password of the account. Value can be null |  |
| `use_ssl` | Boolean | Optional | true |
| `port` | Integer | Optional | 80 |
| `principal_url` | String | Required. Value can be null |  |
| `account_name` | String | Required. Visible info about the account. Value can be null |  |
| `url` | String | Required |  |
| `username` | String | Required. Value can be null |  |
| `password` | String | Required. Value can be null |  |
| `use_ssl` | Boolean | Optional | true |
| `account_name` | String | Required. Visible description. Value can be null |  |
| `host_name` | String | Required. |  |
| `username` | String | Required. Username of the account. Value can be null |  |
| `password` | String | Required. Value can be null |  |
| `use_ssl` | Boolean | Optional | true |
| `port` | Integer | Optional | 8443 |
| `principal_url` | String | Required. Value can be null |  |
| `label` | String | Required. Name of the webclip |  |
| `is_removable` | Boolean | Optional | true |
| `url` | Boolean | Optional |  |
| `precomposed_icon` | Boolean | Required | false |
| `fullscreen_icon` | Boolean | Optional | false |
| `icon` | String | Required. Base64 encoded image |  |
| `apn_name` | String | Required |  |
| `apn_username` | String | Required. Value can be null |  |
| `apn_password` | String | Required. Value can be null |  |
| `proxy_server` | String | Optional. Value can be null |  |
| `proxy_server_port` | Integer | Optional | 0 |
| `app` | Integer | Required. App ID |  |
| `disable_touch` | Boolean | Optional | false |
| `disable_device_rotation` | Boolean | Optional | false |
| `disable_volume_buttons` | Boolean | Optional | false |
| `disable_ringer_switch` | Boolean | Optional | false |
| `disable_sleep_wake_button` | Boolean | Optional | false |
| `disable_auto_lock` | Boolean | Optional | false |
| `enable_voice_over` | Boolean | Optional | false |
| `enable_zoom` | Boolean | Optional | false |
| `enable_invert_colors` | Boolean | Optional | false |
| `enable_assistive_touch` | Boolean | Optional | false |
| `enable_speak_selection` | Boolean | Optional | false |
| `voice_over` | Boolean | Optional | false |
| `zoom` | Boolean | Optional | false |
| `invert_colors` | Boolean | Optional | false |
| `assistive_touch` | Boolean | Optional | false |
| `home_screen_wallpaper` | Integer | Required. Base64 encoded image. | - |
| `lock_screen_wallpaper` | Boolean | Required. Base64 encoded image. Value can be null | - |
| `proxy_type` | String | Required. Values can beManual,Auto |  |
| `proxyserver` | String | Required whenproxy_typeis set toManual |  |
| `proxy_server_port` | String | Required whenproxy_typeis set toManual |  |
| `proxy_user_name` | String | Required whenproxy_typeis set toManual. Value can be null |  |
| `proxy_password` | String | Required whenproxy_typeis set toManual. Value can be null |  |
| `proxy_pac_url` | String | Required whenproxy_typeis set toAuto |  |
| `proxy_pac_fallback_allowed` | Boolean |  | false |
| `proxy_captive_login_allowed` | Boolean |  | false |
| `lock_screen_footnote` | String | Required. Value can be null | - |
| `asset_tag_information` | String | Required. Value can be null | - |
| `whitelist_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `blacklist_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `mandatory_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `catalogues` | List / Array | Optional. List of integers representing the corresponding catalogue IDs. | - |
| `-` | - | - | - |
| `-` | - | - | - |
| `-` | - | - | - |


---


# ANDROID Policies

**Source:** https://www.hexnode.com/mobile-device-management/developers/policies/android-policies/

**Total Parameters:** 99

**Required:** 19

**Optional:** 74


## Android Policies

Thepassworddictionary can contain the following keys:
Ifpasscode_requirementis set to complexvalue, the following fields may be required:
Therestrictionsdictionary can contain following keys:
Thewifidictionary contains the following keys:
Theemaildictionary contains the following keys:
Theactivesyncdictionary contains the following keys:
Theapplockdictionary contains the following keys:
Thewallpaperdictionary may contain the following keys:
Theapp_managementdictionary can contain the following keys:
HTTP Request:
Shell Command:
HTTP Response:


### Parameters

| Argument | Type | Description | Default |
|----------|------|-------------|---------|
| `passcode_requirement` | String | Optional.Possible values can besimple,numbers,alphanumeric,alphabet,complexvalue | simple |
| `min_password_complexity` | String | Optional. Possible values can benone,low,medium,high | low |
| `min_length` | Integer | Optional. Possible values are from4 to 16. Ignored ifpasscode_requirementis set tosimpleornumbers |  |
| `max_pinage_in_days` | Integer | Optional. Specifies the number of days for which the passcode can remain unchanged. Minimum value is1and maximum value is730 |  |
| `max_inactivity` | Integer | Optional. Possible values are1,2,3,4,5,10and15 |  |
| `pin_history` | Integer | Optional. Possible values are from1to50 |  |
| `max_failed_attempts` | Integer | Optional. Possible values are from4to10 |  |
| `min_uppercase_letters` | Integer | Optional. Possible values are from1to5 | - |
| `min_lowercase_letters` | Integer | Optional. Possible values are from1to5 | - |
| `min_non_alphapets` | Integer | Optional. Possible values are from1to5 | - |
| `min_num_letters` | Integer | Optional. Possible values are from1to5 | - |
| `min_symbols` | Integer | Optional. Possible values are from1to5 | - |
| `allow_camera` | Boolean | Optional | true |
| `allow_usb_mass_storage` | Boolean | Optional | true |
| `allow_network_time` | Boolean | Optional | true |
| `allow_wifi` | Boolean | Optional | true |
| `enforce_wifi` | Boolean | Optional | true |
| `allow_bluetooth` | Boolean | Optional | true |
| `allow_data_network` | Boolean | Optional | true |
| `allow_bgdata_sync` | Boolean | Optional | true |
| `allow_auto_background_sync` | Boolean | Optional | true |
| `allow_mobile_app` | Boolean | Optional | true |
| `allow_usb_tethering` | Boolean | Optional | true |
| `allow_mock_locations` | Boolean | Optional | true |
| `allow_wireless_location` | Boolean | Optional | true |
| `allow_gps_location` | Boolean | Optional | true |
| `allow_non_google_app` | Boolean | Optional | true |
| `enforce_app_verification` | Boolean | Optional | true |
| `allow_backup_google` | Boolean | Optional | true |
| `allow_auto_restore` | Boolean | Optional | true |
| `allow_roaming` | Boolean | Optional | true |
| `enforce_device_encrypt` | Boolean | Optional | true |
| `disable_keyguard` | Boolean | Optional | true |
| `allow_password_visible` | Boolean | Optional | true |
| `enforce_gps_location` | Boolean | Optional | true |
| `allow_mdm_removal` | Boolean | Optional | true |
| `service_set_identifier` | String | Required |  |
| `autojoin` | Boolean |  | true |
| `hidden_network` | Boolean |  | false |
| `security_type` | String | Required. Possible values arenone,wep,wpa,eap |  |
| `password` | String | Required ifsecurity_typeis set toweporwpa |  |
| `eap_type` | String | Required ifsecurity_typeis set toeap. Possible values arepeap,ttls,pwd |  |
| `user_name` | String | Required ifsecurity_typeis set toeap |  |
| `enterprise_password` | String | Optional. Value can be set to null |  |
| `phase2_authentication` | String | Required ifeap_typeis set topeap. Possible values areNone,PAP,MSCHAP,MSCHAPv2,GTC |  |
| `outer_identity` | String | Required ifeap_typeis set topeap. |  |
| `account_name` | String | Value can be null |  |
| `account_description` | String | Required. Account description |  |
| `incoming_account_type` | String | Optional. Possible values arepop3andimap | pop3 |
| `email_address` | String | Optional. Email address for the account. Value can be set to null |  |
| `incoming_server_host_name` | String | Required |  |
| `incoming_server_port` | Integer | Optional | 143 |
| `incoming_server_username` | Integer | Optional. Value can be null |  |
| `incoming_password` | String | Optional. Value can be null |  |
| `incoming_server_use_ssl` | Boolean | Optional | true |
| `incoming_server_use_tls` | Boolean | Optional | false |
| `incoming_server_use_certificate` | Boolean | Optional | false |
| `out_account_type` | Boolean | Required. Possible values arepop3andsmtp |  |
| `out_server_host_name` | String | Required |  |
| `out_server_port` | Integer | Optional | 587 |
| `out_server_username` | String | Optional. Outgoing username for the email. Value can be null |  |
| `out_password` | String | Optional. Password for account authentication. Value can be null |  |
| `out_server_use_ssl` | Boolean | Optional | true |
| `out_server_use_tls` | Boolean | Optional | false |
| `out_server_use_certificate` | Boolean | Optional | false |
| `account_name` | String | Optional. Visible account description |  |
| `host` | String | Required. Exchange ActiveSync Host |  |
| `domain` | String | Optional. Use%domain%as user’s domain. Value can be null |  |
| `email_address` | String | Required. Email address for the account. Use%email%for users’ email address. |  |
| `username` | String | Required. Use%username%for the username |  |
| `password` | String | Optional. Value can be null |  |
| `no_past_days_to_sync` | String | Optional. Possible values areauto,manual,15,30,60,120,240 | auto |
| `use_ssl` | Boolean | Optional | true |
| `apps` | Array | Optional. Apps array have dictionaries which contain keysidwhose value is the app ID andhidewhose value is boolean |  |
| `toggle_wifi` | Boolean | Optional | true |
| `allow_wifi` | Boolean | Optional | true |
| `enable_hexnode_browser` | Boolean | Optional | false |
| `auto_launch_app` | Integer | Optional. ID of app added in apps. Ignored if apps key is missing |  |
| `auto_launch_delay` | Integer | Optional. Delay in seconds. Ignored if apps key is missing |  |
| `allow_change_brightness` | Boolean | Optional | true |
| `brightness_level` | Integer | Required ifallow_change_brightnessis set tofalse | 0 |
| `keep_screen_on` | Boolean | Optional | false |
| `allow_bluetooth` | Boolean | Optional | true |
| `allow_user_location_checkin` | Boolean | Optional | true |
| `kiosk_manual_exit` | Boolean | Optional | true |
| `kiosk_password` | String | Optional. If this field is not configured, set to null, or given an empty string (“”), the value specified underAdmin > General Settings > Global Exit Settingscan be used to exit kiosk mode. |  |
| `exit_passcode_tap_count` | Integer | Required ifkiosk_manual_exitis set to true. Specify the number of taps to display the popup to enter the exit passcode. The entered value should be between 5 and 15. | 10 |
| `exit_kiosk_with_app_open` | Boolean | Optional. Specify if the user can exit manually from kiosk mode while an app is open. | false |
| `exit_kiosk_after_reboot` | Boolean | Optional. Allows exiting kiosk mode during launch delay after a reboot. Users can exit the kiosk mode by tapping on the kiosk home screen and entering the local/global exit passcode during this launch delay. | false |
| `relaunch_app` | Integer | Required, ifexit_kiosk_after_rebootis set true. Specify the time in seconds after which the app relaunches itself in kiosk mode. | 20 |
| `mobile_wallpaper` | String | Required. Base64 image |  |
| `tablet_wallpaper` | String | Required. Base64 image |  |
| `whitelist_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `blacklist_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `mandatory_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `catalogues` | List / Array | Optional. List of integers representing the corresponding catalogue IDs. | - |
| `-` | - | - | - |
| `-` | - | - | - |
| `-` | - | - | - |


---


# WINDOWS Policies

**Source:** https://www.hexnode.com/mobile-device-management/developers/policies/windows-policies/

**Total Parameters:** 74

**Required:** 23

**Optional:** 42


## Windows Policies

Thewin_passworddictionary can contain the following keys:
Thewin_wifidictionary contains the following keys:
If thesecurity_typefield is set toWEP, WPA-PSK/WPA2-PSK, or WPA/WPA2 enterprisethe following fields must also be provided:
If theproxy_typefield is set toManualthe following fields must also be provided:
Thewinvpnpolicydictionary contains the following keys:
Thewindows_defenderdictionary contains the following keys:
Theapp_managementdictionary can contain the following keys:
HTTP Request:
Shell Command


### Parameters

| Argument | Type | Description | Default |
|----------|------|-------------|---------|
| `allow_simple` | Boolean | Optional. | true |
| `require_alphanumeric` | String | Optional.Values can bealphanumeric,numericoruser_can_choose. | user_can_choose |
| `min_length` | Integer | Optional. Values can be from 4 to 16. |  |
| `min_complex_chars` | String | Optional. Values can bedigits_only,digits_lower_lettersordigits_lower_upper_letters. | digits_only |
| `max_pinage_in_days` | Integer | Optional. Values can be from0to730. |  |
| `max_inactivity` | Integer | Optional. Values can be from0to999 |  |
| `pin_history` | Integer | Optional. Possible values are from0to24 |  |
| `max_failed_attempts` | Integer | Optional. |  |
| `service_set_identifier` | String | Required |  |
| `connection_mode` | String | Optional. Values can be Auto, Manual. | Auto |
| `non_broadcast` | Boolean | Optional | false |
| `security_type` | String | Required. Possible values areopen,WEP,WPA-PSK/WPA2-PSK,WPA/WPA2 enterprise | open |
| `proxy_type` | String | Optional. Values can be None and Manual | None |
| `password` | String | Required |  |
| `authentication` | String | Required if WPA-PSK/WPA2-PSK, or WPA/WPA2 enterprise is set. Values can be WPA, WPA2, or open. | open |
| `eap_type` | String | Required ifsecurity_typeis set toWPA/WPA2. Values can bePEAP-MSCHAPv2orEAP TLS | EAP TLS |
| `proxyserver` | String | Required. The proxy server’s network address. | - |
| `proxy_server_port` | Integer | Required. The proxy server’s port number. | - |
| `nativeprotocoltype` | String | Values can beL2TP,PPTP, orIKEv2. | L2TP |
| `profilename` | String | Required. Specifies the profile name for the VPN connection. |  |
| `server` | String | Required. Specifies the server address for the VPN connection. |  |
| `advanceconnection` | Boolean | Optional | false |
| `routelist` | Array | Required if advanceconnection is true. Specifies the list of routes for the VPN connection. |  |
| `domainnameinfolist` | Array | Required if advanceconnection is true. Specifies the list of domain names for the VPN connection. |  |
| `routingpolicytype` | String | Required if advanceconnection is true. Specifies the routing policy type for VPN connection. Values can beallows_traffic_through_vpn_and_local_network_connection or force_all_traffic_through_vpn | allows_traffic_through_vpn_and_local_network_connection |
| `proxytype` | String | Optional. Values can benone, manual or auto_detect. | none |
| `proxyserver` | String | Required if proxytype is manual. Specifies the proxy server for the VPN connection. |  |
| `proxyurl` | String | Required if proxytype is auto_detect. Specifies the proxy server for the VPN connection. |  |
| `connprcol` | String | Required if connection type is IKEv2. Specifies the connection protocol for the VPN connection. Values can be EAP or machine_certificate. | EAP |
| `userauth` | String | The user authentication type for the VPN connection. Values can be password or shared_secret. | password |
| `presharedkey` | String | Required if the connection type is L2TP. The pre-shared key for the VPN connection. |  |
| `traficfiltriplst` | Array | The list of traffic rules for the VPN connection. |  |
| `remembrcredntil` | Boolean | Optional. The option to remember credentials for the VPN connection. | false |
| `alwayson` | Boolean | Optional. The option to enable always-on VPN for the connection. | false |
| `bypassforlocal` | Boolean | Optional. The option to allow local intranet traffic to bypass the VPN connection. | false |
| `trustednetwork` | String | The trusted network for the VPN connection. Multiple entries should be comma-separated. |  |
| `enable_application_guard` | Boolean | Required. | false |
| `clipboard_settings` | String | Required. Specifies the clipboard settings for the application guard. Values can becompletely_turn_off_the_clipboard_functionality_for_the_application_guard, turn_on_clipboard_operation_from_an_isolated_session_to_the_host, turn_on_clipboard_operation_from_the_host_to_an_isolated_session, or turn_on_clipboard_operation_in_both_the_directions. | completely_turn_off_the_clipboard_functionality_for_the_application_guard |
| `clipboard_file_type` | String | Required. Specifies allowed file types for clipboard operations in the application guard. Values can beallow_copying_texts,allow_copying images, orallow_copying_text_and_images. | allow_copying_texts |
| `printing_settings` | Array | Specifies the printing settings for the application guard. |  |
| `block_non_enterprise_content` | Boolean | Optional. | false |
| `allow_data_persistence` | Boolean | Optional | false |
| `allow_virtual_gpu` | Boolean | Optional | false |
| `save_files_to_host` | Boolean | Optional | false |
| `certificate_thumbprints` | String | Specifies the certificate thumbprints for the application guard. |  |
| `allow_camera_microphone_redirection` | Boolean | Optional | false |
| `hide_account_protection_area` | Boolean | Optional | true |
| `hide_app_and_browser_protection_area` | Boolean | Optional | false |
| `prevent_users_from_modifying_settings` | Boolean | Optional | false |
| `hide_device_security_area` | Boolean | Optional | true |
| `hide_tpm_firmware_update_recommendation` | Boolean | Optional | false |
| `hide_tpm_troubleshooter_page` | Boolean | Optional | true |
| `disable_clear_tpm_button` | Boolean | Optional | true |
| `hide_secure_boot_area` | Boolean | Optional | true |
| `notifications` | String | Optional. Specifies the notification settings for the application guard. Values can bedisplay_all_notifications, display_only_critical_notifications, or disable_all_notifications. | display_all_notifications |
| `hide_family_options_area` | Boolean | Optional | true |
| `hide_device_performance_and_health_area` | Boolean | Optional | true |
| `hide_firewall_and_network_protection_area` | Boolean | Optional | true |
| `hide_virus_and_threat_protection_area` | Boolean | Optional | true |
| `hide_ransomware_data_recovery_area` | Boolean | Optional | true |
| `configure_customized_notifications` | Boolean | Optional | false |
| `show_customized_contact_information` | Boolean | Optional | false |
| `contact_company_name` | String | Required if‘show_customized_contact_information’is true. Specifies the company name for customized contact information in the application guard. |  |
| `contact_email` | String | Required if‘show_customized_contact_information’is true and when ‘contact_phone’ and ‘contact_website’ fields are not specified. Specifies the email address for customized contact information in the application guard. |  |
| `contact_phone` | String | Required if‘show_customized_contact_information’is true. and when ‘contact_email’ and ‘contact_website’ fields are not specified. Specifies the phone number for customized contact information in the application guard. |  |
| `contact_website` | String | Required if‘show_customized_contact_information’is true and when ‘contact_email’ and ‘contact_phone’ fields are not specified. Specifies the website URL for customized contact information in the application guard. |  |
| `hide_windows_security_systray` | Boolean | Optional. | false |
| `whitelist_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `blacklist_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `mandatory_apps` | Dictionary | Optional. A dictionary containing the explicit keysapp(whose value is a list of app IDs) andgroup(whose value is a list of app group IDs). | - |
| `catalogues` | List / Array | Optional. List of integers representing the corresponding catalogue IDs. | - |
| `-` | - | - | - |
| `-` | - | - | - |
| `-` | - | - | - |


---
