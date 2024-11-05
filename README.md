# rpcapd-android-builds

This repository hosts pre-built Android executables for `rpcapd`, compiled for multiple architectures using the GCC and musl toolchain. The executables are built with optimization and static linking to support a wide range of Android devices and environments.

## About rpcapd

`rpcapd` is a remote packet capture daemon that enables capturing network packets over a remote connection. It is particularly useful for debugging, network monitoring, and forensic analysis on Android devices.

## Build Details

The executables in this repository are compiled with the following specifications:

- **Compiler**: GCC with musl toolchain
- **Compilation Flags**: `-O2 -static -fPIE`
- **Supported Architectures**:
  - `aarch64`
  - `arm`
  - `i686`
  - `x86_64`

These settings ensure efficient performance, static linking for portability, and Position Independent Executable (PIE) support, which enhances security on Android platforms.

## Dependencies

- [libpcap](https://github.com/the-tcpdump-group/libpcap): `rpcapd` relies on `libpcap` for packet capturing functionality. `libpcap` provides a portable framework for low-level network traffic capture.
- [libxcrypt](https://github.com/besser82/libxcrypt): This project also uses `libxcrypt` for cryptographic functionalities, enhancing security and password hashing compatibility.

For further details on `libpcap` and `libxcrypt`, please refer to their official repositories.

## Usage

To use the `rpcapd` executable on your Android device, download the appropriate binary for your device's architecture, then transfer and set executable permissions. Usage examples and additional setup may vary based on your specific Android environment.

## Disclaimer

Please ensure that you have permission to perform network packet capture on the target device. Unauthorized network monitoring may violate privacy and security policies.

## License

This repository follows the licensing of `rpcapd`, `libpcap`, and `libxcrypt`. Please refer to the original projects' licenses for details.
