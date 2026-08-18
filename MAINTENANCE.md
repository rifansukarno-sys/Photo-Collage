# Maintenance & Release Checklist

This project uses a lightweight maintenance-agent contract in `AGENTS.md` plus a GitHub Actions quality gate in `.github/workflows/maintenance.yml`.

## Before every release

- [ ] Verify the editor loads with zero JavaScript syntax errors.
- [ ] Add 1, 2, 3, 4, 5, 7, 10, 13, 17 and 25 images.
- [ ] Confirm every image is visible and there are no empty cells.
- [ ] Add a second batch and verify the total never exceeds 25.
- [ ] Reset while images are loading and verify no stale image returns.
- [ ] Delete first, middle and last images.
- [ ] Reorder with drag and with ↑/↓ controls.
- [ ] Select an image and change horizontal/vertical focus.
- [ ] Drag the selected image directly in the preview on touch/pointer devices.
- [ ] Test Fit and Fill.
- [ ] Test all layouts and background choices.
- [ ] Export PNG and JPG after loading completes.
- [ ] Test desktop and narrow mobile layouts.
- [ ] Test HEIC/HEIF with internet available and confirm a clear fallback message when the decoder cannot load.
- [ ] Confirm no application server receives image bytes.

## Non-negotiable scope

Only `rifansukarno-sys/Photo-Collage` is in scope for this product. Do not touch `rifansukarno-sys/my-learning-os` without an explicit user request.
