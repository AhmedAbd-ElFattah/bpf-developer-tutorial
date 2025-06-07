# eBPF Tutorial by Example 0: Introduction to Core Concepts and Tools

## Introduction to eBPF: Secure and Efficient Kernel Extension

eBPF (extended Berkeley Packet Filter) allows developers to run small programs safely and efficiently in the kernel space. It enables dynamic customization and optimization of network behavior without modifying kernel source code, loading modules, or disrupting system operations. 

### What Makes eBPF So Powerful?

- **Direct Kernel Interaction:** eBPF programs execute within the kernel, interacting with system-level events such as network packets, system calls, or tracepoints.
- **Safe Execution:** eBPF ensures safety through a verifier that checks the logic of the program before it runs, preventing potential kernel crashes or security breaches.
- **Minimal Overhead:** eBPF achieves near-native execution speed by employing a Just-In-Time (JIT) compiler, which translates eBPF bytecode into optimized machine code for the specific architecture.

## eBPF: Past, Present, and Future
Some key areas where eBPF is widely used today:

- **Networking:** eBPF offers real-time, high-speed packet filtering and processing within the kernel, allowing for the creation of custom protocol parsers and network policies without needing new drivers or system restarts. This enables highly efficient network management in cloud and data center environments.

- **Observability:** eBPF enables developers to gather detailed insights into system behavior by collecting custom metrics and performing in-kernel data aggregation. By tapping into kernel tracepoints and function calls, eBPF helps identify performance issues and track down elusive bugs.

- **Tracing & Profiling:** eBPF provides powerful tracing and profiling capabilities by attaching to kernel functions, tracepoints, and even user-space probes. This allows developers to gain deep insights into system and application behavior, enabling them to optimize performance and resolve complex system issues.

- **Security:** eBPF plays a vital role in real-time security monitoring. It enables deep inspection of system calls, network traffic, and other kernel activities, helping to enforce dynamic security policies and detect anomalous behavior, providing an efficient way to safeguard infrastructure.

- **Scheduler Optimization:** eBPF is increasingly used to enhance CPU scheduling, offering the ability to monitor CPU load and optimize how tasks are distributed across cores. This can lead to more efficient use of CPU resources and improved system responsiveness.

- **HID (Human Interface Device) Driver Enhancements:** Developers use eBPF to optimize HID drivers for devices like keyboards, mice, and touchscreens. By adding custom logic for handling input events, eBPF improves responsiveness in latency-sensitive applications.

---

### Tools for eBPF Development

- **BCC**: A Python-based toolchain that simplifies writing, compiling, and loading eBPF programs. It offers many pre-built tracing tools but has limitations with dependencies and compatibility.
- **eBPF Go Library**: A Go library that decouples the process of obtaining eBPF bytecode from the loading and management of eBPF programs.
- **libbpf-bootstrap**: A modern scaffold based on `libbpf` that provides an efficient workflow for writing eBPF programs, offering a simple one-time compilation process for reusable bytecode.
- **eunomia-bpf**: A toolchain for writing eBPF programs with only kernel space code. It simplifies the development of eBPF programs by dynamically loading them.

These tools help reduce the complexity of developing eBPF programs, making the process more accessible to developers aiming to optimize system performance, security, and observability.

## Some Tips on Learning eBPF Development

This article will not provide a more detailed introduction to the principles of eBPF, but here is a learning plan and reference materials that may be of value:

### Introduction to eBPF (5-7h)

- Google or other search engines: eBPF
- Ask ChatGPT-like things: What is eBPF?

Recommended:

- Read the introduction to ebpf: <https://ebpf.io/> (30min)
- Briefly understand the ebpf kernel-related documentation: <https://docs.ebpf.io/> (Know where to queries for tech details, 30min)

Answer three questions:

1. Understand what eBPF is? Why do we need it? Can't we use kernel modules?
2. What functions does it have? What can it do in the Linux kernel? What are the types of eBPF programs and helpers (not all of them need to be known, but need to know where to find them)?
3. What can it be used for? For example, in which scenarios can it be used? Networking, security, observability?

### Understand how to develop eBPF programs (10-15h)

Understand and try eBPF development frameworks:

- bpftrace tutorial：<https://eunomia.dev/tutorials/bpftrace-tutorial/> （Try it，1h）
- Examples of developing various tools with BCC: <https://github.com/iovisor/bcc/blob/master/docs/tutorial_bcc_python_developer.md> (Run through, 3-4h)
- Some examples of libbpf: <https://github.com/libbpf/libbpf-bootstrap> (Run any interesting one and read the source code, 2h)
- Tutorials: <https://github.com/eunomia-bpf/bpf-developer-tutorial> (Read part 1-10, 3-4h)

Other development frameworks: Go or Rust language, please search and try on your own (0-2h)

Have questions or things you want to know, whether or not they are related to this project, you can start discussing in the discussions of this project.

Answer some questions and try some experiments (2-5h):

1. How to develop the simplest eBPF program?
2. How to trace a kernel feature or function with eBPF? There are many ways, provide corresponding code examples;
3. What are the solutions for communication between user mode and kernel mode? How to send information from user mode to kernel mode? How to pass information from kernel mode to user mode? Provide code examples;
4. Write your own eBPF program to implement a feature;
5. In the entire lifecycle of an eBPF program, what does it do in user mode and kernel mode?

## References

- eBPF Introduction: <https://ebpf.io/>
- BPF Compiler Collection (BCC): <https://github.com/iovisor/bcc>
- eunomia-bpf: <https://github.com/eunomia-bpf/eunomia-bpf>

You can also visit our tutorial code repository <https://github.com/eunomia-bpf/bpf-developer-tutorial> or website <https://eunomia.dev/tutorials/> for more examples and complete tutorial source code. All content is open source. We will continue to share more content about eBPF development practices to help you better understand and master eBPF technology.".
