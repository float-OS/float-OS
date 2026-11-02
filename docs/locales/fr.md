| [KR 한국어](./ko.md) | [US English](../../README.md) | [JP 日本語](./ja.md) | [CN 简体中文](./zh-CN.md) | [ES Español](./es.md) |
| :---: | :---: | :---: | :---: | :---: |
| [FR Français](./fr.md) | [DE Deutsch](./de.md) | [RU Русский](./ru.md) | [SA العربية](./ar.md) | [IN हिन्दी](./hi.md) |

---

# Bonjour, je suis Aidan Vance (`@float-OS`) 🛠️

```text
  _   _             _             ___  ____  
 | | | | ___ _   _  | |_ ___      / _ \/ ___| 
 | |_| |/ _ \ | | | | __/ _ \    | | | \___ \ 
 |  _  |  __/ |_| | | || (_) |   | |_| |___) |
 |_| |_|\___|\__, |  \__\___/_____\___/|____/ 
             |___/         |_____|            
  "Si un programme ne peut pas tourner sur du silicium froid sans câble réseau, c'est un service, pas un logiciel."
```

Je suis un ingénieur logiciel système et passionné de matériel basé à Trondheim, en Norvège. Le jour, je conçois des pipelines de télémétrie à faible latence et des modules de communication déterministes en temps réel ; la nuit, je développe des micro-noyaux expérimentaux basés sur les capacités, des synthétiseurs audio sans allocation dynamique et des outils compacts en ligne de commande.

Je défends des logiciels qui respectent la mémoire, fonctionnent de manière prévisible sous forte charge et survivent aux cycles éphémères des frameworks modernes.

---

## 🧭 Philosophie d'Ingénierie

- **Zéro allocation sur le chemin critique (Hot Path)** : Si une boucle interne fait appel à un allocateur de tas dynamique, cela doit être considéré comme un défaut architectural jusqu'à preuve du contraire.
- **Latence prévisible plutôt que débit de pointe brut** : Un système capable de traiter 100 000 requêtes/seconde mais souffrant d'une latence résiduelle incontrôlée de 2 secondes est défaillant pour le contrôle physique en temps réel.
- **Sympathie mécanique (Mechanical Sympathy)** : Comprenez l'alignement des lignes de cache, la prédiction de branchement du processeur et les goulets d'étranglement du contrôleur mémoire avant d'incriminer le compilateur.
- **Fonctionnement hors-ligne et autonome** : Chaque outil doit pouvoir être compilé de manière reproductible et hermétique dans un environnement isolé, sans jamais dépendre d'une télémétrie externe dans le cloud.

---

## 🚀 Projets Open-Source Majeurs

| Projet | Domaine | Langages & Technologies | État d'avancement |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Micro-noyau orienté capacités avec IPC synchrone zéro-copie pour architectures x86_64 et AArch64 | Rust, Zig, ASM | Phase de conception d'architecture |
| **`wave-forge`** | Bibliothèque modulaire de synthèse DSP sans allocation sur le tas, accélérée par SIMD (AVX2 / NEON) | Modern C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Moteur d'interface de terminal en mode immédiat offrant un rendu sous la milliseconde | C99, POSIX / Win32 | Maintenu |
| **`ferro-raft`** | Machine à états distribuée déterministe basée sur des journaux pour capteurs autonomes | Rust | Déployé sur le terrain |

---

## 🧰 Matrice Technologique

### Systèmes & Langages
- **Langages fondamentaux** : Rust (crates core, `no_std`, embarqué bare-metal), Modern C++ (C++20/23, métaprogrammation de modèles, SIMD), Zig (outillage de compilation croisée, glue runtime), C99/C11 (interfaces POSIX, couches pilotes).
- **Langages secondaires & Scripting** : POSIX Shell, Python 3 (analyse de benchmarks, tracés de données, simulation de signaux), Lua 5.4 (scripting pour moteurs embarqués).
- **Assembleur** : x86_64, AArch64, ARM Cortex-M (séquences d'amorçage bare-metal, primitives de commutation de contexte).

### Noyau, Embarqué & Outillage
- **Analyse de Noyau & Runtime** : QEMU, GDB / LLDB, perf, valgrind, Linux eBPF, FreeBSD bhyve.
- **Compilateurs & Chaînes de compilation** : Clang/LLVM, compilateurs croisés GCC, cargo, ninja, make.
- **Matériel & Analyse de signaux** : Analyseur logique Saleae Logic Pro 16, oscilloscope Siglent SDS1104X-E, sondes de débogage JTAG/SWD (ST-Link, J-Link), décodage de bus I2C/SPI.

### Protocoles & Moteurs de Stockage
- **Protocoles binaires** : Zero-copy Cap'n Proto, FlatBuffers, trames binaires personnalisées sur CAN / UART / UDP.
- **Moteurs de stockage** : Arbres LSM (Log-Structured Merge), tampons circulaires mappés en mémoire (mmap), répartition brute sur blocs NVMe.

---

## 🔬 Atelier & Configuration Quotidienne

```text
[Environnement Matériel]
  ├── Ordinateur portable : ThinkPad T480 (Core i7-8650U, 64 Go DDR4, Double NVMe 1 To, OpenBSD / Void Linux)
  ├── Station de labo      : Machine sur mesure AMD Ryzen 9 7950X, 128 Go RAM ECC, Debian 12 Stable (Build farm)
  ├── Équipement audio    : Rack modulaire Eurorack sur mesure, DAC/ADC Motu M4, Sennheiser HD600
  └── Claviers            : Clavier ergonomique scindé Corne (Switches Boba U4T lubrifiés, firmware QMK maison)
```

---

## 📈 Recherches & Explorations en Cours

- Rédaction de spécifications formelles TLA+ pour les poignées de main asynchrones de capacités entre processus dans `float-OS`.
- Optimisation d'algorithmes en virgule fixe pour oscillateurs polyphoniques à tables d'ondes sur cibles Cortex-M4 à ressources restreintes.
- Conception expérimentale d'un backend de compilateur auto-hébergé minimaliste générant des binaires ELF purs sans liaison à la libc.

---

## 📬 Me Contacter

Je suis toujours ravi d'échanger sur la programmation système, l'ingénierie audio et la conception d'outils minimalistes, ainsi que de recevoir des revues de code et des rapports d'anomalies.

- **Courriel** : `float.os.kernel@gmail.com`
- **Empreinte GPG** : `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC** : `aidan_v` sur Libera.Chat (`#osdev`, `#rust-embedded`)
- **Soumission de correctifs** : Envoi de correctifs formatés via `git-send-email` ou GitHub Pull Requests.

---

<sub>Rédigé artisanalement en Markdown brut. Sans badges externes, sans traceurs, géré à 100% par un humain.</sub>
