# Getting Started

## Adding Keymaps

Summary of the expected structure:
```
├── keymaps
│   ├── clueboard_california_keymap.json
│   ├── dz60
│   │   └── keymap.c
│   └── jj50_keymap.c
├── layouts
│   └── ortho_4x12
│       └── keymap.c
├── rules.mk
├── config.h
├── <user>.c
└── <user>.h
```

#### Supports:

* Regular keymaps
* Configurator exports
* Community layouts

#### Usual userspace items:

The following should exist at the top level of the repo:

* `<user>.h`
* `<user>.c`
* `config.h`
* `rules.mk`

Apply to all keyboards, see <https://docs.qmk.fm/#/feature_userspace> for more info.

#### Conversion table:

| Type | qmk_firmware | qmk_userspace |
|---|---|---|
| Simple flat | `keyboards/<keyboard>/keymaps/<user>/keymap.c` | `keymaps/<keyboard>_keymap.c` |
| Configurator export | `keyboards/<keyboard>/keymaps/<user>/keymap.json` | `keymaps/<keyboard>_keymap.json` |
| Regular old keymap | `keyboards/<keyboard>/keymaps/<user>/keymap.c`<br>`keyboards/<keyboard>/keymaps/<user>/config.h` | `keymaps/<keyboard>/keymap.c`<br>`keymaps/<keyboard>/config.h` |
| Keymap within revision | `keyboards/<keyboard>/<revision>/keymaps/<user>/keymap.c` | `keymaps/<keyboard>/<revision>/keymap.c` |
| Community layout | `layouts/community/<layout>/<user>/keymap.c` | `layouts/<layout>/keymap.c` |

## Configuration

The defaults will work for most users. However for those who want to tinker, a `.env` file at the root of the repo can be customized with the following options:

| Variable | Default | Notes|
|---|---|---|
| QMK_USER | `<GitHub_Username>` | Ideal if your username does not conform to the QMK keymap name rules |
| QMK_REPO | qmk/qmk_firmware | Can be used to point to another qmk_firmware fork, maybe your own? |
| QMK_REF | master | Can be set to the name of a branch ( eg `develop`) or to an exact commit ( eg `53e9213a2255cebf9ec2c3f8302241ede8d16f07`) |

The format for setting the above is the usual dotenv format:

```properties
QMK_REPO=zvecr/qmk_firmware
QMK_REF=53e9213a2255cebf9ec2c3f8302241ede8d16f07
```

## Local Development

TODO