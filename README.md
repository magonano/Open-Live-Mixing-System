# Open Live Mixing System (OLMS)

[![License](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![Status](https://img.shields.io/badge/Status-PoC%20Recruiting-red.svg)](./issues/1)
[![Sample Rate](https://img.shields.io/badge/Sample%20Rate-48%20kHz-orange.svg)]()
[![RTL Target](https://img.shields.io/badge/RTL%20Target-%3C%2010ms-green.svg)]()

OLMS: The Open Live Mixing System. Transforms any Mini-PC into a dedicated, professional digital rack mixer. Built on a Real-Time Linux Core, Ardour Headless, and PipeWire, offering reliable, low-latency audio control via a responsive Web UI/OSC bridge. Open Core (GPLv3).

---

## 📢 THE CRITICAL CHALLENGE: LEAD/SUPERVISOR RECRUITMENT

We are seeking **Founders**—individuals who will be credited for the launch of the GPL Core. Your reward is prestige, full authority in your domain, and **absolute priority** for a paid role, contract, or equity share in the future commercial phase.

### The Application Test for Lead/Supervisor Roles

Resolving the **Proof of Concept (PoC) Issue #1** is the **mandatory technical application** for the following three roles: **Lead UX/UI**, **Lead Developer (Control)**, and **Lead Architect/Core Maintainer**.

**To Apply:** Submit a Pull Request that successfully resolves one of the tasks below, or comment on [Issue #1](https://github.com/magonano/Open-Live-Mixing-System/issues/1) stating which PoC Task you intend to tackle.

### Issue #1 Summary: Stable Linux RT Core, Ardour Headless & Minimal OSC Bridge

| Task PoC | Responsible Role | Expected Output | RTL Target | X-Run Target |
| :--- | :--- | :--- | :--- | :--- |
| **PoC-1** | Lead UX/UI | Static HTML/CSS page of a **Single Channel Fader**, fully responsive and touch-friendly. Includes defining the overall **UX/UI architecture and philosophy** for reativity. | N/A | N/A |
| **PoC-2** | Lead Developer (Control) | Functional Bridge Server + JS/OSC Integration to connect PoC-1 to the **Fader of Ardour Channel 1**. Immediate fader movement required. | N/A | N/A |
| **PoC-3** | Lead Architect / Core Maintainer | Complete configuration (RT Kernel + PipeWire + Ardour Headless) capable of routing **1 Input → Ardour → 1 Output** at **48 kHz**, controlled remotely via PoC-2, with **ZERO X-runs in 1 hour**. | **< 10 ms** (Goal: < 5 ms) | **ZERO (0)** in one hour of stress test under load. |

---

## THE OPEN LIVE MIXING SYSTEM (OLMS) MANIFESTO

### Vision: The Death of the Proprietary Rack Mixer

> "Our core idea is to transform a common, affordable computer—ideally a **Mini-PC fanless with certified USB audio cards**—into a dedicated, reliable, rack-mounted digital mixer, controllable entirely via Wi-Fi network."

The Open Live Mixing System (OLMS) is a challenge to the status quo. We are building the next generation of professional, dedicated digital mixing systems based entirely on free and open-source software. We aim to replicate the **"turn it on and mix"** reliability and simplicity of expensive, dedicated commercial systems. This is achieved through a rigid **hardware certification process** and a custom, self-installing Linux operating system (the OLMS distro). The system will operate at a fixed **48 kHz Sample Rate** to ensure stability and compatibility.

### The Technical Challenge: Real-Time Audio for Everyone

We are committed to delivering stable, multi-channel live audio with minimal latency.

Our technology stack is built on rock-solid open-source foundations:
* **Base Platform:** A custom Linux distribution with a **Real-Time (RT) kernel** for minimal latency.
* **Audio Core:** **Ardour** (DAW/Mixer) running in **headless mode** (without a Graphical User Interface).
* **Audio Server:** **PipeWire (PW)**, replacing JACK, configured for maximum Real-Time (RT) priority.
* **Control:** A full-featured, responsive, and touch-friendly **Web Browser User Interface** (HTML5/JS) communicating with Ardour via an **OSC Bridge Server**.

### The Open Core Pledge and Commercial Sustainability

The critical mixing system core—the OLMS Distro, the RT Kernel, PipeWire configuration, Ardour Headless, the Web GUI, and the OSC Bridge Server—is **100% Open Source** and released under the **GPLv3 License**.

Our path to sustainability is an **Open Core Hybrid Model**. The commercial strategy is to focus on value, ensuring long-term integrity and full functionality for advanced, certified plugins through the **Official OLMS Activation Service** and by offering **Service Level Agreements (SLA)** and pre-configured hardware. This model guarantees stability and continuous development for the free core.

### Deliverable 0.3: Latency and Multi-Card Stability Certification

Practical tests and documentation are required to validate multi-card stability on PipeWire at **48 kHz** without X-runs for a prolonged period. The Round-Trip Latency tolerance must be less than $10 \text{ ms}$ ($< 10 \text{ ms}$). The long-term architectural goal is to achieve below $5 \text{ ms}$.
