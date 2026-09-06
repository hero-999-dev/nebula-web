# nebula-web

The documentation site for **[Nebula](https://github.com/hero-999-dev/nebula)**,
behind a password gate.

**https://hero-999-dev.github.io/nebula-web/**

The app itself is open source and its installers are public — the gate is here
so the documentation link does not travel further than it is handed to. Nothing
behind it would be a problem to read.

## How it works

`index.html` asks for a password and derives
`p-<sha256("nebula:<password>")[:20]>/` in the browser. Neither the password nor
the directory name appears in the page source; a wrong password requests a
directory that does not exist and gets a 404.

## Do not edit the page by hand

The page inside the gate directory is generated. It is
`site/index.html` in the Nebula repository, built by `npm run site` and pushed
here by `npm run publish-site` at the end of every release. An edit made here
would be overwritten by the next release.

## The app

| | |
|---|---|
| Source | https://github.com/hero-999-dev/nebula |
| Download | https://github.com/hero-999-dev/nebula/releases/latest |
