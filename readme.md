# Maimai Finale to Maimai DX wrapper

The most non-elegant way of making Maimai DX playable on Maimai Finale Cabinet on Rust.

# Setup


# About


## How does it work?
It takes inputs from Cabinet Touchscreen/JVS/NFC reader COM Ports, modifies it in the way that DX can understand
and sends it to other virtual COM ports (via [com0com]() or other programs) that game will read.
## Touchscreen difference
If you played both Finale and DX version, you know that DX have new additional touch zones as well as a new game mechanic - touch notes.

Here is the difference between Finale (on the left) and DX (on the right) 

![](https://i.imgur.com/w8sUFHy.png)

Since the layout is pretty much the same, we simply mapped new zones to the closest existing ones. 
E.g. if you press B1, the E1 and E2 will also activate.
Same with A and D zones.

## Why keyboard emulation with JVS?

I just didn't figure out how to make DX read from JVS COM port. 

In theory, it uses a combination of `COM4` and `\\.\mxjvs`, but the game never send anything to these ports.

If you know how to solve this, please make a PR or DM me on [Discord](https://discordapp.com/users/161178211596763137)