# MSFS Addon Dispatch

**Organize your add-ons. Find your next destination. Prepare what the simulator loads.**

MSFS Addon Dispatch is a Windows add-on manager for **Microsoft Flight Simulator 2024**. Keep your add-ons in a library outside Community, browse them as covers, a list or scenery points on an offline map, and activate the content you want for your next flight.

[**Download the latest version**](https://github.com/lavoied/msfs-addon-dispatch-Releases/releases/latest) · [Release notes](https://github.com/lavoied/msfs-addon-dispatch-Releases/releases)

## What you can do

- **Manage an existing library.** Scan your library, including its subfolders, to discover add-ons and read package information from their manifests.
- **Import archives.** Drop ZIP, RAR or 7z files onto the application, or use **Add new addon**. Review the detected information and keep editing tags, subcategories and other details while extraction runs. Multiple archives can be queued together. Archives containing multiple MSFS packages are not supported yet.
- **Activate content without duplicating it.** Dispatch creates directory links in Community. Deactivating an add-on removes its link while keeping its source files in your library.
- **Organize your collection.** Use configurable subcategories, shared tags, favorites and star ratings. Filter by category, country, developer, tags, rating or activation status.
- **Choose your view.** Browse image covers with adjustable sizes, or use a sortable list with resizable, reorderable and selectable columns.
- **Explore scenery on an offline map.** View scenery with detected coordinates, including individual airports within multi-airport packs. Activate or deactivate add-ons using the map, including a selected area.
- **Personalize thumbnails.** Keep package images, paste an image from the clipboard or use Google Images to find one. Optional in-app image search is available with your own Serper API key. Store multiple thumbnails and select a main image.
- **Reuse your setup.** Save frequently used filters as pinned views and save active add-on sets as activation groups.
- **Keep track of your data.** View installed versions, added and updated dates, folder sizes and available location information. Use manual database backups or enable weekly backups.
- **Stay up to date.** Dispatch can check for updates at startup and display an indicator beside **About**. You decide when to install an available update.

The interface is available in **English and French**, with **Day and Night** modes.

## Getting started

1. Download **MSFSAddonDispatch.exe** from the [latest release](https://github.com/lavoied/msfs-addon-dispatch-Releases/releases/latest), place it in a writable folder and run it.
2. In the welcome setup, select your **MSFS 2024 Community folder**. Use automatic detection if available, then verify the selected path.
3. Select your **add-on library folder**. Use a separate folder from Community; your existing subfolder organization can stay in place.
4. Run **Scan** to build the catalog. Run it again after adding or changing add-on folders manually.
5. Browse, filter and activate the add-ons you need for your flight.

To import a new archive, drag it anywhere onto the application window or click **Add new addon**.

## Understanding the sidebar

![Annotated guide to the MSFS Addon Dispatch sidebar](images/sidebar-guide.png)

*The illustration currently uses French annotations. The explanations below describe the same controls in English.*

### Add new addon

Open the import window with the button, or drop one or more ZIP, RAR or 7z archives onto Dispatch. Each import entry lets you review the add-on information and assign tags and a subcategory.

### Uncategorized

Find add-ons that do not have a subcategory yet. Select an add-on and use the Details panel to classify it.

### Pinned views

A pinned view remembers a set of filters, such as scenery in a particular country or add-ons with a specific tag. Configure your filters, choose **Pin view**, and give the view a name. Click it later to restore those criteria.

Pinned views change **what you see**, not which add-ons are active. Removing a pinned view does not delete its add-ons.

### Activation groups

An activation group stores a set of add-ons to use together.

1. Activate the add-ons you want to include.
2. Click **+** beside **Activation Groups** and enter a name.
3. Use the menu beside the group to **Apply**, **Edit**, **Rename** or **Delete** it.

**Apply** activates the group's members and deactivates other add-ons in the configured library. Clicking a group name alone does not apply it. **Edit** lets you change its members, then save or cancel. Deleting a group does not delete the add-on files.

> **Pinned views save what you want to see. Activation groups save what you want to activate.**

## Requirements

- **Windows 10 or Windows 11, x64.**
- **Microsoft Flight Simulator 2024.** Dispatch currently targets MSFS 2024.
- **Microsoft Edge WebView2 Runtime.** It is included with Windows 11 and already installed on the vast majority of Windows 10 devices. If Dispatch reports that it is missing, install the **Evergreen WebView2 Runtime** from [Microsoft's official download page](https://developer.microsoft.com/en-us/microsoft-edge/webview2/#download-section).

The portable release does **not** require a separate .NET installation or an installed copy of 7-Zip. Internet access is used for update checks and online image searches; the scenery map works offline.

## Settings, backups and troubleshooting

Settings, the SQLite catalog, custom thumbnails, backups and diagnostic logs are stored in:

```text
%LOCALAPPDATA%\MSFSAddonDispatch
```

The executable is portable; its user data is stored in LocalAppData rather than beside the executable. Updates preserve that data.

In **Settings**, you can create a database backup, open the backup folder or schedule a restore. Diagnostic logs are available through **Open logs folder** and are retained for 14 days with size-based rotation.

## About this repository

This repository contains the application's **public releases**, user-facing documentation and the manifest used by the update checker. It does not contain the application source code.

See the [release notes](https://github.com/lavoied/msfs-addon-dispatch-Releases/releases) for the changes in each published version.
