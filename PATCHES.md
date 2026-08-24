# Local Patches

## Phase 9.9.0.8.2: Minimal VLCKit PiP Diagnostic Fork and Start Repair

- Extend `VLCPictureInPictureWindowControlling` protocol in `VLCDrawable.h` with state properties and event handlers.
- Add `requestStartPictureInPicture` to `VLCPictureInPictureWindowControlling`.
- Expose internal AVKit PiP state (`isPictureInPicturePossible`, `isPictureInPictureActive`, `isPictureInPictureSuspended`) from `AVPictureInPictureController`.
- Expose `pictureInPictureController:failedToStartPictureInPictureWithError:` delegate callback in `VLCPictureInPictureController.m`.
- Expose exact PiP lifecycle events.
- Instrument the SampleBuffer renderer (`VLCSampleBufferDisplay.m`) for UI window and layer state.

## Phase R1.3J / R1.4F: LGPL Compliance and Player-Only Profile

- `0015-apple-build.conf-disable-gpl-modules.patch`: Strips GPL modules (`syslog`, `rotate`, `motion`, `sap`, `stream_out_rtp`) for strict LGPL v2.1 compliance.
- `0016-apple-build.conf-player-only-profile.patch`: Implements reproducible `YEEVLCKIT_PROFILE=player-only` (disabling stream output, VLM, and unused encoders/muxers while preserving 100% of audio and video decoders).
