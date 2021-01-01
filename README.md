# QMK Userspace

> Cloud build your QMK keymaps

TODO:

- [ ] automatically use qmk_firmware fork if it exists
- [ ] refactor github actions to script
- [ ] add build filter for community layouts

## Getting Started

1. Fork this template repo
1. Add keymap files
1. Wait for your firmware files to be automatically built for you!

## Adding Keymaps

TODO: add structure example

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

## Official Website

[qmk.fm](https://qmk.fm) is the official website of QMK, where you can find links to this page, the documentation, and the keyboards supported by QMK.
