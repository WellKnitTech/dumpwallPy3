## Introduction

This project converts SonicWall configuration export files into readable text output that can be versioned alongside the original `.exp` files in Git/SVN workflows.

This repository is a maintained fork of the original project. It keeps the tool Python 3 compatible and improves documentation and packaging hygiene while preserving the original purpose: making binary SonicWall exports easier to diff and audit.

## Current supported commands

## Requirements

- Python 3 (the script is now Python 3 only)

## Usage

Run the parser with Python 3 and an exported `.exp` configuration file:

```bash
python3 python/dumpwall.py -i sonicwall-TZ_210-5_9_0_4-127o.exp
```

Example output:

```
python3 python/dumpwall.py -i sonicwall-TZ_210-5_9_0_4-127o.exp
interface id '0' name 'X0' type 'Physical interface'
interface id '1' name 'X1' type 'Physical interface'
interface id '2' name 'X2' type 'Physical interface'
interface id '3' name 'X3' type 'Physical interface' portshield with 'X0'
interface id '4' name 'X4' type 'Physical interface' portshield with 'X0'
interface id '5' name 'X5' type 'Physical interface' portshield with 'X0'
interface id '6' name 'X6' type 'Physical interface' portshield with 'X0'
interface id '7' name 'U0' type 'Unknown' portshield with 'X0'
interface id '8' name 'U1' type 'Unknown' portshield with 'X0'
interface id '9' name 'X0:V90' type 'Virtual interface' vlan '90'
interface id '10' name 'X0:V100' type 'Virtual interface' vlan '100'
```

## Status

This program is a work in progress. The utility generates text-based dumps of saved configuration that can be printed and compared across versions using diff tools.

This fork (and the original software) is not associated with, related to, or sponsored by SonicWall or Dell. Use it at your own risk.

## License

This project is Free Software covered by the GNU General Public License, version 3 or any later version (GPL-3.0-or-later).


## GPL compliance notes

- The full GPLv3 license text is provided in both `LICENSE` and `COPYING`.
- Source files include an SPDX license identifier (`GPL-3.0-or-later`).
- This repository distributes source code directly, satisfying GPL source-availability requirements for this project distribution.
