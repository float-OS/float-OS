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
  "If it cannot run on cold silicon without a network cable, it is a service, not a program."
```

Sou engenheiro de software de sistemas sênior estabelecido em Trondheim, Noruega. Ao longo da última década, meu trabalho concentrou-se em pipelines de telemetria de latência ultrabaixa, protocolos de comunicação determinísticos em tempo real e arquitetura de sistemas de alta confiabilidade. Fora do expediente, construo microkernels experimentais baseados em capacidades, motores modulares de síntese DSP de áudio com alocação zero no heap e utilitários minimalistas de linha de comando.

Desenvolvo sistemas a partir dos primeiros princípios: limites estritos de memória, concorrência determinística sem corridas de dados, simpatia mecânica com caches de CPU e software robusto que sobrevive aos ciclos transitórios de frameworks.

---

## 🧭 Princípios Fundamentais de Engenharia

- **Zero Alocação no Caminho Crítico (Hot Path)**: Alocações dinâmicas no heap dentro de laços de alta frequência são tratadas como falhas arquiteturais até prova lógica em contrário.
- **Concorrência Determinística e Livre de Corridas**: Buffers circulares lockless, filas SPSC e passagem de mensagens com isolamento de capacidades em vez de locks de estado compartilhado.
- **Latência Previsível sobre Throughput Bruto**: Um sistema que processa 100.000 req/s mas sofre picos descontrolados de tail latency é inviável para controle físico de precisão.
- **Simpatia Mecânica (Mechanical Sympathy)**: Projeto com consciência direta de alinhamento de linhas de cache L1/L2, preditores de desvio e largura de banda do barramento de memória.
- **Segurança por Design (Secure-by-Design)**: Isolamento rigoroso de fronteiras, primitivas criptográficas em tempo constante e compilação hermética reprodutível offline.

---

## 🚀 Principais Projetos de Código Aberto

| Projeto | Domínio | Arquitetura & Tecnologias | Status |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Microkernel baseado em capacidades com IPC de cópia zero para x86_64 e AArch64 | Rust, Zig, Bare-metal ASM | Em desenvolvimento ativo |
| **`wave-forge`** | Biblioteca modular DSP de síntese de áudio com aceleração SIMD (AVX2 / NEON) | Modern C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Motor de interface de terminal em modo imediato com despacho em menos de um milissegundo | C99, POSIX / Win32 | Em manutenção contínua |
| **`ferro-raft`** | Máquina de estados distribuída determinística para redes de sensores isoladas (air-gapped) | Rust | Em produção em campo |

---

## 📬 Contato

- **Email**: `float.os.kernel@gmail.com`
- **GPG Fingerprint**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` no Libera.Chat (`#osdev`, `#rust-embedded`)

---

<sub>Feito à mão com Markdown puro. Sem badges externos, sem scripts de rastreamento, 100% humano.</sub>
