# qpdf-arm64-distro
qpdf compiled for linux arm64 so we can use it on arm64 containers running on linux

# How to generate the qpdf file?

- Clone the qpdf repository, and choose a release https://github.com/qpdf/qpdf/releases
- Inside the qpdf folder, you can run the following commands to compile the qpdf for arm64

```
mkdir build
cd build
cmake ..
make -j$(nproc)
cpack -G STGZ
```

These commands will generate a ./qpdf-<version>-Linux.sh file that you can use to install qpdf on your arm64 linux machine.
You can copy the generated file to this repository.
