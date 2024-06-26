----!
Presentation
----!

# Hands-on exercises
## Implementing a simple BUS system that operates down to Stop mode

- Step-by-step guide on using HAL/LL/BSP libraries to manage BUS system
-	Utilizing DMA, LPTIM, RTC, Comparator, and Glass LCD in low-power condition
-	Verify consumption in STM32CubeMonitor-PWR

# Wired BUS System
Let imagine simple BUS architecture one Master Panel and multiple End devices.

- Two wires BUS 
    - DC power supply + communication
    - VSS
- Data stream are modulated as Edges in power line
- Defined Low pulse widths for 1/0 bit in range hundred of microseconds to few milliseconds
- Proprietary protocol
    - typically start bit + data + stop bits

![image](./img/MasterBusEnd.png)

![image](./img/stream.png)

# Prerequisites
- Software:
  - **[STM32CubeMX](https://www.st.com/en/development-tools/stm32cubemx.html)** from version 6.11.0
  - **[STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)** from version 1.15.1
  - **[STM32U0 Cube library](https://www.st.com/en/embedded-software/stm32cubeu0.html)** from version 1.0.0
  - **[STM32Cube Monitor Power](https://www.st.com/en/development-tools/stm32cubemonpwr.html)** from version 1.2.1
<br>
- Hardware:

  - **2 USB-C** cables 
  <br>
  - **2 female-female wires** (min 10cm length) to connect header pins 
  <br>
  - **[NUCLEO-U083RC](https://www.st.com/en/evaluation-tools/nucleo-u083rc.html)** board 
  <br>
  ![image](./img/nucleo.png)
  <br>
  - **[STM32U083C-DK](https://www.st.com/en/evaluation-tools/stm32u083c-dk.html)** board 
  <br>
  ![image](./img/DK.png)
  <br>
  - **[STLINK-V3PWR](https://www.st.com/en/development-tools/stlink-v3pwr.html)** board 
  <br>
  ![image](./img/V3PWR.png)
  <br>
  - Alternatively you can take your own multimeter with 1uA current measurement range
  <br>

