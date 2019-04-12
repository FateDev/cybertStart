# Computer Hardware

#### Motherboard

There are many types of motherboard, these are the sizes in order of largest to smallest:

- E-ATX
- ATX
- micro-ATX
- mini-ATX

Motherboards have **socket types**, and will only accept CPU's of the correct socket type, such as AM4 or LGA2011, for example.

They also have **buses**, which effectively move data between the components, think of them as a physical connection to the motherboard, and as such, physical connections in between the components.

#### CPU

The **CPU** is made up of an *ALU* and a *Control Unit*, along with many registers to process data (though cores generally contain those, and the CPU generally contains multiple cores). The front of the processor typically has a silver lid on it, and the back has small gold pins, which connect it to the motherboard. These pins are arranged according to the *socket specification*, and as such go in a motherboard of a compatible socket type.

Each processor contains **cores**, which are responsible for actually processing data and executing instructions. Modern processors generally have multiple cores to allow them to perform multiple tasks in parallel, and older processors may have had a single core, but by using context switching, they could achieve what would appear to be multi tasking.

Back to instructions in a PC, the **clock speed** is the number of instructions it can execute per second, so 4GHz means it can execute 4 billion instructions per second.

The **context switching** I mentioned before is just the CPU allocating processor time between multiple applications, thereby giving the user the illusion that multiple tasks are occurring at the same time.

#### RAM

**Random Access Memory** (RAM), is a type of **volatile storage** that your CPU can access very fast, and so it is used to hold programs that are currently in use, which greatly decreases the latency between user input to a program and the output, making everything appear faster. A stick of RAM has gold connectors at the bottom, and slot into your motherboard. 8GB is a pretty common RAM capacity nowadays.

As mentioned before, the **speed** of the RAM (the read and write speeds to/from it), far outmatch other forms of storage such as a hard disk, so it makes it easier for the processor to access the data it needs. The processor accesses data by referring to specific memory locations in RAM.

Also, as I mentioned before, it is volatile, so that once energy is turned off and then on again, all of the data that was previously there, will be gone, so as such, it is not a suitable replacement to a hard disk drive, or some non-volatile storage, despite its speed advantage.

RAM will also have compatibility issues if the motherboard doesn't accept it's type. RAM has types, such as **DDR2/DDR3/DDR4** (from older to newest). DDR4 is the newest one, and a lot of older motherboards don't support it, but DDR3 was released in 2007, so many motherboards will accept it, though it has mostly become obsolete in the newer computer market. RAM also has a speed, measured in MHz, so like DDR4-3200, is DDR4 RAM with a maximum speed of 3200MHz

#### Storage

This is typically a **HDD** or **SSD**, and have 2 main varieties, the physical size varieties that is: **2.5 inch** (generally for laptops) and **3.5 inch** (generally for desktops).

The **capacity** is different from the size, it is the largest amount of data that can be stored on the drive. However drives tend to have a slightly lower than advertised capacity, so 4TB drives are generally more like 3.8TB.

There are also another 2 types of drive, which isn't dependent on size: **solid state** and mechanical drives. Mechanical drives contain moving parts, and can become unreliable over large periods of time, especially if they were cheap, though there are many enterprise level solutions which are made to be able to withstand a lot of vibration (assuming it's in an array of many drives). They are also comparatively slow compared to SSDs. SSDs are both more reliable and significantly faster, but are generally more expensive than HDDs, and also have a limited number of read/write cycles they can perform. 

#### GPU

The **Graphics Processing Unit** is an optional component, so many computers have integrated graphics, but it is not necessary, as it essentially does lots of complex calculations very fast, so they can be done on the CPU, but much slower than a dedicated GPU. A **graphics card** has a GPU and dedicated RAM for the GPU on it, where computer graphics are stored, and this card is plugged into the motherboard. 

A modern graphics card generally has a heatsink and a fan (to cool the components and keep heat from damaging sensitive components) on it, and the back generally has a number of different output ports such as VGA, HDMI and Display Port. The GPU can also be called a General Processing Unit, as *it does excel at number crunching*, so programs can use it for encryption, 3D rendering and machine learning, which require lots of complex mathematical calculations.

#### Input Devices

**Input Devices** can send data to your computer when connected to it, and as such can be used to control the computer. The keyboard and mouse are examples of input devices, and specifically the category known as **HIDs**, Human Interface Devices, as they allow humans to interface with the computer.

The **USB** (Universal Serial Bus) is the most common way of connecting an input device, and there are many types of USB connectors: USB A, USB B, USB Micro A, USB Micro B, USB Mini A, USB Mini B and USB Type-C.

And there have also been several upgrades to the USB standard in the past USB 1 (transfer speed of 1.5Mbit/s), USB 2 (480 Mbit/s), USB 3 (4 GBit/s), USB 3.1 (10 GBit/s) (and has a turquoise-like color). USB 3.2 now also exists and can transfer up to 20 GBits/s, and USB 3, 3.1 and 3.2 have all recently been renamed to USB 3.2 Gen1x1, USB 3.2 Gen1x2 and USB 3.2 Gen 2x2 respectively. USB 4 is apparently going to be arriving in 2020 as well, with 40 GBits/s.

Older input devices used PS/2 ports (Keyboards and Mice did anyway).

#### Output Devices

These *accept data from the computer*, and could be a printer, a monitor or any such device. A monitor accepts data and displays an image, a printer gets data and prints something, and all devices with similar functionality are classified as an output device.

The output ports include VGA, DVI, HDMI, Display Port and USB-C. **VGA** is the oldest, and either side has thumbscrews to secure the connection, **DVI** is newer, but now outdated, and again has two thumbscrews, the main difference from VGA is that it transfers more data and the port looks quite different. **HDMI** is the more modern connection, and transmits both video and audio, and there are a few variations of them: Standard A, Dual-Link B, Mini C, Micro D and 'Automotive Connection System'. An even newer port is the **Display Port**, which can transmit more data than the HDMI along with audio just like HDMI. The newest of course is **USB-C**, but only a few modern monitors support video output over this.

#### Heat Sinks

Computers generally have many fans to divert heat, but this is not enough a lot of the time, so **Heat Sinks** are used to move heat away from sensitive components. It is a metal block with many fins, and is made of a thermally conductive material, and the fins allow more surface area for the air passing through the vents in the case to carry out the heat, so basically enables more efficient cooling. To attach a Heat Sink to a component, you spread **thermal paste** between it and the component, as it fills any minute imperfections between the component and the heat sink, and generally gets rid of air between them, (as air is a good insulator), thereby making thermal conduction more efficient. The CPU, GPU and motherboard generally have heat sinks (though the motherboard is small enough that it doesn't need a dedicated fan, as the case fans can generally take care of those needs).

#### Power Supply

The **PSU** (Power Supply), is responsible for taking power from either the mains power supply or a batter (for laptops), and converting and then delivering it to the computer components. It is usually connected to the motherboard, the graphics card(s), the hard drive(s) and the fans. All the other components (like the CPU) are usually powered by the motherboard.

Each PSU will have a certain power rating, and that is the maximum amount of power it will be able to deliver to your system, if the system doesn't have sufficient power to run, it may not turn on, or it may randomly turn off when the components require more power.

The PSU has a built in fan to cool it down during operation. IT also has different cables to power components. A 4 pin connector (where the pin holes are usually round) are used to power the fans, a **SATA (Serial ATA) power connector** is used for powering hard drives, and it also has a main **ATX connection** which runs to the motherboard, and has 20 holes for 20 pins, but has an additional, optional, 4 pin-holes, in case the motherboard has 24 pins. There is also a **12V power connector** running to the motherboard, it generally has 8 pin holes, and depending on the motherboard 4 of the pin holes, or 8 of the pin holes may be used. There is also the **PCI-E power connector**, which usually runs to the graphics card, some cards need six pins, some need eight, and as such it is normal to find cables with an optional extra two pins on them.