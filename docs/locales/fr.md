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
  "If it cannot run on cold silicon without a network cable, it is a service, not a program."
```

Ingénieur logiciel système senior basé à Trondheim, en Norvège. Au cours de la dernière décennie, mes travaux se sont concentrés sur les pipelines de télémétrie à très faible latence, les protocoles de communication déterministes en temps réel et l'architecture de systèmes à haute assurance. En dehors de mon travail, je conçois des micro-noyaux expérimentaux basés sur les capabilités, des moteurs de synthèse audio DSP sans allocation dynamique et des outils en ligne de commande épurés.

Je conçois les systèmes selon des principes fondamentaux : isolation rigoureuse de la mémoire, concurrence déterministe sans concurrence critique, sympathie mécanique avec les caches CPU et logiciels pérennes face aux modes éphémères.

---

## 🧭 Principes d'Ingénierie Fondamentaux

- **Zéro Allocation sur le Chemin Critique** : Toute allocation sur le tas au sein d'une boucle à haute fréquence est considérée comme un défaut d'architecture jusqu'à preuve du contraire.
- **Concurrence Déterministe et Absence de Conflits** : Utilisation de tampons circulaires sans verrou (lockless), files SPSC et passage de messages isolés par capabilités plutôt que verrouillage d'état partagé.
- **Latence Prévisible plutôt que Débit Brut** : Un système traitant 100 000 requêtes/seconde mais souffrant de pics de latence incontrôlés est inutilisable en contrôle cyber-physique de précision.
- **Sympathie Mécanique (Mechanical Sympathy)** : Conception prenant directement en compte l'alignement des lignes de cache L1/L2, les prédicteurs de branchement et la bande passante mémoire.
- **Sécurité dès la Conception (Secure-by-Design)** : Cloisonnement strict des processus, cryptographie en temps constant et reproductibilité des compilations hors ligne.

---

## 🚀 Projets Open-Source Majeurs

| Projet | Domaine | Architecture & Technologies | Statut |
| :--- | :--- | :--- | :--- |
| **`float-OS`** | Micro-noyau à capabilités avec IPC synchrone zéro-copie pour x86_64 et AArch64 | Rust, Zig, ASM Bare-metal | En développement actif |
| **`wave-forge`** | Bibliothèque modulaire DSP de synthèse audio sans allocation, accélérée SIMD (AVX2 / NEON) | Modern C++ (C++20) | Stable Core v0.8.4 |
| **`tinytui`** | Moteur d'interface de terminal en mode immédiat avec rendu sub-milliseconde | C99, POSIX / Win32 | Maintenu activement |
| **`ferro-raft`** | Machine à états distribuée déterministe pour réseaux de capteurs isolés (air-gapped) | Rust | Déploiement en production |

---

## 📬 Contact

- **Email**: `float.os.kernel@gmail.com`
- **GPG Fingerprint**: `7E9B 4410 F302 89A1 55B8  0DC4 91D2 00A3 EF27 C418`
- **IRC**: `aidan_v` sur Libera.Chat (`#osdev`, `#rust-embedded`)

---

<sub>Rédigé à la main en Markdown pur. Sans badges externes ni scripts de traçage, 100% humain.</sub>
