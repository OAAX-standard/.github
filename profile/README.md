# OAAX — Open AI Accelerator eXchange

**OAAX** (Open AI Accelerator eXchange) is an open standard and reference implementation for running AI models across heterogeneous hardware accelerators — CPUs, GPUs, NPUs, VPUs, and emerging XPUs — with a unified runtime interface.

OAAX is a **Linux Foundation AI & Data** project, initiated by **Network Optix**, focused on defining a common runtime and model exchange layer that bridges AI frameworks, toolchains, and hardware vendors.

---

## 🌐 Vision

AI acceleration is fragmented. Each hardware vendor exposes different APIs, runtimes, and model formats — creating silos and duplication.

OAAX aims to **unify the interface between AI frameworks and hardware accelerators** by:
- Defining a **standard runtime API** that all AI accelerators can implement.
- Providing **toolchains** that convert models (e.g. ONNX) into AI accelerator-specific model packages.
- Enabling developers to **run the same model across diverse AI accelerators** without code changes.

---

## 🚀 Compliant AI accelerators

- CPUs
- Intel GPUs & NPUs
- NVIDIA GPUs
- DEEPX M1 and H1
- HAILO-8 and HAILO-8L

---

## 🏗️ Resources

- For general information about OAAX, visit its website at [https://www.oaax.org/](https://www.oaax.org/)
- To learn about which AI accelerators are compliant with the OAAX standard, visit this page: [Compliant AI Accelerators
](https://docs.oaax.org/Compliant%20XPU/)
- To learn how to deploy on a compliant AI accelerator, visit the tech docs at [https://docs.oaax.org/](https://docs.oaax.org/) and go to the page associated with the desired AI accelerator.
- To improve an existing runtime/toolchain implementation or implement a bug fix, visit the relevant repository on Github's repositories list at [https://github.com/orgs/OAAX-standard/repositories](https://github.com/orgs/OAAX-standard/repositories) to get started.
