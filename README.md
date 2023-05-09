<a href="https://mutant.revolt.chat">
    <img src="https://raw.githubusercontent.com/mutant-remix/.github/master/assets/banner.png" style="margin: 20px 0; width: 80%"></img>
</a>

This repository contains all of the files required to build a custom Mutant Remix package using Orxporter.

Mutant Remix is not affiliated with [Mutant Standard](https://mutant.tech/). This is a transformation of the original Mutant Standard emoji pack, created by nizune for [Revolt](https://revolt.chat/).

## Download
You can download the latest release of Mutant Remix from the [releases page](https://github.com/mutant-remix/mutant-remix/releases)

Alternatively, you can [build it yourself](#building)

## Contributing
If you would like to contribute to Mutant Remix, please read the [CONTRIBUTING guide](./CONTRIBUTING.md).

You can see the full list of contributors in [CONTRIBUTORS](./CONTRIBUTORS.md).

## Building

To build Mutant Remix, clone this repository recursively or otherwise run:

```bash
git submodule init
git submodule update
```

### Prerequisites
This repository has no warranty and has only been tested with Arch Linux. Windows users may need to use WSL and users of other distributions may need to use Docker.

Check out the [contributing guide](./CONTRIBUTING.md) for a more comprehensive explanation.

You will need:
- [Orxporter prerequisites](https://github.com/mutant-remix/orxporter#prerequisites)
- [Node.js](https://nodejs.org/en/)
- `yarn`
- `wget`

### Script usage
- Calculate unicode coverage
    - Generate `out/test_json/mtnt_test.json`
    - Generate `out/coverage/coverage.md`, `json`, `png` and `svg`
```
sh out_coverage.sh
```

- Short tests instead of building the full pack every time
```
sh out_test_svg.sh # ideal for development
sh out_test_png.sh
sh out_final_basic.sh
sh out_web_content_json.sh
```

- Build the full pack
```
sh out_final_full.sh
sh out_web_content.sh
```

## License

Everything directly in this repository is licensed under a [Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License](https://creativecommons.org/licenses/by-nc-sa/4.0/). Refer to separate licenses in the `assets`, `coverag-calculator`, `forc` and `orxporter` submodules for their respective licenses.
