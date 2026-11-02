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

I am a senior systems software engineer and hardware tinkerer based in Trondheim, Norway. Over the past decade, my work has focused on low-latency telemetry pipelines, deterministic real-time communication protocols, and high-assurance systems architecture. Outside my day job, I build experimental capability-based microkernels, zero-allocation modular DSP engines, and minimal command-line tooling.

I design systems around first principles: rigorous memory boundaries, deterministic concurrency without data races, mechanical sympathy with CPU caches, and robust software that outlives transient framework trends.

---

## 🧭 Core Engineering Principles

- **Zero Allocation in the Hot Path**: Heap allocation inside high-frequency processing loops is treated as an architectural defect until mathematically proven unavoidable.
- **Deterministic Concurrency & Race-Freedom**: Lockless ring buffers, single-producer single-consumer queues, and capability-isolated message passing over shared-state locking.
- **Predictable Latency over Raw Peak Throughput**: A system handling 100,000 req/sec with unmanaged tail latency spikes is unacceptable for precision telemetry and cyber-physical control.
- **Mechanical Sympathy**: Design with direct awareness of L1/L2 cache lines, branch predictor behavior, and memory bus bandwidth rather than relying on compiler guesswork.
- **Defensive & Secure-by-Design**: Strict boundary isolation, constant-time cryptographic primitives, and hermetic offline build reproducibility.

---

## 🚀 Key Open-Source Projects

| Project | Domain | Architecture & Stack | Status |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Capability-based microkernel with synchronous zero-copy IPC for x86_64 & AArch64 | Rust, Zig, Bare-metal ASM | Active Development |
| **`wave-forge`** | Zero-allocation, SIMD-accelerated modular DSP audio synthesis library (AVX2 / NEON) | Modern C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Immediate-mode terminal interface engine with sub-millisecond frame dispatch | C99, POSIX / Win32 | Actively Maintained |
| **`ferro-raft`** | Deterministic, log-structured distributed state-machine for air-gapped sensor grids | Rust | Production Deployment |

---

## 🧰 Technology Matrix

### Systems & Languages
- **Primary**: Rust (core, `no_std`, embedded targets), Modern C++ (C++20/23, template metaprogramming, SIMD intrinsics), Zig (cross-platform toolchains, runtime glue), C99/C11 (POSIX interfaces, driver layers).
- **Secondary & Scripting**: POSIX Shell, Python 3 (benchmarking rigs, signal simulation, telemetry plotting), Lua 5.4 (embedded scripting).
- **Assembly**: x86_64, AArch64, ARM Cortex-M (bare-metal boot routines, context switching primitives).

### Architecture, Kernel & Tooling
- **Debugging & Profiling**: QEMU, GDB / LLDB, Linux perf, valgrind, Linux eBPF, FreeBSD bhyve.
- **Toolchains & Build Systems**: Clang/LLVM, GCC cross-compilers, cargo, ninja, make.
- **Hardware & Signals**: Saleae Logic Pro 16, Siglent SDS1104X-E Oscilloscope, JTAG/SWD debug probes (ST-Link, J-Link), I2C/SPI/CAN protocol analyzers.

### Protocols & Storage
- **Wire Protocols**: Zero-copy Cap'n Proto, FlatBuffers, custom binary framing over CAN / UART / UDP.
- **Storage Engines**: Log-Structured Merge (LSM) trees, memory-mapped ring buffers, raw NVMe block dispatch.

---

## 🔬 Hardware Workbench

```text
[Engineering Workbench]
  ├── Primary Rig  : ThinkPad T480 (Core i7-8650U, 64GB DDR4, Dual NVMe, OpenBSD / Void Linux)
  ├── Build Server : AMD Ryzen 9 7950X, 128GB ECC RAM, Debian 12 Stable (Hermetic build environment)
  ├── Audio Rig    : Custom Eurorack modular synthesizer, Motu M4 DAC/ADC, Sennheiser HD600
  └── Keyboards    : Corne split ergonomic keyboard (Lubed Boba U4T switches, custom QMK firmware)
```

---

## 📈 Ongoing Research & Focus Areas

- Writing formal TLA+ specifications for asynchronous inter-process capability handshakes in `float-OS`.
- Developing fixed-point arithmetic routines for polyphonic wave-table oscillators on resource-constrained Cortex-M4 silicon.
- Constructing minimal self-hosting compiler backends that emit bare ELF binaries without dynamic runtime dependencies.

---

## 📬 Contact & Collaboration

I welcome technical discussions, peer code reviews, defect reports, and conversations regarding systems programming, audio DSP, and minimalist software engineering.

- **Email**: `float.os.kernel@gmail.com`
- **GPG Fingerprint**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` on Libera.Chat (`#osdev`, `#rust-embedded`)
- **Git Contribution Flow**: Formatted `git-send-email` patches or GitHub pull requests.

---

<sub>Crafted by hand with plain Markdown. No external badges, no tracking scripts, 100% human-written.</sub>
