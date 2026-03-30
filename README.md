# AltTextLab GTM Template

A tag template for **Google Tag Manager (Web)** that connects the AltTextLab Web Snippet and automatically generates alt-text for images.

- Loads the AltTextLab Web Snippet from a CDN
- Improves accessibility (WCAG/ADA) and SEO
- Works without changing your website code (via GTM)

## Requirements

- **Google Tag Manager Web** container
- AltTextLab access data:
  - `Site ID`
  - `Public Key`

## Install in GTM
1. Install the GTM template
2. On [https://app.alttextlab.com/web-snippets](https://app.alttextlab.com/web-snippets) create a new Web Snippet and copy the provided `Site ID` and `Public Key`
3. Publish the tag

## Configure the tag

Fill in the fields:

- `Site ID` - the site identifier in AltTextLab
- `Public Key` - the project public key
- `Language` - the generation language (default `en`)
- `Style` - text style:
  - `descriptive`
  - `neutral` (default)
  - `matter-of-fact`
  - `minimal`

Recommended start trigger: **All Pages**.

## Check that it works

1. In GTM enable **Preview**
2. Open your site and make sure the tag fired
3. In DevTools verify:
   - the presence of `window.__alttextlab_config`
   - that `https://cdn.alttextlab.com/embed.js` is loaded

## Template permissions

The template uses standard GTM permissions:

- `access_globals` - access to `__alttextlab_config`
- `inject_script` - loads the script from `https://cdn.alttextlab.com/embed.js*`
- `logging` - logging in debug environments

## Possible issues

- The tag doesn't fire: check the trigger and container publication
- No output: make sure `Site ID` and `Public Key` are set correctly

## Useful links

- Site: https://www.alttextlab.com/
- Web Snippet documentation: https://www.alttextlab.com/docs/web-snippet

