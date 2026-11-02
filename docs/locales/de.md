| [KR 한국어](./ko.md) | [US English](../../README.md) | [JP 日本語](./ja.md) | [CN 简体中文](./zh-CN.md) | [ES Español](./es.md) |
| :---: | :---: | :---: | :---: | :---: |
| [FR Français](./fr.md) | [DE Deutsch](./de.md) | [RU Русский](./ru.md) | [SA العربية](./ar.md) | [IN हिन्दी](./hi.md) |

---

# Hallo, ich bin Aidan Vance (`@float-OS`) 🛠️

```text
  _   _             _             ___  ____  
 | | | | ___ _   _  | |_ ___      / _ \/ ___| 
 | |_| |/ _ \ | | | | __/ _ \    | | | \___ \ 
 |  _  |  __/ |_| | | || (_) |   | |_| |___) |
 |_| |_|\___|\__, |  \__\___/_____\___/|____/ 
             |___/         |_____|            
  "Wenn ein Programm nicht auf kaltem Silizium ohne Netzwerkkabel laufen kann, ist es ein Dienst, kein Programm."
```

Ich bin Systemsoftware-Entwickler und Hardware-Bastler aus Trondheim, Norwegen. Tagsüber entwerfe ich Telemetrie-Pipelines mit extrem geringer Latenz und deterministische Echtzeit-Kommunikationsmodule; nachts entwickle ich experimentelle, fähigkeitsbasierte Mikrokernels, heapanalysierende DSP-Audiosynthesizer ohne dynamische Allokation und kompakte Kommandozeilenwerkzeuge.

Ich schätze Software, die sparsam mit Speicher umgeht, unter Volllast vorhersagbar arbeitet und den schnellen Hype-Zyklus kurzlebiger Web-Frameworks überdauert.

---

## 🧭 Technische Grundsätze

- **Keine dynamische Allokation im kritischen Pfad (Hot Path)**: Wenn eine innere Schleife den dynamischen Heap-Allokator berührt, gilt dies als architektonischer Fehler, solange nicht das Gegenteil bewiesen ist.
- **Vorhersagbare Latenz vor rohem Spitzendurchsatz**: Ein System, das 100.000 Anfragen pro Sekunde verarbeitet, dabei aber eine unkontrollierte Tail-Latenz von 2 Sekunden aufweist, ist für reale cyber-physische Steuerungen unbrauchbar.
- **Mechanische Sympathie (Mechanical Sympathy)**: Verstehe, wie Cache-Zeilen ausgerichtet sind, wie die Sprungvorhersage arbeitet und wo der Speichercontroller an seine Grenzen stößt, bevor du dem Compiler die Schuld gibst.
- **Offline-First und autark**: Werkzeuge müssen sich in abgeschotteten Build-Umgebungen hermetisch kompilieren lassen und zuverlässig funktionieren, ohne externe Cloud-Telemetrie anzufunken.

---

## 🚀 Wichtige Open-Source-Projekte

| Projekt | Schwerpunkt | Sprache & Stack | Status |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Fähigkeitsbasierter Mikrokernel mit synchroner Zero-Copy-IPC für x86_64 und AArch64 | Rust, Zig, ASM | Aktive Architekturphase |
| **`wave-forge`** | Zero-Allocation, SIMD-beschleunigte modulare DSP-Synthesebibliothek (AVX2 / NEON) | Modernes C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Immediate-Mode-Terminal-UI-Engine mit Submillisekunden-Frame-Rendering | C99, POSIX / Win32 | Kontinuierlich gepflegt |
| **`ferro-raft`** | Deterministische, log-strukturierte verteilte Zustandsmaschine für isolierte Sensorknoten | Rust | Im Feldeinsatz erprobt |

---

## 🧰 Technologie-Matrix

### Systeme & Programmiersprachen
- **Hauptsprachen**: Rust (Core-Crates, `no_std`, Bare-Metal-Embedded), Modernes C++ (C++20/23, Template-Metaprogrammierung, SIMD), Zig (Cross-Compilation-Toolchain, Laufzeit-Bindeglied), C99/C11 (POSIX-Schnittstellen, Treiberentwicklung).
- **Zusatz & Skripting**: POSIX Shell, Python 3 (Benchmark-Auswertungen, Daten-Plotting, Signalsimulation), Lua 5.4 (Skripting für Embedded-Engines).
- **Assembler**: x86_64, AArch64, ARM Cortex-M (Bare-Metal-Bootcode, Kontextwechsel-Primitive).

### Kernel, Embedded & Analyse-Tools
- **Kernel- & Laufzeitanalyse**: QEMU, GDB / LLDB, perf, valgrind, Linux eBPF, FreeBSD bhyve.
- **Compiler & Toolchains**: Clang/LLVM, GCC-Cross-Compiler, cargo, ninja, make.
- **Hardware & Signalanalyse**: Saleae Logic Pro 16 Logikanalysator, Siglent SDS1104X-E Oszilloskop, JTAG/SWD-Debug-Sonden (ST-Link, J-Link), I2C/SPI-Busüberwachung.

### Protokolle & Speicherarchitektur
- **Binärprotokolle**: Zero-Copy Cap'n Proto, FlatBuffers, anwendungsspezifisches Binär-Framing über CAN / UART / UDP.
- **Speicher-Engines**: Log-Structured Merge (LSM)-Bäume, speicherabgebildete Ringpuffer (mmap), direkte NVMe-Blockverarbeitung.

---

## 🔬 Werkbank & Tägliches Arbeitsumfeld

```text
[Hardware-Setup]
  ├── Haupt-Notebook : ThinkPad T480 (Core i7-8650U, 64 GB DDR4, 2x 1TB NVMe, OpenBSD / Void Linux)
  ├── Labor-Rechner  : Eigenbau AMD Ryzen 9 7950X, 128 GB ECC-RAM, Debian 12 Stable (Hermetische Build-Farm)
  ├── Audio-Rig      : Individuelles Eurorack-Modularsystem, Motu M4 DAC/ADC, Sennheiser HD600
  └── Tastaturen     : Geteilte ergonomische Corne-Tastatur (Geschmierte Boba U4T Switches, eigene QMK-Firmware)
```

---

## 📈 Aktuelle Forschungsschwerpunkte

- Verfassen formaler TLA+-Spezifikationen für asynchrone Prozess-Fähigkeits-Handshakes in `float-OS`.
- Optimierung von Festkomma-Arithmetik für polyphone Wavetable-Oszillatoren auf ressourcenbeschränkten Cortex-M4-Mikrocontrollern.
- Entwicklung eines extrem schlanken, selbst-hostenden Compiler-Backends, das eigenständige ELF-Binärdateien ohne Bindung an die libc erzeugt.

---

## 📬 Kontakt

Ich freue mich stets über fundierte technische Diskussionen, Code-Reviews und Fehlermeldungen rund um Systemprogrammierung, Audiotechnik und minimalistisches Software-Design.

- **E-Mail**: `float.os.kernel@gmail.com`
- **GPG-Fingerprint**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` auf Libera.Chat (`#osdev`, `#rust-embedded`)
- **Patch-Einreichung**: Bevorzugt via `git-send-email` formatierte Patches oder reguläre GitHub Pull Requests.

---

<sub>Von Hand in reinem Markdown gestaltet. Keine externen Badges, keine Tracking-Skripte, zu 100% von einem Menschen betreut.</sub>
