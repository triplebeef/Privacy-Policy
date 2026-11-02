# CipherPix Privacy Policy

**Updated:** 2 November 2026  
**App:** CipherPix (`com.cipherpix.app`) for Android  

> [!IMPORTANT]
> **In short:** CipherPix has no internet permission. It cannot send your photos, videos, files,
> passwords or anything else off your device, and the developer never receives any of it. There
> are no ads, analytics, crash reporting or tracking. CipherPix is built with privacy at its core.

## Contents

- [What CipherPix stores](#what-cipherpix-stores)
- [What CipherPix does not collect](#what-cipherpix-does-not-collect)
- [Permissions](#permissions)
- [Purchases and tips](#purchases-and-tips)
- [Sharing and exporting](#sharing-and-exporting)
- [Backups](#backups)
- [Deleting your data](#deleting-your-data)
- [Children](#children)
- [Changes to this policy](#changes-to-this-policy)
- [Contact](#contact)

## What CipherPix stores

Everything CipherPix stores stays on your device, or in a folder you choose yourself.

| Data | Where it is kept | How it is protected |
| --- | --- | --- |
| Photos, videos and files you add to the vault, with their names and types | App storage, or external storage if you choose it | Encrypted with AES-256-GCM using a key derived from your PIN, password or pattern |
| FakeSafe (decoy vault) contents | App storage | Encrypted separately, with its own credential |
| Intruder photos, if you turn on intruder detection | App storage | Encrypted with a key held in the Android Keystore |
| The time and number of failed attempts for each intruder photo | App storage, alongside the photo | Android's app sandbox |
| Settings, such as theme, language and lock options | App storage | Android's app sandbox |
| Whether you own Premium or a subscription | App storage | Android's app sandbox |
| Debug log, only if you turn on debug mode | App cache | Records only timestamps, item counts and the storage location, never file names or contents |

Your PIN, password and pattern are never stored. CipherPix keeps only an encrypted key that your
credential unlocks. If you forget your credential, the developer cannot recover your vault.

## What CipherPix does not collect

CipherPix does **not** collect, transmit, sell or share:

- your photos, videos, files or their names
- your PIN, password, pattern or biometric data
- your location, contacts, call logs or messages
- device identifiers, advertising IDs or usage analytics
- crash reports

CipherPix contains no advertising or analytics SDKs. The app's manifest removes the internet and
network-state permissions, so CipherPix itself has no network access at all.

## Permissions

Each permission is optional unless noted, and is used only on your device.

| Permission | Why CipherPix asks for it |
| --- | --- |
| Camera | The secure camera, which encrypts photos and videos as they are captured, and intruder detection |
| Microphone | Sound for videos taken with the secure camera |
| Photos and videos / storage / all files access | Importing items you pick into the vault, browsing folders in the built-in file browser, writing and restoring backups, and the photo gallery shown by the Photos disguise |
| Biometrics | Unlocking the vault with your fingerprint or face, if you turn it on. Android handles the biometric check; CipherPix never receives biometric data |
| Notifications | Progress of long imports and exports |
| Google Play billing | Buying Premium, subscribing, or leaving a tip through Google Play |

## Purchases and tips

Premium, the yearly subscription and tips are sold through **Google Play**. Payment is handled
entirely by the Google Play Store app; CipherPix never sees your payment details.

CipherPix receives only what Google Play reports about your purchases, such as which product you
bought and whether the payment is complete, and keeps on your device whether Premium is unlocked.
Google's handling of your purchase is covered by the
[Google Privacy Policy](https://policies.google.com/privacy).

## Sharing and exporting

Nothing leaves the vault unless you choose to export or share it.

- **Export** saves a decrypted copy of the items you choose to a location you choose. You can choose
  to remove location, camera and date details from exported photos.
- **Share without saving a copy** gives the app you pick temporary access to the items you choose,
  without writing an unencrypted copy to storage. Access ends after 10 minutes without use, after an
  hour at most, or when you lock the vault.

Once an item is shared or exported, the app or service that receives it handles it under its own
privacy policy.

## Backups

- **Android and Google cloud backup:** CipherPix excludes its data from Android's cloud backup and
  device-to-device transfer.
- **Local Backup and the persistent encrypted library:** these write encrypted `.cpx` files only to
  a folder you choose. Their contents stay encrypted. Keep them somewhere safe, since anyone with a
  copy can try to guess your password.

## Deleting your data

- **Uninstalling CipherPix** deletes everything in its app storage, including the vault, FakeSafe,
  intruder photos and settings.
- **Settings › Reset CipherPix** erases every vault and returns the app to its factory settings.
- **Backups and persistent library files** in folders you chose are not deleted by uninstalling.
  Delete them yourself from that folder.
- **Purchase records** are kept by Google Play. See your Google account for those.

Because the developer never receives your data, there is nothing for the developer to delete on
request.

## Children

CipherPix is not directed at children under 13 and does not knowingly collect information from
anyone, including children.

## Changes to this policy

If this policy changes, the new version will be published at this address with a new effective
date. Significant changes will also be noted in the app's changelog.

## Contact

Questions about this policy can be sent to **triplebeef28@gmail.com**.
