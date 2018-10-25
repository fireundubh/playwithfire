<!-- TITLE: Using Steam to Download Previous Versions -->

[&larr; Pathfinder: Kingmaker](/kingmaker)

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Using Steam to Download Previous Versions
## Step by Step

1. With Steam running, press `Win+R` and enter this URL: `steam://nav/console` ([link](steam://nav/console)).
2. Enter the following command: `download_depot <app_id> <depot_id> <manifest_id>` (refer to the Reference tables below)
3. The depot will begin downloading. You should receive a notification when the download is complete.

The depot will likely download to: `C:\Program Files (x86)\Steam\steamapps\content\app_640820\depot_640821\` (or wherever Steam is installed)

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

### Example

Download the game content:

```
download_depot 640820 640821 6741447117850778077
```

## Optional

### Change the download path

You cannot change the path to which the depot downloads; however, you can "trick" Steam into downloading depots wherever you want using Junction Points.

What are Junction Points? Junction Points are a type of symbolic link unique to the NTFS file system.

If Steam was installed on your `C:` drive, and you wanted to download the depot to `D:`, you would do the following:

1. Delete the `app_640820` folder, if any, in `C:\Program Files (x86)\Steam\steamapps\content`.
2. Create a folder on `D:` named `app_640820`, such as `D:\app_640820`.
3. In a cmd shell, type: `mklink /J "C:\Program Files (x86)\Steam\steamapps\content\app_640820" "D:\app_640820"`
4. Then, run the `download_depot` command in the Steam Console.

If you do not know how to open the cmd shell, press `Win+R`, type `cmd`, and press `Enter`.

## Reference

### App and Depots

Type | Value | Description
:--- | :--- | :---
App ID | `640820` | Pathfinder: Kingmaker
Depot ID | `640821` | Pathfinder: Kingmaker Content

### Depot: _Pathfinder: Kingmaker Content_

Manifest ID | Version | Date | Size (GB) | Comments
:--- | :--- | :--- | ---: | :---
`332037904899851076` | 1.0.13 | October 25, 2018 – 10:31:50 UTC | |
`6319724708078102732` | 1.0.12 | October 24, 2018 – 10:31:45 UTC | 8.03 | Size delta
`6843022900013123261` | 1.0.11 | October 22, 2018 – 10:20:05 UTC | 9.79 | Size delta
`4137201467282432792` | 1.0.10 | October 18, 2018 – 09:55:03 UTC | 8.02 | Size delta
`3329346642708156469` | 1.0.9 | October 16, 2018 – 11:47:06 UTC | 15.2 | Size delta
`7773343900112385919` | 1.0.8c | October 12, 2018 – 18:21:28 UTC | 4.78 | Size delta
`4551845841087663139` | 1.0.8b | October 11, 2018 – 15:07:55 UTC | 20.8 | Size delta
`5750998838144035341` | 1.0.7 | October 9, 2018 – 13:38:33 UTC | 23.49 | Size delta
`3625063316203614488` |  | October 8, 2018 – 19:33:21 UTC | 7.04 | Size delta with `946625482595150857`
`403950949019027651` |  | October 7, 2018 – 14:22:42 UTC | 2.9 | Size delta, no binaries, audio only
`946625482595150857` |  | October 7, 2018 – 13:17:17 UTC | 23.8 | Size delta
`6336459653349909543` | 1.0.6 | October 5, 2018 – 15:50:10 UTC | | Forgot to get size
`7894022154904016667` | 1.0.5 | October 5, 2018 – 09:08:33 UTC | 15.5 | Size delta
`4920380694923421717` |  | October 3, 2018 – 04:47:08 UTC | | Forgot to get size
`6358573070219561752` | 1.0.4 | October 2, 2018 – 16:30:02 UTC | 10.7 | Size delta
`229482041491868730` | 1.0.3 | September 29, 2018 – 18:17:02 UTC | 9.81 | Size delta
`2451367926564256244` | 1.0.2 | September 28, 2018 – 18:13:51 UTC | 10.7 | Size delta
`1412067188604596331` | 1.0.1 | September 27, 2018 – 16:48:23 UTC | 7.42 | Size delta
`336132831154623931` |  | September 25, 2018 – 14:20:24 UTC | 5.49 | Size delta
`6741447117850778077` |  | September 25, 2018 – 14:02:04 UTC |  34.3 | Assets only, no binaries

## Other Depots and Manifests

You can [find additional depots and manifests](https://steamdb.info/app/640820/depots/) at SteamDB.