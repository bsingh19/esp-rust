# RUST on ESP32 

Follow this book for more information - [Book](https://esp-rs.github.io/book/introduction.html)

# Setup on Windows 11 (tested)
## Step 1 - rustup
1. Download and install rustup [Download](https://rustup.rs/)
2. Make sure you follow the steps
3. It will instal Visual Studio

Install following tools
```shell
$ cargo install cargo-generate
$ cargo install ldproxy
$ cargo install cargo-espflash
```

## Step 2 - espup
Follow the RISC-V and Xtensa targets [here](https://esp-rs.github.io/book/installation/index.html#risc-v-and-xtensa-targets)
1. cargo will be installed in last step, make sure you add  *C:\Users\USER_NAME\.cargo\bin* in system **PATH**.
2. Install espup
```shell 
cargo install espup
```
3. Once espup is installed, do the following:
```shell
espup install
```
4. On each terminal session first run following (Windows - %USERPROFILE%\export-esp.ps1)
```shell
. \path\export-esp.ps1
```

## Step 3 - Tools
1. cargo-espflash 
```shell
cargo install cargo-espflash
```
2. espmonitor
```shell
cargo install espmonitor
```

3. cargo-espflash 
```shell
cargo install cargo-espflash
```

## Step 4 - Template Code Example
```shell
$ cargo generate --git https://github.com/esp-rs/esp-idf-template cargo
🤷   Project Name : esp-rust-app
🔧   Destination: /home/alice/esp-rust-app ...
🔧   Generating template ...
✔ 🤷   MCU · esp32
✔ 🤷   Configure project to use Dev Containers (VS Code, GitHub Codespaces and Gitpod)? (beware: Dev Containers not available for esp-idf v4.3.2) · false
✔ 🤷   STD support · true
✔ 🤷   ESP-IDF native build version (v4.3.2 = previous stable, v4.4 = stable, mainline = UNSTABLE) · v4.4
[ 1/10]   Done: .cargo/config.toml
[ 2/10]   Done: .cargo
[ 3/10]   Done: .gitignore
[ 4/10]   Done: .vscode
[ 5/10]   Done: Cargo.toml
[ 6/10]   Done: build.rs
[ 7/10]   Done: rust-toolchain.toml
[ 8/10]   Done: sdkconfig.defaults
[ 9/10]   Done: src/main.rs
[10/10]   Done: src
🔧   Moving generated files into: `/home/alice/esp-rust-app`...
💡   Initializing a fresh Git repository
✨   Done! New project created /home/alice/esp-rust-app
```

## Step 5 - Build
```shell
cargo build
```

## Step 6 - Flash
Make sure you change directory to you project folder (app_folder)
```shell
espflash COM15 .\target\xtensa-esp32-none-elf\debug\app_folder
```

## Step 7 - Monitor
```shell
espflash serial-monitor COM15
```

# References
1. Connect ESP32 to WiFi with Rust - [here](https://medium.com/@rajeshpachaikani/connect-esp32-to-wifi-with-rust-7d12532f539b)
2. Rust on ESP-IDF "Hello, World" template - [here](https://github.com/esp-rs/esp-idf-template)
3. Rust on ESP-IDF "Hello, World" with PlatformIO - [here](https://github.com/esp-rs/esp-idf-template/blob/master/README-pio.md)
4. Rust - [here](https://www.rust-lang.org/)
5. Rust on ESP32 - [here](https://kerkour.com/rust-on-esp32)
6. Libraries, crates and examples for using Rust on Espressif SoC's [esp-rs](https://github.com/esp-rs)
7. Awesome ESP Rust [here](https://github.com/esp-rs/awesome-esp-rust)
8. Embedded Rust on Espressif [ESPRESSIF](https://esp-rs.github.io/espressif-trainings/01_intro.html)
