# Photo-Collage Maintenance Agent

## Scope
This repository is independent. Never modify `rifansukarno-sys/my-learning-os` or any other repository unless explicitly instructed.

## Product contract
- Mobile-first static web app; no backend required.
- Maximum 25 photos.
- Device picker, camera capture, and desktop drag/drop.
- JPG/JPEG, PNG, WebP, GIF, BMP, AVIF and HEIC/HEIF when the HEIC decoder CDN is reachable.
- No photo upload to an application server.
- Every selected photo must appear in the collage; never render an empty slot.
- Users can reorder photos, select a photo, and change that photo's crop focus.
- Export PNG and JPG.

## Maintenance rules
1. Preserve the 25-photo limit and client-side privacy model.
2. Never introduce a server dependency for image bytes unless explicitly requested.
3. Test odd counts: 1, 2, 3, 4, 5, 7, 10, 13, 17, 25.
4. Test add, add-again, reset-during-load, delete, reorder, export, and layout changes.
5. Test touch/pointer interactions and keyboard activation of the picker.
6. Treat HEIC as an optional dependency: fail clearly, never crash the whole editor.
7. Keep export disabled while images are loading.
8. Avoid unbounded canvas dimensions and memory growth.
9. Keep accessibility labels on icon-only controls.
10. Before shipping, inspect the final file for JavaScript syntax errors and verify that every UI control has a handler.

## Agent behavior
When asked to maintain the app: inspect first, identify regressions, fix only this repository, add/update tests or CI where practical, and report exact commits and remaining environment limitations. Never claim device coverage that was not actually tested.
