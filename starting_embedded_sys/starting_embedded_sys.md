# How to Self-Learn Embedded Systems in 2021

![Printed Circuit Board](https://i.imgur.com/WJPItsO.jpg)

In a couple of days, the year 2020 will come to a climax. It has been a rollercoaster of a year. During the course of the past few months, I got a lot of questions regarding how to start out in the field of Embedded systems especially in a place like Africa where opportunities to learn are scarce. That made me see a need to put up this article. Asides from this article, I will be dishing out content relating to Embedded Systems and the Internet of things has I have made getting more people into the embedded domain one of my goals for the new year. So join me on this journey!

For context, what is Embedded Systems? It can be defined as a combination of hardware and software which resides on the hardware, brought together to perform a specific function or specific user requirement. As opposed to a computer that can perform several operations, embedded systems are meant to perform specific tasks. Examples of such systems include Microwaves, Washing Machines, Digital thermometers, e.t.c

In order to provide a clear path to learn this interesting and ever dynamic field, I will like to segment the learning path into two:

1. Embedded Software
1. Embedded Hardware

## Embedded Software

* Learn C: About 95% of embedded systems applications are written in C. Understanding it will help you a lot in your Embedded systems journey. There are other programming languages (such as C++, Assembly, and Rust) that you must add to your arsenal as you progress. But for starters, C should come first. I recommend the book [Learn C the hard way by Zed Shaw](https://www.amazon.com/Learn-Hard-Way-Practical-Computational/dp/0321884922).

* Real-Time Operating System(RTOS): When an Embedded application makes use of various communication interfaces, has more interrupt sources, and uses more functions, it is usually imperative to make use of RTOS has it helps to effectively manage resources. I usually recommend FreeRTOS as it is free and most commonly used.

* Learn Embedded Linux: For learning Embedded Linux, I will recommend [Yocto](https://www.yoctoproject.org). This is because Yocto helps you to build an Embedded Linux application that is not hardware architecture agnostic. Yocto makes use of [Openembedded](https://www.openembedded.org/wiki/Main_Page) as it's build system.

One thing I want to make clear is that it's not a rule of thumb to learn all the three components of embedded software mentioned above first before venturing into the hardware part. A clear understanding of C is good enough to get you started.
