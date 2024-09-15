## percy - forward error correction in hardware

percy is an open source IP core that you can use to implement Reed-Solomon encoding, built according to existing open source implementations. It's permissively licensed, fully hackable, and well tested, so you can entrust it with your project's workload

## Motivation

There's already several very capable hardware IPs available for FEC. Why build another?

I certainly don't believe I'm able to deliver the cleanest or most performant implementation, especially if I'm not allowed the use of privileged compiler intrinsics or internal FPGA details to optimize my design, but I do believe in the power of open source, and this is something I wish we had in our satellite lab back in college. So I wanted to build something that benefitted students and the wider community alike.

## Roadmap

Currently, percy is just a hobby project, and likely to stay that way for a long time while I don't have an FPGA to test on. I'm trying to build this in a way that it can at least be tested on CI, without any actual hardware. We'll have to see if toolchains exist that work that way.

# Items to knock out
- high z mode output
- architecture for processing state machine of rsfec.c
- shared memory for state and payload etc
- simplex or duplex implementations
- synchronization/lockon to incoming stream
- fully plug and play transmitter/receiver pair
- plug it into a tailscale style architecture to do automatic secure discovery of peers
