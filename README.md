# Thread Scheduling, Synchronization, and Memory Optimization for Simulated Kernel

## Overview
This project is an implementation of advanced thread scheduling and synchronization mechanisms within a simulated kernel environment. It was developed as part of an operating systems course to explore low-level design and concurrency management techniques. The project focuses on efficient thread management, multi-level priority scheduling, and virtual memory optimization.

## Key Features
- **Thread Scheduling Algorithms**: Includes nested priority donation and optimized round-robin scheduling, achieving faster context switching and reduced overhead.
- **Low-Level Synchronization Mechanisms**: Implements thread blocking, ordered sleep lists, and multi-level priority donation to handle contention and race conditions efficiently.
- **Memory Optimization**: Employs fixed-point arithmetic for CPU scheduling and load tracking, minimizing computational overhead and improving system responsiveness.
- **Support for Concurrency**: Designed to handle synchronization challenges in multi-threaded environments.

## Directory Structure
```
pa1-team-19-main/
|-- .github/            # GitHub-specific configurations (e.g., workflows).
|-- .gitignore          # Defines ignored files and directories.
|-- README.md           # Documentation for the project.
|-- src/                # Source code and implementation.
    |-- devices/        # Device drivers and related code.
    |-- examples/       # Example programs and demonstrations.
    |-- filesys/        # File system implementation.
    |-- lib/            # Shared libraries and utilities.
    |-- misc/           # Miscellaneous utilities.
    |-- tests/          # Test cases for validation.
    |-- threads/        # Core thread scheduling and synchronization code.
    |-- userprog/       # User-level program support.
    |-- vm/             # Virtual memory management components.
```

## Technologies Used
- **Programming Language**: C
- **Build System**: Make
- **Key Concepts**: Multithreading, Kernel Design, Priority Scheduling, Fixed-Point Arithmetic, Synchronization

## Setup and Compilation
1. Clone the repository:
   ```bash
   git clone <repository-link>
   ```
2. Navigate to the `src/` directory:
   ```bash
   cd pa1-team-19-main/src
   ```
3. Build the project using `make`:
   ```bash
   make
   ```
4. Run tests to validate the implementation:
   ```bash
   make check
   ```

## How to Run
1. After building the project, navigate to the appropriate directory (e.g., `threads/`).
2. Execute the program or test specific components using the provided executables.
3. Check logs and results for validation.

## Key Algorithms
### Thread Scheduling
- Implements a priority-based scheduler with nested priority donation to prevent priority inversion.
- Optimized round-robin scheduling reduces context switch times by 2x compared to a baseline round-robin scheduler.

### Synchronization Mechanisms
- Ordered sleep lists minimize contention and ensure efficient wake-up operations.
- Multi-level priority donation supports efficient handling of complex thread dependencies.

### Memory Optimization
- Fixed-point arithmetic for CPU load tracking and priority calculations reduces computational overhead.

## Testing
- Comprehensive test cases located in the `tests/` directory.
- Validates thread scheduling, priority donation, and synchronization features.
- Includes edge case testing for complex multi-threaded scenarios.

## License
This project is licensed under the MIT License. See the `LICENSE` file in the `src/` directory for details.

## Acknowledgments
- **Course Materials**: Leveraged Pintos documentation, course texts, and lecture notes.
- **Additional Resources**: Referenced external articles and repositories for inspiration and guidance.

## Future Improvements
- Implement a 64-queue priority scheduler for better scalability.
- Enhance support for virtual memory features such as demand paging and page eviction policies.
- Further optimize synchronization mechanisms to handle higher concurrency levels.



