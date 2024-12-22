# Demo Code of modified-Poac for C++ Advent Calendar 2024 Day 20

## Prerequisites

1. Setup/Install [poac prerequisites](https://github.com/poac-dev/poac/blob/main/INSTALL.md).
1. Build and install [modified poac](https://github.com/wx257osn2/poac/tree/cxx_adc_2024).
    - ```console
      $ git clone -b cxx_adc_2024 https://github.com/wx257osn2/poac
      $ cd poac
      $ make RELEASE=1 -j $(nproc)
      $ make PREFIX=/path/to RELEASE=1 install
      ```

## Run

```console
$ git clone https://github.com/wx257osn2/cxx_adc_2024_day20_poac-demo
$ cd cxx_adc_2024_day20_poac-demo/test_application
$ poac build
 Compiling libtest.a v0.1.0 (/path/to/cxx_adc_2024_day20_poac-demo/libtest)
  Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.63s
 Compiling test_application v0.1.0 (/path/to/cxx_adc_2024_day20_poac-demo/test_application)
  Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.92s
$ poac-out/debug/test_application
this is test application
output from libtest
$ sed -i 's/libtest/the library/' ../libtest/src/lib.cpp
$ poac build
 Compiling libtest.a v0.1.0 (/path/to/cxx_adc_2024_day20_poac-demo/libtest)
  Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.64s
 Compiling test_application v0.1.0 (/path/to/cxx_adc_2024_day20_poac-demo/test_application)
  Finished `dev` profile [unoptimized + debuginfo] target(s) in 0.74s
$ poac-out/debug/test_application
this is test application
output from the library
```
