# IDA-EVM
[IDA](https://www.hex-rays.com/products/ida/) Processor Module for the [Ethereum Virtual Machine](https://github.com/trailofbits/evm-opcodes) (EVM).

This plugin is under active development. New issues and contributions are welcome, and are covered by bounties from Trail of Bits. Join us in #ethereum on the [Empire Hacking Slack](https://empireslacking.herokuapp.com) to discuss Ethereum security tool development.

IDA Pro 7.0 or newer is required to use IDA-EVM.

![Screenshot](/images/screenshot.png)

# Installation
* Copy `evm-loader.py` to `%IDA%/loaders`
* Copy `evm-cpu.py` and `known_hashes.py` to `%IDA%/procs`
* Restart IDA

# What's New in ida-evm-enhanced
- Forked from crytic/ida-evm, enhanced jump dest address analysis.
- Previously, jump dest addr can only be resolved when the direct previous instruction is PUSH, but not working on other instructions.
- Now ida-evm-enhanced can resolve & display the jump dest addr under all instructions.
- e.g.:![image](https://user-images.githubusercontent.com/17793687/183290524-3c53a3eb-049c-4c13-905e-f36f314c73e3.png)
- The only thing left is, it doesn't follow all branches when there's multiple upperstream code branches. As a workaround, it displays all the upperstream branches in the comments of the jump instruction.
- e.g.:![image](https://user-images.githubusercontent.com/17793687/183290588-03cdbf7e-3444-4d6e-a693-5c7b95f89268.png)
