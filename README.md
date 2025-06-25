# Doom

This is a **minimally patched version** of the original 1997 open-source release of DOOM by id Software.

The goal of this fork is to keep the codebase as close to the original as possible, while making it buildable and runnable on modern Unix-like systems.

Most of the changes are related to:

- Fixing compiler issues on modern toolchains.
- Replacing deprecated or obsolete X11 behavior.
- Introducing support for TrueColor visuals (24-bit).

## Usage

1. Build the project.
   ```sh
   make -C linuxdoom-1.10
   ```
2. Run the executable. This assumes that you have a WAD file. See [WAD files](#wad-files).
   ```sh
   ./linuxdoom-1.10/linux/linuxxdoom
   ```

## WAD files

WAD files contain the game’s data: levels, graphics, music, sounds, and more.

There are two types:
- **IWADs** (Internal WADs): Standalone game data files used as the base for playing Doom.
  - Examples: `doom.wad` (full registered Doom), `doom2.wad`, `tnt.wad`, `plutonia.wad`
  - `doom1.wad` is the shareware IWAD and only includes the first episode.
- **PWADs** (Patch WADs): Add-on or replacement data that modifies or extends an IWAD.

To play Doom with an IWAD:
```sh
./linuxdoom-1.10/linux/linuxxdoom -iwad /path/to/doom.wad
```

To play with an additional PWAD:
```sh
./linuxdoom-1.10/linux/linuxxdoom -iwad /path/to/doom.wad -file mymap.wad
```

If `-iwad` is not specified, Doom will look for an IWAD in the current directory,
or in paths specified by `DOOMWADDIR` or `DOOMWADPATH` environment variables.

## Command-line arguments

### New command-line arguments
- `-5`, `-6`, `-7`, `-8`: Additional screen scaling factors. These behave similarly to the original `-2`, `-3` and `-4` options.

### Original Doom arguments

You can find the full list of parameters on the [Doom parameter reference](https://doomwiki.org/wiki/Parameter)
and the [Unix port command-line options](https://doomwiki.org/wiki/Unix_port_parameters).
