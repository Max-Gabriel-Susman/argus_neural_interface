# Argus Neural Interface

Argus Neural Interface Emulates a Micro Electrode Array(MEA) and receives neural data the Argus Brain Sim and Sends it to the rest of the Argus Cybernetics Stack

## System Requirements

Was developed for the Nvidia Jetson Orin Nano Super Developer Kit and Ubuntu 22.04 and is currently only supported for this setup. You can probably get it to run in a different enviroment  but this repositories documentation assume the reader is using the same setup. 

## Local setup

After cloning this repository run this at the repo's root: 
```
sudo apt update
sudo apt install -y build-essential cmake

mkdir -p build
cmake -S . -B build -DCMAKE_BUILD_TYPE=Release
cmake --build build -j
./build/argus_neural_interface
```
