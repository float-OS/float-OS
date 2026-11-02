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
  "Si no puede ejecutarse en silicio frío sin un cable de red, es un servicio, no un programa."
```

Soy un ingeniero de software de sistemas y entusiasta del hardware radicado en Trondheim, Noruega. De día, diseño canalizaciones de telemetría de baja latencia y módulos deterministas de comunicación en tiempo real; de noche, construyo microkernels experimentales basados en capacidades, sintetizadores de audio con cero asignaciones dinámicas y herramientas compactas para la línea de comandos.

Creo firmemente en el software que respeta la memoria, opera de manera predecible bajo alta carga y sobrevive a las modas pasajeras de los frameworks modernos.

---

## 🧭 Filosofía de Ingeniería

- **Cero asignación en la ruta crítica (Hot Path)**: Si un bucle interno invoca a un asignador dinámico de memoria, se considera un error arquitectónico hasta que se demuestre lo contrario.
- **Latencia predecible sobre rendimiento pico**: Un sistema capaz de procesar 100.000 peticiones por segundo pero con una cola de latencia descontrolada de 2 segundos está roto para el control físico en el mundo real.
- **Simpatía mecánica (Mechanical Sympathy)**: Comprende cómo se alinean las líneas de caché, cómo predice el hardware las bifurcaciones y dónde se ahoga el controlador de memoria antes de culpar al compilador.
- **Primero fuera de línea y autónomo**: Todas las herramientas deben compilarse de forma hermética en entornos aislados y funcionar con dignidad sin llamar a servidores externos de telemetría.

---

## 🚀 Proyectos de Código Abierto Destacados

| Proyecto | Enfoque | Lenguaje y Pila | Estado |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Microkernel basado en capacidades con IPC sincrónico de copia cero para x86_64 y AArch64 | Rust, Zig, ASM | Fase activa de arquitectura |
| **`wave-forge`** | Biblioteca de síntesis modular DSP con aceleración SIMD (AVX2 / NEON) y sin asignaciones en heap | Modern C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Motor de interfaz de terminal en modo inmediato con renderizado de fotogramas en sub-milisegundos | C99, POSIX / Win32 | En mantenimiento |
| **`ferro-raft`** | Máquina de estados distribuida y estructurada en log determinista para nodos sensoriales aislados | Rust | En producción en kits de campo |

---

## 🧰 Matriz de Tecnologías

### Sistemas y Lenguajes
- **Dialectos principales**: Rust (crates core, `no_std`, bare-metal embebido), Modern C++ (C++20/23, metaprogramación de plantillas, SIMD), Zig (entorno de compilación cruzada, pegamento de runtime), C99/C11 (interfaces POSIX, controladores).
- **Secundarios / Scripting**: POSIX Shell, Python 3 (análisis de rendimiento, trazado de gráficos, simulación de señales), Lua 5.4 (scripting de motores embebidos).
- **Ensamblador**: x86_64, AArch64, ARM Cortex-M (rutinas de arranque bare-metal, primitivas de cambio de contexto).

### Kernel, Embebidos y Herramientas
- **Análisis de Kernel y Runtime**: QEMU, GDB / LLDB, perf, valgrind, Linux eBPF, FreeBSD bhyve.
- **Compiladores y Cadenas de Montaje**: Toolchain Clang/LLVM, compiladores cruzados GCC, cargo, ninja, make.
- **Hardware y Análisis de Señal**: Analizador lógico Saleae Logic Pro 16, osciloscopio Siglent SDS1104X-E, sondas de depuración JTAG/SWD (ST-Link, J-Link), inspección de buses I2C/SPI.

### Protocolos y Almacenamiento
- **Protocolos binarios**: Cap'n Proto de copia cero, FlatBuffers, tramas binarias a medida sobre CAN / UART / UDP.
- **Motores de almacenamiento**: Árboles Log-Structured Merge (LSM), búferes circulares mapeados en memoria (mmap), despacho directo a bloques NVMe.

---

## 🔬 Banco de Trabajo y Configuración Cotidiana

```text
[Estación de Hardware]
  ├── Portátil principal : ThinkPad T480 (Core i7-8650U, 64GB DDR4, Dual 1TB NVMe, OpenBSD / Void Linux)
  ├── Sobremesa de lab   : AMD Ryzen 9 7950X personalizado, 128GB ECC RAM, Debian 12 Stable (Granja de compilación)
  ├── Equipo de audio    : Rack modular Eurorack artesanal, Motu M4 DAC/ADC, Sennheiser HD600
  └── Teclados           : Teclado ergonómico dividido Corne (Interruptores Boba U4T lubricados, firmware QMK propio)
```

---

## 📈 Exploraciones Actuales

- Redacción de especificaciones formales en TLA+ para acuerdos asincrónicos de capacidades interproceso en `float-OS`.
- Optimización de aritmética de punto fijo para osciladores de tabla de ondas polifónicos en arquitecturas Cortex-M4 con memoria limitada.
- Experimentación con un backend de compilador auto-hospedado ultra-ligero que genera binarios ELF puros sin enlazar libc.

---

## 📬 Contacto

Agradezco profundamente los debates técnicos rigurosos, revisiones de código reflexivas y reportes de errores sobre programación de sistemas, ingeniería de audio y herramientas minimalistas.

- **Correo electrónico**: `float.os.kernel@gmail.com`
- **Huella digital GPG**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` en Libera.Chat (`#osdev`, `#rust-embedded`)
- **Flujo de parches**: Se prefiere el envío de parches formateados vía `git-send-email` o Pull Requests de GitHub.

---

<sub>Elaborado a mano en Markdown puro. Sin insignias externas, sin scripts de seguimiento, 100% gestionado por un humano.</sub>
