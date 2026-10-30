<p align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" width="45%" srcset="https://raw.githubusercontent.com/OAAX-standard/OAAX/74de2ec57606be7886acaf8dd11cc54a07add5c8/media/logo%20-%20white.png">
  <source media="(prefers-color-scheme: light)" width="45%" srcset="https://raw.githubusercontent.com/OAAX-standard/OAAX/_media/media/logo%20-%20black.png">
  <img alt="Open AI Accelerator eXchange (OAAX)" width="45%" src="https://raw.githubusercontent.com/OAAX-standard/OAAX/_media/media/logo%20-%20black.png">
</picture>
</p>

# OAAX — Open AI Accelerator eXchange

> **OAAX 2.0 is released.** Read the [Specification](https://docs.oaax.org/Specification/). Runtimes and toolchains for
> [CPU](https://github.com/OAAX-standard/reference-implementation/releases/tag/v2.0.0),
> [Intel](https://github.com/OAAX-standard/intel-acceleration/releases/tag/v2.0.0),
> [NVIDIA](https://github.com/OAAX-standard/nvidia-acceleration/releases/tag/v2.0.0),
> [Hailo](https://github.com/OAAX-standard/hailo-acceleration/releases/tag/v2.0.0) and
> [DEEPX](https://github.com/OAAX-standard/deepx-acceleration/releases/tag/v2.0.0) are published; other chips follow in 2.1.

**OAAX** is an open standard for running AI models on any AI accelerator (CPU, GPU, NPU, VPU, ...) through one
runtime interface. Convert your ONNX model once per chip, load the chip's runtime, and your application code stays the
same.

OAAX is a **Linux Foundation AI & Data** project, initiated by **Network Optix**.

## How it works

```
 ONNX model ──▶ [ Conversion toolchain ] ──▶ chip-specific model ──▶ [ Runtime library ] ──▶ results
                 (Docker image, per chip)                            (.so / .dll, per chip, same C API)
```

- **Toolchain**: a Docker image that turns an ONNX model into the format a given chip needs.
- **Runtime**: a shared library that loads that model and runs inference on the chip. Every chip's runtime exposes the
  same API, so your host application does not change when you swap accelerators.

## Start here

| I want to... | Go to |
|---|---|
| Understand the standard | [Welcome to OAAX](https://docs.oaax.org/) and the [FAQ](https://docs.oaax.org/FAQ/) |
| Run a model on an accelerator | [Getting Started](https://docs.oaax.org/Getting%20Started/) (face detection on CPU and Intel, OAAX 2.0) |
| Call a runtime from my own program | [`examples`](https://github.com/OAAX-standard/examples): a standalone C example, `bash c-example/build-run.sh` runs it on the CPU |
| Drive a runtime from Python | [`PythonBindings`](https://github.com/OAAX-standard/PythonBindings) ([PyPI](https://pypi.org/project/oaax/), `import oaax`): load any OAAX runtime with NumPy arrays, with CPU examples |
| Download a runtime or toolchain, checksum-verified | [`oaax-manager`](https://github.com/OAAX-standard/oaax-manager) ([PyPI](https://pypi.org/project/oaax-manager/)): `uvx oaax-manager fetch runtime cpu` |
| Check a runtime or toolchain against the spec | [`oaax-conformance`](https://github.com/OAAX-standard/conformance) ([PyPI](https://pypi.org/project/oaax-conformance/)) |
| Implement OAAX for my chip | [Specification (2.0)](https://docs.oaax.org/Specification/) and the [`reference-implementation`](https://github.com/OAAX-standard/reference-implementation) to copy from |
| Fix a bug or improve a runtime | The chip's repository below, then [CONTRIBUTING](https://github.com/OAAX-standard/OAAX/blob/main/CONTRIBUTING.md) |

## Compliant AI accelerators

| Accelerator | Hardware | Repository |
|---|---|---|
| CPU | x86_64 and ARM64 | [`reference-implementation`](https://github.com/OAAX-standard/reference-implementation) |
| Intel | CPU, GPU, NPU | [`intel-acceleration`](https://github.com/OAAX-standard/intel-acceleration) |
| NVIDIA | CUDA GPUs | [`nvidia-acceleration`](https://github.com/OAAX-standard/nvidia-acceleration) |
| DEEPX | DX-M1, DX-H1 | [`deepx-acceleration`](https://github.com/OAAX-standard/deepx-acceleration) |
| Hailo | Hailo-8, Hailo-8L | [`hailo-acceleration`](https://github.com/OAAX-standard/hailo-acceleration) |

Details and per-chip setup: [Compliant AI Accelerators](https://docs.oaax.org/Compliant%20XPU/).
Building a runtime for another chip? Open an issue in [OAAX](https://github.com/OAAX-standard/OAAX/issues).

## Repositories

- [`OAAX`](https://github.com/OAAX-standard/OAAX): the specification, documentation site and interface headers
- [`reference-implementation`](https://github.com/OAAX-standard/reference-implementation): reference runtime and toolchain
- [`examples`](https://github.com/OAAX-standard/examples): host-application examples
- [`PythonBindings`](https://github.com/OAAX-standard/PythonBindings): Python bindings (`oaax` on PyPI) for any OAAX runtime
- [`oaax-manager`](https://github.com/OAAX-standard/oaax-manager): download and verify runtimes and toolchains
- [`conformance`](https://github.com/OAAX-standard/conformance): the conformance suite for runtimes and toolchains
- `*-acceleration`: one runtime and toolchain per chip (table above)
- [`steering-committee`](https://github.com/OAAX-standard/steering-committee): governance, meeting notes and roadmap

## Get involved

- Browse the [open issues](https://github.com/orgs/OAAX-standard/repositories) of any repository and pick one.
- Commits need a DCO sign-off (`git commit -s`); see [CONTRIBUTING](https://github.com/OAAX-standard/OAAX/blob/main/CONTRIBUTING.md).
- Follow the [roadmap and meeting notes](https://github.com/OAAX-standard/steering-committee).
- Website: [oaax.org](https://www.oaax.org/)
