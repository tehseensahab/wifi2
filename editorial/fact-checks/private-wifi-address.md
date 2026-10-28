# Fact-check record: private-wifi-address

Internal record. Not published. Research date: 2026-10-28.

## Research log

| # | Claim | Verbatim quote | Source | Pub / effective date | Geography | Qualifications |
|---|---|---|---|---|---|---|
| 1 | Apple: Fixed option | "When set to Fixed, your device uses a private address, but the private address doesn't rotate..." | https://support.apple.com/en-nz/102509 | Published Dec 9, 2025 | global | |
| 2 | Apple: Rotating every two weeks | "When set to Rotating, your device uses a private address that rotates to a different private address every two weeks." | same | | | |
| 3 | Apple: Off uses hardware MAC | "When set to Off, your device uses its hardware MAC address." | same | | | |
| 4 | Apple: privacy reason | "This allows a kind of user tracking or profiling that affects all devices on all Wi-Fi networks." | same | | | refers to a constant address |
| 5 | Apple: update before turning off | "If your device can't join a Wi-Fi network, can't access network resources or the internet after joining..." / "you should install the latest software updates. Then try again before you decide whether to turn this feature off." | same | | | |
| 6 | Apple: Off/Fixed/Rotating need iOS 18 etc.; earlier systems on/off | (fetch summary) choices require iOS 18, iPadOS 18, macOS Sequoia 15, watchOS 11, visionOS 2 or later; earlier: on or off | same | | | paraphrase from fetch; fact-checker to confirm |
| 7 | Apple: default Fixed for WPA2+; Rotating for weak/no security | (fetch summary) Fixed "default for new networks using WPA2 or stronger security"; Rotating default for weak or no security | same | | | paraphrase; fact-checker to confirm |
| 8 | Apple: reset network settings → new address | "it uses a different private address the next time it joins the network" (after a reset) | https://support.apple.com/guide/platform-support/sup56da67cfd/web ("Manage private Wi-Fi settings on iPhone and iPad") | | | |
| 9 | Apple: private addresses can interfere with systems relying on device identification | "private Wi-Fi addresses might be interfering with network systems that rely on device identification."; "Network uses MAC address filtering or device identification systems" | same | | | |
| 10 | Apple steps iPhone | Settings > Wi-Fi > More Info button > Private Wi-Fi Address (Off/Fixed/Rotating on iOS 18+) | 102509 | | | paraphrase of steps |
| 11 | Android 10+ randomized by default | "For devices running Android 10 or higher, the framework uses a randomized MAC address by default." | https://source.android.com/docs/core/connect/wifi-mac-randomization-behavior | last updated 2026-10-09 | global (AOSP) | manufacturers may customize |
| 12 | Android: disabling uses factory MAC | "If you disable MAC randomization for a network, the framework uses the factory MAC address (globally unique address)." | same | | | |
| 13 | Android persistent MAC until factory reset; forget/re-add doesn't change | "This MAC address remains the same until a factory reset."; "The MAC address doesn't get re-randomized if you forget and re-add the Wi-Fi network, because the MAC address depends on the network profile's parameters." | same | | | persistent mode is the default |
| 14 | Android non-persistent conditions | "The DHCP lease duration has expired and more than 4 hours have elapsed since the device last disconnected from this network."; "The current randomized MAC for the network profile was generated more than 24 hours ago." | same | | | Android 12+, only some networks (app request or OEM overlay off by default) |
| 15 | Android steps (ASUS) | "Tap Network and Internet." "Select Wi-Fi." "Tap the gear icon next to your home Wi-Fi connection." "Tap MAC address type." "Select Device MAC." | https://www.asus.com/us/support/FAQ/1044277 | Last Update 2026/02/10 | | menu names vary by phone maker |
| 16 | ASUS: device appears as new after MAC changes | "after your device is assigned a new MAC address, that device appears in device list as a newly connected device." | same | | | |
| 17 | ASUS: affected features | "Content filters assigned to a specific device will not work if the MAC address changes."; "MAC and IP Address Binding"; "Wireless MAC Filter"; "Any MAC related features will be affected." | same | | | |
| 18 | eero: affected features | "IP reservations and port forwarding"; "New device notifications"; "Device nicknames and identification"; "Pausing and blocking devices"; "Profile assignment and schedules" | https://eero.com/support/articles/what-is-mac-address-randomization | no date | US | |
| 19 | eero: home vs public | "MAC address randomization is a good way to protect your privacy in public places."; "this protection may not be necessary for devices in your home" | same | | | |
| 20 | Linksys: recommends Fixed over Rotating | Fixed "masks the true MAC address of your device and will use a unique, non-rotating MAC address," "This option is recommended."; Rotating: "This option is NOT recommended if you are using any of the features mentioned above." | https://support.linksys.com/kb/article/170 | no date | | |
| 21 | Linksys: parental controls schedules fail | "the device keeps getting online during the scheduled time" | same | | | |
| 22 | Windows random hardware addresses: steps and purpose | Settings > Network & internet > Wi-Fi > Random hardware addresses; per network via Manage known networks; "make it harder for people to track you when your device scans for networks and connects" | https://support.microsoft.com/windows/060ad2e9-526e-4f1c-9f3d-fe6a842640ed | no date | | |

## Independent fact-check (2026-10-28, separate agent)

Re-fetched: Apple 102509, Microsoft, ASUS FAQ 1044277, Linksys KB 170.

Apple verbatim confirmed: "Your device will choose Fixed by default when joining a new network that uses WPA2 or stronger security."; "Your device will choose Rotating by default when joining a new network that uses weak security or no security."; forgetting a network forgets its private address "unless it has been less than 24 hours since the last time it was made to forget that network" (iOS 18 etc.; two weeks earlier); Mac three-way choice "Requires macOS Sequoia 15 or later". Microsoft page applies to "Windows 10 Windows 11"; "If your Wi-Fi hardware supports it". ASUS affected list confirmed ("Time Scheduling," "Block Internet Access," "Web & Apps Filters," "DHCP Server – Manually Assigned IP," "MAC and IP Address Binding," "Wireless MAC Filter"). Linksys: "Instant-Privacy," "Linksys Parental Controls," "MAC Filtering".

- VERIFIED: Off/Fixed/Rotating definitions, two-week rotation, defaults, version gate, tracking and update quotes, reset behavior, Android quotes, Windows, eero, ASUS, Linksys rows.
- NOT VERIFIED, fixed: 24-hour exception misread (counts from last time network was forgotten, not rejoin) → corrected in body and FAQ.
- QUALIFIED, fixed: "stops networks from tracking" → "makes it harder"; "Android calls the setting" → "on many Android phones"; Windows hardware-support caveat added; Fixed + reservation caveat adds "or forget the network"; eero reasoning separated from eero quote; "Rotating will break it" → "when the address changes, about every two weeks"; non-persistent Android wording softened.
