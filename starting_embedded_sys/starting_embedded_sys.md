# How to Self-Learn Embedded Systems in 2021

![Printed Circuit Board](https://i.imgur.com/WJPItsO.jpg)

In a couple of days, the year 2020 will come to a climax. It has been a rollercoaster of a year. During the course of the past few months, I got a lot of questions regarding how to start out in the field of Embedded systems especially in a place like Africa where opportunities to learn are scarce. That made me see a need to put up this article. Asides from this article, I will be dishing out content relating to Embedded Systems and the Internet of things has I have made getting more people into the embedded domain one of my goals for the new year. So join me on this journey!

For context, what is Embedded Systems? It can be defined as a combination of hardware and software which resides on the hardware, brought together to perform a specific function or specific user requirement. As opposed to a computer that can perform several operations, embedded systems are meant to perform specific tasks. Examples of such systems include Microwaves, Washing Machines, Digital thermometers, e.t.c

In order to provide a clear path to learn this interesting and ever dynamic field, I will like to segment the learning path into two:

1. Embedded Software
1. Embedded Hardware

## Embedded Software

* **Learn C:** About 95% of embedded systems applications are written in C. Understanding it will help you a lot in your Embedded systems journey. There are other programming languages (such as C++, Assembly, and Rust) that you must add to your arsenal as you progress. But for starters, C should come first. I recommend the book [Learn C the hard way by Zed Shaw](https://www.amazon.com/Learn-Hard-Way-Practical-Computational/dp/0321884922).

* **Real-Time Operating System(RTOS):** When an Embedded application makes use of various communication interfaces, has more interrupt sources, and uses more functions, it is usually imperative to make use of RTOS has it helps to effectively manage resources. I usually recommend FreeRTOS as it is free and most commonly used.

* **Learn Embedded Linux:** For learning Embedded Linux, I will recommend [Yocto](https://www.yoctoproject.org). This is because Yocto helps you to build an Embedded Linux application that is not hardware architecture agnostic. Yocto makes use of [Openembedded](https://www.openembedded.org/wiki/Main_Page) as it's build system.

One thing I want to make clear is that it's not a rule of thumb to learn all the three components of embedded software mentioned above first before venturing into the hardware part. A clear understanding of C is good enough to get you started.

## Embedded Hardware

![STM32F407 Development Board](https://i.imgur.com/w3X0Bfy.jpg)

This is where you start to get your hands dirty. I would like to state categorically that a lot of perseverance and resilience is needed here as you will surely need it when you get stuck with a problem.

* **Learn Basic Electronics:** Every hardware system will surely consist of electronic components so understanding what they look like, how they work and their area of application is very important. Also, learning about their schematic symbol will also help when you want to read a circuit diagram. I recommend you pick up a development board such as the STM32F407 discovery board shown above and try to identify the components on it. Try this for every board you come across and see how fast you learn.

* **Read Device Datasheets:** The device datasheet is the Embedded Systems Engineer's "best friend". It contains all the relevant information that aids firmware and hardware development. For example, when it comes to configuring registers of peripherals in a microcontroller, your best bet is to consult the device datasheet. So before you embark on that project, ensure you consult the appropriate datasheet. Later in the coming year, I will publish an article that elaborates more on how to read datasheets.

* **Learn About Power Supply:** No matter how impressive an embedded product is if the power supply section is not well designed, the entire system is flawed. The power supply section is the section that brings your entire system to life so learning proper power supply design is important. There are four major types of power supply designs but for a start, pay attention to Linear regulated and Switching(SMPS) power supply.

* **Learn Printed Circuit Board(PCB) design:** The design of a PCB is what comes next after a prototype has been iterated on properly. The PCB brings your design to a complete physical form ready for use by the intended target market. Learn basic schematic and PCB using free but powerful tools such as Kicad. I recommend Kicad because it is free and has huge community support. Other professional tools include Altium, Diptrace, Eagle, EasyEda, ExpressPCB, etc. From basic designs, you can then move on to more advanced designs(2 layers and above).

* **Measurement and Test Equipment:** Measurement and test equipment helps Engineers make informed decisions and so are essential to successful design implementation. Learn how to use tools like Logic analyzers, Multimeters, Oscilloscope, etc.

* **Debugging:** There is no one size fits all when it comes to debugging. The design you are working on determines the debugging approach to be used. But two things remain constant. **PERSEVERANCE AND PATIENCE**. These two attributes will really help you in your journey.
