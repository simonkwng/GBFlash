# GBFlash
GBFlash is a rapid burner for GB/GBA flash cards. Its design was inspired by the GBXcart, yet it adopts an entirely different design approach.

The GBXcart is a remarkable design that brings entirely new ways of playing to retro game enthusiasts, enabling them to burn their favorite games easily and conveniently. It has received widespread acclaim among enthusiasts. However, it also has some imperfections. Firstly, the performance of the microcontroller used is not very high. Secondly, the burning speed is a little slow  . Hence, I came up with the idea of creating a fast burner, and thus GBFlash was born.

In terms of hardware, GBFlash utilizes a 32-bit ARM processor and connects directly to the computer via USB 2.0, theoretically achieving a transfer speed of up to 12 megabits per second. Regarding software, carefully designed efficient code allows for bidirectional concurrent data transmission.  Analysis and implementation of the L1 protocol from FlashGBx enables support for most of FlashGBx's features.  Thanks to these software and hardware advantages, GBFlash performs outstandingly, with the fastest transfer speed exceeding 550 kilobytes per second.


GBFlash needs to work in conjunction with FLASHGBX. I am extremely grateful to Lesserkuma, the author of FlashGBX, for creating such a useful burning software for us retro game enthusiasts. To enable FlashGBX to connect directly to GBFlash, I have carried out some work:
● Developed a USB-Serial driver on the microcontroller to simulate CH340.
● Analyzed the FlashGBX source code to sort out the FlashGBX communication protocol and ported the protocol to GBFlash.
● Disguised GBFLASH as GBXcart, including the hardware version number and software version number.


Through the above efforts, GBFLASH can successfully connect to the official version of FlashGBX (without any modifications) and operate normally. The read and write speed of GBFlash is several times faster than that of GBXcart, which is indeed very impressive. It greatly reduces the game burning time, especially for some large-capacity game cards.

The reason why GBFlash is fast is not only due to the USB direct connection but also because GBFlash has larger memory resources and a well-designed software structure. Here is a comparison chart of the internal operation timing. If GBXcart also employed my method, I think its speed could be further enhanced.

#GBXcart：
![gbxcart](https://github.com/simonkwng/GBFlash/assets/16648497/7195967a-48f3-4e8c-8111-255c62b8555e)

#GBFlash:
![gbflash](https://github.com/simonkwng/GBFlash/assets/16648497/f9d11f63-f0d5-4827-8db4-6da51df33229)

Recently, I got in touch with Lesserkuma, hoping that FlashGBX can directly support GBFlash so that there is no need to simulate GBXcart to achieve the connection with FlashGBX. I am honored to have received his support. I am extremely grateful to Lesserkuma. And now, FLASHGBX has officially supported GBFLASH.  

