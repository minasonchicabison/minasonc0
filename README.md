# Customized Lucide fork

This is a customized copy of the original `lucideproxy/svg` project.

## Ad filtering removed

Ad filtering has been removed entirely. The proxy always uses the normal, unfiltered route (`/piers/`), the "Filter ads on proxied sites" setting no longer exists, and any previously saved `adblock` preference is ignored. This keeps game-streaming services such as GeForce NOW on the standard proxy route.

Websites opened through the proxy can display their own ads, since nothing filters them.

## Advertising cleanup

This fork removes the original app's injected advertising scripts and ad-promotional notices, and removes the original Google Analytics loader. Websites opened through the proxy can display their own ads; those ads come from the third-party website, not this app.

## Maintaining this fork

The original signed-release auto-updater has been disabled so it cannot silently replace this fork's customized files with files from the upstream repository. Update this fork by committing changes to your own GitHub repository. jsDelivr will serve the files from that repository.
