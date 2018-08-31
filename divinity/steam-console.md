<!-- TITLE: Using Steam to Download Previous Versions -->

[&larr; Divinity Series](/divinity)

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Using Steam to Download Previous Versions
## Step by Step

1. With Steam running, press `Win+R` and enter this URL: `steam://nav/console` ([link](steam://nav/console)).
2. Enter the following command: `download_depot <app_id> <depot_id> <manifest_id>` (refer to the Reference tables below)
3. The depot will begin downloading. You should receive a notification when the download is complete.

The depot will likely download to: `C:\Program Files (x86)\Steam\steamapps\content\app_379430\depot_37943x\` (or wherever Steam is installed)

Once downloaded, you can move the depot anywhere.

## Syntax

```
download_depot <app_id> <depot_id> <manifest_id> [<delta_manifest_id>]
```

Parameter | Required | Description
--- | --- | ---
`app_id` | `true` | the game's App ID
`depot_id` | `true` | the Depot ID corresponding to a content package (e.g., binaries, game assets)
`manifest_id` | `true` | the Manifest ID corresponding to a version of the content package
`delta_manifest_id` | `false` | the Manifest ID corresponding to a previous version of the content package

If the `delta_manifest_id` argument is not omitted, Steam will download only the differences between the target manifest and delta manifest.

## Optional

### Change the download path

You cannot change the path to which the depot downloads; however, you can "trick" Steam into downloading depots wherever you want using Junction Points.

What are Junction Points? Junction Points are a type of symbolic link unique to the NTFS file system.

If Steam was installed on your `C:` drive, and you wanted to download the depot to `D:`, you would do the following:

1. Delete the `app_435150` folder, if any, in `C:\Program Files (x86)\Steam\steamapps\content`.
2. Create a folder on `D:` named `app_435150`, such as `D:\app_435150`.
3. In a cmd shell, type: `mklink /J "C:\Program Files (x86)\Steam\steamapps\content\app_435150" "D:\app_435150"`
4. Then, run the `download_depot` command in the Steam Console.

If you do not know how to open the cmd shell, press `Win+R`, type `cmd`, and press `Enter`.

## Reference

### App and Depots

Type | Value | Description
--- | --- | ---
App ID | `435150` | Divinity: Original Sin 2
Depot ID | `435151` | Content - This depot contains the game assets and binaries.
Depot ID | `717550` | Engine Data - This depot contains engine assets for the editor.

### Depot: Content

Manifest ID | Version | Date
--- | --- | ---
`176056573245315941` | `2.0.164.992` | September 15, 2016 – 17:11:33 UTC

## Other Depots and Manifests

You can [find additional depots and manifests](https://steamdb.info/app/379430/depots/) at SteamDB.