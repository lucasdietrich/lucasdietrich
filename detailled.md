Hi, my name is Lucas, I'm 25 years old, I'm an embedded software engineer, working for Actimage GmbH since end of 2020. You can find on my GitHub most of my personnals projects related to embedded. Some are PoC, others are unachieved (yet) projects and others should even work ! And somehow documentated. 😃

# Projects 

- **On AVR architecture µC** :
    - [AVRTOS](https://github.com/lucasdietrich/AVRTOS#readme) : RTOS attempt for AVR 8bits microcontrollers: Multithreading (coop/prempt), scheduler, mutex, and more ... Compatible with (most of) AVR Arduino boards !
    - Reference application based on `AVRTOS` : [avr-can-tool](https://github.com/lucasdietrich/avr-can-tool) : Firmware for Arduino Pro/Mega in order to send and receive messages over a CAN bus using a shell over the UART. The purpose is to offer a tool to debug CAN devices messages.

- **ARMv7 architecture (Cortex-M4) + Zephyr RTOS** :
    - stm32f429zi :
        - **Currently working on** : [stm32f429zi-caniot-controller](https://github.com/lucasdietrich/stm32f429zi-caniot-controller), Firmware for a controller in order to monitor telemetry messages and send commands from/to (CAN) nodes. The controller will also have a interface for the Thread (or BLE) protocol in order to communicate with wireless devices in the same manner than devices on the CAN bus.
        - PoC (abandoned) [stm32f429zi-getting-started-zephyr-mbed-tls](https://github.com/lucasdietrich/stm32f429zi-getting-started-zephyr-mbed-tls#readme)

- **"CANIOT"**
    - Note :"CANIOT" stands for "CAN" and "IoT" because it is an IoT project based on CAN bus:
    - The purpose is to create an ecosystem of CAN devices and one (or several) controllers, in order to centralize control like switching lights, controlling garage doors or monitoring temperature.
    The controller works as a gateway and allow to interact with CAN devices from the Smartphone.

    - The current CANIOT controller is written in Python for a Raspberry PI (see [caniot-pycontroller](https://github.com/lucasdietrich/caniot-pycontroller#readme)) but I'm currently working on a C version for a Nucleo stm32F429zi with Zephyr RTOS (Introduced above [stm32f429zi-caniot-controller](https://github.com/lucasdietrich/stm32f429zi-caniot-controller))

    - As nodes are mostly based on AVR 8bits µC and the future controller will run on a ARM 32bits µC, I'm working on a library (see [caniot-lib](https://github.com/lucasdietrich/caniot-lib)) gathering all required functions and helpers to handle this home-made "CANIOT" protocol on several architectures using a common codebase. Current CANIOT implementation is in here : [caniot-common](https://github.com/lucasdietrich/caniot-common) with the implementation for the garage doors controller [caniot-garagedoorcontroller](https://github.com/lucasdietrich/caniot-garagedoorcontroller).

    - Specification and project for AVR nodes: [caniot](https://github.com/lucasdietrich/caniot)

- **PoC Thread / Matter** :
    - [thread-nrf52840-getting-started](https://github.com/lucasdietrich/thread-nrf52840-getting-started#readme)
    - [nrf52840-matter-getting-started](https://github.com/lucasdietrich/nrf52840-matter-getting-started#readme)

- **Others** (non-embedded) :
    - [gsurface](https://github.com/lucasdietrich/gsurface#readme) : Python library to simulate and plot simple or structured point masses guided by 2D surfaces using a Newton 2nd Law Approach

# Contributions

- Zephyr RTOS
    - Networking (mbedTLS and TCP stack) :
        - [net:sockets:tls MBEDTLS Heap optimisation and API support for chained X509 certificates in DER format #40267](https://github.com/zephyrproject-rtos/zephyr/issues/40267)
            - [[ v2.6-branch] net: sockets: tls: Support for DER cert chain and NOCOPY optimisation #40255](https://github.com/zephyrproject-rtos/zephyr/pull/40255)
            - [[ main ] net: sockets: tls: Support for DER cert chain and NOCOPY optimisation #40627](https://github.com/zephyrproject-rtos/zephyr/pull/40627)
        - [poll() not notified when a TLS/TCP connection is closed without TLS close_notify #39660](https://github.com/zephyrproject-rtos/zephyr/issues/39660)

    - Drivers CAN :
        - [drivers: can: Fixed timeout values comparison ](https://github.com/zephyrproject-rtos/zephyr/pull/40331)
    - Random Fix :
        - [kernel: Z_MEM_SLAB_INITIALIZER MACRO not compatible with C++ #38219](https://github.com/zephyrproject-rtos/zephyr/issues/38219)
            - [kernel/mem_slab: reorder Z_MEM_SLAB_INITIALIZER() initializers #38221](https://github.com/zephyrproject-rtos/zephyr/pull/38221)



---

![](https://github-readme-stats.vercel.app/api/top-langs/?username=lucasdietrich&langs_count=4&layout=compact)
