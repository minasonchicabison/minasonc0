# Customized Lucide fork

This is a customized copy of the original `lucideproxy/svg` project.

## Ad-filter setting

Open **Settings → Browsing → Ad filtering on proxied sites**.

- **ON** uses the filtered proxy route (`/fairs/`).
- **OFF** uses the normal, unfiltered proxy route (`/piers/`). This fully bypasses the ad-filtering route and is the recommended setting to try when GeForce NOW streaming, sign-in, or game launch is affected.

Changing the switch saves the setting and restarts the proxy controller with the selected route. After changing it, allow the controller to restart before opening the site you want to use.

## Advertising cleanup

This fork removes the original app's injected advertising scripts and ad-promotional notices, and removes the original Google Analytics loader. Websites opened through the proxy can still display their own ads when filtering is OFF; those ads come from the third-party website, not this app.

## Maintaining this fork

The original signed-release auto-updater has been disabled so it cannot silently replace this fork's customized files with files from the upstream repository. Update this fork by committing changes to your own GitHub repository. jsDelivr will serve the files from that repository.
