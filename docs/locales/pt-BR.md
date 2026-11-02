| [KR 한국어](./ko.md) | [US English](../../README.md) | [JP 日本語](./ja.md) | [CN 简体中文](./zh-CN.md) | [ES Español](./es.md) |
| :---: | :---: | :---: | :---: | :---: |
| [FR Français](./fr.md) | [DE Deutsch](./de.md) | [RU Русский](./ru.md) | [SA العربية](./ar.md) | [IN हिन्दी](./hi.md) |

---

# Olá, sou Aidan Vance (`@float-OS`) 🛠️

```text
  _   _             _             ___  ____  
 | | | | ___ _   _  | |_ ___      / _ \/ ___| 
 | |_| |/ _ \ | | | | __/ _ \    | | | \___ \ 
 |  _  |  __/ |_| | | || (_) |   | |_| |___) |
 |_| |_|\___|\__, |  \__\___/_____\___/|____/ 
             |___/         |_____|            
  "Se não roda em silício frio sem um cabo de rede, é um serviço, não um programa."
```

Sou engenheiro de software de sistemas e entusiasta de hardware vivendo em Trondheim, Noruega. De dia, projeto pipelines de telemetria de baixíssima latência e módulos de comunicação determinística em tempo real; à noite, construo microkernels experimentais baseados em capacidades, sintetizadores de áudio com alocação zero de memória e ferramentas compactas para terminal.

Acredito em softwares que respeitam a memória, comportam-se de forma previsível sob carga extrema e sobrevivem aos ciclos passageiros dos frameworks da moda.

---

## 🧭 Filosofia de Engenharia

- **Alocação Zero no Caminho Crítico (Hot Path)**: Se um loop interno invoca um alocador dinâmico de heap, isso é considerado uma falha arquitetural até prova em contrário.
- **Latência previsível acima de vazão de pico bruta**: Um sistema que processa 100.000 req/s, mas com uma cauda de latência descontrolada de 2 segundos, é inútil para controle ciberfísico real.
- **Simpatia Mecânica (Mechanical Sympathy)**: Entenda o alinhamento das linhas de cache, a previsão de desvios do processador e onde o controlador de memória engargala antes de culpar o compilador.
- **Offline First e Autossuficiente**: Toda ferramenta deve ser compilada de forma hermética em ambientes isolados e rodar perfeitamente sem enviar telemetria a servidores em nuvem.

---

## 🚀 Principais Projetos de Código Aberto

| Projeto | Foco | Linguagem & Stack | Status |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Microkernel orientado a capacidades com IPC síncrono zero-copy para x86_64 e AArch64 | Rust, Zig, ASM | Fase ativa de arquitetura |
| **`wave-forge`** | Biblioteca de síntese modular DSP com aceleração SIMD (AVX2 / NEON) sem alocações dinâmicas | Modern C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Motor de interface de terminal em modo imediato com renderização em sub-milissegundos | C99, POSIX / Win32 | Mantido ativamente |
| **`ferro-raft`** | Máquina de estados distribuída determinística em log estruturado para nós sensores isolados | Rust | Em produção em kits de campo |

---

## 🧰 Matriz de Tecnologias

### Sistemas & Linguagens
- **Linguagens principais**: Rust (crates core, `no_std`, bare-metal embarcado), Modern C++ (C++20/23, metaprogramação de templates, SIMD), Zig (toolchain de compilação cruzada, runtime glue), C99/C11 (interfaces POSIX, drivers de dispositivos).
- **Apoio & Scripts**: POSIX Shell, Python 3 (benchmarks, gráficos de dados, simulação de sinais), Lua 5.4 (scripting para engines embarcadas).
- **Assembly**: x86_64, AArch64, ARM Cortex-M (inicialização bare-metal, troca de contexto).

### Kernel, Embarcados & Ferramentas
- **Análise de Kernel & Runtime**: QEMU, GDB / LLDB, perf, valgrind, Linux eBPF, FreeBSD bhyve.
- **Compiladores & Toolchains**: Toolchain Clang/LLVM, compiladores cruzados GCC, cargo, ninja, make.
- **Hardware & Análise de Sinais**: Analisador lógico Saleae Logic Pro 16, osciloscópio Siglent SDS1104X-E, sondas de depuração JTAG/SWD (ST-Link, J-Link), decodificação de barramentos I2C/SPI.

### Protocolos & Armazenamento
- **Protocolos binários**: Cap'n Proto zero-copy, FlatBuffers, enquadramento binário customizado sobre CAN / UART / UDP.
- **Engines de armazenamento**: Árvores LSM (Log-Structured Merge), ring buffers mapeados em memória (mmap), despacho direto de blocos NVMe.

---

## 🔬 Bancada de Trabalho & Setup Diário

```text
[Ambiente de Hardware]
  ├── Laptop principal : ThinkPad T480 (Core i7-8650U, 64GB DDR4, Dual 1TB NVMe, OpenBSD / Void Linux)
  ├── Desktop de lab   : AMD Ryzen 9 7950X sob medida, 128GB ECC RAM, Debian 12 Stable (Build farm isolada)
  ├── Estúdio de áudio : Rack modular Eurorack artesanal, Motu M4 DAC/ADC, Sennheiser HD600
  └── Teclados         : Teclado ergonômico dividido Corne (Switches Boba U4T lubrificados, firmware QMK)
```

---

## 📈 Explorações & Pesquisas Atuais

- Redação de especificações formais em TLA+ para handshakes assíncronos de capacidades entre processos no `float-OS`.
- Otimização de aritmética em ponto fixo para osciladores wavetable polifônicos em microcontroladores Cortex-M4 de baixo consumo.
- Criação de um backend mínimo de compilador auto-hospedado que gera binários ELF puros sem vincular à libc.

---

## 📬 Contato

Discussões técnicas minuciosas, revisões criteriosas de código e relatórios de bugs sobre programação de baixo nível, engenharia de áudio e ferramentas minimalistas são sempre bem-vindos.

- **E-mail**: `float.os.kernel@gmail.com`
- **GPG Fingerprint**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` na Libera.Chat (`#osdev`, `#rust-embedded`)
- **Envio de Patches**: Preferencialmente via patches formatados com `git-send-email` ou Pull Requests no GitHub.

---

<sub>Feito artesanalmente em Markdown puro. Sem badges externas, sem scripts rastreadores, 100% mantido por um humano.</sub>
