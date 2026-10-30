# VideoBx

VideoBx turns a web page into a broadcast video source on a Mac. It renders a page offscreen (with audio) and sends it out as:

- **NDI** (video and audio)
- **SDI** through a Blackmagic DeckLink card (optional)
- **SRT** (optional)

It is built for church and broadcast installs: drop it between a web page (lyrics, lower thirds, a streaming service, a dashboard) and vMix, ProPresenter, OBS, a switcher or a projector.

## Download

Get the latest build from the **[Releases](../../releases/latest)** page. Download the `.dmg`, open it and drag **VideoBx** to **Applications**. The `.zip` holds the same app plus a *READ ME FIRST* and the third-party licences.

Requirements: macOS 13 or later, Apple silicon or Intel.

## First launch

The app is not notarized by Apple, so macOS will block it the first time. Either:

- right-click **VideoBx** in Applications, choose **Open**, then click **Open**, or
- run this once in Terminal:

  ```
  xattr -dr com.apple.quarantine /Applications/VideoBx.app
  ```

## What it does

- **Web page to video:** any URL, with saved pages, back, forward, reload and freeze. Output size and frame rate are set in Settings.
- **Outputs:** NDI, DeckLink SDI and SRT, each switched on or off separately.
- **Audio routing:** page audio to NDI, with a level meter.
- **Control:** an HTTP API on port 8080 for Bitfocus Companion and scripts, ProPresenter RossTalk control, and TSL tally and UMD.
- **Test signal generator:** colour bars, ramps, grids, a motion box, an A/V sync pattern, and audio tones, GLITS, sweep and pink noise, all with an on-screen overlay.
- **Quality monitor:** a Leader-style waveform and vectorscope view.
- **Menus and Settings:** a modular side panel, a Settings window (⌘,) and menu-bar access to the main actions.

## Notes

- This repository only hosts the prebuilt downloads. The source is private.
- Includes the NDI runtime library. NDI is a trademark of Vizrt NDI AB. Other licences (libsrt, mbedTLS) are in the zip's *Third-party licences* folder.
- It is early software, tested mainly with NDI. DeckLink SDI and SRT on other receivers have had little real-hardware testing, so report anything odd.
