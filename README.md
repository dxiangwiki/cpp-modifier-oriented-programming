# C++ 面向修饰符编程（Modifier-Oriented Programming）
A creative C++ programming paradigm inspired by **Vue event modifiers**, which decouples the core logic of functions from behavior variants through predefined modifiers.

## 🌟 Core Idea
The core of this paradigm is to **separate "core business logic" and "behavior variant logic"**:
- The core function focuses only on the basic implementation.
- The modifier acts as a "behavior switch" to drive different function behaviors without invading the core code.

## ✨ Key Advantages
1. **Semantic clarity**: Modifier names are intuitive (e.g., `zero` means "return 0 for negative numbers").
2. **Compile-time error checking**: Predefined modifier instances avoid runtime hidden errors caused by string parameters.
3. **Zero-overhead abstraction**: Complies with C++'s design philosophy, no additional runtime overhead.
4. **High scalability**: Add new modifiers without modifying existing core logic (open-closed principle).
5. **Standardized semantics**: Use function overloading to clearly distinguish "no modifier" and "with modifier".

## 🚀 Quick Start
### Environment Requirements
- C++11 or higher
- Any standard-compliant C++ compiler (GCC, Clang, MSVC)

### Basic Example
Compile and run the basic absolute value demo:
```bash
g++ examples/basic_abs_demo.cpp -o abs_demo -std=c++11
./abs_demo
```

#### Output Result
```plaintext
=== No modifier (default absolute value) ===
2
1
0
1
2

=== Modifier: original (return original value) ===
-2
-1
0
1
2

=== Modifier: zero (return 0 for negative numbers) ===
0
0
0
1
2
```

## 📚 Detailed Documentation
### 1. Basic Implementation Principle
- **Modifier Namespace**: Encapsulate modifier carriers and instances to avoid naming conflicts.
- **Modifier Carrier**: Use lightweight struct to hide underlying implementation details.
- **Predefined Modifiers**: Use `constexpr` to create compile-time constants for type safety.
- **Function Overloading**: Distinguish "no modifier" and "with modifier" versions to clarify semantics.

### 2. Advanced Optimization Schemes
- **Type-safe Optimization**: Use `enum class` to prevent illegal modifier construction.
- **Strategy Pattern Optimization**: Replace switch with strategy functions for better scalability.
- **Modifier Combination**: Support multiple modifier combinations via bitwise OR operations.

> See the `examples/` directory for all optimization versions.

## 🎯 Applicable Scenarios
- **Data processing**: Image processing (grayscale, blur), numerical conversion (round, floor).
- **Log output**: Control log level (debug, info, error) and output format (text, JSON).
- **Interface adaptation**: Control data serialization (Protobuf, JSON) and encryption methods (AES, RSA).
- **Tool functions**: String processing, mathematical calculations that require multiple behavior variants.

## 📄 License
This project is licensed under the MIT License - see the `LICENSE` file for details.

## 💡 Contribution Guide
1. Fork the repository.
2. Create your feature branch (`git checkout -b feature/amazing-feature`).
3. Commit your changes (`git commit -m 'Add some amazing feature'`).
4. Push to the branch (`git push origin feature/amazing-feature`).
5. Open a Pull Request.

## 🙏 Acknowledgments
- Inspired by Vue event modifiers (`.stop`, `.prevent`).
- Adheres to C++'s zero-overhead abstraction design philosophy.

---
