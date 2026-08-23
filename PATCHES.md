# Local Patches

## Phase 9.9.0.8.2: Minimal VLCKit PiP Diagnostic Fork and Start Repair

- Extend `VLCPictureInPictureWindowControlling` protocol in `VLCDrawable.h` with state properties and event handlers.
- Add `requestStartPictureInPicture` to `VLCPictureInPictureWindowControlling`.
- Expose internal AVKit PiP state (`isPictureInPicturePossible`, `isPictureInPictureActive`, `isPictureInPictureSuspended`) from `AVPictureInPictureController`.
- Expose `pictureInPictureController:failedToStartPictureInPictureWithError:` delegate callback in `VLCPictureInPictureController.m`.
- Expose exact PiP lifecycle events.
- Instrument the SampleBuffer renderer (`VLCSampleBufferDisplay.m`) for UI window and layer state.
