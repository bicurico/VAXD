# VAXD

<p align="left">
  <img src="screenshots/VAXD%20-%20Small.png" alt="VAXD Logo" width="180">
</p>

**VAXD** is a lightweight Windows disassembler, PE inspection tool, and patch-assistance environment for native Windows executable files.

It is designed for fast analysis of Windows PE EXE and DLL files, with a practical workflow focused on disassembly, navigation, strings, jumps, calls, patch planning, pseudo-code generation, and binary patching.

VAXD focuses on speed, simplicity, and usability. It is intended for users who want a quick and focused tool for inspecting native Windows executables without the complexity and overhead of larger reverse-engineering suites.

---

## Screenshot

![VAXD main window](screenshots/Screenshot.png)

---

## Features

### PE File Analysis

VAXD opens and analyses native Windows PE executable files, including EXE and DLL files.

It provides a structured view of the loaded file and allows the user to inspect discovered code, functions, exports, strings, patches, and references.

Main PE analysis features include:

* Native Windows PE EXE/DLL inspection
* Automatic PE architecture detection
* Function/subroutine listing
* DLL export detection
* Fast function navigation
* File information display
* Integrated analysis workflow

---

### Disassembly View

The main disassembly view shows the decoded instructions of the selected function.

Each line displays the instruction address, decoded instruction, operands, and related analysis information. The view is optimized for readability and fast manual inspection.

Disassembly features include:

* Function-based disassembly
* Address and instruction display
* Syntax highlighting
* Jump and call recognition
* Patched instruction highlighting
* User comments
* String reference comments
* Multi-line selection
* Copy selected disassembly lines to the clipboard

---

### HEX Opcode Column

VAXD displays the raw HEX bytes next to the corresponding disassembled instruction line.

This makes it easier to compare the decoded assembly instruction with the original machine code bytes.

The HEX opcode column is useful for:

* Inspecting original instruction bytes
* Comparing patched and unpatched code
* Copying byte sequences
* Understanding jump and call encoding
* Searching for opcode patterns
* Verifying patch results

---

### Jump and Call Visualization

VAXD provides visual assistance for understanding control flow inside a function.

Jump and call instructions are detected and displayed with navigation support, making it easier to follow branches and understand execution paths.

Jump and call features include:

* Conditional jump detection
* Unconditional jump detection
* Call instruction detection
* Visual jump arrows
* Branch target navigation
* Go to jump destination
* Back and forward navigation
* Relative jump calculation
* Call target navigation

---

### Patch Assistance

VAXD includes helper functions for common binary patching operations.

The goal is to make simple patching tasks faster, clearer, and less error-prone by calculating the required instruction bytes automatically where possible.

Patch features include:

* NOP selected instruction
* NOP multiple selected lines
* Invert conditional jumps
* Change jump destination
* Force conditional jump to unconditional jump
* Automatic relative offset calculation
* Patch list display
* Patch navigation
* Double-click patch entry to return to the patched instruction
* Save patched executable when licensed

Patched instructions are visually highlighted in the disassembly view.

---

### Pseudo-Code Generation

VAXD includes pseudo-code generation for selected functions.

The pseudo-code view provides a simplified, readable approximation of the selected assembly routine. It is intended as an analysis aid, helping the user quickly understand the general structure and logic of a function.

Pseudo-code generation can help identify:

* Function structure
* Conditional branches
* Calls
* Return points
* Basic control flow
* Common logical patterns

The generated pseudo-code is not intended to be a perfect decompilation. It is a practical helper for faster manual analysis.

---

### Strings View

VAXD includes a string inspection view for locating and analysing text found inside the executable.

This is useful for identifying messages, prompts, file paths, registry keys, URLs, error strings, command-line text, and other embedded data.

String features include:

* Extracted string listing
* String search
* Optional string filtering
* Column sorting
* String reference navigation where available
* View surrounding strings in memory order
* Copy selected strings

The string tools support both direct search and exploratory analysis.

---

### Search and Navigation

VAXD includes several navigation helpers to reduce the time spent manually scrolling through large functions or switching between related areas of code.

Navigation features include:

* Function list navigation
* Jump target navigation
* Call target navigation
* String reference navigation
* Patch list navigation
* Back and forward navigation
* Search inside the current disassembly
* Search for byte sequences
* Search strings
* Double-click navigation from lists to code

---

### Project Save and Load

VAXD can save and reload analysis projects when licensed.

A saved project preserves the current analysis state, allowing work to continue across multiple sessions.

Project data may include:

* Loaded file information
* Disassembly state
* Function list
* Strings
* User comments
* Patch list
* Navigation and analysis data

---

### User Comments

VAXD allows user comments to be added to disassembly lines.

Comments are useful for recording analysis notes, marking important instructions, documenting suspected logic, or explaining patch decisions.

Typical uses include:

* Marking important branches
* Labelling calls
* Documenting license checks
* Recording patch purpose
* Adding reminders for later review
* Explaining analysis findings

---

## Typical Use Cases

VAXD is intended for legitimate software analysis and inspection tasks, including:

* Analysing native Windows executables
* Inspecting DLL files
* Understanding program control flow
* Studying jump and call behaviour
* Locating string references
* Inspecting binary patches
* Learning assembly
* Educational reverse-engineering exercises
* Malware triage in controlled environments
* Debugging and interoperability research
* Analysing software you own or are authorized to inspect

---

## Download

Download the latest release package from the GitHub Releases section:

https://github.com/bicurico/VAXD/releases/latest

---

## Release Package

The release package includes the VAXD application, required runtime components, short documentation, third-party license notices, and the full user guide.

Typical package contents:

* `VAXD.exe`
* `Iced.dll`
* `README.txt`
* `VAXD User Guide.pdf`

---

## License

The free version allows inspection and analysis.

Saving projects, exporting patched files, and generating patched executables require a license.

For license requests, contact:

**[vma@norcam.pt](mailto:vma@norcam.pt)**

---

## Intended Use Notice

VAXD is intended for legitimate software analysis, education, debugging, interoperability research, malware triage, and inspection of software you own or are authorized to analyse.

VAXD is not intended to promote unauthorized software modification, circumvention, cracking, piracy, or misuse of third-party software.

The user is responsible for ensuring that any analysis or modification performed with VAXD complies with applicable laws, license agreements, and authorization boundaries.

---

## Third-Party Components

VAXD uses `Iced.dll`, based on the Iced disassembler library.

Iced is licensed under the MIT License.

The required third-party license text is included in the distributed documentation.

---

## Version History

* **0.19** - First release
* **0.20** - Internal release
* **0.21** - Added HEX values next to opcode lines
* **0.22** - Added pseudo-code generation
* **0.23** - Added string list sorting/filtering and multi-line copy support
* **1.00** - First official public release
