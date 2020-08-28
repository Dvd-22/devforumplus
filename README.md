# devforumplus

A browser extension designed to makes the Roblox DevForum that bit nicer.

Feel free to port to other browsers if you want, the main part is just `devforumplus.js`.

## Install

Firefox: https://addons.mozilla.org/en-US/firefox/addon/devforum/

Chrome: https://chrome.google.com/webstore/detail/devforum%20/obannamndmafaddpcghdkilafpcckebl

## Features

- Completely hide users' posts (WIP, may break some things)
- Flairs the OP
- Flairs new members (as network efficient as it can be; one request per user, caches for tab life)
- Highlights posts by Roblox staff members (useful for skimming announcements)
- Highlights excessive bumps (it gets redder the more of a bump it is)
- PM Templates

## Known bugs

- Flairs disappear when you expand a previous reply.
- Roblox account is marked as new member

## Contributions

PRs welcome. Please respect the style guide in the editorconfig and prettierrc.

### Development

Webpack is used to build the final `devforumplus.js` file because I hate browser js.

The actual code is in the `src` file, with `src/index.js` being the entry point.

See the `webpack.config.js` for more information.

### Compiling for release (Firefox)

`npm run prerelease-firefox` will call webpack (to build devforumplus.js) and will use the
`web-ext build` command in Mozilla's Extension Workshop to create the .zip file.
