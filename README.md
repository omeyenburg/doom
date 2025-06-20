# Doom

This is a **minimally patched version** of the original 1997 open-source release of DOOM by id Software.

The goal of this fork is to keep the codebase as close to the original as possible, while making it buildable and runnable on modern Unix-like systems.

Most of the changes are related to:

- Fixing compiler issues on modern toolchains
- Replacing deprecated or obsolete X11 behavior
- Introducing minimal support for TrueColor visuals (24-bit)

## Usage

1. Obtain a WAD file (e.g. doom1.wad). These are widely available online.
2. Place the WAD file in the root directory of this repository.
3. Build the project by running:
   ```sh
   make -C linuxdoom-1.10
   ```
4. Run the executable:
   ```sh
   ./linuxdoom-1.10/linux/linuxxdoom
   ```
