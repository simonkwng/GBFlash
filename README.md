# GBFlash
GBFlash is a fast burner for GB/GBA flash cards.  Its design was inspired by the GBXcart, but it employs a completely different design approach.

GBXcart is a remarkable design, it brings all new ways of playing to retro game enthusiasts, allowing them to easily and conveniently burn their
favorite games, and it has received widespread acclaim among enthusiasts.

However, it also has some imperfections; 1) the performance of the microcontroller used is not very high, 2) the burning speed is somewhat slow.
So I came up with the idea of creating a fast burner, and thus GBFlash was born.

For hardware, GBFlash uses a 32-bit ARM processor and connects directly to the computer via USB 2.0, theoretically achieving a transfer speed of up to 12 MBits/s. 
For software, Carefully designed efficient code allows for bi-directional concurrent data transmission. Reverse engineering and implementation of the L1 protocol from FlashGBx enables support for most of FlashGBx's features. 
Thanks to these software and hardware advantages, GBFlash performs outstandingly, with the fastest transfer speed exceeding 550 KB/s.

I think GBFLASH might become a competitor to GBXcart. However, competition isn’t necessarily a bad thing; it leads to progress and allows us to create better products

GBFlash needs to work in conjunction with FLASHGBX. I am very grateful to Lesserkuma, the author of FlashGBX, for creating such a useful burning software for us retro game enthusiasts. 
To allow FlashGBX to connect directly to GBFlash, I have done some work:
1. Developed a USB-Serial driver on the microcontroller to simulate CH340.
2. I analyzed the FlashGBX source code to sort out the FlashGBX communication protocol and ported the protocol to GBFlash.
3. Disguised GBFLASH as GBXcart, including the hardware version number and software version number.

Through the above work, GBFLASH can successfully connect to the official version of FlashGBX (without any modifications) and work normally. The read and write speed of GBFlash is several times faster than GBXcart, which is indeed very impressive, greatly reducing the game burning time, especially for some large-capacity game cards.

The reason why GBFlash is fast is not only because of the USB direct connection, but also because GBFlash has larger memory resources and a well-designed software structure.
This is a comparison chart of the internal operation timing. If GBXcart also used my method, I think its speed could be further improved.

#GBXcart：
![gbxcart](https://github.com/simonkwng/GBFlash/assets/16648497/7195967a-48f3-4e8c-8111-255c62b8555e)

#GBFlash:
![gbflash](https://github.com/simonkwng/GBFlash/assets/16648497/f9d11f63-f0d5-4827-8db4-6da51df33229)

Recently, I contacted Lesserkuma, hoping that FlashGBX can directly support GBFlash, so there is no need to simulate GBXcart to achieve the connection with FlashGBX. I am honored to have received his support, and I am very grateful to Lesserkuma. The latest firmware version by Lesserkuma is still in beta testing, and the new version will soon support GBFlash. Let’s look forward to it."

