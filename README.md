# sdcpp-google-colab-binary

Stable-Diffusion-CPP Binaries for Google Colab

Since the [original repo](https://github.com/leejet/stable-diffusion.cpp/releases) does not supply bins for linux cuda

# Updates

Compiling takes 30 mins, so I will not constantly do this repeatedly. More or less one build per month, or if I need a certain version of stable-diffusion.cpp

# Procedure

Same as the [official guide](https://github.com/leejet/stable-diffusion.cpp/blob/master/docs/build.md#build-with-cuda) but on [Google Colab](https://colab.research.google.com/)'s Tesla T4 GPU

```python
!git clone --recursive https://github.com/leejet/stable-diffusion.cpp
%cd stable-diffusion.cpp

!mkdir build
%cd build
!cmake .. -DSD_CUDA=ON
!cmake --build . --config Release -j$(nproc)

%cd /content
```

# Binaries

Will be in the [releases](https://github.com/NUROISEA/sdcpp-google-colab-binary/releases). Updated manually. Same naming scheme as the original repo.

# Repo trust

Do not run these things in your own machine. I may or may not inject malware into my `bin`s. You have been warned.

Do not run these in a colab that's connected to your Google Drive, for the same reason.