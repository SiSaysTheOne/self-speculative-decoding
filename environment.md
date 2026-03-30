This guide uses Micromamba to set up a Conda envirnoment.

Before setting up a Conda environment, this project's CUDA libraries do not install without errors with modern g++ libraries.
```bash
# Capture your current g++ version
g++ --version

# Install and configure a compatible g++ version on your system 
sudo apt install g++-11
sudo update-alternatives --install /usr/bin/g++ g++ /usr/bin/g++-11 11 --slave /usr/bin/gcc gcc /usr/bin/gcc-11
sudo update-alternatives --config g++
```

Set up the Micromamba environment
```bash
micromambda create -f ssd.yml --channel-priority flexible
```
