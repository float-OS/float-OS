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
  "If it cannot run on cold silicon without a network cable, it is a service, not a program."
```

Ich bin Senior Systems Software Engineer und Hardware-Tüftler mit Sitz in Trondheim, Norwegen. Im letzten Jahrzehnt lag mein Schwerpunkt auf Telemetrie-Pipelines mit extrem geringer Latenz, deterministischen Echtzeit-Kommunikationsprotokollen und hochzuverlässigen Systemarchitekturen. Außerhalb meiner Haupttätigkeit entwickle ich fähigkeitsbasierte Mikrokernels, allokationsfreie modulare DSP-Audiosynthesizer und minimalistische CLI-Werkzeuge.

Ich entwerfe Systeme nach First-Principles: strenge Speichergrenzen, deterministische Nebenläufigkeit ohne Race Conditions, mechanische Sympathie mit CPU-Caches und robuste Software jenseits kurzlebiger Framework-Hypes.

---

## 🧭 Zentrale Ingenieurprinzipien

- **Keine Heap-Allokation im Hot Path**: Dynamische Allokationen innerhalb hochfrequenter Schleifen gelten als Architekturfehler, solange ihre Unvermeidbarkeit nicht mathematisch bewiesen ist.
- **Deterministische Nebenläufigkeit ohne Race Conditions**: Lock-freie Ringpuffer, SPSC-Warteschlangen und fähigkeitsisoliertes Message Passing statt Shared-State Locking.
- **Vorhersehbare Latenz vor maximalem Durchsatz**: Ein System mit 100.000 req/s, das unter unkontrollierten Tail-Latency-Spitzen leidet, ist für hochpräzise Steuerungsaufgaben unbrauchbar.
- **Mechanische Sympathie (Mechanical Sympathy)**: Entwicklung unter direkter Berücksichtigung von L1/L2-Cache-Zeilen, Verzweigungsvorhersagen und Speicherbusbandbreiten.
- **Sicherheit durch Design (Secure-by-Design)**: Strenge Prozessgrenzen, kryptographische Operationen in konstanter Zeit und hermetisch reproduzierbare Offline-Builds.

---

## 🚀 Wichtige Open-Source-Projekte

| Projekt | Schwerpunkt | Architektur & Stack | Status |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Fähigkeitsbasierter Mikrokernel mit synchronem Zero-Copy IPC für x86_64 und AArch64 | Rust, Zig, Bare-metal ASM | In aktiver Entwicklung |
| **`wave-forge`** | Allokationsfreie, SIMD-beschleunigte DSP-Audiosynthese-Bibliothek (AVX2 / NEON) | Modern C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Immediate-Mode Terminal-UI-Engine mit Sub-Millisekunden-Framedispatch | C99, POSIX / Win32 | Kontinuierlich gepflegt |
| **`ferro-raft`** | Deterministische, log-strukturierte verteilte Zustandsmaschine für isolierte Sensorknoten | Rust | Im Produktiveinsatz |

---

## 📬 Kontakt

- **Email**: `float.os.kernel@gmail.com`
- **GPG Fingerprint**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` auf Libera.Chat (`#osdev`, `#rust-embedded`)

---

<sub>Von Hand in reinem Markdown verfasst. Ohne externe Badges, ohne Tracking-Skripte, 100% von Menschenhand gepflegt.</sub>
