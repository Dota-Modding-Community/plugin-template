# Dota 2 Minify - Plugin Template

A starter template for building plugins for [Dota 2 Minify](https://github.com/egezenn/dota2-minify).

## Mod Submission

Submit a PR to [community](https://github.com/Dota-Modding-Community/community) repository.

## Repository Structure

```text
plugin-template/
├── plugin/
│   ├── manifest.json       # Plugin metadata
│   ├── ui/                 # Installable plugin files
│   └── src/                # Editable source; excluded from release archives
├── .github/workflows/
│   └── release.yml         # Packages plugin/ and publishes a GitHub Release
└── README.md
```

## Getting Started

Update `plugin/manifest.json` for your plugin, then add its installable files to
`plugin/`. Keep editable source and build files in `plugin/src/`; this directory
is deliberately excluded from the release archive. Include generated/runtime
files outside `src/` (for example, in `plugin/ui/`) so they are shipped.

Push a version tag to publish a zip containing the contents of `plugin/`, other
than `plugin/src/`:

```bash
git tag v1.0.0
git push origin v1.0.0
```
