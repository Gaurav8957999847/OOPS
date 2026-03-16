# 🚗 Object-Oriented Programming (OOP) Concepts in C++

A hands-on learning repository that demonstrates the **four pillars of OOP** — Encapsulation, Abstraction, Inheritance, and Polymorphism — using a real-world **Car** analogy. Each concept is illustrated with its own standalone C++ file, making it easy to study and run independently.

---

## 📂 Project Structure

| File | OOP Concept | Description |
|------|-------------|-------------|
| `encapsulation.cpp` | **Encapsulation** | Bundling data & methods together with access control |
| `abstraction.cpp` | **Abstraction** | Hiding implementation details behind an interface |
| `inheritance.cpp` | **Inheritance** | Parent–child class relationships for code reuse |
| `staticpolym.cpp` | **Static Polymorphism** | Compile-time polymorphism via method overloading |
| `DynamicPolymorphism.cpp` | **Dynamic Polymorphism** | Runtime polymorphism via method overriding & virtual functions |
| `all.cpp` | **All Concepts Combined** | A unified example showcasing every OOP pillar together |

---

## 🧠 Concepts Covered

### 1. Encapsulation — `encapsulation.cpp`

> *An object's data and behaviour are bundled together, and access is controlled via access modifiers.*

- A `SportsCar` class wraps all attributes (`brand`, `model`, `currentSpeed`, etc.) as **private** members.
- Public **getters/setters** (`getSpeed()`, `setTyreCompany()`) provide controlled access to internal state.
- Demonstrates why direct access (e.g., `myCar->currentSpeed = 500`) is prevented for data integrity.

### 2. Abstraction — `abstraction.cpp`

> *An abstract class defines WHAT an object can do, not HOW it does it.*

- An abstract `Car` class declares pure virtual methods (`startEngine()`, `accelerate()`, `brake()`, etc.).
- The `SportsCar` concrete class inherits `Car` and provides the actual implementation.
- Uses the analogy of a car's pedals and buttons — the driver interacts with the interface without knowing the internal mechanics.

### 3. Inheritance — `inheritance.cpp`

> *Child classes inherit common properties from a parent class and add their own specialised features.*

- A base `Car` class defines shared attributes (`brand`, `model`, `currentSpeed`) and methods (`startEngine()`, `accelerate()`).
- `ManualCar` extends `Car` and adds a **gear system** (`shiftGear()`).
- `ElectricCar` extends `Car` and adds a **battery system** (`chargeBattery()`).
- Both child classes reuse the parent's engine and speed logic — demonstrating **code reusability**.

### 4. Static Polymorphism (Compile-Time) — `staticpolym.cpp`

> *The same method name can behave differently based on its parameters — resolved at compile time.*

- `ManualCar` has two versions of `accelerate()`:
  - `accelerate()` — increases speed by a **fixed** 20 km/h.
  - `accelerate(int speed)` — increases speed by a **custom** amount.
- This is classic **method overloading** — the compiler picks the right version based on the call signature.

### 5. Dynamic Polymorphism (Runtime) — `DynamicPolymorphism.cpp`

> *Objects from the same family respond to the same method call differently — resolved at runtime.*

- The base `Car` class declares `accelerate()` and `brake()` as **pure virtual** methods.
- `ManualCar` overrides them with gear-based acceleration logic.
- `ElectricCar` overrides them with battery-aware acceleration and regenerative braking.
- Both objects are accessed through a **`Car*` base pointer**, and the correct overridden method is called at runtime via the vtable.

### 6. All Concepts Combined — `all.cpp`

> *A single file that brings together encapsulation, abstraction, inheritance, and both forms of polymorphism.*

- Combines the `Car` (abstract base), `ManualCar`, and `ElectricCar` classes.
- Shows method **overloading** (static polymorphism) and **overriding** (dynamic polymorphism) side by side.
- Serves as a comprehensive reference for all OOP pillars in one place.

---

## 🔧 How to Compile & Run

Each file is a **self-contained program** with its own `main()` function. Compile and run any file individually using a C++ compiler:

```bash
# Using g++
g++ -o encapsulation encapsulation.cpp && ./encapsulation
g++ -o abstraction abstraction.cpp && ./abstraction
g++ -o inheritance inheritance.cpp && ./inheritance
g++ -o staticpolym staticpolym.cpp && ./staticpolym
g++ -o dynamic DynamicPolymorphism.cpp && ./dynamic
g++ -o all all.cpp && ./all
```

> **Requirements:** Any C++ compiler supporting C++11 or later (g++, clang++, MSVC).

---

## 🎯 Real-World Analogy

All examples revolve around a **Car** theme to make abstract OOP concepts intuitive:

| Real-World Element | OOP Mapping |
|--------------------|-------------|
| Car's pedals, buttons, steering wheel | **Abstraction** (interface for the driver) |
| Engine internals hidden under the hood | **Encapsulation** (private implementation) |
| Manual Car & Electric Car are both Cars | **Inheritance** (shared parent, specialised children) |
| Same "accelerate" pedal, different behaviour | **Polymorphism** (different responses to the same action) |

---

## 📌 Key Takeaways

- **Encapsulation** = Data protection via access modifiers + getters/setters.
- **Abstraction** = Pure virtual functions define *what*, concrete classes define *how*.
- **Inheritance** = `class Child : public Parent` enables code reuse and hierarchy.
- **Static Polymorphism** = Method overloading (same name, different parameters) — compile-time.
- **Dynamic Polymorphism** = Method overriding (virtual functions) — runtime, via base class pointers.

---

## 📜 License

This project is for **educational purposes**. Feel free to use, modify, and share.
