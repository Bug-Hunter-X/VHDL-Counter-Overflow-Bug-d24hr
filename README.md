# VHDL Counter Overflow Bug

This repository demonstrates a common VHDL coding error: an integer counter that doesn't handle overflow correctly. The `buggy_counter.vhdl` file contains the buggy code, while `fixed_counter.vhdl` provides a corrected version. 

**Bug Description:**
The original code lacks a mechanism to prevent the counter from exceeding its defined range (0 to 15). When the counter reaches 15, incrementing it results in undefined behavior. In simulation, this may lead to unexpected values or even a simulation crash. In hardware, the outcome is unpredictable.

**Solution:**
The solution uses the `mod` operator to wrap the counter value around when it reaches the maximum value. This ensures the counter behaves as expected, continuously cycling from 0 to 15.

This example highlights the importance of carefully handling integer ranges and potential overflow situations when coding in VHDL or any other hardware description language.