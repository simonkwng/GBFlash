# GBFlash
GBFlash is a fast burner for GB/GBA flash cards.  Its design was inspired by the GBXcart, but it employs a completely different design approach.

GBXcart is a remarkable design, it brings all new ways of playing to retro game enthusiasts, allowing them to easily and conveniently burn their
favorite games, and it has received widespread acclaim among enthusiasts.

However, it also has some imperfections; 1) the performance of the microcontroller used is not very high, 2) the burning speed is somewhat slow.
So I came up with the idea of creating a fast burner, and thus GBFlash was born.

For hardware, GBFlash uses a 32-bit ARM processor and connects directly to the computer via USB 2.0, theoretically achieving a transfer speed of up to 12 MBits/s. 
For software, Carefully designed efficient code allows for bi-directional concurrent data transmission. Reverse engineering and implementation of the L1 protocol from FlashGBx enables support for most of FlashGBx's features. 
Thanks to these software and hardware advantages, GBFlash performs outstandingly, with the fastest transfer speed exceeding 550 KB/s.
