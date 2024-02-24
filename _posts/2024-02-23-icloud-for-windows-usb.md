---
layout: post
title: "iCloud for Windows on USB"
slug: icloud-for-windows-usb
categories: software apple icloud icloud-for-windows
date: 2024-02-23T23:45:37.968Z
---

I wanted to have my iCloud Drive and Photos automatically backed up to an external USB drive using iCloud for Windows. You know, because having backups are important.

We'll unfortunately need to use Windows's Command Prompt and also utilize the `mklink` command to create a symbolic link, with the `/J` option (to create a Directory Junction).

## iCloud Drive

1. In iCloud for Windows, Turn off iCloud Drive; it will have you remove all files via `Delete from PC`. And in File Explorer, delete the `iCloudDrive`.

2. Create a symbolic link by opening the Command Prompt and run the following (make sure to edit before running):

    ```sh
    mklink /J "C:\Users\chris\iCloudDrive" "D:\iCloudDrive"
    ```

3. Create the `iCloudDrive` folder on the USB drive.

4. In iCloud for Windows, Turn on iCloud Drive and select the symbolic link as the location.

If iCloud for Windows starts mistakenly delete your iCloud Drive files, see [Recovering A Bad Sync](#recovering-a-bad-sync).

## iCloud Photos

We're going to do almost the same with iCloud Photos.

1. In iCloud for Windows, Turn off iCloud Photos; it will have you remove all files via `Delete from PC`. (same with Shared Albums if you want those backed up as well.). And in File Explorer, delete the `iCloud Photos` from within your Pictures folder.

1. Create a symbolic link by opening the Command Prompt and run the following (make sure to edit before running):

    ```sh
    mklink /J "C:\Users\chris\Pictures\iCloud Photos" "D:\iCloud Photos"
    ```

1. Create the `iCloud Photos` folder on the USB drive.

1. You'll also need to create the `Photos` folder and the `Shared` *within* the `iCloud Photos` folder

1. In iCloud for Windows, Turn on iCloud Photos (and Shared Albums if you want those backed up as well.) and select the symbolic link as the location.

### Recovering A Bad Sync

If you ran into the same issue as me, where iCloud for Windows mistakenly deleted all photos after syncing to a blank location, do not worry!

1. Simply open up [iCloud on the web](https://www.icloud.com/).
2. Open iCloud Photos or iCloud Drive.
3. Click on Recently Deleted.
4. Select the first item and use shift+click to select the last item.
5. On the top right, click "Recover".
