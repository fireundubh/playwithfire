<!-- TITLE: Using Steam to Download Previous Versions -->

[&larr; Divinity Series](/divinity)

If you want to see more resources like this, [become a Patreon supporter!](https://www.patreon.com/fireundubh) 

# Using Steam to Download Previous Versions
## Step by Step

1. With Steam running, press `Win+R` and enter this URL: `steam://nav/console` ([link](steam://nav/console)).
2. Enter the following command: `download_depot <app_id> <depot_id> <manifest_id>` (refer to the Reference tables below)
3. The depot will begin downloading. You should receive a notification when the download is complete.

The depot will likely download to: `C:\Program Files (x86)\Steam\steamapps\content\app_435150\depot_xxxxxx\` (or wherever Steam is installed)

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
`167072590693741559` | `???` | August 31, 2018 – 01:29:08 UTC
`1171886874743914236` | `???` | August 30, 2018 – 16:31:59 UTC
`244373317272729760` | `???` | May 16, 2018 – 15:13:57 UTC
`1389547995064105059` | `???` | May 16, 2018 – 07:34:06 UTC
`191036283777788044` | `???` | March 21, 2018 – 16:44:44 UTC
`5046830741005571502` | `???` | March 7, 2018 – 16:13:01 UTC
`2256105192537027573` | `???` | February 12, 2018 – 15:16:22 UTC
`267319309418886073` | `???` | February 2, 2018 – 20:12:48 UTC
`3398161497796942030` | `???` | February 1, 2018 – 15:00:39 UTC
`7007123960744699418` | `???` | January 18, 2018 – 16:52:15 UTC
`5421202735820611391` | `???` | December 20, 2017 – 13:50:30 UTC
`4074285774433215355` | `???` | December 7, 2017 – 10:20:54 UTC
`5893374657274645937` | `???` | December 5, 2017 – 15:25:55 UTC
`203109788023908411` | `???` | November 3, 2017 – 16:30:15 UTC
`565713323437375164` | `???` | October 31, 2017 – 14:44:38 UTC
`2101725439366670610` | `???` | October 27, 2017 – 18:00:13 UTC
`8669483029989635186` | `???` | October 26, 2017 – 14:32:20 UTC
`6763538787763586284` | `???` | October 9, 2017 – 16:01:36 UTC
`6924015759185419165` | `???` | October 9, 2017 – 14:33:38 UTC
`5032607589693146677` | `???` | October 7, 2017 – 18:30:11 UTC
`3481662379655802339` | `???` | October 6, 2017 – 11:28:46 UTC
`6502635156278872050` | `???` | September 28, 2017 – 14:04:29 UTC
`5346795891051093195` | `???` | September 21, 2017 – 22:48:24 UTC
`6094009947358344996` | `???` | September 21, 2017 – 20:04:11 UTC
`1713994409719494278` | `???` | September 21, 2017 – 16:42:18 UTC
`7285063415068754865` | `???` | September 21, 2017 – 11:39:32 UTC
`4915083391496169033` | `???` | September 18, 2017 – 19:16:12 UTC
`2864838041695293605` | `???` | September 17, 2017 – 18:52:00 UTC
`7634517375182509514` | `???` | September 15, 2017 – 18:01:35 UTC
`1428015599965561224` | `???` | September 14, 2017 – 20:50:37 UTC
`5753691202891746710` | `???` | September 14, 2017 – 14:53:11 UTC
`2565278018179312552` | `???` | May 26, 2017 – 12:36:54 UTC
`7787012528413011186` | `???` | May 24, 2017 – 14:56:27 UTC
`5775428352633111097` | `???` | March 31, 2017 – 11:02:37 UTC
`7189509260682239857` | `???` | March 28, 2017 – 14:35:36 UTC
`7390093447938671847` | `???` | February 9, 2017 – 15:45:51 UTC
`8382597800282017479` | `???` | February 2, 2017 – 14:21:10 UTC
`5651734831006894397` | `3.0.15.252` | December 1, 2016 – 15:41:08 UTC
`313863331557428430` | `3.0.5.530` | October 19, 2016 – 17:17:10 UTC
`7010031956707004956` | `2.0.165.341` | September 16, 2016 – 12:28:04 UTC
`176056573245315941` | `2.0.164.992` | September 15, 2016 – 17:11:33 UTC

## Other Depots and Manifests

You can [find additional depots and manifests](https://steamdb.info/app/435150/depots/) at SteamDB.