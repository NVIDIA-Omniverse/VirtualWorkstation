# launcher-release-pipeline

Template Repo for the Launcher Release Pipeline. Please refer to [Decoupled releases, Launcher and everything](https://docs.google.com/document/d/1g0ajB0a3NEpx2ned1jeSb75cTeih6VIMv2SNGmObusY/edit#heading=h.6pzdc6qye28n) for more information.

This template repo contains the configuration and CI jobs (via GitLab CI) to properly publish your product in the Launcher. Of course an API Key needs to be shared and a Product ID issued, but those are one time events when you set up to publish a new product. Please understand that in this context the word product covers apps, experiences, connectors, Nucleus, Cache, etc. Essentially anything that is “a thing” you can add to/remove from your Omniverse Library. 

Fork or Copy this repo (do not clone) and follow the same naming scheme but replace `launcher` with your app name. Example: For the Create app this repo was forked and renamed to `create-release-pipeline`.

The repo must contain the following files:
README.md
CHANGELOG.md
description.toml
launcher.toml
package.xml

Templates can be found in the **templates** folder.

Note that TOML is used because it’s the official configuration file format of Omniverse. For machine-to-machine communication we will often use json but not for human-to-machine communication.

When making new versions of a product a developer will create a new branch from the previous version, this is the same workflow as was outlined for the Workstation Installer repo. The branch name must include the version number. We have 3 buckets available depending on where this release should go. Your branch names should start with one of these 3 values and end with your version number:

- `DEV-XXXX` - Internal dev builds for daily testing
- `INTEG-XXXX` - Internal builds for release candidate testing
- `PROD-XXXX` - Production builds for full release to customer

# README.md

This is just the usual README explaining the purpose of the repo - will probably be mostly unchanged from the root fork version.

# CHANGELOG.md

This file will contain the changes made to the product leading up to this version. For most Launcher products this is simply a copy of text that should already exist in the development repos. Once packman contains this information in the packages we could also just source it from there automatically. But for now this is the simplest solution.

# description.toml

This file should contain a short description of the product and a URL to an icon.  A long-form description can also be included.

# launcher.toml

This is the star of the show - where the magic happens. It’s actually quite simple:
- A reference to the packman package
- A section with installation information (for many products this section isn’t needed)
- A section with launch information (some products will not need this)
