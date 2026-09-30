# PALASTHOTEL Gallery Sharing

> **Deprecated — no longer maintained.**
> Version 1.0.1 is the final release. Please deactivate and delete the plugin.

This plugin let editors share galleries between separate WordPress installations:
it registered a public API endpoint on each site and inserted a shortcode that
fetched a gallery's rendered HTML from another site over HTTP.

## Why it is deprecated

- **Unused.** Palasthotel no longer runs it on any site, and it has very few
  installations elsewhere.
- **Obsolete UI.** The whole authoring flow is a classic-editor TinyMCE button
  (`mce_buttons` / `mce_external_plugins`). It never appears in the block editor,
  the WordPress default since 5.0 (2018), so on any current WordPress the plugin
  is effectively invisible.
- **Unmaintained since 2017**, last tested against WordPress 4.7.
- **Insecure by design.** Sharing works by fetching rendered HTML across sites and
  storing remote HTTP Basic Auth credentials in plain options. Making it safe would
  mean rewriting its model, which is not worth it for an unused feature.

There is no successor plugin.

## Final release (1.0.1)

The last release closes one concrete security issue and adds the deprecation
notice. Before the fix, the unauthenticated gallery endpoint
(`/__api/ph_gallery_sharing/get/{id}`) rendered a gallery post's content
regardless of its status, so **draft, pending and private galleries were exposed
to anonymous requests**. It now serves only published galleries (or posts the
current user may read).

Known, unfixed issues (the plugin is retired — deactivate and delete instead of
relying on it): the settings form has no nonce (CSRF), and it stores and displays
remote Basic Auth credentials in plain text.

## What to do

Deactivate and delete the plugin. Any `[ph-gallery-sharing]` shortcodes will stop
rendering shared galleries; remove them from affected posts.

## License

GPL-3.0-or-later. See [LICENSE](LICENSE).
