# Abstract

This is a demo container runtime to showcase how various Linux features, like namespaces, are used to create containers.

![](screenshot.png)

# Warning #1

THIS CODE IS INTENDED FOR DEMONSTRATION PURPOSES ONLY AND IS NOT SUITABLE FOR A PRODUCTION ENVIRONMENT!

# Warning #2

YOU SHOULD PROBABLY NOT RUN THIS ON YOUR LAPTOP! Parts of this codebase mess with mount points, etc and could destroy
your files. Or eat your cat. And maybe burn down your house. You have been warned.

# Contents

- [Simple demo applications for each aspect of containerization and detailed readmes](demo)
- [Complex container runtime](runtime)

# Compiling

## Pre-requisits
I had to install thest packages before compiling in ubuntu-18.04
```
sudo apt-get -y install cmake libcap-ng-dev
sudo apt install zlib1g-dev
```
If you want to compile this demo, you need at least cmake 3.5 and the libseccomp header files. Compilation can be done
with cmake:

```
cmake .
make
```

This will generate a number of binaries:

- demo/namespaces/mount/demo_namespaces_mount
- demo/namespaces/net/demo_namespaces_net
- demo/namespaces/pid/demo_namespaces_pid
- demo/namespaces/uts/demo_namespaces_uts
- demo/seccomp/demo_seccomp
- runtime/demo_runtime

Each of these is documented in the readme of their respective folder.

# Further reading

The operational theory of this runtime is explained in detail [on my blog](https://pasztor.at/blog/under-the-hood-of-docker).
