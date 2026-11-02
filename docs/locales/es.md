| [KR 한국어](./ko.md) | [US English](../../README.md) | [JP 日本語](./ja.md) | [CN 简体中文](./zh-CN.md) | [ES Español](./es.md) |
| :---: | :---: | :---: | :---: | :---: |
| [FR Français](./fr.md) | [DE Deutsch](./de.md) | [RU Русский](./ru.md) | [SA العربية](./ar.md) | [IN हिन्दी](./hi.md) |

---

# Hola, soy Aidan Vance (`@float-OS`) 🛠️

```text
  _   _             _             ___  ____  
 | | | | ___ _   _  | |_ ___      / _ \/ ___| 
 | |_| |/ _ \ | | | | __/ _ \    | | | \___ \ 
 |  _  |  __/ |_| | | || (_) |   | |_| |___) |
 |_| |_|\___|\__, |  \__\___/_____\___/|____/ 
             |___/         |_____|            
  "If it cannot run on cold silicon without a network cable, it is a service, not a program."
```

Soy un ingeniero de software de sistemas sénior afincado en Trondheim, Noruega. Durante la última década me he centrado en el diseño de conductos de telemetría de latencia ultrabaja, protocolos de comunicación deterministas en tiempo real y arquitectura de sistemas de alta fiabilidad. Fuera de mi trabajo habitual, desarrollo microkernels experimentales basados en capacidades, motores de síntesis de audio DSP modulares sin asignación dinámica de memoria y herramientas de consola minimalistas.

Diseño sistemas desde los primeros principios: límites de memoria rigurosos, concurrencia determinista sin carreras de datos, simpatía mecánica con los procesadores y software robusto que perdura más allá de las modas tecnológicas.

---

## 🧭 Principios Fundamentales de Ingeniería

- **Cero Asignación Dinámica en la Ruta Crítica**: Cualquier asignación en el heap dentro de un bucle de alta frecuencia se considera un defecto arquitectónico hasta demostrarse lo contrario.
- **Concurrencia Determinista y Ausencia de Carreras**: Uso de búferes circulares sin bloqueos (lockless), colas SPSC y paso de mensajes con aislamiento de capacidades frente al bloqueo de estado compartido.
- **Latencia Predecible frente a Rendimiento Máximo Bruto**: Un sistema que procese 100.000 req/s con picos incontrolados de latencia de cola es inaceptable en sistemas de control físico de precisión.
- **Simpatía Mecánica (Mechanical Sympathy)**: Diseño con conocimiento directo de la alineación de líneas de caché L1/L2, predicción de saltos y ancho de banda de memoria.
- **Seguridad por Diseño (Secure-by-Design)**: Aislamiento estricto de límites, operaciones criptográficas en tiempo constante y reproducibilidad de compilación hermética sin conexión.

---

## 🚀 Proyectos de Código Abierto Destacados

| Proyecto | Especialidad | Arquitectura y Tecnologías | Estado |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Microkernel basado en capacidades con IPC de copia cero para x86_64 y AArch64 | Rust, Zig, ASM Bare-metal | En desarrollo activo |
| **`wave-forge`** | Librería modular de síntesis DSP con aceleración SIMD (AVX2 / NEON) sin asignación en heap | Modern C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Motor de interfaz de terminal en modo inmediato con despacho en menos de un milisegundo | C99, POSIX / Win32 | Mantenimiento continuo |
| **`ferro-raft`** | Máquina de estados distribuida y determinista para nodos de sensores aislados (air-gapped) | Rust | En producción operativa |

---

## 🧰 Matriz Tecnológica

### Sistemas y Lenguajes
- **Principales**: Rust (núcleo, `no_std`, embebidos), Modern C++ (C++20/23, metaprogramación, SIMD), Zig (entornos de compilación cruzada, pegamento de runtime), C99/C11 (POSIX, drivers).
- **Secundarios**: POSIX Shell, Python 3 (bancos de pruebas, simulación de señales, visualización), Lua 5.4.
- **Ensamblador**: x86_64, AArch64, ARM Cortex-M (arranque bare-metal, cambio de contexto).

---

## 📬 Contacto

- **Email**: `float.os.kernel@gmail.com`
- **GPG Fingerprint**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` en Libera.Chat (`#osdev`, `#rust-embedded`)

---

<sub>Escrito a mano con Markdown puro. Sin insignias externas, sin scripts de seguimiento, 100% humano.</sub>
