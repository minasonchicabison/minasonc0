# Customized Lucide fork

This is a customized copy of the original `lucideproxy/svg` project.

## GeForce NOW compatibility and ad filtering

Ad filtering is **OFF by default** so game-streaming services such as GeForce NOW use the normal proxy route. On the first load after this update, the app also performs a one-time migration that changes an older saved `adblock: true` preference to OFF. After that migration, the setting remains under your control.

Open **Settings → Browsing → Filter ads on proxied sites** to change it:

- **ON** uses the filtered proxy route (`/fairs/`).
- **OFF** uses the normal, unfiltered proxy route (`/piers/`). Keep it OFF when using GeForce NOW if the filtered route interferes with sign-in, streaming, or game launch.

This is a global proxy setting, not a GeForce NOW-only exception: turning filtering off also allows third-party websites elsewhere to display their own ads. Changing the switch saves the setting and restarts the proxy controller with the selected route. After changing it, allow the controller to restart before opening the site you want to use.

## Advertising cleanup

This fork removes the original app's injected advertising scripts and ad-promotional notices, and removes the original Google Analytics loader. Websites opened through the proxy can still display their own ads when filtering is OFF; those ads come from the third-party website, not this app.

## Maintaining this fork

The original signed-release auto-updater has been disabled so it cannot silently replace this fork's customized files with files from the upstream repository. Update this fork by committing changes to your own GitHub repository. jsDelivr will serve the files from that repository.
