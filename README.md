# dircolors-hd

[![Build Status](https://travis-ci.org/sharkdp/dircolors-hd.svg?branch=master)](https://travis-ci.org/sharkdp/dircolors-hd)

**WORK IN PROGRESS**

A manager for `LS_COLORS` expressions (similar to `dircolors`). It uses a YAML-based configuration
file for the [filetype-database](config/filetypes.yml) and the [color themes](themes/molokai.yml).

Usage:
``` bash
export LS_COLORS="$(dircolors-hd generate filetypes.yml --theme themes/molokai.yml)"
```

![Preview of "ls -R"](https://i.imgur.com/oekLIya.png)

## True color

By default, `dircolors-hd` runs in truecolor mode (24-bit). If you don't use a [terminal
that supports 24-bit colors](https://gist.github.com/XVilka/8346728), use the `--color-mode 8-bit`
option when running `dircolors-hd`.

## Installation

### On Debian-based systems

``` bash
wget "https://github.com/sharkdp/dircolors-hd/releases/download/v0.1.0/dircolors-hd_0.1.0_amd64.deb"
sudo dpkg -i dircolors-hd_0.1.0_amd64.deb
```

### On other distrubutions

Check out the [release page](https://github.com/sharkdp/dircolors-hd/releases) for binary builds.

### Via cargo

If you have Rust 1.30 or higher, you can install `dircolors-hd` from source via `cargo`:
```
cargo install dircolors-hd
```

## License

Licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Similar and related projects

- https://github.com/karlding/dirchromatic
- https://github.com/trapd00r/LS_COLORS
- https://geoff.greer.fm/lscolors/
- `LS_COLORS` themes:
   - https://github.com/seebi/dircolors-solarized
   - https://github.com/ivoarch/dircolors-zenburn
   - https://github.com/arcticicestudio/nord-dircolors
