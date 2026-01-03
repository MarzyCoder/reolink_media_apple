Reolink Apple HLS Playback (Home Assistant)

This repository contains a custom Home Assistant integration that wraps the core
Reolink integration and adds ffmpeg-backed HLS playback for Apple/Safari clients.

What it does:
- Reuses the core Reolink integration for devices, entities, and media browsing.
- Adds HLS proxy endpoints under `/api/reolink/hls/...` to serve VOD through ffmpeg.
- Uses a Safari user-agent check in the media source to route playback to HLS,
  while other browsers follow the default core playback behavior.

Notes:
- ffmpeg must be available in the Home Assistant container.
- This integration does not replace the core Reolink integration; it extends it.
