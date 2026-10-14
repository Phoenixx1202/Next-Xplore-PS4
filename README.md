# Next-Xplore PS4

<img width="1917" height="1077" alt="image" src="https://github.com/user-attachments/assets/cc2230c7-2f5b-498a-b2f0-a859a0589cb8" />


**Next-Xplore** is a native PS4 file manager designed for fast, clear navigation through the system filesystem, internal storage, USB devices, files, folders and future archive and media features.


> Current status: functional alpha. Filesystem navigation and directory listing are available; write operations and advanced viewers are still in development.

## Goals

- Build a fast native file manager for PS4.
- Provide access to the filesystem outside the application sandbox on a compatible homebrew-enabled console.
- Bring internal storage, USB devices, files, folders, packages and media into one interface.
- Keep the interface clean, readable and optimized for the DualShock 4 controller.
- Detect the console language automatically with English as the fallback.

## Available features

### File explorer

- Starts at the root path `/`.
- The root shows directories only.
- Subfolders show both directories and files.
- Press **X** to enter, select or open an item.
- Press **O** to return to the parent directory.
- Automatic vertical scrolling when the list is larger than the panel.
- Folders are listed before files and sorted case-insensitively.
- Displays name, type, size and modification date.
- File icons for folders, images, videos, music, PKG, BIN, SFO and generic files.
- The `data` folder uses a yellow icon and `mnt` uses a purple icon.

### Storage devices

- Root filesystem access through `/`.
- Internal storage detection through `/dev_hdd0` and `/data` when available.
- Detection of already-mounted USB paths under `/mnt/usb0` to `/mnt/usb3` and `/usb0` to `/usb1`.
- Switch between available devices with **L1/R1**.
- USB icons are shown in the breadcrumb and the lower device card when a USB path is active.

### Root filesystem access

The project enables `LIBJBC` to restore the process credentials required to browse outside the application sandbox.

### Interface

- Three-column layout with sidebar, file list and details panel.
- Custom background, logo, application icon and startup artwork.
- Glassmorphism panels and cards.
- System clock and date.
- Native PS4 controller glyphs for X, O, square, triangle, L1 and R1.
- Visual scrollbar for long directory listings.

### Languages

The native interface uses the language reported by the PS4 system:

- English (`en-US`)
- French (`fr`)
- Spanish (`es`)
- Brazilian Portuguese (`pt-BR`)

English is used when the system language cannot be identified or a translation is unavailable. Explorer translations are stored in `resources/i18n/<locale>/next_xplore.json`.

## Planned features

### File operations

- Copy and paste files and folders.
- Move items between directories and storage devices.
- Rename files and folders.
- Delete items with confirmation.
- Create folders.
- Multi-selection.
- Filename search, filters and configurable sorting.

### Archive support

Archive support is planned, starting with:

- ZIP: browse, extract and create archives.
- TAR and GZ.
- 7Z.
- RAR, depending on library availability and distribution terms.

The intended behavior is to treat an archive as a virtual folder, allowing its contents to be viewed and extracted to the internal storage or a USB device without leaving the explorer.

### PKG support

- Read PKG metadata such as image, Title ID, title, version, Content ID and size.
- Browse package contents.
- Install PKG files from the explorer.
- Installation queue and progress feedback.

### Images, audio and video

- Image preview for common formats.
- Audio playback.
- Video playback.
- Codec, resolution, duration, audio-track and subtitle information.

### USB improvements

- Automatic USB mounting integration.
- Refresh the device list when a USB device is connected or removed.
- Display the device name when the system provides one.

## License and dependencies

Next-Xplore uses OpenOrbis and other open-source components. Each dependency retains its own license and distribution terms.
