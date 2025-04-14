# CS-350: Emerging Systems Architectures and Technologies  
**Southern New Hampshire University | Cody VanGosen**

This repository contains project files and final submissions for the CS-350 course, showcasing embedded systems applications developed using Python, Raspberry Pi hardware, and various I/O components.

---

## 🔧 Project Overview

Throughout this course, I developed two embedded systems applications that demonstrate my ability to interface with hardware, implement concurrent programming principles, and manage system state logic using Python.

- **Artifact 1: `TemperatureSensorIntegration.py`**  
  This script displays temperature and humidity data on a 16x2 LCD and allows the user to toggle between Celsius and Fahrenheit using a physical button input.  
- **Artifact 2: `Thermostat.py`**  
  This program expands on the previous artifact by implementing a fully functional smart thermostat, incorporating three states (Off, Heat, Cool), temperature setpoint adjustments, LED indicators, UART communication, and real-time display updates via LCD.

---

## 💡 Key Takeaways & Reflection

Both projects were designed to solve the challenge of presenting real-time environmental data in a readable and interactive format, while maintaining responsiveness and stability under concurrent operations.

During the implementation of `TemperatureSensorIntegration.py`, I encountered and resolved a race condition that caused corrupted characters on the display. This issue was traced to unsynchronized access to the LCD from multiple threads. By applying Python’s `Lock` mechanism from the `threading` module, I resolved the issue and ensured consistent behavior under rapid user input (Python Software Foundation, 2023).

One area I performed particularly well in was the integration of hardware interfaces with clean, modular code. Each function was supported by detailed, line-by-line comments to enhance maintainability and collaboration. However, I recognize the opportunity to improve code reusability by refactoring repeated structures in the display and LED logic.

To support future development, I adopted several resources into my toolkit:  
- **Libraries:** `gpiozero`, Adafruit's sensor/display packages  
- **Documentation:** Python threading API, UART protocols, and LCD pinout references  
These tools significantly strengthened my confidence in diagnosing hardware behavior and implementing multithreaded workflows.

Skills developed in this course—especially state machine modeling, concurrent programming, and sensor integration—are directly transferable to future coursework and real-world IoT projects. Both artifacts reflect my growing ability to design scalable embedded systems that balance clarity, responsiveness, and functionality.

---

## ✅ Design Considerations

To ensure long-term maintainability:
- Clear naming conventions and modular class design were enforced
- State transitions were modeled using the `statemachine` package
- Thorough documentation and changelogs were included in all code
- Threading logic was isolated and protected with locks to avoid race conditions
- UART output was structured for future integration with external systems

---

## 🎥 Video Demonstrations

### Module Six Lab Demonstration  
[![Watch the video](https://img.youtube.com/vi/e_fi43AeBDw/maxresdefault.jpg)](https://www.youtube.com/watch?v=e_fi43AeBDw)

### Final Project Lab Demonstration  
[![Watch the video](https://img.youtube.com/vi/XHy1QBI6wC8/maxresdefault.jpg)](https://www.youtube.com/watch?v=XHy1QBI6wC8)

---

## 📚 References

Python Software Foundation. (2023). *threading — Thread-based parallelism*. https://docs.python.org/3/library/threading.html  
Pressman, R. S., & Maxim, B. R. (2020). *Software engineering: A practitioner’s approach* (9th ed.). McGraw-Hill Education.  
Bovet, D. P., & Cesati, M. (2005). *Understanding the Linux Kernel* (3rd ed.). O’Reilly Media.  
Microchip Technology Inc. (2023). *PIC32 family reference manual*. https://www.microchip.com/design-centers/32-bit  
NXP Semiconductors. (2023). *i.MX RT1060 Crossover MCU Family*. https://www.nxp.com/products/i.MX-RT1060  
