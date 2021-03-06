<!-- TITLE: Using Steam to Download Previous Versions -->

[&larr; Kingdom Come](/kingdomcome)

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

### Examples

Download the v1.6.2 game assets:

```
download_depot 379430 379432 7120882668146484686
```

Download the v1.6.2 binaries:

```
download_depot 379430 379433 8342093289043735329
```

Download only the v1.6.2 game assets that have changed since v1.6:

```
download_depot 379430 379432 7120882668146484686 6018900492685079222
```

## Optional

### Change the download path

You cannot change the path to which the depot downloads; however, you can "trick" Steam into downloading depots wherever you want using Junction Points.

What are Junction Points? Junction Points are a type of symbolic link unique to the NTFS file system.

If Steam was installed on your `C:` drive, and you wanted to download the depot to `D:`, you would do the following:

1. Delete the `app_379430` folder, if any, in `C:\Program Files (x86)\Steam\steamapps\content`.
2. Create a folder on `D:` named `app_379430`, such as `D:\app_379430`.
3. In a cmd shell, type: `mklink /J "C:\Program Files (x86)\Steam\steamapps\content\app_379430" "D:\app_379430"`
4. Then, run the `download_depot` command in the Steam Console.

If you do not know how to open the cmd shell, press `Win+R`, type `cmd`, and press `Enter`.

## Reference

### App and Depots

Type | Value | Description
--- | --- | ---
App ID | `379430` | Kingdom Come: Deliverance
Depot ID | `379432` | goldmaster - This depot contains the game assets. (Max size: 37.17 GB)
Depot ID | `379433` | goldmaster_bin - This depot contains the game binaries. (Max size: 43.6 MB)

### Depot: goldmaster

#### Reference

```
download_depot 379430 379432 4726149695433587359 7992763947464641746
```

#### Table

Date | Manifest ID | Version | Patch Notes
:--- | :--- | :--- | :---
2018-11-21 14:57:20 UTC | `6574029890339916306` | 1.7.2 | 
2018-10-24 15:00:06 UTC | `4726149695433587359` | 1.7.1 | 
2018-10-18 10:40:32 UTC | `7992763947464641746` | | CN Localization Hotfix
2018-10-16 15:04:50 UTC | `5591422340763860770` | 1.7 | 
2018-07-31 15:01:27 UTC | `7120882668146484686` | 1.6.2 | 
2018-07-05 18:10:20 UTC | `6968523114347920066` | 1.6.x | 
2018-06-27 14:27:07 UTC | `7785937864061191860` | 1.6.x | 
2018-06-26 08:19:10 UTC | `6018900492685079222` | 1.6 | 
2018-06-05 11:40:00 UTC | `554336772426200654` | 1.5 | 
2018-04-25 15:12:03 UTC | `6599714174046783889` | 1.4.3 | 
2018-04-09 17:36:43 UTC | `1956773116114829879` | 1.4.2 | 
2018-03-30 16:01:30 UTC | `3366038057672856335` | 1.4.1 | 
2018-03-29 23:16:26 UTC | `5725479270789300781` | 1.4 | without HD textures
2018-03-29 20:34:19 UTC | `8087559557021397984` | 1.4 | with HD textures
2018-03-23 18:52:42 UTC | `5914698958093409181` | 1.3.4 | 
2018-03-14 12:05:18 UTC | `2336283802842258594` | 1.3.3 | 
2018-03-10 17:01:41 UTC | `5466979519765255293` | 1.3.2 | 
2018-03-09 18:02:55 UTC | `6648306801271692541` | 1.3.1 | 
2018-03-09 15:23:15 UTC | `5922355296132692872` | 1.3 | 
2018-02-21 16:55:57 UTC | `189591112647295182` | 1.2.5 | Hotfix
2018-02-20 16:07:25 UTC | `5015448431446448432` | 1.2.5 | 
2018-02-13 19:09:01 UTC | `7728356487649391633` | 1.2 | Chinese localization
2018-02-13 08:01:41 UTC | `1574197374724500814` | 1.1 | 


### Depot: goldmaster_bin

#### Reference

```
download_depot 379430 379433 2399540122942266164 4111290527857171027
```

#### Table

Date | Manifest ID | Version
:--- | :--- | :---
2018-11-21 14:57:20 UTC | `7294492902202468617` | 1.7.2
2018-10-24 15:00:06 UTC | `2399540122942266164` | 1.7.1
2018-10-16 15:04:50 UTC | `4111290527857171027` | 1.7
2018-07-31 15:01:27 UTC | `8342093289043735329` | 1.6.2
2018-06-26 08:19:10 UTC | `8575847395542381973` | 1.6
2018-06-05 11:40:00 UTC | `5023449653178090326` | 1.5
2018-04-25 15:12:03 UTC | `7196528537818374131` | 1.4.3
2018-04-09 17:36:43 UTC | `2984004457424079313` | 1.4.2
2018-03-30 16:01:30 UTC | `1106887327694715381` | 1.4.1
2018-03-29 20:34:19 UTC | `1406427307048670137` | 1.4
2018-03-23 18:52:42 UTC | `7411158086922740023` | 1.3.4
2018-03-14 12:05:18 UTC | `8258487847145245731` | 1.3.3
2018-03-09 18:02:55 UTC | `6942593791365390981` | 1.3.1
2018-03-09 15:23:15 UTC | `7652858052225644863` | 1.3
2018-02-20 16:07:25 UTC | `4042719886608370500` | 1.2.5
2018-02-15 09:05:12 UTC | `3337151599264696796` | 1.2.2
2018-02-14 12:37:09 UTC | `8998644657350293708` | 1.2.1
2018-02-13 19:09:01 UTC | `4430868609853567107` | 1.2
2018-02-13 08:01:41 UTC | `4903570955311779730` | 1.1

## Other Depots and Manifests

You can [find additional depots and manifests](https://steamdb.info/app/379430/depots/) at SteamDB.