# cs269q-quantum-computer-programming

## Setting up a virtual environment for pyQuil
PyQuil is a library that generates and executes Quil programs on the Rigetti Forest platform. The current version, pyQuil 2.0, requires Python version 3.6 or higher. I only had Python 3.4 and 2.7. To activate a virtual environment,
```bash
virtualenv --python=python3 cs269
source cs269/bin/activate
```
You can deactivate the environment with
```bash
deactivate
```

## Installing the simulator and compiler
The Rigetti Quantum Virtual Machine (`qvm`) simulates Quil programs. The Rigetti Quil Compiler (`quilc`) compiles Quil programs and optimizes them to native gate sets. Both are needed for us to use the Rigetti Forest SDK.

One thing to watch out for Debian users is that the installation looks for `libssl.so.1.0.2`. I had `libssl.so.1.0.0`, so I changed the link:
```bash
cd /lib/x86_64-linux-gnu
sudo ln -s libssl.so.1.0.0 libssl.so.1.0.2
```
I'll update this REAME if I run into problems later.