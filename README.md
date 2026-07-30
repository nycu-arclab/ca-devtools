# CA Development Tools

Prebuilt development tools for the Computer Architecture course.

## Releases

- `linux_2026`: Ubuntu 24.04 x86-64
- `apple_darwin_2026`: macOS

## Included Tools

- RISC-V GNU Compiler Toolchain 14.2.0
- Icarus Verilog 12.0

## Linux Installation

Download the tools:

```bash
cd ~

wget https://github.com/nycu-arclab/ca-devtools/releases/download/linux_2026/riscv32-unknown-elf-gcc-14.2.0-linux.tar.gz

wget https://github.com/nycu-arclab/ca-devtools/releases/download/linux_2026/iverilog-12-linux.tar.gz
```

Install the tools:

```bash
sudo tar -xzvf riscv32-unknown-elf-gcc-14.2.0-linux.tar.gz -C /opt
sudo tar -xzvf iverilog-12-linux.tar.gz -C /
```

Add them to `PATH`:

```bash
echo 'export PATH=/opt/riscv/bin:/opt/iverilog-12/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
```

Verify the installation:

```bash
riscv32-unknown-elf-gcc --version
iverilog -V
```

## Licensing

The distributed binaries were built without modifications to the upstream source code. This repository does not introduce additional licensing terms beyond those of the respective upstream projects.

The tools are redistributed under their respective upstream licenses.

Source code and license information are available from the upstream projects:

- [RISC-V GNU Compiler Toolchain](https://github.com/riscv-collab/riscv-gnu-toolchain)
- [Icarus Verilog](https://github.com/steveicarus/iverilog)

Copyright remains with the respective upstream authors and contributors.
