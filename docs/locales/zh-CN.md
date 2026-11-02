| [KR 한국어](./ko.md) | [US English](../../README.md) | [JP 日本語](./ja.md) | [CN 简体中文](./zh-CN.md) | [ES Español](./es.md) |
| :---: | :---: | :---: | :---: | :---: |
| [FR Français](./fr.md) | [DE Deutsch](./de.md) | [RU Русский](./ru.md) | [SA العربية](./ar.md) | [IN हिन्दी](./hi.md) |

---

# 你好，我是 Aidan Vance（`@float-OS`）🛠️

```text
  _   _             _             ___  ____  
 | | | | ___ _   _  | |_ ___      / _ \/ ___| 
 | |_| |/ _ \ | | | | __/ _ \    | | | \___ \ 
 |  _  |  __/ |_| | | || (_) |   | |_| |___) |
 |_| |_|\___|\__, |  \__\___/_____\___/|____/ 
             |___/         |_____|            
  "If it cannot run on cold silicon without a network cable, it is a service, not a program."
```

我是一名定居在挪威特隆赫姆的资深系统软件工程师。过去十年间，我主要专注于超低延迟遥测管线、确定现实时通信协议以及高可靠系统架构设计。工作之余，我致力于构建基于能力的微内核、零内存分配模块化音频 DSP 引擎以及极简命令行工具。

我坚持从第一性原理出发进行设计：严苛的内存边界、无数据竞争的确定性并发、与硬件 CPU 缓存的机械共鸣（Mechanical Sympathy），以及超越浮躁技术潮流的扎实工程实践。

---

## 🧭 核心工程设计准则

- **核心执行路径零内存分配（Zero Allocation in Hot Path）**：高频循环内部的动态堆内存分配，在从数学和逻辑上被证明不可避免之前，一律视为架构设计缺陷。
- **确定性并发与无数据竞争**：避免过度依赖共享锁，全面拥抱无锁环形缓冲区、SPSC 单生产者单消费者队列以及基于能力的隔离消息传递机制。
- **可预测延迟优于盲目峰值吞吐**：即便系统每秒可处理 10 万次请求，若尾部延迟（Tail Latency）不可控，在精密物理控制与遥测系统中仍属于严重缺陷。
- **机械共鸣（Mechanical Sympathy）**：不依赖编译器的臆测，在系统设计初始阶段便精细考量 L1/L2 缓存行对齐、分支预测器模式与总线带宽瓶颈。
- **原生安全设计（Secure-by-Design）**：严密界限隔离、常数时间（Constant-time）密码学运算、无外部网络依赖的封闭可重现构建。

---

## 🚀 核心开源项目

| 项目 | 领域 | 架构与技术栈 | 当前状态 |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | 面向 x86_64 与 AArch64 的基于能力的微内核与同步零拷贝 IPC | Rust, Zig, 原生 ASM | 核心架构开发中 |
| **`wave-forge`** | 零堆分配、SIMD 加速（AVX2 / NEON）模块化音频 DSP 合成库 | Modern C++ (C++20) | 稳定核心 v0.8.4 |
| **`tinytui`** | 具备亚毫秒级帧调度性能的即时模式（Immediate-mode）终端交互引擎 | C99, POSIX / Win32 | 持续维护中 |
| **`ferro-raft`** | 面向物理隔离（Air-gapped）传感器网络的确定性日志结构分布式状态机 | Rust | 现场部署运行中 |

---

## 🧰 技术栈矩阵

### 系统与语言
- **主力语言**: Rust（core, `no_std`, 嵌入式裸机）, Modern C++（C++20/23, 模板元编程, SIMD 指令集）, Zig（跨平台工具链, 运行时胶水）, C99/C11（POSIX 接口, 设备驱动层）。
- **辅助与脚本**: POSIX Shell, Python 3（基准评测套件, 信号仿真, 遥测数据分析）, Lua 5.4。
- **汇编语言**: x86_64, AArch64, ARM Cortex-M（裸机引导例程, 上下文切换原语）。

### 内核、工具与硬件
- **调试与性能剖析**: QEMU, GDB / LLDB, Linux perf, valgrind, Linux eBPF, FreeBSD bhyve。
- **工具链与构建**: Clang/LLVM, GCC 交叉编译器, cargo, ninja, make。
- **硬件与信号仪器**: Saleae Logic Pro 16 逻辑分析仪, Siglent SDS1104X-E 示波器, JTAG/SWD 探针, I2C/SPI/CAN 协议分析仪。

---

## 📬 交流与协作

欢迎就系统编程、音频 DSP 及高性能低级工程领域展开深入技术探讨、代码审查与缺陷反馈。

- **Email**: `float.os.kernel@gmail.com`
- **GPG 指纹**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` on Libera.Chat (`#osdev`, `#rust-embedded`)

---

<sub>无外部徽章，无追踪脚本，纯 Markdown 手工编写。100% 人工维护。</sub>
