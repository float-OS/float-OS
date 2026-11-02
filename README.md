| [KR 한국어](./docs/locales/ko.md) | [US English](./README.md) | [JP 日本語](./docs/locales/ja.md) | [CN 简体中文](./docs/locales/zh-CN.md) | [ES Español](./docs/locales/es.md) |
| :---: | :---: | :---: | :---: | :---: |
| [FR Français](./docs/locales/fr.md) | [DE Deutsch](./docs/locales/de.md) | [RU Русский](./docs/locales/ru.md) | [SA العربية](./docs/locales/ar.md) | [IN हिन्दी](./docs/locales/hi.md) |

---

# Hey there, I'm Aidan Vance (`@float-OS`) 🛠️

```text
  _   _             _             ___  ____  
 | | | | ___ _   _  | |_ ___      / _ \/ ___| 
 | |_| |/ _ \ | | | | __/ _ \    | | | \___ \ 
 |  _  |  __/ |_| | | || (_) |   | |_| |___) |
 |_| |_|\___|\__, |  \__\___/_____\___/|____/ 
             |___/         |_____|            
  "If it cannot run on cold silicon without a network cable, it is a service, not a program."
```

I am a systems software engineer and hardware tinkerer based in Trondheim, Norway. By day, I design low-latency telemetry pipelines and deterministic real-time communication modules; by night, I build experimental capability-based microkernels, zero-allocation audio synthesizers, and compact command-line tooling.

I believe in software that respects memory, operates predictably under load, and outlives the hype cycle of transient frameworks.

---

## 🧭 Engineering Philosophy

- **Zero Allocation in the Hot Path**: If an inner loop touches a dynamic heap allocator, treat it as an architectural bug until proven otherwise.
- **Predictable Latency over Raw Peak Throughput**: A system that processes 100,000 req/sec with an unmanaged 2-second tail latency is broken for real-world cyber-physical control.
- **Mechanical Sympathy**: Know how cache lines align, how branch predictors guess, and where the memory controller bottlenecks before blaming the compiler.
- **Offline First & Self-Contained**: Tools should build cleanly with hermetic toolchains and run gracefully without calling home to external cloud telemetry.

---

## 🚀 Key Open-Source Projects

| Project | Focus | Language & Stack | Status |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Capability-based microkernel with synchronous zero-copy IPC for x86_64 and AArch64 | Rust, Zig, ASM | Active Architecture Phase |
| **`wave-forge`** | Zero-allocation, SIMD-accelerated modular DSP synthesis library (AVX2 / NEON) | Modern C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Immediate-mode terminal interface engine with sub-millisecond frame rendering | C99, POSIX / Win32 | Maintained |
| **`ferro-raft`** | Deterministic, log-structured distributed state-machine for air-gapped sensor nodes | Rust | Production in Field Kits |

---

## 🧰 Technology Matrix

### Systems & Languages
- **Primary Dialects**: Rust (core crates, `no_std`, embedded), Modern C++ (C++20/23, template metaprogramming, SIMD), Zig (cross-compilation tooling, runtime glue), C99/C11 (POSIX interfaces, driver layers).
- **Secondary / Scripting**: POSIX Shell, Python 3 (benchmarking scripts, plotting, signal simulation), Lua 5.4 (embedded engine scripting).
- **Assembly**: x86_64, AArch64, ARM Cortex-M (bare-metal startup code, context switching primitives).

### Tooling, Kernel & Embedded
- **Kernel & Runtimes**: QEMU, GDB / LLDB, perf, valgrind, Linux eBPF, FreeBSD bhyve.
- **Compilers & Toolchains**: Clang/LLVM toolchain, GCC cross-compilers, cargo, ninja, make.
- **Hardware & Signals**: Saleae Logic Pro 16, Siglent SDS1104X-E Oscilloscope, JTAG/SWD debug probes (ST-Link, J-Link), I2C/SPI bus sniffing.

### Protocols & Storage
- **Wire Protocols**: Zero-copy Cap'n Proto, FlatBuffers, custom binary framing over CAN / UART / UDP.
- **Storage Engines**: Log-Structured Merge (LSM) trees, memory-mapped ring buffers, raw NVMe block dispatch.

---

## 🔬 Workbench & Daily Driver Setup

```text
[Hardware Rig]
  ├── Host Machine : ThinkPad T480 (Core i7-8650U, 64GB DDR4, Dual 1TB NVMe, OpenBSD / Void Linux)
  ├── Lab Desktop  : Custom AMD Ryzen 9 7950X, 128GB ECC RAM, Debian 12 Stable (Hermetic build farm)
  ├── Audio Rig    : Custom Eurorack modular rack, Motu M4 DAC/ADC, Sennheiser HD600
  └── Keyboards    : Corne split ergonomic keyboard (Lubed Boba U4T switches, custom QMK firmware)
```

---

## 📈 Current Explorations

- Writing formal TLA+ specifications for asynchronous inter-process capability handshakes in `float-OS`.
- Investigating fixed-point arithmetic optimizations for polyphonic wave-table oscillators on resource-constrained Cortex-M4 targets.
- Experimenting with minimal self-hosting compiler backends that emit bare ELF binaries without linking libc.

---

## 📬 Reaching Out

I welcome technical discussions, thoughtful code reviews, bug reports, and conversations regarding systems programming, audio engineering, and minimalist tooling.

- **Email**: `float.os.kernel@gmail.com`
- **GPG Fingerprint**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` on Libera.Chat (`#osdev`, `#rust-embedded`)
- **Git Patch Flow**: Preferred submission via formatted git-send-email patches or pull requests.

---

<sub>Crafted by hand with plain Markdown. No external badges, no tracking scripts, 100% human-made.</sub>
