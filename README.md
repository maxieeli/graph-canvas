# Building

## Build skia from source

## Pull pre-build skia binary from GitHub

You can pull skia pre-build binaries if you just care the `Rust` part:

```sh
# Clone the code:
$ git clone --recurse-submodules https://github.com/Brooooooklyn/canvas.git
$ cd canvas

# Download Skia binaries:
# It will pull the binaries match the git hash in `./skia` submodule
$ node scripts/release-skia-binary.js --download

# Install NPM packages, build the Node.js addon:
$ npm install -g yarn
$ yarn install --mode=skip-build
$ sudo dnf install clang # https://fedora.pkgs.org/34/fedora-x86_64/clang-12.0.0-0.3.rc1.fc34.x86_64.rpm.html
$ yarn build

# All done! Run test cases or examples now:
$ yarn test
$ node example/tiger.js
```
